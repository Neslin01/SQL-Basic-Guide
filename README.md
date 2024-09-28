1.
SELECT *FROM crime_scene_report WHERE type='murder' AND date='20180115' AND city='SQL City'
Output:

![image](https://github.com/user-attachments/assets/ac42761f-8931-4ab1-a6f5-ecab18da8ab8)



2.
SELECT * FROM person
  where address_street_name='Northwestern Dr'
  order by address_number DESC   
Output:

![image](https://github.com/user-attachments/assets/ff913a58-927c-496c-8662-fd3eb6e887e6)




3. 
SELECT * FROM person WHERE address_street_name='Franklin Ave' And name like 'Annabel%';
Output:

![image](https://github.com/user-attachments/assets/765e5ad6-a427-487b-98b5-920c3b2da5a1)


id
name
license_id
address_number
address_street_name
ssn
16371
Annabel Miller
490173
103
Franklin Ave
318771143



4.
SELECT * FROM interview WHERE person_id in ('14887','16371');

Output:

person_id
transcript
14887
I heard a gunshot and then saw a man run out. He had a "Get Fit Now Gym" bag. The membership number on the bag started with "48Z". Only gold members have those bags. The man got into a car with a plate that included "H42W".
16371
I saw the murder happen, and I recognized the killer from my gym when I was working out last week on January the 9th.


5.
Select* from get_fit_now_check_in WHERE membership_id like'48Z%'and check_in_date='20180109'
Output:

membership_id
check_in_date
check_in_time
check_out_time
48Z7A
20180109
1600
1730
48Z55
20180109
1530
1700


6. 
Select* from get_fit_now_member WHERE id in ('48Z7A','48Z55');
Output:

id
person_id
name
membership_start_date
membership_status
48Z55
67318
Jeremy Bowers
20160101
gold
48Z7A
28819
Joe Germuska
20160305
gold

7. 
Select* from person where id in ('67318','28819');

Output:

id
name
license_id
address_number
address_street_name
ssn
28819
Joe Germuska
173289
111
Fisk Rd
138909730
67318
Jeremy Bowers
423327
530
Washington Pl, Apt 3A
871539279


8.
Select * from drivers_license where id in ('173289','423327');

Output:

id
age
height
eye_color
hair_color
gender
plate_number
car_make
car_model
423327
30
70
brown
brown
male
0H42W2
Chevrolet
Spark LS


9.
Did you find the killer?
1
INSERT INTO solution VALUES (1, 'Jeremy Bowers');
SELECT value FROM solution;
value
Congrats, you found the murderer! But wait, there's more... If you think you're up for a challenge, try querying the interview transcript of the murderer to find the real villain behind this crime. If you feel especially confident in your SQL skills, try to complete this final step with no more than 2 queries. Use this same INSERT statement with your new suspect to check your answer.




10.
Select* from drivers_license where hair_color='red' and gender='female' and car_make='Tesla ' and car_model= 'Model S' ;

Output:

id
age
height
eye_color
hair_color
gender
plate_number
car_make
car_model
202298
68
66
green
red
female
500123
Tesla
Model S
291182
65
66
blue
red
female
08CM64
Tesla
Model S
918773
48
65
black
red
female
917UU3
Tesla
Model S



11.
Select* from person where license_id in ('202298','291182','918773');

Output:

id
name
license_id
address_number
address_street_name
ssn
78881
Red Korb
918773
107
Camerata Dr
961388910
90700
Regina George
291182
332
Maple Ave
337169072
99716
Miranda Priestly
202298
1883
Golden Ave
987756388


12.
Select* from facebook_event_checkin where person_id in ('78881','90700','99716');

Output:

person_id
event_id
event_name
date
99716
1143
SQL Symphony Concert
20171206
99716
1143
SQL Symphony Concert
20171212
99716
1143
SQL Symphony Concert
20171229



13.
Did you find the killer?
1
INSERT INTO solution VALUES (1, 'Miranda Priestly');
SELECT value FROM solution;
value
Congrats, you found the brains behind the murder! Everyone in SQL City hails you as the greatest SQL detective of all time. Time to break out the champagne!


