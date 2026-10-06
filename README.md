# insertSQLDataPHP

Clone this repo into your documents folder. In the command prompt cd into the repo folder. Make sure that you are "in" the correct folder and that appears in the command prompt. Type ***git clone your-repo-url*** (Get your repo url from github after creating the repo). Then cd into the folder you have just cloned by typing ***cd sswdW4lab-yourgithubid***. Once you are in the correct folder, keep this command window open so you can type in your git commands as required.

Open another command prompt window to run the web server. cd into your repo folder so that the folder name shows in the prompt. Make sure you are "in" your repo folder before running the command to start the webserver.

In lab machine:

***PHP -c "PHP_ext folder" -S localhost:8000 -t ./***

In your PC: 

***PHP -S localhost:8000 -t ./***


Leave this window open as it will be running the webserver. The other command window is where you can issue your git commands.

# Part 1
Open heidisql and connect to the database using the credentials.

username: root
password: Pass4!
port: 3306

Use the sql script in the file CreateDatabase.sql to create the database for this exercise. This is a simple database called tennisclub which will include three tables, Members, |Courts and Bookings along with some test data.

Create a new SQL query window, type ***Select * from Member;*** and execute the query by pressing the "play/execute" button. You should see a list of six members of the tennisclub.

Once the script has been executed and the database has been created, modify the credentials in the insertSQLData.php script so that the correct credentials are used to connect to the database. Make sure the database name has been updated to reflect the database name you have just created "tennisclub". Execute the PHP script in insertSQLData.php by visiting http://localhost/week4Lab-yourGithubID/insertSQLData.php. If the credentials are correct a new Member called John Doe should have been inserted as a Member of the tennisclub.

Once you get this working, commit your code with a good meaningful message and push your code into your repo.

# Part 2
Create a PHP file called Part2.php which contains all the code from insertSQLData.php. 

To add this file to your repo type ***git add .*** and then push your file by typing ***git commit -am 'added Part2.php'*** 

Retrieve the HTML code from the Week3 lab which showed a HTML form with firstname and surname. 

Save this html code to a file in your repo folder called newMember.php. Add and push this file by typing ***git add .*** and then push your file by typing ***git commit -am 'added newMember.html'***

Modify the HTML form so that the "action" in the form tag is "Part2.php" and change the "method" attribute so that the form will use the POST method rather than GET.  

Modify the code in Part2.php so that rather than inserting hard-coded data "John Doe" into the database, the program retrieves the data submitted by the newMember.html form and inserts it into the database as a new member.

Test your code by visiting http://localhost/week4Lab-yourGithubID/newMember.html.

Give the new member's details and submit the form. 

Go to the database HeidiSQL app and type ***select * from Member*** to verify that the Member was inserted into the database.

Once you get this working, commit your code with a good meaningful message and push your code into your repo.

# Part 3
Create a PHP file called Part3.php which contains all the code from insertSQLData.php. To add this file to your repo type ***git add .*** and then push your file by typing ***git commit -am 'added Part3.php'*** 


Look up the Database section under PHP on the w3schools website. On the left bar, scroll down to the MySQL Data section and find the MySQL Select Data example. Make sure you scroll passed the MySQL Object Oriented version of the example to the MySQLi-Procedural version of the example. Take the relevant code from the example (i.e. the SQL query, the command that executes the query and the while loop that outputs the results) and paste this code into your Part3.php file at the appropriate point - i.e. replace the "insert into" aspects of that code reflecting the fact that you will now be pulling data from the db rather than inserting it. You will need to modify the SQL select query and the associative array variables to reflect slightly different column names in the Member table of your database.

Test your code by visiting http://localhost/sswdw4Lab-yourGithubID/Part3.php. The code should show members of the database displayed on the screen in list form separated by commas.

Once you get this working, commit your code with a good meaningful message and push your code into your repo.



