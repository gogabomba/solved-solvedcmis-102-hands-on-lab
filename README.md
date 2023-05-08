Download Link: https://assignmentchef.com/product/solved-solvedcmis-102-hands-on-lab
<br>
Week 8 Overview

This hands-on lab allows you to follow and experiment with the critical steps of developing a program including the program description, analysis, test plan, and implementation with C code. The example provided uses sequential, repetition, selection statements, functions, strings and arrays.

Program Description

This program will input and store meteorological data into an array. The program will prompt the user to enter the average monthly rainfall for a specific region and then use a loop to cycle through the array and print out each value. The program should store up 5 years of meteorological data. Data is collected once per month. The program should provide the option to the user of not entering any data.

Analysis

I will use sequential, selection, and repetition programming statements and an array to store data.I will define a 2-D array of Float number: Raindata[][] to store the Float values input by the user. To store up to 5 years of monthly data, the array size should be at least 5*12 = 60 elements. In a 2D array this will be RainData[5][12]. We can use #defines to set the number of years and months to eliminate hardcoding values.A float number (rain) will also be needed to input the individual rain data.

A nested for loop can be used to iterate through the array to enter Raindata. A nested for loop can also be used to print the data in the array.

A array of strings can be used to store year and month names. This will allow a tabular display with labels for the printout.

Functions will be used to separate functionality into smaller work units. Functions for displaying the data and inputting the data will be used.

A selection statement will be used to determine if data should be entered.

Test Plan

To verify this program is working properly the input values could be used for testing:

TestCase

Input

ExpectedOutput

1

Enter data?= y1.2 2.2 3.32.210.212.22.3 0.4 0.2 1.12.1

year 201120112011201120112011201120112011201120112011

monthJanFebMarAprMayJunJulAugSepOctNovDec

rain1.20 2.20 3.302.20 10.20 12.202.30 0.40 0.201.10 2.100.40

0.4 1.1 2.2 3.32.210.212.22.3 0.4 0.21.1 2.1 0.4 1.1 2.2 3.32.210.212.22.3 0.4 0.2 1.1 2.1 0.4 1.1 2.2 3.32.210.212.22.3 0.4 0.21.1 2.1 0.4 1.1 2.2 3.32.210.212.22.3 0.4 0.2 1.12.10.4

201220122012201220122012201220122012201220122012201320132013201320132013201320132013201320132013201420142014201420142014201420142014201420142014201520152015201520152015201520152015201520152015Please trythe Precipit again.

JanFebMarAprMayJunJulAugSepOctNovDecJanFebMarAprMayJunJulAugSepOctNovDecJanFebMarAprMayJunJulAugSepOctNovDecJanFebMarAprMayJunJulAugSepOctNovDec at

1.102.20 3.30 2.2010.20 12.20 2.300.40 0.20 1.102.10 0.40 1.102.20 3.30 2.2010.20 12.20 2.300.40 0.20 1.102.10 0.40 1.102.20 3.30 2.2010.20 12.20 2.300.40 0.20 1.102.10 0.40 1.102.20 3.30 2.2010.20 12.20 2.300.40 0.20 1.102.10 0.40 ion program

2

Enterdata? = n

No data wasinput at this time.

Please try the Precipitation programagain.

C Code

The following is the C Code that will compile inexecute in the online compilers.

// C code

// This program will input and store meteorological data into anarray.

// Developer: FacultyCMIS102

// Date: Jan 31, XXXX

#define NUMMONTHS 12

#define NUMYEARS 5

#include

// function prototypesvoid inputdata(); void printdata();

// Global variables

// These are available toall functions float Raindata[NUMYEARS][NUMMONTHS];

char years[NUMYEARS][5] ={“2011″,”2012″,”2013″,”2014″,”2015”}; char months[NUMMONTHS][12]

={“Jan”,”Feb”,”Mar”,”Apr”,”May”,”Jun”,”Jul”,”Aug”,”Sep”,”Oct”,”Nov”,”Dec”};int main () {

char enterData = ‘y’;

printf(“Do you want to inputPrecipatation data? (y for yes)
”);scanf(“%c”,&amp;enterData);if (enterData == ‘y’) {

// Call Function to Input data inputdata();

// Call Function to display data printdata();

}else {

printf(“No data was input at thistime
”);

}

printf(“Please try the Precipitationprogram again. 
”); return 0;

}

// function to inputdatavoid inputdata() {

/* variable definition: */ float Rain=1.0; // Input Data

for (int year=0;year &lt; NUMYEARS; year++){ for (int month=0; month&lt;NUMMONTHS; month++) {printf(“Enter rain for %d, %d:
”, year+1, month+1); scanf(“%f”,&amp;Rain);

Raindata[year][month]=Rain;

}

}

}

// Function to printdatavoid printdata(){ // Print data

printf (“yeart monthtrain
”); for (int year=0;year&lt; NUMYEARS; year++) { for (intmonth=0; month&lt; NUMMONTHS; month++) { printf(“%st %st%5.2f
”,

years[year],months[month],Raindata[year][month]);

}

}

}

Setting up the code and the input parameters inideone.com:

You can change these values to any valid integervalues to match your test cases.

Results from running the programming at ideone.com

Learning Exercises for you to complete

1.Modify the program to add a function to sum therainfall for each year. (Hint: you need to sum for each year. You can do thisusing a looping structure). Support your experimentation with screen capturesof executing the new code.

2.Enhance the program to allow the user to enter anothermeteorological element such as windspeed (e.g. 2.4 mph). Note, the user shouldbe able to enter both rainfall and windspeed in your new implementation.Support your experimentation with screen captures of executing the new code.

3.Prepare a new test table with at least 2 distinct testcases listing input and expected output for the code you created after step 2.

4.What happens if you change the NUMMONTHS and NUMYEARSdefinitions to other values? Be sure to use both lower and higher values.Describe and implement fixes for any issues if errors results. Support your experimentation with screencaptures of executing the new code.

Grading guidelines

Submission

Points

Successfully demonstrates execution of this lab with onlinecompiler. Includes a screen capture.

2

Modifies the code to add a function to sum the rainfall foreach year. Support your experimentation with screen captures of executing thenew code

2

Enhances the program to allow the user to enter anothermeteorological element such as windspeed (e.g. 2.4 mph). Support yourexperimentation with screen captures of executing the new code.

2

Provides a new test table with at least 2 distinct testcases listing input and expected output for the code you created after step2.

1

Describes what would happen if you change theNUMMONTHS and NUMYEARS definitions to other values? Appliesboth lower and higher values. Describes and implements fixes for any issuesif errors results. Support yourexperimentation with screen captures of executing the new code

2

Document is well-organized, and contains minimal spellingand grammatical errors.

1

Total

10