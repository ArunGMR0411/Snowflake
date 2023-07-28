How to connect to Snowflake using Snow SQL:
===========================================
Firstly, snowsql is a CLI used to connect and execute queries on Snowflake from Terminal/CMD.

The First step is to setup the configuration to Snowflake Server from my System(Client):  
**Provinding username and password directly:**  
> snowsql -a <account_name> -u <username> - The Password should be entered when prompted.

**Using a config file for snowsql:**  
Create a config file inside snowsql directory ~/.snowsql/config  
And enter the following details, the blocked parts in the URL corresponds to specific values:   
>account_name = <account_name> (https:/app.snowflake.com/ap-southeast-1/**en28569**/worksheets)  
login_name = <login_name> - This will be available in the Profile section  
password = <password_value>  
region = <region_value> (https:/app.snowflake.com/**ap-southeast-1**/en28569/worksheets)  
And then enter snowsql, it will fetch the username and password from the config file and connect to the server.

Setup logging of snowsql
========================
Logging file can be setup in the same config file as in username and password.
> log_file = <path_with_access/snowsql.log>

Thus all the logs will get written into this log file.  


Debug Mode
==========
When starting snowsql, add option to it to enable debugging mode when you need more details to debug.

>snowsql -o log_level=DEBUG