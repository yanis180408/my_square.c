# Welcome to My Square
***

## Task
The goal of this project is to write a function `my_square(width, height)` that draws a rectangle in the terminal using only ASCII characters.
The corners are drawn with `o`, the horizontal edges with `-` and the vertical edges with `|`. The inside of the rectangle is filled with spaces.
The challenge lies in handling every size correctly, including the edge cases (a single row, a single column, a single character), while only using the allowed functions of the subject.

## Description
I solved this problem by drawing the rectangle row by row and deciding, for each position, which character to print:
- **Corners** : the four corners (first/last row, first/last column) are printed as `o`.
- **Horizontal edges** : the first and last rows are filled with `-` between the corners.
- **Vertical edges** : the first and last columns of every other row are printed as `|`, and the inside is filled with spaces.
- **Edge cases** : when the width or the height is `1`, the shape collapses to a single line or column and only the corners (`o`) and edges that still fit are printed.
- **Argument Handling** : `main` converts the two command line arguments into integers and passes them to `my_square`.

## Installation
The project includes a Makefile for easy compilation.
1. Compile the project :
```bash
make
```

2. Recompile (clean and build) :
```bash
make re
```

3. Clean object files :
```bash
make clean
```

4. Clean everything (executable and objects) :
```bash
make fclean
```

## Usage
The program takes the width and the height of the rectangle as arguments.

**Syntax :**
```bash
./my_square [WIDTH] [HEIGHT]
```

**Examples :**

`my_square(5, 3)` should display:
```
$>./a.out 5 3
o---o
|   |
o---o
$>
```

`my_square(5, 1)` should display:
```
$>./a.out 5 1
o---o
$>
```

`my_square(1, 1)` should display:
```
$>./a.out 1 1
o
$>
```

`my_square(1, 5)` should display:
```
$>./a.out 1 5
o
|
|
|
o
$>
```

`my_square(4, 4)` should display:
```
$>./a.out 4 4
o--o
|  |
|  |
o--o
$>
```

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
