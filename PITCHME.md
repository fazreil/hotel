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
  - r_number is passed as a parameter referencing the owner of the room
- display_all_customer function
- show_customer function

+++

### customer modifications

- modify_customer function

Modification of customer information is carried out in such way where the the file/database is read and overwritten. Hotel class function modify_customer_record is being called to perform modification.

+++

### saving modification into database/file

- save_customer function

Save customer function provide the user with utility to add more customers. By doing so, it open the file/database and insert customer information. Hotel class function add_customer is called to create the data before inserting into the file/database.

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

This function asks the user to input number of nights, type of room and number of rooms as variables and calculate the total price

```c
if (type==1)
price = 100;

else if(type==2)
price = 150;

else if (type==3)
price = 200;

totalprice = price*rooms*night;
```

totalprice is then shown to the user.

+++

### add_customer

The function then asks the user to input their details to store as a hotel object

```c
  cout<<"\nEnter The Room Number: ";
  cin>>room_number;

  cout<<"\nEnter The Customer's name: ";
  cin.ignore();
  cin.getline(name,30);

  cout<<"\nEnter The Customer's address: ";
  cin.ignore();
  cin.getline(address,50);

  cout<<"\nEnter The Customer's phone #: ";
  cin.ignore();
  cin.getline(phone,10);
```

for each cin.getline a property of hotel is brought together to store as one of hotel property, the second argument is the size of input allowed.

+++

### show_customer

show_customer function is similar to display functions where it retrieve the variables and display them on the console

```c
void show_customer()
{
  cout<<"\nRoom Number: "<<room_number;
  cout<<"\nCustomer's Name: "<<name;
  cout<<"\nCustomer's Address: "<<address;
  cout<<"\nCustomer's Phone: "<<phone;
}
```

+++

### modify_customer_record

modify_customer_record overwrites the customer record as saved in the hotel object.

```c
void modify_customer_record()
{
  cout<<"\nRoom number : "<<room_number;
  cout<<"\nModify Customer's Name : ";
  cin.ignore();
  cin.getline(name,30);
  cout<<"\nModify Customer's address: ";
  cin.ignore();
  cin.getline(address,50);
  cout<<"\nModify Customer's phone #: ";
  cin.ignore();
  cin.getline(phone,10);
}
```

The program display the room number and asks the user to input the new customer details.


+++

### report function

The report function displays the current value that each of the variable holds.
The format of the display is indented by using setw()

```c
void report()   // format and display the current value for each variable
{
cout<<room_number<<setw(10)<<name<<setw(20)<<address<<setw(20)<<phone<<endl;
}
```

---

## Q & A

+++

## Prepared by:

---
