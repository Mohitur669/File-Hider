# Hide Files in MySQL Database

This is a Java project that allows you to hide files in a MySQL database. The files are encrypted using AES encryption
and then stored in the database. The files can be retrieved from the database and decrypted.

## Prerequisites

You will need to have the following installed on your computer:

1. Java (I used 21)
2. MySQL
3. Apache Maven
4. Google generated app password (for sending emails)

## Maven Dependencies

The following dependencies are required for this project:

1. mysql-connector-java
2. javax.mail

Add these dependencies to your pom.xml file:

```xml
<dependencies>
    <!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.33</version>
    </dependency>

    <!-- https://mvnrepository.com/artifact/com.sun.mail/javax.mail -->
    <dependency>
        <groupId>com.sun.mail</groupId>
        <artifactId>javax.mail</artifactId>
        <version>1.6.2</version>
    </dependency>

</dependencies>
```

Note: Always check for proper version of dependencies regarding your project.

## Using the Project

1. Create the database using the following SQL command:

```sql
CREATE DATABASE fileHider;
```

Now switch to the database:

```sql
USE fileHider;
```

2. Create the following tables (users, data) in the database:

```sql
create table users
(
    id int primary key auto_increment,
    name varchar(100),
    email varchar(100) unique
);
```

```sql
create table data
(
    id int primary key auto_increment,
    name varchar(100),
    path varchar(255),
    email varchar(100),
    bin_data blob
);
```

3. If all things done correctly, you should be able to run the project and use it.

# Running the Project

1. Clone the project to your computer
2. Open the project in your IDE
3. Run the "Main" class inside /src/main/java

## About Me
I am Mohd Mohitur Rahaman, a tech geek, currently pursuing a Master's in Computer Applications from KIIT, Bhubaneswar. And with a deep passion for coding and a strong love for science & technology, I am dedicated to honing my skills and achieving proficiency as a developer.

## Connect with me
- [LinkedIn](https://www.linkedin.com/in/mohitur02/)