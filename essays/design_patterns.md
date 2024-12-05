---
layout: essay
type: essay
title: "Design Patterns: Declassified!"
# All dates must be YYYY-MM-DD format!
date: 2024-12-05
published: true
labels:
  - Design Patterns
---

<img width="300px" class="rounded float-start pe-4" src="../img/design-patterns/proxy_example.png">

## Hidden Intent

In the complex nature of software design, there are common problems that reoccur with solutions that can be repeatedly used to address them. Design patterns are these repeatable solutions, and they can be classified according to their intent.

* Creation
* Structure
* Behavior

Design patterns with the intent of creation address how objects are created in code. Ideally, these objects are made flexible for use and utilize abstraction. If this sounds familiar, these are principles of object-oriented programming. Creational design patterns help programmers build programs that are adaptable, reusable, and maintainable.

Design patterns with the intent of affecting structure, address the structure of objects and classes. To better explain structural design patterns, I will share examples. The Proxy Pattern allows a programmer to create an object that can act as an intermediary between the user and a target object. This proxy object adds functionality to the target object without changing the target’s interface; adding flexibility, adaptability, and easier maintainability.

Design patterns with the intent of affecting behavior, address how objects and classes interact with each other. Behavioral design patterns include the Iterator Pattern, which lets an iterator traverse the elements of a collection of objects without accessing its implementation. Again, allowing for adaptable programming.

## Usage

Patterns exist within programs to solve intricate problems. The example of design patterns that I have explained were part of my own code. Most notably throughout my ICS courses, I have used an Iterator class to iterate through data.

```cpp
  int main() {
    // Declare variables
    const int numCandidates = 5;
    Candidate candidates[numCandidates];
    int totalVotes = 0;

    // Get input for candidate details
    for(int i = 0; i < numCandidates; i++){
        candidates[i].getCandidateDetails(i);
        totalVotes += candidates[i].votesReceived;
    }
```

The above code is an example of an Iterator pattern, with an iterator used in the main function to process each candidate's array. This is C++ code from an ICS 212 assignment. The Iterator design pattern is widely used for its consistency and abstraction. This allows us, programmers, to focus on what an object does rather than how it does it. So, in a simpler way, my code can access each candidate's array for the array's details without worrying about how to go through arrays of candidates to access details.

I had read that design patterns are discovered and named by programmers. As programmers, we use design patterns to create optimized code. But, I can channel the ideology of a meme- the scene between Gojo and Geto- to rephrase this sentence: “Design patterns use programmers.” Design patterns are built on our tendencies to use similar solutions to similar problems.

## Credits

I used AI to reference flexibility and abstraction in object creation, as well as details on iterators. Primarily, I referenced this [LinkedIn article](https://www.linkedin.com/pulse/7-design-patterns-you-should-know-hayk-simonyan/) and [StackExchange post](https://softwareengineering.stackexchange.com/questions/141854/design-patterns-do-you-use-them).
