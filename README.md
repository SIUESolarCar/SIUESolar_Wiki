# Introduction
This repository holds the Docker Compose for the team's BookStack Wiki. This wiki is inteded to hold all internal documentation for the team to pass down knowledge.

# Setup
Only a few lines of the compose.yaml need to be modified inorder to use the wiki. 

1. The Database Password
     
    ``` 
    - DB_PASS=<yourdbpass>
    - MYSQL_ROOT_PASSWORD=<yourdbpass>
    - MYSQL_PASSWORD=<yourdbpass>
    ```
2. The URL

    ```
    - APP_URL=https://bookstack.example.com
    ```
3. Path to Volumes
    ```
    - /path/to/bookstack_app_data:/config
    - /path/to/bookstack_db_data:/config
    ```