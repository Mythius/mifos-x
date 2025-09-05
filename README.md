# Mifos X Accounting Program Full Docker Deployment
This project works as of Sep 5, 2025.

This is for a docker deployment with nginx.

1. Add nginx config to your enabled sites, and change https://fs.mentorsglobal.org to your domain.
2. Edit docker/docker-compose.yml lines 7 and 8, to have your domain. 
3. Run `docker compose up -d`, this usually takes 1-2 minutes for the back end to start running.

The docker-compose.yml also allows access to reference services on the host, such as a mail server, so if you want to set up email sending set up an email server on the on the host device (or in another container), and set the ip address of the mail server to `host.docker.internal` in your web app configuration. 

Note: The webserver runs on port 4200, and the backend server runs on port 8080, and the postgres database runs on 5432, and the compose file exposes these 3 ports.