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

shmatci of project:

mainMenu ---> project ---> {PatientPart,LabinofPart,ResultPart} --->Services(Services_patient,Services_Labinfo)  ---> DynamicDB.py 

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

========================== Pateints Operations ===================

1. Show Patient List (10 Patients)

2. Insert Patient Data

3. Update Patient Data

4. Delete Patient Data

5. Back to the Main Menu

======================================================================

Please select an option (1-5):

 with press 2 user can add pateint infromation: 

Enter Patient Code: 1

Enter Patient Name: davai 

Enter Patient Family: goaly

Enter Patient Age: 23 

Enter Patient Gender(male/female): male

Enter Patient Tel: 45456

Press Enter to continue...

to show result press 1 in the patient part:

```python
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|     1     |    davai     |     goaly     |   23   |   male    | 45456  |
|    23     |     mina     |     jefri     |   34   |  female   | 345345 |
+-----------+--------------+---------------+--------+-----------+--------+
```

Press Enter to continue...

for updating press 3:

Selcet from list is based on the condiotion(ex: PateintID=1)

Enter Condition: 

user can enter condition like PatAge>20

Enter Condition: PatAge>20

You select this Patient:

```python
+-----------+--------------+---------------+--------+-----------+--------+
| PateintID | PatFirstName | PatFamilyName | PatAge | PatGender | PatTel |
+-----------+--------------+---------------+--------+-----------+--------+
|     1     |    davai     |     goaly     |   23   |   male    | 45456  |
|    23     |     mina     |     jefri     |   34   |  female   | 345345 |
+-----------+--------------+---------------+--------+-----------+--------+
```

You must selected just one Row

Enter Condition:

As seen, for udadating only one row of the table is needed. Therefore, the user must select a condition that 
result in a single row

now we Enter `PateintID=1`

and the program shows: 

```python
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













