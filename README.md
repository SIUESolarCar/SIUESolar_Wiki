# Introduction
This repository holds the Docker Compose for the team's BookStack Wiki. This wiki is inteded to hold all internal documentation for the team to pass down knowledge.

# Setup

1.  Create a file called `.env` in your project directory and paste the following code in:

    ``` 
    DB_USER=bookstack
    DB_PASS=<yourdbpass>
    APP_URL=https://bookstack.example.com
    ```

2. Modify the `.env` file to your use case. 

> [!CAUTION]
> Use secure passwords!! These services can be accessed on the open internet. Be Smart

3. Run the Docker Compose in the terminal.

    ```
    $ docker compose up