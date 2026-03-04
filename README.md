# CSCI-101-Final-Project-M08
This is the git repo for my Computer Science final project in Module 8. The purpose of this project is to extract data and manipulate it using C++

The full description of the project: 
Using the data provided, process it and:
. determine the maximum x and y values
. create a 2D array initialized with spaces 
. fill the array with characters from the input data
. print the array to reveal the answer of block annotated letters 

Required documents:
. Flowchart to demonstrate step by step logic 
. UML to model the behavior and interactions of each step
. All source code 
. Screen Shot of final answer 
. Github url (optional but I will include) 

Within this repository are different folders containing different tasks required for the project including the initialization of my VS code. 
---------------------------------------------------------------------------------------
a.	Program Overview
i.	This program works by reading coordinate fata from an external file and uses the data that’s been read to construct a 2D grid. Each line of the file read has an x coordinate, a block character that’s either opaque or partially transparent, and a y coordinate. Using this information, my program then determines the max dimensions of the grid and creates a blank 2D array that it goes in an fills with the data parsed from the external file. When it goes to output the information, it shows a hidden message in block letters. The block letters are created using the opaque and transparent blocks provided with the x and y coordinates. 
ii.	My program reads from the “InputData.txt” file that is saved in the same folder as my main application. Each line has a “x symbol y” formatting much like this: 
a.	87 █ 3
b.	23 ░ 2
c.	61 █ 4
iii.	The program works by 
1.	Opening the external file using ifstream. It checked immediately to validate a successful opening.
2.	Read the data using getline() and stringstream. For every valid line the x, y, and symbol values are extracted and held in a vector all while updating the maxX and maxY values to determine the size of the grid needed. 
3.	After reading the data, and determining the size needed, it creates a 2D array. The 2D vector is created using “Rows = maxY + 1” and “Columns = maxX + 1”. Then the grid is initialized with blank spaces. 
4.	Next it fills the grid with the data collected using “grid[x][y] = symbol;” this takes a spot like (57, 4) and fills it with the corresponding transparent or opaque block. 
5.	Finally, it prints the grid to output. It does this by printing from the highest row down to 0. This was to ensure that the output is correctly displayed. 
iv.	Key Concepts Used:
1.	File input using ifstream
2.	String parsing with stringstream
3.	Dynamic 2D vectors
4.	Nested loops
5.	Coordinate mapping
6.	Unicode character handling 
v.	Some problems I encountered while working with this program were dynamic. First, I have been coding primarily in python for the last couple of years on windows. I recently switched over to a MacBook making this course overall a learning curve. I had to relearn the terminal commands I already knew for windows, recreate my VS Code environment, and successfully add C/C++ as well as a compiler to my Mac, where C languages are not native. The coding environment aside, the information that is read from the word document proved to be challenging, so I had to create a text file storing the data to be able to successfully read the inputs. The Unicode blocks weren’t recognized originally by my code, so I needed to use string instead of char. Lastly, the printing order kept coming out upside down. While I could understand what it was printing, I knew that wasn’t the correct final answer. I had to find a way to flip the way it was printed to avoid the upside-down output.  

