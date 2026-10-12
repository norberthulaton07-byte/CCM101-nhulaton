# Mission Reflection

Before this laboratory, I thought deploying an application meant a lot of typing, installing, and hoping nothing broke. Writing a docker-compose.yml file changed that. Instead of typing a long command for every container and remembering each port, password, and image name, I wrote everything once in a file and started the whole system with a single command. That makes a cloud engineer's job easier because the setup is saved, so it can be repeated or fixed without starting from scratch.

The tradeoff is that YAML is very strict. It uses spaces to figure out which settings belong to which service, so one wrong indent, like using a Tab instead of spaces, can cause an error. Docker Compose will not run until the file is fixed, which was annoying, but it taught me to double check my spacing.

Another important part of the file was the environment variables. They let us pass settings like the database name, user, and password into the containers without changing the image itself, and they made sure the app and the database used the same login details so they could connect. I also noticed that writing passwords directly in the file is not very safe, so in a real project I would keep them somewhere more private.

Honestly, the best part was seeing Nextcloud come up in just a few minutes. I expected a cloud storage system to take hours of installing and configuring, but it took one command and a short wait. Seeing the setup page in my browser made me feel like I built something real.

Looking back at Mission 1, cloud computing felt like a buzzword I only half understood. Now I see it as tools that help you build and run things quickly, and I have actually practiced it with containers, networking, and a two-tier setup. I still have a lot to learn, but I feel much more confident than before.
