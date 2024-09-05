---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "HotelSystem"
date: 2023-12-09
published: true
labels:
  - Management
  - Group Project
  - C++
summary: "We developed a basic hotel management system that allows users to add new rooms with features and search available rooms, check in and check out, search customer, and generate guest reports."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

HotelSystem was a final project assigned in our ICS 212 course. We were assigned into groups to nurture team collaboration, but task assignments were left to every group's discretion. A sample output was provided but there was no starter code. It was around a week long endeavour, and every group was expected to present their program to the class.

For this project, I took initiative as a leader to work with every member to decide on each of our responsibilities. While I maintained communication with everyone in our group, I programmed the getter functions to get available rooms and to get available room numbers. As the project went on, I added code at various spots of the program that did not produce the expected output, most notably in the checkOutRoom function and in the main. Before presentation day, I went through the program to clean up the code as much as possible. I was also in charge of documentation, so I made sure to include an implementation description that specified the names of who contributed what code, and to include comments that explained essential functions, variables, etc. Our group received an A.

Here is an excerpt from the program that demonstrates the getter functions I was tasked with:

```cpp
    // @Ciara's getter, it returns the total number of available rooms that exist
    int getAvailableRooms(vector<Room>& rooms){
      int roomCount = 0;
      for(int i = 0; i < rooms.size(); i++){
        if(rooms[i].getAvailability() == true){
          roomCount++; // counts number of available rooms
      }
    }
      return roomCount;
    }
    // @Ciara's getter, it returns the list of available room numbers
    string getAvailableRoomNumbers(vector<Room>& rooms){
        string roomNum;
        int room;
        for(int i = 0; i < rooms.size(); i++){
            room = rooms[i].getRoomNumber();
            if(rooms[i].getAvailability() == true){
                roomNum += to_string(rooms[i].getRoomNumber()) + " ";
            }
        }
        return roomNum;
    }
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
