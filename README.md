# Introduction
This repository contains the Compose configuration for deploying the BookStack Wiki for the team. BookStack is used to manage and store internal documentation, providing a collaborative platform for knowledge sharing within the team.

# Setup

1.  Create and Modify a `.env` with contents:

    ``` 
    DB_USER=bookstack
    DB_PASS=<yourdbpass>
    APP_URL=https://bookstack.example.com
    PORT=6875
    ```

> [!CAUTION]
> Use secure passwords!! These services can be accessed on the open internet. Be Smart

2. Launch the container(s) with the terminal.

    ```
    $ docker compose up

    or

    $ podman compose --file compose.yaml up 
    ```