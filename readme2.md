
# Final Project CS50P: Your Heart/Liver in Risk Or NOT

Test My Regular express:https://pythex.org

[Video]()

## Defination
This project based on the user lab data, detect the pateint is in fatty liver or heart diseases.
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

## Looging Of the Error(s)
All error(s) occured in the project saved in file(s) in Errors/error_(data now).txt 
as seen: Show the location of error, for exmaple in class in funvtion deleteRecord with the error message

as an example:

Error in Class/Function:( DB: deleteRecord )=====================================

time: 15:35:07

Error Message :Incorrect number of bindings supplied. The current statement uses 1, and there are 3 supplied.


## dynamic database
create the object with database name and table name and can insert/update/select/delete from database
the middle calss(,) are know the filelds and pass to the this class

for expmle `InsertData(self,tableName,**fields):` user can put any field based on the table

# Usages

               =================== Main Menu ===================

___________________________ Liver/Heart in Risk ______________________________ 

1. Patients Entry Operations

2. Labratories Data Operation

3. The Patient's Laboratory Result

4. Exit
_______________________________________________________________________________

Please select an option (1-4):

Please select an option (1-4):

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










