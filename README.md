# OpenEMR

A simple guide for setting up [OpenEMR](https://www.open-emr.org/) using Docker for local use.

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)

## Getting Started

### Install Prerequisites

Ensure you have Docker and Docker Compose installed on your system.

### Copy Environment File

Make sure to copy the `.env.example` file to `.env` before proceeding:

```sh
cp .env.example .env
```

### Start the Application

Run the following command to start the application in detached mode:

```sh
docker compose up -d
```

This will initiate a quick setup process, which typically takes around 5–10 minutes.

### (Optional) Monitor Setup Progress

To check if the setup is still running or has completed, use the following command:

```sh
docker compose logs --follow
```

Press `Ctrl-C` to exit the log view.

To confirm that the quick setup has finished, look for the following lines in the logs:

```
Running quick setup!

OpenEMR configured.
Setup Complete!
Setting user 'www' as owner of openemr/ and setting file/dir permissions to 400/500
Default file permissions and ownership set, allowing writing to specific directories
Setting sites/default/documents permissions to 700
Removing remaining setup scripts
Setup scripts removed, we should be ready to go now!

Love OpenEMR? You can now support the project via the open collective:
 > https://opencollective.com/openemr/donate

Starting apache!
```

## Access the Application

Once the quick setup is complete, you can access the web application by visiting:

```
https://localhost:8443
```
