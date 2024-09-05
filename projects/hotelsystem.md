---
layout: project
type: project
image: img/hotel.jpg
title: "HotelSystem"
date: 2023-12-09
published: true
labels:
  - Management
  - Group Project
  - C++
summary: "We developed a basic hotel management system that allows users to add new rooms with features and search available rooms, check in and check out, search customer, and generate guest reports."
---


HotelSystem was a final project assigned in our ICS 212 course. We were assigned into groups to nurture team collaboration, but task assignments were left to every group's discretion. A sample output was provided but there was no starter code. It was around a week long endeavour, and every group was expected to present their program to the class.

For this project, I took initiative as a leader to work with every member to decide on each of our responsibilities. While I maintained communication with everyone in our group, I programmed the getter functions to get available rooms and to get available room numbers. As the project went on, I added code at various spots of the program that did not produce the expected output, most notably in the checkOutRoom function and in the main. Before presentation day, I went through the program to clean up the code as much as possible. I was also in charge of documentation, so I made sure to include an implementation description that specified the names of who contributed what code, and to include comments that explained essential functions, variables, etc. Our group received an A.

Here is an excerpt from the program that demonstrates some of my code in the checkOutRoom function:

```cpp
 if(customers[i].getRoomCheckedInto() == roomNum) {
          cout << "Customer Name: " << customers[i].getName() << endl;
          cout << "Room Number: " << roomNum << endl;
          cout << "Address: " << customers[i].getAddress() << endl;
          cout << "Phone: " << customers[i].getPhone() << endl;
          totalAmountInt = dailyRate * numDays; // @Ciara - I changed this, lmk if it works
          cout << "Total Amount Due: " << totalAmountInt << endl;
          cout << "Advance Paid: " << customers[i].advancePaid << endl;
          advancePaidInt = std::stoi(customers[i].advancePaid);
          finalAmountInt = totalAmountInt - advancePaidInt; // @Ciara - I changed it to the int form of final amount, in case errors happen with calculations using string = int - int , so it's int = int - int instead
          cout << "*** Total Payable: " << finalAmountInt << "/ only" << endl; // prints string
          //@Ciara - I added the rest of the code in this loop to remove customer data
          customers.erase(customers.begin()+i); // erase customer info at the element 0+i
        }
```

You can view the source code at [HotelSystem](https://github.com/kngcr/HotelSystem/tree/main).
