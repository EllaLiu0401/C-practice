# DotNetAPICourse

Hello and welcome to this C# Dotnet Core course!

Inside of this repository you will find all of the code from various sections of the course.

If you are opting to skip the SQL section of the course you can also use the SQL scripts inside of this repository to prepare your database for the interactions from the API.

Congratulations on taking this step in your learning journey, and I am excited to see you inside!

# Mac/Linux Install MS SQL Server - Notes

Hello!

If you are using MacOS or Linux, it is a little bit more complex to get MS SQL Server up and running.

In the next lecture we are going to set up MS SQL Server in Docker on MacOS and this approach will also work on Linux.

You can copy the link and commands from here to make the process a little easier.

This is currently the only option for MacOS, however there is another option for Linux described in a Microsoft Article linked at the bottom.

For the approach we are taking to work in Linux, you will also need to run all docker commands as sudo commands.

1. Install Docker:
   MacOS: https://docs.docker.com/desktop/install/mac-install/

Linux: https://docs.docker.com/desktop/install/linux-install/

2. Increase RAM allocation for Docker

--I would suggest increasing to 4GB

3. Create and Run a container for the Image:
   docker run -e "ACCEPT_EULA=1" -e "MSSQL_USER=SA" -e "MSSQL_SA_PASSWORD=SQLConnect1!" -e "MSSQL_PID=Developer" -p 1433:1433 -d --name=sql_connect mcr.microsoft.com/azure-sql-edge

4. Check if the container is running

docker container ls -a

5. Stop and Start Container

docker stop sql_connect

docker start sql_connect
