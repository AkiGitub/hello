# Final Project CS50P: Your Heart/Liver in Risk Or NOT

Test My Regular express: https://pythex.org

[Video]()

## Defination
This project based on the user lab data, detect the pateint is in fatty liver or heart diseasse.
All the lab and user inforamtion saved in database.

Files of Project:

project.py

test_project.py

ErrorLog.py

DynamicDB.py

Services.py

PatientPart.py

LabinofPart.py

ResultPart.py

requirements.txt

README.md

Schematic of the project::

(mainMenu) ---> (project) ---> {PatientPart,LabinofPart,ResultPart} <---> (Services(Services_patient,Services_Labinfo)) <---> (DynamicDB)

## Loging Of the Error(s)
All errors of the project were saved in the file(s) located at Errors/error_(date now).txt 

As seen: The location of the error is shown, for example, in the class deleteRecord, in the function deleteRecord, along with the error message.

As an example:

Error in Class/Function:( DB: deleteRecord )=====================================

time: 15:35:07

Error Message :Incorrect number of bindings supplied. The current statement uses 1, and there are 3 supplied.


## dynamic database

create the object with database name and table name and can insert/update/select/delete from database

the middle calss(,) are know the filelds and pass to the this class

for expmle `InsertData(self,tableName,**fields):` user can put any field based on the table

# Usage
with: python project.py : user sees the main menu as:
```
               =================== Main Menu ===================
___________________________ Liver/Heart in Risk ______________________________
1. Patients Entry Operations
2. Labratories Data Operation
3. The Patient's Laboratory Result
4. Exit
_______________________________________________________________________________
Please select an option (1-4):
```


when press the wrong the programs shows:  your choice is not in the list

when press 1:

```
========================== Pateints Operations ===================
1. Show Patient List (10 Patients)
2. Insert Patient Data
3. Update Patient Data
4. Delete Patient Data
5. Back to the Main Menu
======================================================================
Please select an option (1-5):
```

 with press 2 user can add patient infromation: 
```
Enter Patient Code: 1
Enter Patient Name: davai 
Enter Patient Family: goaly
Enter Patient Age: 23 
Enter Patient Gender(male/female): male
Enter Patient Tel: 45456
Press Enter to continue...
```

to show result press 1 in the patient part:

```
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|     1     |    davai     |     goaly     |   23   |   male    | 45456  |
|    23     |     mina     |     jefri     |   34   |  female   | 345345 |
+-----------+--------------+---------------+--------+-----------+--------+
```

Press Enter to continue...

for updating press 3:
```
Selcet from list is based on the condiotion(ex: PateintID=1)
Enter Condition: 
```

user can enter condition like PatAge>20

```
Enter Condition: PatAge>20
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|     1     |    davai     |     goaly     |   23   |   male    | 45456  |
|    23     |     mina     |     jefri     |   34   |  female   | 345345 |
+-----------+--------------+---------------+--------+-----------+--------+
You must selected just one Row
Enter Condition:
```
As seen, for udadating only one row of the table is needed. Therefore, the user must select a condition that 
result in a single row

now we Enter `PateintID=1`

and the program shows: 

```
Enter Condition: PateintID=1
You select this Patient:
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|     1     |    davai     |     goaly     |   23   |   male    | 45456  |
+-----------+--------------+---------------+--------+-----------+--------+
Enter Pateint Updating Data===========================================
Enter Patient Code: 2
Patient Already inserted, You cannot use other one code
Enter Patient Code: 23
Enter Patient Name: new name 
Enter Patient Family: new family
Enter Patient Age: 34
Enter Patient Gender(male/female): male
Enter Patient Tel: 456456
Record Updated
Press Enter to continue...

```
But in Deleting the data, you can choice more than one row:

