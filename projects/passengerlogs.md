---
layout: project
type: project
image: img/passlogs/airport.jpg
title: "PassengerLogs"
date: 2023-11-22
published: true
labels:
  - Data Modification
  - Contribution
  - Java
summary: "This was a friend's project for ICS 111 that reads flight and passenger data from a file then modifies the data to output as desired on the console, the latter of which I programmed a fix for."
---


PassengerLogs was an assignment issued to my friend in ICS 111 at the time. The majority of the program was written by her, but she was unable to program the scanner to traverse the file and accurately store the data. I requested to obtain a copy of her files and with her permission, try to program a solution using her pre-existing code.

To reach a solution, I had to first read the program she had written to develop an understanding of its functions and variable designations. I also had to consult with the csv file that contained the flight and passenger data to see how it was formatted. The issue had been that the scanner was not properly traversing each substring, which was strictly separated by commas. My fix was to assign three index variables: i for string (the substring to be stored as a string or other type), c for the first comma (before the string), and d for the last comma (after the same string). I chose to use a while loop to increment these indices because Java has a hasNextLine() method that can be used to make a boolean condition with scanner- meaning that as long as there is more text, the loop will continuously run. From there, I stored indices by calling the string array, data, and utilizing the indexOf() and lastIndexOf() methods to obtain the indices for the commas. Further steps were also written to complete this code, but the indices incremented properly to store the correct input and achieve the output required.

Here is the while loop that I programmed:

```cpp
            while (scanner.hasNextLine()) {
            	int i = 0; // Index of String
            	int c = 0; // Index of first Comma
            	int d = 0; // Index of last Comma
                String[] data = scanner.nextLine().split("\\t"); // Assuming tab-separated data
                c = data[i].indexOf(",");
                d = data[i].lastIndexOf(",");
                String name = data[i].substring(0,c);
                c++;
                boolean frequentFlyer = (data[i].substring(c,d)).equalsIgnoreCase("TRUE");
                d++;
                int miles = Integer.parseInt(data[i].substring(d,data[i].length()));
                passengers.add(new Passenger(name, frequentFlyer, miles));
            }
```

You can view the source code at [PassengerLogs](https://github.com/kngcr/PassengerLogs).

<ins>Fun Fact:</ins> This program became the reason I convinced my now best friend to pursue a Computer Science major! She was observing my programming process.

Thanks to this project, I realized how there is a distinction between writing code and understanding code. To come up with a solution to a program that I initially knew nothing of, I needed to effectively communicate with my friend about what the program needed to do, what necessary files / classes / functions / variables did it require, and more. It was not until I reached enough of an understanding of this program that I have been able to start brainstorming solutions. Then, implement solutions. This is a project that I completed within a time frame that surprised me. It was also a crucial time frame that changed the course of someone else's future (see fun fact).
