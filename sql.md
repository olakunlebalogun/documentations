# Structure Query Language (SQL)

## Basic Knowledge  
Logging in from the Terminal  
`mysql --user=username --password=password`  
Other options are:  
`--host=hostname --port=port`

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

