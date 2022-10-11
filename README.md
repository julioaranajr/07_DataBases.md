# 07_MySQL_DataBases.md
Hands on Labs [MySQL + Docker] -> Movie Management Projects

# MySQL 

### MySQL docker

Using a container makes things easy to run an application. Just run the following command to map the right folder to the container data folder.

```sh
# mkdir <folder_name>
mkdir ~/src/Talent-Academy/database
```
```sh
#docker run --name <container_name> -p 3306:3306 -v <folder_name>:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=<password> -d mysql:latest
docker run --name movie-db-mysql -p 3306:3306 -v ~/src/Talent-Academy/database/var/lib/mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:latest
```

You can also perform other commands with your docker, e.g.:
```sh
# list all (running/exited) containers
docker ps -a

# Stop a running container
docker stop container_name

# Start a stopped container
docker start container_name

# Start a stopped container
docker rm container_name
```

### Install client

```sh
brew install mysql-client
```

Open the `~/.zshrc` to add the `export` variable. This will make sure that all binaries for mysql is available to be use.

```sh
code ~/.zshrc
# or
vi ~/.zshrc
```

```sh
# mysql
export PATH="/usr/local/opt/mysql-client/bin:$PATH"
export PATH="/opt/homebrew/opt/mysql-client/bin:$PATH"
```

Close your terminal and re-open it.

### Connect to your database

```sh
mysql -h 127.0.0.1 -u root -p
```

# Exercises

> - Connect to your database **(Create the database inside mysql)**
> - Create Database (movie)
> - Create Tables **(directors,movies,main_actors, movie_actors)**
> - Addin more data...

**all that exercises you can find it in movie_managment_project on my repositories)**
Follow this link to the labs exercises [Movie_Managment_Project](https://github.com/julioaranajr/movies-managment-project)
