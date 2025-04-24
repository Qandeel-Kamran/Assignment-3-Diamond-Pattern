# Assignment-3-Diamond-Pattern

🔹 Code Overview:
The code is divided into two parts:

Top half of the diamond (increasing stars)

Bottom half of the diamond (decreasing stars)

🔸 Part 1: Top Half of the Diamond
python
Copy
Edit
x = 5

for i in range(1, 6):
    for q in range(1, x + 1):
        print(" ", end="")
    for j in range(1, i + 1):
        print("*", end=" ")
    print()
    x = x - 1
🔍 Step-by-step Explanation:
x = 5: This variable keeps track of how many spaces we need to print before the stars so the shape is center aligned.

for i in range(1, 6):
This outer loop runs 5 times, for lines 1 to 5. Each loop prints one row of the top half.

Inner Loop 1:
python
Copy
Edit
for q in range(1, x + 1):
    print(" ", end="")
This prints spaces to push the stars to the right.

Initially prints 5 spaces, then 4, 3, etc. as x decreases.

Inner Loop 2:
python
Copy
Edit
for j in range(1, i + 1):
    print("*", end=" ")
This prints the stars in each row.

It prints 1 star in the first row, 2 in second, up to 5 in the fifth row.

End of Loop:
python
Copy
Edit
print()
x = x - 1
print() moves to the next line.

x = x - 1 reduces the number of spaces for the next row.

✅ Output After Top Half:
markdown
Copy
Edit
     * 
    * * 
   * * * 
  * * * * 
 * * * * * 
🔸 Part 2: Bottom Half of the Diamond
python
Copy
Edit
x = 1
for i in range(5, 0, -1):
    for q in range(1, x + 1):
        print(" ", end="")
    for j in range(1, i + 1):
        print("*", end=" ")
    print()
    x = x + 1
🔍 Step-by-step Explanation:
x = 1: Resets the space counter for the bottom half.

for i in range(5, 0, -1):
This loop goes backward from 5 to 1, creating the bottom half of the diamond.

Inner Loop 1:
python
Copy
Edit
for q in range(1, x + 1):
    print(" ", end="")
Prints increasing spaces: 1, 2, 3, etc. so the stars move inward.

Inner Loop 2:
python
Copy
Edit
for j in range(1, i + 1):
    print("*", end=" ")
Prints decreasing number of stars from 5 to 1.

End of Loop:
python
Copy
Edit
print()
x = x + 1
x increases after each line to add more space in the next row.

✅ Final Output (Full Diamond):
markdown
Copy
Edit
     * 
    * * 
   * * * 
  * * * * 
 * * * * * 
 * * * * * 
  * * * * 
   * * * 
    * * 
     * 
🔚 Summary:
The first part builds the top triangle of the diamond.

The second part builds the bottom inverted triangle.

x is used to align the stars in the center by controlling the spaces before them.
