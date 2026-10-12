## What is a Two-Tier Architecture?

A two-tier architecture is a way of building an application by splitting it into two separate parts, or "tiers," that each have their own job. The first tier is the web/application tier, which is the part users actually interact with. The second tier is the database tier, which is where all the data is kept. The two tiers talk to each other over a network connection, but they run independently, so each one can be set up, fixed, or scaled without having to rebuild the whole thing.

## The Web/Application Tier

This tier is the front door of the application. Its main role is to serve the user interface (the pages, buttons, and forms people see in their browser) and to handle incoming HTTP requests. When someone logs in or submits a form, this tier receives the request, runs the application logic, and decides what to do with it. If it needs to save or look up data, it asks the database tier instead of storing anything itself. Then it sends a response back to the user. A web server like Nginx or Apache, or an app built with Flask or Node.js, would live here.

## The Database Tier

This tier is the memory of the application. Its role is to store persistent data, meaning information that has to stick around even after the app restarts, like user accounts, passwords, posts, or orders. It also takes care of retrieving, updating, and deleting that data when the web tier asks for it. It doesn't deal with the user interface at all. It just keeps the data organized, safe, and available. MySQL, PostgreSQL, and MariaDB are common examples.

## Why Separate Them?

Putting the web server and the database in two separate containers means a problem in one doesn't automatically take down the other. For example, you can restart or update the web app without risking the data. It also lets you scale each part on its own, like adding more web containers when traffic goes up without touching the database. On top of that, it's safer, because the database can be kept off the public network so only the web tier can reach it.
