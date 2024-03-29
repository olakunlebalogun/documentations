# Structure Query Language (SQL)

## Basic Knowledge  
Logging in from the Terminal  
`mysql --user=username --password=password`  
Other options are:  
`--host=hostname --port=port`  

To display all privileges/permission for a given user   
`SHOW GRANTS FOR 'docker_db'@'172.18.0.1';
`


To grant all access to user docker_db  
`> GRANT ALL PRIVILEGES ON *.* TO 'docker_db'@'172.18.0.1' IDENTIFIED BY '<password>'`;

To create a new user using authentication_plugin as security    
`CREATE USER 'username'@'host' IDENTIFIED WITH authentication_plugin BY 'password';`




To check MySQL version  
`SELECT VERSION();`  

To display all the databases  
`SHOW DATABASES;`  

### Modes
There are two modes in MySQL
- **Interactive Mode**: This involves writing database queries direct into the terminal or using the GUI e.g *Workbench*, *DataGrip* and *Dbeaver*.
- **Batch Mode**: This involves loading database queries from a file using the SOURCE keyword and the path to the file e.g  
`SOURCE file.sql` 

## Help  
Getting help in MySQL, use the `HELP` command in the terminal  
To get documentation of different sections use `HELP Contents` 
To get specific information on a section use *HELP SECTION* e.g for Data Manipulation  
`HELP Data Manipulation`


## Shortcuts 
`\?` or `\h`  Informative help  

## Entity Relatioship Diagram  

- Entity is a rectangle  
- Attributes are oval  
- Multivalued attributes are double-ovaled  
- Composite atrributes have further oval attributes  
- Primary attributes are underlined.  
- Relationships are diamond shaped  
- Relationships too can have attributes.  
- Cardinality of entity relationship.. M:M, 1:M, M:1, 1:1  
- Relationships betwwen entity can be partial or total  
- Total relationship are double-lined between entity box and the relationship diamond  
- Weak entities have total participation  
- Weak entities are double-rectangled and their primary keys are dashed lined  
 

 ## References
 - [Digital Ocean documentatiom](https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql)