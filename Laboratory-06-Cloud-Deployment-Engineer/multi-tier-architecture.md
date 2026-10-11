# Two-Tier Architecture

## The Web/Application Tier
This tier serves the user interface and handles HTTP requests from users' browsers. In this mission, it is the Nextcloud container, which processes file uploads, renders the web pages, and talks to the database tier for anything that needs to be stored.

## The Database Tier
This tier stores persistent data such as user accounts, login credentials, and file metadata. In this mission, it is the MariaDB container, which keeps this information in tables that the application tier queries.

## Why Separate Them?
Separating the web tier from the database tier lets each one scale, update, and fail independently; for example, the web tier can be restarted or scaled up without touching the stored data. It also improves security, since the database does not need to be exposed directly to users. Finally, it mirrors how real enterprise systems are built, making the setup easier to maintain and troubleshoot.
