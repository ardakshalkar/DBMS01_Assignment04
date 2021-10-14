## How to answer?
Write your query into file answers.md

# Problem 01

**P01.A** Find Customers who are also Staff by comparing First Name, Last Name

|first_name|last_name|
|----------|---------|
|BARBARA|JONES|
|LINDA|WILLIAMS|
|MARY|SMITH|
|PATRICIA|JOHNSON|

---

**P01.B** Find Staff who are not Customers

|first_name|last_name|
|----------|---------|
|JON|STEPHENS|
|MIKE|HILLYER|

---
**P01.C** You need to display all Customers and Staff
|first_name|last_name|
|----------|---------|
|AARON|SELBY|
|ADAM|GOOCH|
|ADRIAN|CLARY|
|AGNES|BISHOP|
|...|...|
|ZACHARY|HITE|


# Problem 02

**P02.A**  
We have table `rental`, which contains information about film rental (especially `rental_date` which contains date and time of renting).

Now you have to find average number of rents, and minimum, maximum for each day of week, as if it is shown in table below:


|weekday|average|count|min|max|
|--:|--:|--:|--:|--:|
|0|464.0|5|154|679|
|1|449.4|5|158|671|
|2|223.9090909090909|11|8|643|
|3|446.2|5|137|649|
|4|440.0|5|174|621|
|5|454.4|5|166|641|
|6|462.2|5|196|634|

## How to do it?
You have to use `subquery`, which counts how many times items were rent on each day, and display its weekday by index (Friday, Saturday etc.)

Based on this `subquery`, display resulting table.

### Extra information:
To get only date from field you should use `date(fieldname)` where fieldname is placeholder for real field name.

To get weekday from field you should use `strftime('%w',fieldname)` which displays number between 0 and 6, where 0 is Sunday.

______

**P02.B**  
Write query that will show last 5 customers who rent items. Like in table below:

|customer_id|first_name|last_name|
|-----------|----------|---------|
|75|TAMMY|SANDERS|
|187|BRITTANY|RILEY|
|195|VANESSA|SIMS|
|263|HILDA|HOPKINS|
|466|LEO|EBERT|


This can be done by writing subquery that outputs customer ids from last 5 rentals.
To get last 5 rentals you can order rentals by rental date and limit (by LIMIT command) them by 5 results. 
By using subquery above we can display all their names

# Problem 03

**P03.A**  
Show actors that participated in Comedy movies  
`'Comedy'` should be in query.  
This can be done with subquery or joins




|film_id|title|description|
|--:|:--|:--|
|7|AIRPLANE SIERRA|A Touching Saga of a Hunter And a Butler who must Discover a Butler in A Jet Boat|
|28|ANTHEM LUKE|A Touching Panorama of a Waitress And a Woman who must Outrace a Dog in An Abandoned Amusement Park|
|99|BRINGING HYSTERICAL|A Fateful Saga of a A Shark And a Technical Writer who must Find a Woman in A Jet Boat|
|119|CAPER MOTIONS|A Fateful Saga of a Moose And a Car who must Pursue a Woman in A MySQL Convention|
|...|...|...|
|1000|ZORRO ARK|A Intrepid Panorama of a Mad Scientist And a Boy who must Redeem a Boy in A Monastery|


---

**P03.B**  
Display movies with actress with name 'Julia'  
`'Julia'` should be in query.  
This can be done with subquery or joins


|film_id|title|description|
|-------|-----|-----------|
|19|AMADEUS HOLY|A Emotional Display of a Pioneer And a Technical Writer who must Battle a Man in A Baloon|
|34|ARABIA DOGMA|A Touching Epistle of a Madman And a Mad Cow who must Defeat a Student in Nigeria|
|85|BONNIE HOLOCAUST|A Fast-Paced Story of a Crocodile And a Robot who must Find a Moose in Ancient Japan|
|150|CIDER DESIRE|A Stunning Character Study of a Composer And a Mad Cow who must Succumb a Cat in Soviet Georgia|
|172|CONEHEADS SMOOCHY|A Touching Story of a Womanizer And a Composer who must Pursue a Husband in Nigeria|
|273|EFFECT GLADIATOR|A Beautiful Display of a Pastry Chef And a Pastry Chef who must Outgun a Forensic Psychologist in A Manhattan Penthouse|
|...|...|...|
|953|WAIT CIDER|A Intrepid Epistle of a Woman And a Forensic Psychologist who must Succumb a Astronaut in A Manhattan Penthouse|




