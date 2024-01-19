
# COSMOFURY: A SPACE LEGACY

This is a simple space shuttle game with multiple levels in it. This program uses Python and `mysql.connector` module for connecting the program with the MySQL database to load the user data and levels.
## Screenshots

![App Screenshot](https://github.com/Cyber-Zypher/COSMOFURY/blob/main/Screenshots/Screenshot%202024-01-19%20124131.png?raw=true)

![App Screenshot](https://github.com/Cyber-Zypher/COSMOFURY/blob/main/Screenshots/Screenshot%202024-01-19%20124225.png?raw=true)

![App Screenshot](https://github.com/Cyber-Zypher/COSMOFURY/blob/main/Screenshots/Screenshot%202024-01-19%20124310.png?raw=true)

![App Screenshot](https://github.com/Cyber-Zypher/COSMOFURY/blob/main/Screenshots/Screenshot%202024-01-19%20124354.png?raw=true)




## HOW TO RUN
To run this game, You need to install MySQL and Python on your computer. Then you can clone this repository to your system:
```git
git clone https://github.com/Cyber-Zypher/COSMOFURY.git
```
Then you can go to the downloaded and extracted folder and open it on your IDE.

Now you need to create a database and a table in MySQL. Open MySQL Commandline Client and enter these following commands:
```sql
CREATE DATABASE IF NOT EXISTS GAME
USE GAME
CREATE TABLE IF NOT EXISTS user (
    username VARCHAR(20) NOT NULL,
    password VARCHAR(20) NOT NULL,
    level INT DEFAULT 0,
    PRIMARY KEY (username)
);
```
Go to the file named main.py, and scroll all the way down where you can see these following lines:
```python
if __name__ == "__main__":
    conn = conn = dat.connect(
        host="localhost", user="root", passwd="PASSWD", database="GAME")
    cur = conn.cursor()

    Loginform()
```
Enter your MySQL Credentials correctly and run the `main.py` to play the game.
