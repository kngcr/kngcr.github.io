---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "PassengerLogs"
date: 2023-11-22
published: true
labels:
  - Data Modification
  - Contribution
  - Java
summary: "This was a friend's project for ICS 111 that reads flight and passenger data from a file then modifies the data to output as desired on the console, the latter of which I programmed a fix for."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

PassengerLogs was an assignment issued to my friend in ICS 111 at the time. The majority of the program was written by her, but she was unable to program the scanner to traverse the file and accurately store the data. I requested to obtain a copy of her files and with her permission, try to program a solution using her pre-existing code.

To reach a solution, I had to first read the program she had written to develop an understanding of its functions and variable designations. I also had to consult with the csv file that contained the flight and passenger data to see how it was formatted. The issue had been that the scanner was not properly traversing each substring, which was strictly separated by commas. My fix was to assign three index variables: i for string (the substring to be stored as a string or other type), c for the first comma (before the string), and d for the last comma (after the same string). I chose to use a while loop to increment these indices because Java has a hasNextLine() method that can be used to make a boolean condition with scanner- meaning that as long as there is more text, the loop will continuously run. From there, I stored indices by calling the string array, data, and utilizing the indexOf() and lastIndexOf() methods to obtain the indices for the commas. Further steps were also written to complete this code, but the indices incremented properly to store the corrent input and achieve the output required.

Here is the function I assisted with, of which I wrote the while loop and the catch statement:

```cpp
private static ArrayList<Passenger> readPassengerData(String fileName) {
        ArrayList<Passenger> passengers = new ArrayList<>();
        try {
            Scanner scanner = new Scanner(new File("passengers2.csv"));
            // Skipping the header line
            scanner.nextLine();

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
            scanner.close();
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }
        return passengers;
    }
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
