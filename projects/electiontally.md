---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "ElectionTally"
date: 2023-11-19
published: true
labels:
  - Calculations
  - Individual Project
  - C++
summary: "I programmed an election results calculator that takes five candidates and their number of votes for an ICS 212 homework assignment."

---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

ElectionTally was the first C++ homework assignment in ICS 212. The objective was to write a C++ program that allows the user to input five candidate surnames and their number of votes, then return all names and votes in a specific format along with the percentages of votes received by each candidate and the name of the election winner.

In this program, I created a Candidate class and a main function. The class serves to store the candidates' details using the getter function, calculate percentages of votes recieved with another function, and a third function to display candidates' details in the required format. The main serves to create a Candidate class object and call the class functions, while also including code for formatting as well.

Here is some code that illustrates two class functions and how they calculate percentages and format displayed details:

```cpp
        void calculatePercentage(int totalVotes) {
            percentage = (static_cast<double>(votesReceived) / totalVotes)*100;
            percentage = trunc(percentage);
        }

        void displayCandidateDetails() {
            cout << setw(15) << lastName << "\t" << setw(15) << votesReceived << "\t" << setw(10) << fixed << setprecision(0) << percentage << "%" << endl;
        }
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
