# database1
Database basics

OSIO 2 TEHTÄVÄ 1

SELECT * FROM goal;
![O2T1](https://github.com/user-attachments/assets/46af8304-cccd-4993-aa9a-7b14a1cc6caa)

OSIO 2 TEHTÄVÄ 2

SELECT name, type FROM airport WHERE iso_country = "FI" LIMIT 10;
![O2T2](https://github.com/user-attachments/assets/c45e6817-8797-4f4a-a5cd-7b5da8346e1d)

OSIO 2 TEHTÄVÄ 3

SELECT name FROM airport WHERE iso_country = "FI" ORDER BY name ASC LIMIT 10;
![O2T3](https://github.com/user-attachments/assets/95438b6a-4923-4c2f-866f-2ff3db4a6703)

OSIO 2 TEHTÄVÄ 4

SELECT name, type FROM airport WHERE iso_country = "FI" ORDER BY type LIMIT 10;
![O2T4](https://github.com/user-attachments/assets/c3058645-d6d8-4641-b2bc-2c16ce892010)

OSIO 2 TEHTÄVÄ 5 

SELECT name FROM country WHERE name LIKE 'F%';

![O2T5](https://github.com/user-attachments/assets/e6040b9e-4dd2-4684-bf07-ebdfbcd46d73)

OSIO 2 TEHTÄVÄ 6

SELECT name FROM country WHERE name LIKE '%F%';

![O2T06](https://github.com/user-attachments/assets/3151484a-1d81-4d72-a0f1-664f8912ff91)

OSIO 2 TEHTÄVÄ 7

SELECT location FROM game WHERE screen_name = "Vesa";
![O2T7](https://github.com/user-attachments/assets/d209f938-0fe6-46d0-a8cf-494fa6f69ba4)

OSIO 2 TEHTÄVÄ 8

SELECT co2_consumed from game WHERE screen_name = "Ilkka";
![O2T8](https://github.com/user-attachments/assets/3409c8ac-c458-4162-9d0c-d17debb7488d)

OSIO 2 TEHTÄVÄ 9

SELECT distinct co2_budget FROM game;

![O2T9](https://github.com/user-attachments/assets/36741265-71d4-49b7-a39f-71edc46e260b)

# OSIO 2 TENTTI 2

OSIO 2 TENTTI 2 TEHTÄVÄ 1

SELECT country.name as "country name", airport.name as "airport name" from airport, country 
WHERE airport.iso_country = country.iso_country and country.name = "Iceland";

![O2 2T1](https://github.com/user-attachments/assets/d2f2bce3-4522-4aee-93df-e23a400f24ca)


OSIO 2 TENTTI 2 TEHTÄVÄ 2

SELECT airport.name AS "airport name"                              
FROM airport #valitsee pää tietokannan
JOIN country ON airport.iso_country = country.iso_country           
WHERE country.name = "France" AND airport.type = "large_airport";  


![O2 2T2](https://github.com/user-attachments/assets/f76765a7-8598-4edb-a975-361806b91ac0)


OSIO 2 TENTTI 2 TEHTÄVÄ 3

SELECT 'Antarctica' AS "country_name", airport.name AS "airport_name"
    -> FROM airport 
    -> JOIN country ON airport.iso_country = country.iso_country
    -> WHERE country.name = 'Antarctica';

![O2 2T3](https://github.com/user-attachments/assets/18da6bd4-4f8c-4770-8804-8740561cab10)


OSIO 2 TENTTI 2 TEHTÄVÄ 4

SELECT airport.elevation_ft AS "elevation_ft" 
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = "Heini";

![O2 2T4](https://github.com/user-attachments/assets/410e24ff-118a-464e-979c-97c3f73c3b1c)


OSIO 2 TENTTI 2 TEHTÄVÄ 5

SELECT airport.elevation_ft * 0.3048 AS "elevation_m" 
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = "Heini";

![O2 2T5](https://github.com/user-attachments/assets/049114a8-eeb7-43ee-92aa-9521013f72c9)


OSIO 2 TENTTI 2 TEHTÄVÄ 6

SELECT airport.name AS "name" 
FROM airport
JOIN game ON game.location = airport.ident
WHERE game.screen_name = "Ilkka";

![O2 2T6](https://github.com/user-attachments/assets/b68c182c-6076-4d47-bed5-bd6bc93a5fc5)


OSIO 2 TENTTI 2 TEHTÄVÄ 7

SELECT country.name AS "name" 
FROM game
JOIN airport ON game.location = airport.ident
JOIN country ON airport.iso_country = country.iso_country
WHERE game.screen_name = "Ilkka";

![O2 2T7](https://github.com/user-attachments/assets/d9099a56-69b7-4326-9d08-05b71419dec3)


OSIO 2 TENTTI 2 TEHTÄVÄ 8

SELECT name
FROM goal, goal_reached, game
WHERE game.id = game_id 
AND goal.id = goal_id 
AND screen_name = "Heini";

![O2 2T8](https://github.com/user-attachments/assets/dd6052b3-f7f7-4a6c-8680-f0e747dad944)


OSIO 2 TENTTI 2 TEHTÄVÄ 9

SELECT airport.name AS "name"
FROM game
JOIN goal_reached ON game.id = goal_reached.game_id
JOIN goal ON goal_reached.goal_id = goal.id
JOIN airport ON game.location = airport.ident
WHERE game.screen_name = 'Ilkka';

![OSIO 2 2T9](https://github.com/user-attachments/assets/a52575be-ffc1-443a-be94-8a86ef6ca594)


OSIO 2 TENTTI 2 TEHTÄVÄ 10

SELECT country.name AS "name"
FROM game
JOIN goal_reached ON game.id = goal_reached.game_id
JOIN goal ON goal_reached.game_id = goal.id
JOIN airport ON game.location = airport.ident
JOIN country ON airport.iso_country = country.iso_country
WHERE game.screen_name = "Ilkka";


![O2 2T10](https://github.com/user-attachments/assets/0b445ce1-5d4c-4a80-adf4-9fa074dbe180)


OSIO 3 TENTTI 1 TEHTÄVÄ 1

SELECT country.name AS "country name", 
       airport.name AS "airport name"
FROM airport
JOIN country 
ON airport.iso_country = country.iso_country
WHERE country.name = 'Finland'
  AND scheduled_service = "yes";


![O3T1](https://github.com/user-attachments/assets/8706407e-b484-47a6-a71e-ea20897e624f)


OSIO 3 TENTTI 1 TEHTÄVÄ 2

SELECT game.screen_name AS "screen_name", 
       airport.name AS "name"
FROM game
JOIN airport
ON game.location = airport.ident;

![O3T2](https://github.com/user-attachments/assets/9464f09c-2e3c-474c-bf9c-acb15f423ad9)


OSIO 3 TENTTI 1 TEHTÄVÄ 3

SELECT game.screen_name, 
       country.name AS "name"
FROM game
JOIN airport 
  ON game.location = airport.ident
JOIN country 
  ON airport.iso_country = country.iso_country;


![O3T3](https://github.com/user-attachments/assets/b07adcf9-f900-451e-97c1-e8e61810201e)


OSIO 3 TENTTI 1 TEHTÄVÄ 4

SELECT airport.name AS "name", 
       game.screen_name AS "screen_name"
FROM airport
LEFT JOIN game 
  ON airport.ident = game.location
WHERE airport.name LIKE '%Hels%';


![O3T4](https://github.com/user-attachments/assets/cbda3805-2d4e-4a12-880d-bb4c3f4f8c26)


OSIO 3 TENTTI 1 TEHTÄVÄ 5

SELECT goal.name AS "name", 
       game.screen_name AS "screen_name"
FROM goal
LEFT JOIN goal_reached 
  ON goal.id = goal_reached.goal_id
LEFT JOIN game 
  ON goal_reached.game_id = game.id;

  
![O3T5](https://github.com/user-attachments/assets/2bacbfc0-1f7b-4b60-81e3-230c1059b19e)


OSIO 3 TENTTI 2 TEHTÄVÄ 1

SELECT name
FROM country
WHERE iso_country IN (
    SELECT iso_country
    FROM airport
    WHERE name LIKE 'Satsuma%'
);


![O3T2T1](https://github.com/user-attachments/assets/acefe980-f81d-41c8-9c9e-6a46a7abf7f5)


OSIO 3 TENTTI 2 TEHTÄVÄ 2

SELECT airport.name
FROM airport
JOIN country 
  ON airport.iso_country = country.iso_country
WHERE country.name = 'Monaco';


![O3T2T2](https://github.com/user-attachments/assets/f312c1ea-0fba-473d-8c41-359d6967f65f)


OSIO 3 TENTTI 2 TEHTÄVÄ 3

SELECT game.screen_name
FROM game
JOIN goal_reached 
  ON game.id = goal_reached.game_id
JOIN goal 
  ON goal_reached.goal_id = goal.id
WHERE goal.name = 'CLOUDS';


![O3T2T3](https://github.com/user-attachments/assets/b340a61f-7f5d-4744-98f1-d84c1d4f12c7)


OSIO 3 TENTTI 2 TEHTÄVÄ 4

SELECT name 
FROM country
WHERE iso_country NOT IN (
    SELECT iso_country 
    FROM airport
);

![O3T2T4](https://github.com/user-attachments/assets/0e8bb076-49d7-4c58-876e-34150b0f6b85)


OSIO 3 TENTTI 2 TEHTÄVÄ 5 

MariaDB [flight_game]> SELECT name FROM goal WHERE id NOT IN (
SELECT goal.id
FROM goal, goal_reached, game
WHERE game.id = goal_reached.game_id
AND goal.id = goal_reached.goal_id
AND game.screen_name = "Heini"
);

![O3T2T5](https://github.com/user-attachments/assets/990ea63b-3127-413f-b3a2-a80bc35d1d89)


OSIO 4 

OSIO 4 TENTTI 1 TEHTÄVÄ 1

![Screenshot 2024-09-23 at 22 12 26](https://github.com/user-attachments/assets/ab58dc2a-ecdd-45c1-ad63-85ddbcca58e4)

SELECT max(elevation_ft)
FROM airport;


![O4T1T1](https://github.com/user-attachments/assets/023a4b07-f29d-41a8-a4a1-bd93a5f2387a)


OSIO 4 TENTTI 1 TEHTÄVÄ 2

![Screenshot 2024-09-23 at 22 13 00](https://github.com/user-attachments/assets/8f9d93ae-58d7-439a-b9ad-cca5f0523021)

SELECT continent, count(*) 
FROM country
GROUP BY continent;


![O4T1T2](https://github.com/user-attachments/assets/4eb90310-ac24-43a2-9a43-5f11c200a597)


OSIO 4 TENTTI 1 TEHTÄVÄ 3

![Screenshot 2024-09-23 at 22 13 55](https://github.com/user-attachments/assets/584b3d64-37fe-4d28-a9ed-be597c601f2a)

SELECT screen_name, COUNT(*)
FROM game, goal_reached
WHERE game.id = goal_reached.game_id
GROUP BY screen_name;


![O4T1T3](https://github.com/user-attachments/assets/e1ae965c-36d9-46f9-a185-55e25191f1ba)


OSIO 4 TENTTI 1 TEHTÄVÄ 4

![Screenshot 2024-09-23 at 22 14 23](https://github.com/user-attachments/assets/a953d540-14e5-4392-9ce9-6c5de41cb86a)

SELECT screen_name
FROM game
WHERE co2_consumed = (
SELECT MIN(co2_consumed) 
FROM game);


![O4T1T4](https://github.com/user-attachments/assets/5d96dd45-48f9-4958-aaea-7eed1fb01d32)


OSIO 4 TENTTI 1 TEHTÄVÄ 5

![Screenshot 2024-09-23 at 22 10 36](https://github.com/user-attachments/assets/31ba3b9c-e838-4f82-a027-a59e3a883722)

SELECT country.name, COUNT(*)
FROM airport, country
WHERE airport.iso_country = country.iso_country
GROUP BY country.iso_country
ORDER BY COUNT(*) DESC
LIMIT 50;


![O4T1T5](https://github.com/user-attachments/assets/e1879b75-2257-45c7-b476-b76e7c2d7f9e)


OSIO 4 TENTTI 1 TEHTÄVÄ 6

![Screenshot 2024-09-23 at 22 16 11](https://github.com/user-attachments/assets/ca32f8ec-59b8-44b1-b5c2-0e4a3308fedb)


SELECT country.name
FROM airport, country
WHERE airport.iso_country = country.iso_country
GROUP BY country.iso_country
HAVING COUNT(*) >= 1000;


![O4T1T6](https://github.com/user-attachments/assets/7fa1b1f2-ec44-4640-a52c-d87769d06083)


OSIO 4 TENTTI 1 TEHTÄVÄ 7

![Screenshot 2024-09-23 at 22 19 26](https://github.com/user-attachments/assets/81036f47-ad76-4083-a0b9-31d9b5fb20ea)

SELECT name
FROM airport
WHERE elevation_ft = (
    SELECT MAX(elevation_ft)
    FROM airport
);


![O4T1T7](https://github.com/user-attachments/assets/0d706dd5-0879-4d1e-9066-2c50fd7829b8)


OSIO 4 TENTTI 1 TEHTÄVÄ 8
















