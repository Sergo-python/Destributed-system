# Lab_5: Seminar04. SOAP Web Services

## Pre-requirements:
* Only Java 8;
* Maven;

## What to do:
1. Open server folder in console or terminal (the server was provided by the teacher);
2. Run server as following:

	   mvn clean compile exec:java -D exec.args="0.0.0.0 4321"

   * arguments(args) can be yours (you need to enter the `host` and `port`), and you can omit them (the server will run with these settings is the default).
   
3. Open client folder in console or terminal;
4. Run client as following:

	   mvn clean compile exec:java -D exec.args="http://localhost:4321/chat?wsdl"

   * arguments may be yours, but you need to enter the `url` of wsdl location according to address which the server is running; 
   * you can omit them (the client will run with `http://localhost:4321/chat?wsdl`).

## Commands format:

#### `ping`
Testing connection (no parameters).

#### `echo`
Testing sending message. Enter the command and message for echo:

    echo message for testing

#### `login`
Log in on server or create new user. Has 2 parameters (login, password):

    login user_login user_password

#### `list`
Displays active users (no parameters).

#### `msg`
Send message to user. Has 2 parameters (recipient login, message(string)):

    msg to_user text message for another user

#### `file`
Send file to user. Has 2 parameters (recipient login, path to file):

    file to_user /path/to/file

#### `exit`
Shutdown the client (no parameters);


### Bonus task:

When someone else logs in while your application is running, your application automatically send “Hello there, \<username\>”;