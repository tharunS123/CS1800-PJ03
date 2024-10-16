# PJ 03 - Handout

----

- Description
- Instructions
- Testing
- Submit

---- 

### Description

<p>Dear Recordkeeping And Information Security Administration (RAISA) employee,

At the request of the O5 Overseer council, you are hereby tasked with a complete overhaul of the Secure, Contain, Protect (SCP) Foundations database systems. Due to an SCP containment breach, multiple data records have been potentially contaminated. It is of the utmost importance that a new database system be brought into service immediately, and any contaminated data logged in the system. Instructions for completion of your task follow.

You will be writing 4 class files and a java program. A database class named FoundationDatabase.java that will store information on SCPs and Foundation Researchers represented by two object classes SCP.java  and Researcher.java. You will need a special exception class named BadDataException.java  that extends Exception. Lastly, you will write a java program called TheSCPFoundation.java  that will run the database and process inputs from multiple text files.

There will be no System.in inputs nor System.out outputs.  All interaction with the program will happen through the text files “input.txt”, “scpIn.txt”, “researcherIn.txt”, “dataOut.txt”, and “mainOut.txt”. The "input.txt" file name will never change, the other files names should be set using the contents of "input.txt".

You have two weeks to complete this task,
O5 Council mandate – Extreme Urgency

This assignment is based off the SCP Foundation. The SCP Wiki is a collaborative speculative fiction website about the SCP Foundation, a secretive organization that contains anomalous or supernatural items and entities away from the eyes of the public. For this assignment some aspects of the individual SCP entries were randomly generated and may not match that of the original entry and all researcher entries were randomly generated. All instances of UTF-8 characters in object names where replaced with ASCII characters to prevent conversion errors.

Content relating to the SCP Foundation, including the SCP Foundation logo, is licensed under Creative Commons ShareALike 3.0 and all concepts originate from https://scpwiki.com/ and its authors. This assignment being derived from this content, is hereby also released under Creative Commons ShareAlike 3.0.

Note: 5 points of your grade is based on Coding Style.  You will need to update the Starter Code to follow the standards described on Brightspace. Use the "Run" button to check your Coding Style without using a submission.</p>

----

### Instructions

<p>Javadocs for all required class are provided HERE.

The recommend order to write the classes in is as follows:

- BadDataException.java
- Researcher.java
- SCP.java
- FoundationDatabase.java
- TheSCPFoundation.java</p>

#### Example String
##### All valid SCP classifications (objectClass):

```
"SAFE", "EUCLID", "KETER", "THAUMIEL", "NEUTRALIZED", "DECOMMISSIONED", "APOLLYON", "ARCHON"
```

##### Researcher toString()
```
Name,idNumber,clearance,classification,active
Binh Esteban,624876107,5,A,true
```

##### SCP toString()
```
"SCP-",itemNumber,objectName,objectClass,clearanceLevel,contact
SCP-105,"Iris",SAFE,3,false
Note: "" around objectName are not guaranteed.
SCP-186,To End All Wars,EUCLID,1,true
```

##### input.txt example: 
```
scpIn.txt researcherIn.txt dataOut.txt mainOut.txt
1
2
3
6
105
Marcus Castañeda,791370344,4,B,true
7
```

<p>This input.txt has 4 files - 3 for the creation of FoundationDatabase and another to print the results of running the main method.

Note the lines that follow the command "6" are the inputs required to call the method in FoundationDatabase as indicated by 6. In this case they are an int 105 and a String representing a Researcher.

A copy of input.txt, scpIn.txt, and researcherIn.txt have been provided.

example outputs:</p>

###### mainOut: 
```
Foundation Database Started
1 Success
2 Success
3 Failure
6 Success
7 Success
```
###### dataOut.txt: 
```
SCP-105,"Iris",SAFE,3,false,Conner Hiley,275363218,3,D,true,Marcus Castañeda,791370344,4,B,true
SCP-133,Instant Hole,SAFE,4,false,Hector Estacio,42903901,4,A,true
SCP-141,Codex Damnatio,SAFE,2,false,Genaoveva Victoria,703623549,2,A,true
SCP-176,Observable Time Loop,EUCLID,3,false,Seth Enbody,364440049,3,A,true
SCP-186,To End All Wars,EUCLID,1,true,Solomon Basilio,14231368,1,D,true
SCP-265,Black Volga,EUCLID,5,true,VACANT
SCP-327,Not Found,EUCLID,1,true,Kimberly Madera,586995719,1,D,true
SCP-340,Viral Rebreather Membrane,SAFE,1,false,Lenel Malik,7569754,1,D,true
SCP-489,1-555-BUG-BASH,EUCLID,2,true,Ida Finn,909779603,2,C,true
SCP-607,Dorian the Grey Cat,EUCLID,1,false,Celeste Sanjuan,17708213,1,A,true
SCP-698,Judgmental Turtle,EUCLID,5,false,Binh Esteban,624876107,5,A,true
SCP-768,Long-Range Alarm Clock,SAFE,3,true,Jesper Carr,192430489,5,B,true
SCP-841,Reverse Mirror Voodoo Doll Stick Puppet,SAFE,2,false,Amor Sandrian,299997685,2,A,true
SCP-936,Fruit of Man,EUCLID,5,true,VACANT
SCP-969,Brand Mosquito Repellent,EUCLID,2,true,Viven Kartman,780159039,2,C,true
```

### Additional notes: 
- You should not assume all file contents will be valid.
- You should not assume all file contents will be valid.
- Test files can be of any length.
- For SCP and Researcher constructors data resulting in empty fields should be considered invalid, unless otherwise specified.
- Infinite loops will always fail a test case.
- You should assume that all inputs and outputs are case sensitive unless otherwise specified.
- Once a file is read into FoundationDatabase.java the order should not change.
- TheSCPFoundation.java should NEVER crash nor should it throw any Exceptions.

----

### Testing
<p>We have included a RunLocalTest.java file that will check that your constructors for each class are correct. It will then run 2 tests: one to verify that the FoundationDatabase.java class correctly wrote the contents of the database to the file "dataOut.txt" and a second to confirm that TheSCPFoundation.java main method correctly writes to "mainOut.txt".

Take a look at RunLocalTest.java. Read through it and try and understand what it is doing. We do not expect you to completely understand its functionality but you should have a general ideal as to what it is trying to accomplish. The RunLocalTest.java rewrites "input.txt" on each run, if you want to test the program with different input you will need to modify the RunLocalTest.java code, not the "input.txt" file itself.

You can modify the RunLocalTest.java to test any method you like by following the same format. You can either download the program and run the main method or use the "Run" button on Vocareum to run the test. You can repeat this process for each path. </p>

----

### Submit
<p>After testing your solution and verifying that it meets the requirements described in this document, you can submit on Vocareum.  You have 10 submissions. This project is due on Oct 28 at 11:59 PM. After which you may submit the project late for a 10% penalty per day late.</p>