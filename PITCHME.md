---

# Hotel Management Program

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

### the main program

The main program is the program that will interact with the user. It will call the Hotel class from time to time to perform transaction regarding the Hotel management.

the main program handles the introduction, the menu for the user and also provide information for the user by retrieving data from the Hotel class.

+++

### introduction function

```void intro()
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

### The Hotel Class
In the next few slides, we will discuss about the Hotel Class. This include some of the major context relevant to the program:

- Header files
- main Class
- main menu
- add_customer
- show_customer
- modify_customer_record
- save_customer function
- display_a_customer function
- modify_customer function
- delete_customer function
- display_all_customer function
- intro function
---

## Header File Imports

+++

There are several header files being imported for the program

+++
