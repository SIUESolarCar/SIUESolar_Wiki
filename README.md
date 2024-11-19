# Introduction
This repository contains the Compose configuration for deploying the BookStack Wiki for the team. BookStack is used to manage and store internal documentation, providing a collaborative platform for knowledge sharing within the team.

# Setup

1.  Create and Modify a `.env` with contents:

    ```bash
    DB_PASS=secret
    # Set the APP_URL to the URL of bookstack without without a trailing slash APP_URL=https://example.com
    APP_URL=https://bookstack.example.com
    PORT=6875
    # APP_KEY is used for encryption where needed, so needs to be persisted to
    # preserve decryption abilities.
    # Can run `php artisan key:generate` to generate a key
    APP_KEY=SomeRandomStringWith32Characters
    ```

> [!CAUTION]
> Use secure passwords!! These services can be accessed on the open internet. Be Smart

2. Launch the container(s) with the terminal.

    ```bash
    $ docker compose up

    # or when using Podman:

    $ podman compose --file compose.yaml up 
    ```