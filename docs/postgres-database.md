# Postgres Database

When running on Dokku, we use a Postgres database supplied by Dokku.

# Accessing Database Console

* On Dokku, with CLI:
  - Use: `Dokku psql --app app-name-here` 
  - Note that this requires that you have the psql CLI tool installed on your system.  
  - This does work on CSIL, but you may need `Dokku login -i` in order to login on CSIL
  - Example:
   
    ```
    [pconrad@csilvm-03 ~]$ Dokku psql --app demo-spring-react-example
    ›   Warning: Dokku update available from 7.59.1 to 7.59.2.
    --> Connecting to postgresql-tapered-84555
    psql (13.4, server 13.5 (Ubuntu 13.5-2.pgdg20.04+1))
    SSL connection (protocol: TLSv1.3, cipher: TLS_AES_256_GCM_SHA384, bits: 256, compression: off)
    Type "help" for help.

    demo-spring-react-example::DATABASE=> 
    ```
* On Dokku, without CLI: 
  - Upper right of dashboard, select "More" then "Run Console"
    
    <img alt="Dokku Dashboard; More; Run Console" src="https://user-images.githubusercontent.com/1119017/150204550-a1027ab8-6ce7-4770-b566-a43928f5c3a0.png" width="300" />
  - Enter `psql $DATABASE_URL` and click `Run`
   
    <img alt="Enter psql $DATABASE_URL and click Run" src="https://user-images.githubusercontent.com/1119017/150206174-43193825-1afd-49f4-aeaf-cfadf0c0c6f3.png" width="400" />
* Cheatsheet of `psql` commands: <https://www.geeksforgeeks.org/postgresql-psql-commands/>
