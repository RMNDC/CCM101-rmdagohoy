# Technical Documentation

- What does the services: block do?
  It's where we list each container that makes up our application. There are two services, database and app. Each one defines its image, ports, and environment variables, and compose creates a container for each.

- How did the Nextcloud app container know how to find the database container? (Hint: Look at the 
MYSQL_HOST environment variable).
MYSQL_HOST=database tells Nextcloud the database's hostname. No IP address needed, because compose puts both services on a shared network and uses each service name as a DNS name, so database resolves to the MariaDB container automatically.

- What is the difference between docker run (which you used in Mission 4) and docker-compose up -d?
  On the docker run it will start at one container, with the options typed manually each time. While the docker-compose up -d, it reads the a YAML file and then starts at whole stack at once, with networking set up. The -d means it will run it in the background.