```
Enter Condition: PatAge>10
You select this Patient:
+-----------+--------------+---------------+--------+-----------+---------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel  |
+-----------+--------------+---------------+--------+-----------+---------+
|     2     |     Mina     |     darr      |   34   |  female   | 435345  |
|    23     |    David     |     Jefri     |   23   |   male    | 3453453 |
+-----------+--------------+---------------+--------+-----------+---------+
Are You Sure To delete?("yes"or"y","n"or"no"):y
Record deleted
Press Enter to continue...
```

==================================================================
## Section LAB DATA

```
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+
| PateintID | labID | BMI | TG | BP | HDL | LDL | GLCC | Fpg | HDLC | SGPT | WC | Cholesterol | sbp | dbp | GPT |
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+
|     1     |   2   |  4  | 5  | 6  |  6  |  6  |  6   |  6  |  65  |  5   | 5  |      5      |  5  |  5  |  5  |
|    45     |  45   |  4  | 3  | 4  |  5  |  6  |  23  | 45  |  34  |  34  | 34 |     34      | 34  | 34  | 34  |    
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+    
Press Enter to continue...
```
 insert
```
Patient Lab Info Entry===========================================
Enter Patient Code(must already exist): 2
You must select patient id that already existed in the database
Enter Patient Code(must already exist): 23
Enter Lab ID: 1
Enter BMI(1..70): 1
Enter TG(1..1000): 23
Enter BP(1..200): 23
Enter HDL(1..200): 23
Enter LDL(1..110):0
Your entry must be in 1 and 110
Enter LDL(1..110):23
Enter GLCC(20..300): 34
Enter Fpg(20..300): 34
Enter HDLC(20..150): 34
Enter SGPT(20..700): 34
Enter WC(20.105): 34
Enter Cholesterol(20..70): 34
Enter sbp(1..230): 34
Enter dbp(1..150): 34
Enter GPT(20..1000): 34
Data inserted
Press Enter to continue...
```
update / delete is the same as patient part


==================================================================
## Section Result Part
In this section, user can check the result lab data, and detect he / she in risk is or not

```
==========================  Lab Result (your are Heart/Liver Risk or not) ===================
 ---------------------------(your are Heart/Liver Risk or not) ------------------------------
1. Select Based on the Patient Data
2. Just Enter the Lab Data
3. Back to the Main Menu.
======================================================================
```
User can search base on the index or text(like age>10), that's mean, no need to 
write exact field of database

```
Search based on Field(its number or partof it):
Press q ot Q to Exit
PateintID(0) PatFirstName(1) PatFamilyName(2) PatAge(3) PatGender(4) PatTel(5) 
Enter Search Name/Index: 0
Enter Field PateintID: 23
Your Results is:
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|    23     |     mina     |     jefri     |   34   |  female   | 345345 |
+-----------+--------------+---------------+--------+-----------+--------+
Your LAB Results is:
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+
| PateintID | labID | BMI | TG | BP | HDL | LDL | GLCC | Fpg | HDLC | SGPT | WC | Cholesterol | sbp | dbp | GPT |
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+
|    23     |   1   |  1  | 23 | 23 | 23  | 23  |  34  | 34  |  34  |  34  | 34 |     34      | 34  | 34  | 34  |
+-----------+-------+-----+----+----+-----+-----+------+-----+------+------+----+-------------+-----+-----+-----+
Enter labID:1
 risk factor for heart disease in men and women Risk is High to fatty liver disease Because Of 
( HDL < 40 )
 Press Enter to continue...
 ```
Hint: The patient can have mutliple lab data, therefore the user must choice one of the result based on labID 

## Dynamic Searching
Filtering in the database can be dynamic, such as:
When the user types a name, the list contains two fields: PatFirstName and PatFamilyName. Therefore, the filtering in the database is based on these two fields.

```
PateintID(0) PatFirstName(1) PatFamilyName(2) PatAge(3) PatGender(4) PatTel(5) 
Enter Search Name/Index: name
your search based on :['PatFirstName', 'PatFamilyName']
Enter Field PatFirstName: mina
Enter Field PatFamilyName: jefri
```









