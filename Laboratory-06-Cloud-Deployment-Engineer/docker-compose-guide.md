## The Compose File

```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?

The `services:` block is where you list every container that makes up the application. Each name under it (here, `database` and `app`) is one service, and each service becomes its own container when the stack starts.

For every service, you describe how it should run. For example, `image` says which Docker image to use, `ports` says which ports to open to the outside, and `environment` passes in settings like usernames and passwords. In this file, the `database` service runs MariaDB 10.6 and sets up the database and its user, while the `app` service runs Nextcloud and is reachable on port 8080 of the host.

Compose also puts all the services on the same network automatically, which is what lets them talk to each other.

## How did the Nextcloud app container know how to find the database container?

It found the database through the `MYSQL_HOST=database` environment variable. That value tells Nextcloud, "your database is at the host named `database`."

The name `database` matches the service name in the Compose file. When Compose starts the stack, it puts both containers on a shared network and lets each container reach the others by their service name. So when Nextcloud connects to `database`, Docker's built-in DNS translates that name into the database container's IP address. This means I never had to look up or type in an IP address, and it keeps working even if the container's IP changes.

The other `MYSQL_*` variables (user, password, and database name) in the `app` service match the ones in the `database` service. That's how Nextcloud logs in with the right credentials.

## What is the difference between `docker run` and `docker-compose up -d`?

`docker run` starts a single container, and you have to type out all its options (image, ports, environment variables, and so on) in one long command each time. If your app needs two containers, you'd run two separate commands, create a network yourself, and make sure they can find each other.

`docker-compose up -d` reads the `docker-compose.yml` file and starts the whole stack at once. Both containers are created, put on a shared network, and linked together automatically. Because the setup is saved in a file, it's easy to repeat, share with other people, and keep in version control. The `-d` flag means "detached," so everything runs in the background and I get my terminal back.

In short, `docker run` is good for quickly starting one container, while Docker Compose is better when an application is made of several containers that need to work together.
