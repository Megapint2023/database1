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


OSIO 2 TENTTI 2 TEHTÄVÄ 7













