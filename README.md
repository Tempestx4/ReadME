# ReadME

Structure: 
(Neighbourhoods_DB)database - 3 tables: 
1st Table - (Household Information) primary key - owner name, age, and number of people.
2nd Table - (Address) - Primary Key - Street name, Address and Post code.
3rd Table - (House Owner Information) Primary key - Address and the foreign key - Owner name. 
4th Table - (Occupant Information) Primary Key - Occupant ID, Foreign Key - Address, Occupant name and Occupant Age

The first and second are related to the third table through data common to each. 

Schema:
Household Information table
| Owner ID | Owner Name | Age | Number of Occupants | 
|----------|------------|-----|---------------------|
|    01    |Jack Thomson| 52  |         3           |

Location Information Table
|Household ID|          Address        | PostCode|    Street Name    |  
|------------|-------------------------|---------|-------------------|
|     01     |221B BAKER STREET NW1 6XE| NW1 6XE | 221B BAKER STREET | 

House Owner Information Table
|          Address          |  Owner ID  |
|---------------------------|------------|
| 221B BAKER STREET NW1 6XE |     01     |

Occupant Information Table
|Occupant ID|         Address          |Occupant Name|Occupant Age|
|-----------|--------------------------|-------------|------------|
|    01     |221B BAKER STREET NW1 6XE |  Ben Smith  |     50     |

Our API will enable our users to:

-  Store people, houses and addresses (/Ownername=${ownername}&age=${age}&numberofoccupants=${numofoccupants}&Address=${Address}&Postcode=${Postcode}&StreetName=${StreetName})
-  Look up a house, it’s address and owner(/Address=${Address})
-  Look up people in our neighbourhood within certain age brackets and with specific household sizes(/Occupant Age=21&lt41&numberofoccupants=4)

HTTP Verbs - GET & POST


Status Codes - 200 - success, 404 doesnt exist,  201 created