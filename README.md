# code-path-week8
Code Path Week 8 Project: Pentesting Live Targets
# Project 8 - Pentesting Live Targets

Time spent: 4 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection
In this case a user can use the command %27%20OR%20SLEEP(5)=0--%27 when setting the ID. 
This causes the page to take 5 seconds to change and defaults back to the first user David Burke.

![alt text](https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/3.gif)


Vulnerability #2:  Session Hijacking/Fixation
If you log in to the red you can change to blue and the program will stay logged in.

![alt text](https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/5.gif)


## Green

Vulnerability #1: Username Enumeration
If you enter the name like pperson and a random password the error message is bold,
 but it you enter a random user name like david the error message is not bold. The errors
 makes it easier for users to figure out which usernames work.  
 
 ![alt text](https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/2.gif)

Vulnerability #2: Cross-Site Scripting 
The problem with this one is if you enter a alert message into the Contact Us comment section you
will see it everytime you click on the contact messages as admin. 

![alt text](https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/4.gif)


## Red

Vulnerability #1: Insecure Direct Object Reference
When click on the names of the sales persons you will notice a ID = #.  If you change the number
from 1-9 you can see each of the Salespersons. If you put in number 10 you will see a person not 
listed find a salesperson page.  

![alt text]( https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/1.gif)

Vulnerability #2:CSRF
You can spoof a POST request that utilizes the user's session ID to forge a request to the 
database. When you execute that POST request you can edit salesperson information. 
When you return to the sales list you will see the changed salesperson.

![alt text](https://raw.githubusercontent.com/Jasminebuckhalter/code-path-week8/master/7.gif)


## Notes

Describe any challenges encountered while doing the work
