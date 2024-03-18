# Ex03 Time Table
## Date: 14-03-2024

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM
```
<html>
        <head>

            <title> My time table </title>
        </head>
        <body> 
            <img src="logo.png" height="200" width="1200">

            <table border="4" cellspacing="5" cellpadding="4" width="800" height="200">

                <caption> <strong> SLOT TIME TABLE-NITHISH S(212223220070) </caption>

                <tr>
                    <th bgcolor="plum">Day/time</th>
                    <th bgcolor="plum">Monday</th>
                    <th bgcolor="plum">Tuesday</th>
                    <th bgcolor="plum">Wednesday</th>
                    <th bgcolor="plum">Thursday</th>
                    <th bgcolor="plum">Friday</th>
                    <th bgcolor="plum">Saturday</th>
                    </tr>
                <tr>
                    <td bgcolor="plum">8-10</td>
                    <td colspan="4" align="center" bgcolor="BLUE">FREESLOT</td>
                    <td bgcolor="BLUE">FWAD</td>
                    <td bgcolor="BLUE">FREESLOT</td>
                    
                    </tr>

                <tr>
                    <td bgcolor="plum">10-12</td>
                    <td bgcolor="orange">ENG</td>
                    <td bgcolor="orange">C PROG</td>
                    <td bgcolor="orange">MATHS</td>
                    <td bgcolor="orange">C PROG</td>
                    <td bgcolor="BLUE">FREESLOT</td>
                    <td bgcolor="orange">OS</td>
                    
                </tr>

                <tr>
                    <td bgcolor="plum">12-1</td>
                    <td colspan="6" align="center" bgcolor="orange">LUNCH</td>
                  
                    
                </tr>

                <tr>
                    <td bgcolor="plum">1-3</td>
                    <td bgcolor="orange">DS</td>
                    <td bgcolor="orange">FWAD</td>
                    <td bgcolor="orange">ENG</td>
                    <td bgcolor="orange">FWAD</td>
                    <td bgcolor="BLUE">FREESLOT</td>
                    <td bgcolor="orange">MATHS</td>
                    
                </tr>

                <tr>
                    <td bgcolor="plum">3-5</td>
                    <td bgcolor="orange">OS</td>
                    <td colspan="4" align="center" bgcolor="BLUE">FREESLOT</td>
                    
                    <td bgcolor="orange">DS</td>
                    
                </tr>

            </table>


        </body>

</html>



<html>

        <body>

                <table border="1" cellspacing="5" cellpadding="2" width="600" height="300">

                    <tr>

                    <th><strong>S.No.</th>
                    <th><strong>Subject Code</th>
                    <th><strong>Subject Name</th>

                    </tr>


                    <tr>

                        <td>1.</td>
                        <td>19A1304</td>
                        <td>Fundamentals of C Programming (C PROG)</td>

                    </tr>

                    <tr>
                        <td>2.</td>
                        <td>19AI403</td>
                        <td>Introduction to Data Science (DS)</td>
                    </tr>

                    <tr>
                        <td>3.</td>
                        <td>19AI414</td>
                        <td>Fundamentals of Web Application Development (FWAD)</td>
                    </tr>

                    <tr>
                        <td>4.</td>
                        <td>19CS405</td>
                        <td>Operating System (OS)</td>
                    </tr>
                        <td>5.</td>
                        <td>19EN101</td>
                        <td>Communicative English (ENG)</td>

                    </tr>

                    <tr>
                        <td>6.</td>
                        <td>19MA222</td>
                        <td>Probability and Queueing Models (MATHS)</td>
                    </tr>
    
                  </table>



        </body>






</html>

```


## OUTPUT

![alt text](<Screenshot (14).png>)


## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
