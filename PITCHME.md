---

# Hotel Mgmt Program

---

## Introduction

+++

### Objective
The objective of the program is to provide solution for Hotel Management.
The user of this program will be able to :-
- Book a room
- Display all rooms allocated
- Display specific customer record
- Modify customer record
- Delete customer record

+++

### Holistic View of the program

The program as a whole consist of these items:

- Header file
- the main program
- the Hotel class

---

### Header Files

There are five header files being imported into the program

```c
#include<fstream>  //file stream manipulation library
#include<conio.h>  //ms-dos console input output utility
#include<string.h> //String manipulation utility
#include<iomanip>  //manipulate the iostram objects
#include<iostream> //input output stream library

```

+++

### the main program

The main program is the program that will interact with the user. It will call the Hotel class from time to time to perform transaction regarding the Hotel management.

the main program handles the introduction, the menu for the user and also provide information for the user by retrieving data from the Hotel class.

+++

### introduction function

```c
void intro()
{
     system("color 05");
     system("cls");
  cout<<"\t\t\t\t*\t*";
  cout<<"\t\t\t\t**\t**";
   cout<<"\t\t\t\t***\t***";
   cout<<"\t\t\t\t****\t****";
   cout<<"\t\t\t\t*****\t*****";
    cout<<"\t\t\t\t******\t******";
   cout<<"\t\t\t\t*******\t*******";
   cout<<"\t\t\t\t*******\t*******";
   cout<<"\t\t\t\t******\t******";
   cout<<"\t\t\t\t*****\t*****";
   cout<<"\t\t\t\t****\t****";
   cout<<"\t\t\t\t***\t***";
   cout<<"\t\t\t\t**\t**";
   cout<<"\t\t\t\t*\t*";
}```

- clears the screen by calling "cls" command in from the system
- show decorated banner

---

### Display functions

Display functions retrieve data from Hotel Class and print them on the display

Display functions are:
- display_a_customer function
  - r_number is passed as a parameter indicating the room owner
- display_all_customer function
- show_customer function

+++

### customer modifications

- modify_customer function

+++

### saving modification into database/file

- save_customer function

---

### The Hotel Class
In the next few slides, we will discuss about the Hotel Class. This include some of the major context relevant to the program:

- add_customer
- show_customer
- modify_customer_record

+++

### Variables for Hotel class

These are the variables for each of Hotel object
```c
int room_number;  //the number of the room, the key for referencing a customer, stored in an integer
char name[30];    //name of the customer is defined in array of char
char address[50]; //address of the customer is defined in array of char
char phone[10];   //phone numeber of the customer is defined in array of char
```

the variables are accessible through getter functions

+++

### Getters

All of the variables in previous slide have their own getters function.
```c
int getRoomNumber()
{
 return room_number;
}
char* getName()    // the asterisks are returning an array of the defined variable type
{
 return name;
}
char* getAddress()
{
 return address;
}

char* getPhone()
{
 return phone;
}
```
Getters function gets the value for each hotel objects.

---

### add_customer


Q & A

+++

Prepared by:

---
