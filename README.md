# Week04 Quiz2:

## 1. Requirements:

The class representing the quadratic equation `ax^2 + bx + c = 0 (a!=0)` is defined as follows. Utilize the predefined classes to complete this project.

- Writing code using c++
- Use `Quadratic` class to complete your code. 
- Changing the provided class is not allowed. You can `only use the provided class and the functions defined within it`.
- You need to store the `given class definitions` in the `Quadratic.h` files. Store the `function definitions and the main function` in the `main.cpp` file.   
  `(Please submit the above two documents, and if you do not name the main file "main.cpp", the test will not pass and you will receive zero points)`

<br/>
                  
### Quadratic class:
- Complete and use the following class:
  ```C++
  class Quadratic {
	 friend Quadratic add(Quadratic& q1, Quadratic& q2); // Return q3 after storing the quadratic equation q1+q2 result in the new Quadratic object q3.
	 friend Quadratic subtract(Quadratic& q1, Quadratic& q2); // Return q3 after storing the quadratic equation q1-q2 result in the new Quadratic object q3
	public:
	 Quadratic(double a, double b, double c); 
	 std::string toString(); // return ax^2+bx+c=0 format string.
	 void solve(); // Find and output a quadratic equation.
	private:
	 double a{ 1 }; // a can't be zero, otherwise an error will occur.
	 double b{ 0 };
	 double c{ 0 };
	};
  ```
<br/>

- The root formula `(-b +/- sqrt(b^2 - 4ac)) / 2a` is used to obtain and output the solution of the quadratic spin equation.
- If `b^2 - 4ac < 0`, output `"No real roots"`.  
  e.g. `Solution of 2x^2+2.1x+3=0: No real roots`
- If `b^2 - 4ac = 0`, `only one x value` is output.  
  e.g. `Solution of 1x^2+6x+9=0: x=-3.00`
- If `b^2 - 4ac > 0`, output the value `added` by the square root first.  
  e.g. `Solution of 1x^2-6x+8=0: x=4.00 or 2.00`
- The solution of a quadratic equation is `always a fixed decimal point` and is `output to two decimal places`.  
  e.g. `Solution of 2x^2+8x+8=0: x=-2.00`

<br/>

### Input
- The first line input `three double type numbers separate with spaces` as parameters for the first quadratic equation.   
  e.g. `1 3.3 -5`
- The second line input `three double type numbers separate with spaces` as parameters for the second quadratic equation.   
- e.g. `-4 0 0`. 

<br/>

### Output  

- Output the first quadratic equation on the first line in the format of `ax^2+bx+c=0`. If the input number is negative, replace the corresponding '+' with '-'.   
  e.g. `1x^2+3.3x-5=0`
- Output the second quadratic equation on the first line in the format of `ax^2+bx+c=0`. If the input number is negative, replace the corresponding '+' with '-'.   
  e.g. `-4x^2+0x+0=0`
- Output A blank line in the third line.   
- Output the `first quadratic equation with its solution` on the 4th line.   
  e.g. `Solution of 2x^2+2.1x+3=0: No real roots`
- Output the `second quadratic equation with its solution` on the 5th line.  
  e.g. `Solution of 1x^2-6x+8=0: x=4.00 or 2.00`
- Output A blank line in the 6th line.
- Output `the sum of two quadratic equations in the form of a quadratic equation` on the 7th line.  
  e.g. `(1x^2+4x+5=0)+(2x^2+0x+3=0)=3x^2+4x+8=0`
- Output `the difference between two quadratic equations in the form of a quadratic equation` on the 8th line.  
  e.g. `(1x^2+4x+5=0)-(2x^2+0x+3=0)=-1x^2+4x+2=0`
- `No spaces are left between output contents.`

<br/>

### Error handling

- When the first input value is zero, the program outputs an error message and requires re-entry.  
  error message: `Input 'a' cannot be zero. Please input again.`
- The program will continue to request input until it receives a standardized input.

<br/>

### Other tips
- If you need to use the sqrt() function, you must first reference the `<cmath>` header file.
  
<br/>

## 2. Scoring Criteria (5 points in total):

- Uploaded `Quadratic.h` and `main.cpp` two files with no compilation errors: 1 point
- The cpp file calls header files and declares the given functions: 2 point
- The result is correct: 2 point

<br/>

## 3 Examples
### Example1 (Red font for input, blue font for output):  
![image](https://github.com/chyh001228/images/blob/main/w4q2_e1.png)

**Input:**

```
2 2.1 3
1 6 9
```

**Output:**

```
2x^2+2.1x+3=0
1x^2+6x+9=0

Solution of 2x^2+2.1x+3=0: No real roots
Solution of 1x^2+6x+9=0: x=-3.00

(2x^2+2.1x+3=0)+(1x^2+6x+9=0)=3x^2+8.1x+12=0
(2x^2+2.1x+3=0)-(1x^2+6x+9=0)=1x^2-3.9x-6=0
```

**Actual results:**   
![image](https://github.com/chyh001228/images/blob/main/w4q2_c_e1.png)  

<br/>

### Example2 (Red font for input, blue font for output):  
![image](https://github.com/chyh001228/images/blob/main/w4q2_e2.png)

**Input:**

```
0 -6 8
0 3 9
1 -6 8
0 8 8
2 8 8
```

**Output:**

```
Input 'a' cannot be zero. Please input again.
Input 'a' cannot be zero. Please input again.
1x^2-6x+8=0
Input 'a' cannot be zero. Please input again.
2x^2+8x+8=0

Solution of 1x^2-6x+8=0: x=4.00 or 2.00
Solution of 2x^2+8x+8=0: x=-2.00

(1x^2-6x+8=0)+(2x^2+8x+8=0)=3x^2+2x+16=0
(1x^2-6x+8=0)-(2x^2+8x+8=0)=-1x^2-14x+0=0
```

**Actual results:**  
![image](https://github.com/chyh001228/images/blob/main/w4q2_c_e2.png)

<br/>

### Example3 (Red font for input, blue font for output):  
![image](https://github.com/chyh001228/images/blob/main/w4q2_e3.png)

**Input:**

```
1 4 5
2 0 3
```

**Output:**

```
1x^2+4x+5=0
2x^2+0x+3=0

Solution of 1x^2+4x+5=0: No real roots
Solution of 2x^2+0x+3=0: No real roots

(1x^2+4x+5=0)+(2x^2+0x+3=0)=3x^2+4x+8=0
(1x^2+4x+5=0)-(2x^2+0x+3=0)=-1x^2+4x+2=0
```

**Actual results:**  
![image](https://github.com/chyh001228/images/blob/main/w4q2_c_e3.png)

(The deadline is 00:00a.m. on September 28, 2025)

<img src="https://cdn.imweb.me/upload/S201906178853c3e170808/c5d876d707352.jpg" width=30% align=center />
