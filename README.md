# Introduction
This repository contains the Compose configuration for deploying the BookStack Wiki for the team. BookStack is used to manage and store internal documentation, providing a collaborative platform for knowledge sharing within the team.

# Setup

1.  Create and modify a `.env` with contents:

    ```bash
    DB_PASS=secret
    DB_ROOT_PASS=secret
    # Set the APP_URL to the URL of bookstack without without a trailing slash APP_URL=https://example.com
    APP_URL=https://bookstack.example.com
    PORT=6875
    # APP_KEY is used for encryption where needed, so needs to be persisted to
    # preserve decryption abilities.
    # Can run `php artisan key:generate` to generate a key
    APP_KEY=SomeRandomStringWith32Characters
    ```

2.  Setup SMTP by creating and modifying a file `bookstack.env` with contents:

    ```bash
    MAIL_DRIVER=smtp

    # SMTP server host address 
    MAIL_HOST=smtp.provider.tld     # We use our Gmail for this

    # SMTP server port
    # Using port 465 will force connections to be via TLS
    MAIL_PORT=587

    # Connection encryption to use
    # Valid values are: tls, null
    # Using 'tls' will require either TLS or STARTTLS to be used.
    # When using 'null' STARTTLS will still be attempted if announced
    # as supported by your SMTP server.
    # Using port 465 above will force connections to be via TLS.
    MAIL_ENCRYPTION=tls

    # Authentication details for your SMTP service
    MAIL_USERNAME=user@provider.tld
    MAIL_PASSWORD=onlyifneeded

    # The "from" email address for outgoing email
    MAIL_FROM=noreply@yourdomain.tld  

    # The "from" name used for outgoing email
    MAIL_FROM_NAME=BookStack
    ```


3. Launch the container(s) with the terminal.

    ```bash
    $ docker compose up

    # or when using Podman:

    $ podman compose --file compose.yaml up 
    ```