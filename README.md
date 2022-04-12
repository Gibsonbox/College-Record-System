# College-Record-System
This was my software solution for a college project.

-------------------------------------------------------------------------------------------------
The scenario:
In your role as an IT contractor, you have been tasked with solving a problem for an online college. The college is small and has students around the world working 
various subjects, mostly administration.
The college has grown recently, and the paper record system the owner uses to keep track of data is no longer adequate. To streamline services, the college has provided 
you with the data for 2018 which covers the course offered, the number of enrolments and cost of each course. They wish to be able to extract the following information 
in one computer program.

1) The total number of students
2) The total amount of income generated
3) The average course cost
4) The median course cost
5) The average student number for each course
6) The median student number for each course
7) The option to write the information to a document
----------------------------------------------------------------------------------------------

Design of the program:

I made some assumptions about this scenario as it is very vague. These assumptions were made to  create more function for the program as it would have been very limited 
by only designing what was asked.
One of my assumptions is that new students would need to be enrolled into the college system and so this should be a feature of the program. Another assumption is that 
only an administrator should be using the application so a security should be added in the form of a password. When the statistical calulations have been carried out,  
the option to either print or write the information to a document should be given. Another assumption is that when either enrolment or the calculations have been 
completed, it should return the user to a sort of main menu where they can choose to do either option again.

3 data files have been created so that data can be saved and read from different sessions. These files are 'College Data', 'Student Data', and 'MoL Data'. All 3 files 
will be in CSV file format to minimise storage requirements and allow the program to easily identify data within certain rows and columns. 

The program will be designed as a python application as I am most comfortable within this programming language. When developing with python, I can utilise the 
pandas library which offers productive mathematical tools which will assist with the statistical calculations that are a requirement of the program. The pandas library 
also provides useful formatting tools for printing results to a command window. I can use the python CSV library to easily check for existing data within a CSV file.
The user interface for the application will exist within the command window and inputs will be handled through text entries to this window. Input validation will be 
handled by checking what the user has entered against a list of accepted results. The inclusion or exclusion of a capital letter at the beginning of a data entry will 
be accepted on any decision-making entries, except for the password. If the user fails to enter an accepted entry when asked, they will be repeatedly asked until they 
input an accepted entry.

When the application is started, the command window will open, and the user will have to enter a password. If the user fails to enter the correct password after 3 
attempts, the application will close. After each incorrect attempt, the user will be told they entered the wrong password. When the correct password has been entered, 
a welcome message will appear.

Once the password has been accepted the application decision menu will be presented. This will include 3 options to either: enrol a new student within the college as 
data entries in the Student Data CSV file, to produce statistical calculations from the data within the College Data CSV file, or to exit the program. These options 
will be listed beneath some instructional text and the data entries will be ‘Enrol’, ‘Statistics’, or ‘Exit’. The variations of these inputs will be accepted as 
previously stated. 

By entering ‘Enrol’ the admin is instructed to enter the new student’s first name, the second entry is the new student’s surname, the third entry is the new student’s 
phone number. The fourth entry will be what course they want to enrol within. This entry will be validated to ensure that the data entered is an existing course that 
can be enrolled upon. If the input is not an existing course, then the user will be told and asked to try again. Once all entries have been filled a confirmation is 
given and the process is complete. They will return to the first decision menu.

If the user enters ‘Stats’ the College Data CSV file will be printed to the console. Due to using the pandas library this will be visually formatted in a way which is 
simple to read. This allows the user to see the data they will be using for their calculations. An entry is required to either print the calculations to the console 
or to export them to the MoL Data CSV file. The entries will be ‘Print’ for printing them to the console, or ‘Export’ to export them to the CSV file. All variations 
will be accepted as previously stated. If the entry is not accepted the user will be told and asked to try again.

By entering ‘Print’, the mean course cost, the median course cost, the mean student population, the median student population, the total number of students, and the 
total income generated by the college is printed to the console with line breaks between them to make it easier to read. The user will then be returned to the first 
decision menu. If they enter ‘Export’ the calculations will be saved to the MoL Data CSV file with a ‘MoL Version’ number automatically assigned beneath that heading 
in the CSV file. The user will be told the data has been successfully exported and they will return to the first decision menu.
