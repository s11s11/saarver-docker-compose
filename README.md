# Saarver Docker Compose
This repository contains the configuration for all services on my homelab server, known as the Saarver.

## Structure
Each directory contains files for one service, which consists of one or more Docker containers. At a minimum there is a `docker-compose.yml` file, and additional configuration files may be present as required by each application.
<img width="507" height="283" alt="image" src="https://github.com/user-attachments/assets/95a31910-f1cd-4e67-b262-e582c8062ead" />

## External Parameters
Some parameters in `docker-compose.yml` are provided by `.env` files which sit in the same directory. These parameters are written as `${PARAMETER_NAME}`.

Parameters containing passwords or other secrets are handled with Docker Secrets, which reads the parameter from a file. These secret files are not synced to the repository for obvious reasons, but are required to run these services.
