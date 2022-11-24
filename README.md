
# 16a

# final-assignment
Final Assignment C/C++

## The ticket generator you made in C should be turned into a C++ version.
You should create a repository for your ticket-system.
The code should be commented in a way that doxygen could produce a nice output for your software (html, pdf is a bonus).
Your software should use C++ features where appropriate.

***When you are finished, fork the https://github.com/michellundell/14a repository and update the final-assignment.txt file
Then make a pull-request and I can start evaluating your system.***


## The ticket program

```
You should create a program that takes two arguments.
The first argument is a file with flight information.
The second argument is a file with booking information.
Your program should create files with a ticket for each booking.
```
**Compiling the program**

```
make
```

**Example running the program:**
```
ticketsystem flights.csv booking.csv

or

make run
```

**Will produce the files:**

```
ticket-1001.txt ticket-1002.txt ticket-1003.txt ticket-1004.txt
ticket-1005.txt ticket-1006.txt ticket-1007.txt ticket-1008.txt
....
```

## Each row in any flights contain 7 seats. There is an aisle between seat 2 and 3, and 5 and 6.

```
Row seating is 2-3-2 the all flights.

[Window] [seat 1][seat 2] aisle [seat 3][seat 4][seat 5] aisle [seat 6][seat 7] [window]

```

## Flight data-file structure:

flights.csv:
```
flightnumber,departure,destination,date,time,f-rows,b-rows,e-rows
```

## Booking data-file structure:

bookings.csv:
```
bookingnumber,date,time,departure,destination,seatclass,firstname,surname
```

## Output:

The tickets should be written to files with the following filename format:

```
ticket-{bookingnumber}.txt
```

Each file should contain the following information in this format: 

```
BOOKING:{bookingnumber} 
FLIGHT:{flight} DEPARTURE:{dep} DESTINATION: {dest} {date} {time}
PASSENGER {firstname} {surname}
CLASS: {seatclass}
ROW {row} SEAT {seatnumber}
```

### Example of ticket filename:

```
ticket-2007.txt
```

### Example of ticket file content:
```
BOOKING:2007
FLIGHT:304 DEPARTURE:GOT DESTINATION:CPH 2022-10-27 06:30
PASSENGER: Kalle Kula
CLASS: first
ROW:4 SEAT:24
```

## Hints för högre betyg ...

```
C/C++ Betyg
===========
Have a informative README.md in the repository? (1p)
Have a Makefile? (1p)
Creates tickets? (50p)
Student unique design? (2p)
Have flags (using getopt()) ? (1p)
Have cancelled flights? (1p)
Have seatmap? (1p)
Is a C++ program? (1p)
Produce a documentation? (1p)
Have separate C++ sources and headers? (1p)
Using C++ Classes? (1p)
Have separate C++ Class sources and headers? (1p)
Using C++ std::objects? (1p)
Using C++ templates? (1p)
Using C++ try-catch? (1p)
Using C++ inheritance? (1p)

*** Less than 50 is IG ***
*** Anything between 50 and 60 is G ***
*** A total >= 61 p is VG ***
```

