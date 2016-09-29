# elective
This script is written in R to distribute students at Faculty of medicine, Alexandria university to their electives based of their choices with priority to students with higher grades.

# How to run it ?

* Download R on your computer for windows from [here](https://cran.r-project.org/bin/windows/base/R-3.3.1-win.exe) and install it (don't change any thing; just next,next...finish).

* Download the R script that I made. Right click on [here](https://raw.githubusercontent.com/ahmedelmahy/elective/master/elective.R) and choose save link as.

* Go to Start->all programs-> R.

* R will open, copy and paste the following:
```R
source(file.choose())
```
A dialog will open choose the R script that you downloaded whose name is 'elective.R' .


## Design the Google Form well.
Design a Google form that has a format like [this](https://docs.google.com/forms/d/e/1FAIpQLSdZWX7qiIEo-gFScxqoMNtq2hnE7jsE7dwIwrjn-adwGxhiuw/viewform), All courses names, A question about the ID and additional questions. After all students have filled the form, download the google form responses as .csv file

# How the program works ?
The program do these steps in order (to improve the program we will just add more steps). the program will ask you in a user friendly way.

1- A dialog will open to choose the csv file that you just downloaded.

2- the program will ask you to enter the number of students needed for every course (Enter 0 if the course was deleted later).

3-the program will ask you to tell him which question contains the IDs of the students.

4-the program will ask you if there is a question of peope to be excluded e.g. those who will take it outside Egypt and the answer to be excluded i.e. 'yes'.

5-the program will count the number of entries and remove dublicated entries (i.e students who filled the form more than one, only their last fill will stay) , the program will report later a list of students who entered more than once to make things accurate.

### Now Enter the marks
You need to have an Excel file containing the results of the students

6-the program will ask you to enter IDs of the students , open the Excel file and copy the IDs of all students whom this elective is for.  then paste it -every ID in a line.

7-the program will ask you to enter IDs of the students whom ID you have just copied, go back to the excel file copy their results. then paste it -every mark in a line corresponding the lines of the IDs (the program will not continue except if that marks correspond to the IDs- Don't worry about students whose marks are  raseb the program also will give them 0 marks and they will be left down and distributed randomly).

8-the program will also show you the IDs beside their marks, make sure the every ID has the marks beside him. Don't edit any thing just close the dialog. If this is not the case , try to investigate, maybe you copied more IDs than marks and close the program and open it again.

9-the program will compare the IDs in the form with the IDs you entered and will reconise IDs that you didn't enter like 'م45'
. The program now asks you to enter a mark for م45 , you have to do something , Either search for his mark and enter it or give him 0 , then he will be distributed randomly like el mota8ybeen wel rasbeen.

10-Now the program will ask you to enter students who you want to be together ;
(The theory is if two students has the same marks and the same choices , they will be together in most cases)
you will enter something like this    19,59    without spaces meaning you want 19 and 59 to be together (the program is user friendly don't fear).


11-the program will search for the two IDs in the form (They both must fill the form ,If one of them didn't he will be distributed randomly). the program will change their marks to the mean mark . and will change their both choices to be the choices of one of them (exactly, the one who submits later).

12-the program will sort marks descendingly.



