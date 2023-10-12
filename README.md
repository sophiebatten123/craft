# Setting up a project in craft #
## Follow these steps to set up a project in craft ##

1. Open your terminal and ensure that you are in the sites directory
2. Go to https://github.com/sophiebatten123/craft and clone this repository in the terminal
3. The name of the folder created in the sites directory is how you veiw the site e.g. if the folder is called practice_project you would go to practice_project.test
4. Open the project in VSCode and inside the terminal run composer install
5. Go to sequel ace and create a database in localhost by clicking the drop down then add database.
6. Create a .env file in the project and include the DBNAME used in sequel ace.
7. Run ./craft setup and follow the instructions (ensure that the siteurl is hhtp://practice_project.test/)
8. Login to the craft admin by going to practice_project.test/admin with the user name admin and the password what you just wrote in.