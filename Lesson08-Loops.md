# Lesson 08: Loops

*Lesson 08 is an abbreviated version of [this document](https://github.com/czbeatty/FRC-Romi-Programming-Course/blob/main/Lessons/Romi%20Lesson%208%20-%20Loops.pdf). Please use it for reference if necessary.*

1. This lesson is best completed in a standalone Java project. We won't bother uploading this code to GitHub. In VSCode, expand the "Java Projects" section in the lower left, then click the "+" icon.

2. Choose "No build tools" and select a save location. Then enter a project name you'll remember like "RomiLesson08".

3. We'll be editing the file `App.java` in the `src` folder. Once VSCode recognizes the project, you can run the code in the `main` function by clicking "Run" just above it.

4. Using this project, complete the following challenges. If you don't know the necessary syntax, *please* look for answers online.

    * Write a `for` loop that prints out every integer from 0 to 9.

    * Write a `while` loop that outputs every integer from -10 to positive 20.

    * Choose an integer and compute the "sum of squares" from 1 to that number. For example, if you selected 10, the answer would be 1^2 + 2^2 + ... + 10^2. Output the answer. To check your work - if you enter 10, the answer should be 385. If you enter 11, it should be 506.

    * Choose an integer and compute the "square of sum" from 1 to that number. So if they entered 10, it would be (1 + 2 + ... + 10)^2. Output the answer. To check: 10 comes out to 3025, and 11 comes out to 4356.

    * Now calculate the "sum-square difference" - that is, the difference between the square of sum and the sum of squares. If you select 100, the answer should be 25164150.

    * Output a multiplication table for 1-10. You can use `System.out.print()` instead of `System.out.println()` to output a string without a new line.

5. Understanding how to work with loops is critical for writing robot code, but we tend to avoid directly using the types of `for` and `while` loops you practed here. Why might that be? How do loops play a part in the robot code?