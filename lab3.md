# COMMAND: find
---
**-empty**

is used to find all the empty files in the the current directory, useful for checking if there are unneeded files that could be deleted
or forgotten files that aren't supposed to be empty

```
$ find ./911report -empty

```
after entering the command, the next line is empty because there are no empty files in the 911report directory

```
$ find ./biomed -empty

```
same as the previous case, there are also no empty files in the biomed directory so it prints nothing

---
**-newer**

is used to find files that were made after the given file, good to use if you're using time as a point of reference 
```
$ cd 911report
$ find -newer chapter-3.txt
.
./chapter-6.txt
./chapter-7.txt
./chapter-8.txt
./chapter-9.txt
./preface.txt
$ cd ..
```
found and printed the files made after chapter 3 in the 911report directory, we learn that chapter 5 text file was made before 3.

```
$ cd government
$ find -newer Media
.
./Post_Rate_Comm
./Post_Rate_Comm/Cohenetal_comparison.txt
./Post_Rate_Comm/Cohenetal_Cost_Function.txt
./Post_Rate_Comm/Cohenetal_CreamSkimming.txt
./Post_Rate_Comm/Cohenetal_DeliveryCost.txt
./Post_Rate_Comm/Cohenetal_RuralDelivery.txt
./Post_Rate_Comm/Cohenetal_Scale.txt
./Post_Rate_Comm/Gleiman_EMASpeech.txt
./Post_Rate_Comm/Gleiman_gca2000.txt
./Post_Rate_Comm/Mitchell_6-17-Mit.txt
./Post_Rate_Comm/Mitchell_RMVancouver.txt
./Post_Rate_Comm/Mitchell_spyros-first-class.txt
./Post_Rate_Comm/Redacted_Study.txt
./Post_Rate_Comm/ReportToCongress2002WEB.txt
./Post_Rate_Comm/WolakSpeech_usps.txt
$ cd ..
```
found the files made after Media which is the Post_Rate_Comm file and all the files inside it

---
**-iname**

similar to -iname but isn't case sensitive like -name

```
$ cd 911report
$ find -iname chapter-1.txt
./chapter-1.txt
```
returning the path of the file that contains chapter-1.txt in its name

```
$ find -iname chapTer-1.txt
./chapter-1.txt

$ find -name chapTer-1.txt

```
still returning ./chapter-1.txt while searching for chapTer-1.txt incomparison to -name which returns nothing

---
**-size +N/-N**

finds all the files in the current directory that have a smaller or bigger amount of blocks than the given number

```
$ find -size +200
./chapter-1.txt
./chapter-12.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-3.txt
./chapter-6.txt
./chapter-7.txt
./chapter-9.txt
```
returned all the files in 911report that have more than 200 blocks

```
$ find -size -500
.
./chapter-1.txt
./chapter-10.txt
./chapter-11.txt
./chapter-12.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-2.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-8.txt
./chapter-9.txt
./preface.txt
```
returned all the files in 911report that have less than 200 blocks
