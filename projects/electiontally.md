---
layout: project
type: project
image: img/election/voter.jpg
title: "ElectionTally"
date: 2023-11-19
published: true
labels:
  - Calculations
  - Individual Project
  - C++
summary: "I programmed an election results calculator that takes five candidates and their number of votes for an ICS 212 homework assignment."

---


ElectionTally was the first C++ homework assignment in ICS 212. The objective was to write a C++ program that allows the user to input five candidate surnames and their number of votes, then return all names and votes in a specific format along with the percentages of votes received by each candidate and the name of the election winner.

In this program, I created a Candidate class and a main function. The class serves to store the candidates' details using the getter function, calculate percentages of votes recieved with another function, and a third function to display candidates' details in the required format. The main serves to create a Candidate class object and call the class functions, while also including code for formatting as well. Writing this program made me realize the complexities of C++ that differ from a language like Java. The use of namespace std to specifically declare names of classes, functions, variables, and more from the C++ standard library so that the compiler does not have an error identifying what function, for example, is being called; an indicator of how complex C++ libraries are to potentially share classes, functions, variables, and more with similar names.

Here is some code that illustrates two class functions for calculating percentages and formatting displayed details:

```cpp
        void calculatePercentage(int totalVotes) {
            percentage = (static_cast<double>(votesReceived) / totalVotes)*100;
            percentage = trunc(percentage);
        }

        void displayCandidateDetails() {
            cout << setw(15) << lastName << "\t" << setw(15) << votesReceived << "\t" << setw(10) << fixed << setprecision(0) << percentage << "%" << endl;
        }
```

You can view the source code at [ElectionTally](https://github.com/kngcr/ElectionTally).
