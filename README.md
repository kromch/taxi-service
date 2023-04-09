![alt text](https://raw.githubusercontent.com/kromch/taxi-service/master/TAXI.jpg
# TAXI SERVICE

This project is a blueprint for future development and deploying as Taxi Service. 
Was used Java Servlets program model technic and SQL development stack.

# Features
- Add and delete car models
- Add and delete cars 
- Add and delete drivers
- Add drivers to specific cars
- View all cars belonging to the current driver
- Authentication driver (user)

# Project structure
![alt text](https://raw.githubusercontent.com/kromch/taxi-service/master/struct.jpg)
- Controllers:
	- Car contollers: 
		- AddCarController to adding Car model to DB
		- GetAllCarsController to getting all Car models from DB
		- DeleteCarController to deleting Car model in DB
		- AddDriverToCarController to adding Driver model to existed Car model in DB
	- Driver contollers: 
		- AddDriverController to adding Driver model to DB
		- GetAllDriversController to getting all Driver models from DB
		- DeleteDriverController to deleting Driver model in DB
		- GetMyCurrentCarsController to getting existed Car model by Driver ID from DB
	- Manufacturer contollers: 
		- AddManufacturerController to adding Manufacturer model to DB
		- GetAllManufacturersController to getting all Manufacturer models from DB
		- DeleteManufacturerController to deleting Manufacturer model in DB
	- Exception:
		- AuthenticationException class for handling checked exceptions during Authentication process
		- DataProcessingException class for handling checked exceptions during rest processes
	- DAO:
		- CarDaoImpl handler of Car model to DB
		- DriverDaoImpl handler of Driver model to DB
		- ManufacturerDaoImpl handler of Manufacturer model to DB
	- Model:
		- Car model class
		- Driver model class 
		- Manufacturer model class
	- Service:
		- AuthenticationServiceImpl class 
	- Util:
		- ConnectionUtil class for instance connection to DB
	- Web/filter:
		- AuthenticationFilter class for handle Authentication process
- resources: configuration files and database scripts
- webapp/WEB-INF/views: web resources such as CSS and JSP files used as views in the application for cars
						drivers, manufacturers, authentication and include css files
						(that contains CSS files used in the application)

# Getting Started
- Clone this remote repository to your local repository : `git clone https://github.com/kromch/taxi-service.git`
- Run the SQL script located in `src/main/resources/init_db.sql` to initialize the database
- Build the project using Maven command: `mvn clean install`
- Deploy the WAR file to a servlet container such as Tomcat or Jetty

# Used technologies:
- JDK 19.0.1 version
- Maven 3.9.1 version
- JDBC 4.2 version
- MySql 8.0.32 version
- Java Servlets 4.0.1 version
- Apache Tomcat 11.0.0-M4 version

# Authors
Roman Korkonishko