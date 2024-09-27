---
layout: essay
type: essay
title: "Setting standards"
# All dates must be YYYY-MM-DD format!
date: 2024-09-26
published: true
labels:
  - Coding standards
---

<img width="350px" class="rounded float-start pe-4" src="../img/setstandards/code_style.jpg">

## Standards
In a general context, standards are beneficial in providing an expected structure of conduct. Coding standards act as strict expectations for how code should be formatted. Although daunting and potentially frustrating, I believe that software developers benefit best from setting self-imposed restrictions such as these standards. Coding standards are a good practice for writing readable code, which is key for future development to be incorporated into a program with more ease. Readability is an important aspect of coding standards that affects the quality of code in both its current and future state.

## ESLint with VSCode
From my brief experience with ESLint in VSCode over these past few days, my impressions are tentatively positive. I find that fixing the ESLint errors is both useful and a hindrance. This negative aspect is revealed with arrow functions, which require a variable to store the value to return. Here is an example:

```cpp
const numsToStrings = (nums: number[]): string[] => {
  const result: string[] = nums.map(num => `${num}`);
  return result;
};

console.log(numsToStrings(fib()));
```

In this case, ESLint gives an error if you were to directly return the object that is modified by the map function. This modified value needs to be stored as a variable, I presume so that this action is secure. Prior to VSCode and ESLinit, VS Playground would support this return statement without issuing an error.

Otherwise, I find the nuance of a new line after the entire code and specific indentations useful to ensure that proper coding etiquette is pushed on developers. Particularly new developers, who may not understand coding standards just yet.
