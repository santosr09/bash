Bash training

https://linuxconfig.org/bash-scripting-tutorial-for-beginners

Shell prompt:
($ for user)
[username@host ~]$

Shell prompt:
(# for root)
[root@host ~]#

Shebang(#!) is simply an absolute path to the bash interpreter.
Below is an example of the shebang statement:
#! /bin/bash

Find the path to your bash shell:
which bash

Modify the file permissions and allow execution of the script by using the command below:
chmod u+x hello_world.sh

chmod modifies the existing rights of a file for a particular user. We are adding +x to user u.

Run the script:
./hello_world.sh
bash hello_world.sh.

How to define variables
We can define a variable by using the syntax variable_name=value. To get the value of the variable, add $ before the variable:
#!/bin/bash
#A simple variable example
greeting=Hello
name=Tux
echo $greeting $name


Arithmetics operators:
+	addition
-	subtraction
*	multiplication
/	division
**	exponentiation
%	modulus


Numerical expressions can also be calculated and stored in a variable using the syntax below:

var=$((expression))

Let's try an example.

#!/bin/bash

var=$((3+9))
echo $var

Fractions are not correctly calculated using the above methods and truncated.

For decimal calculations, we can use bc command to get the output to a particular number of decimal places. bc (Bash Calculator) is a command line calculator that supports calculation up to a certain number of decimal points.

echo "scale=2;22/7" | bc

Where scale defines the number of decimal places required in the output.


Read user input
In bash, we can take user input using the read command.

read variable_name
To prompt the user with a custom message, use the -p flag.

read -p "Enter your age" variable_name


Numeric comparison logical operators
OPERATION   SYNTAX	EXPLANATION
Equality	num1 -eq num2	is num1 equal to num2
Greater than equal to	num1 -ge num2	is num1 greater than equal to num2
Greater than	num1 -gt num2	is num1 greater than num2
Less than equal to	num1 -le num2	is num1 less than equal to num2
Less than	num1 -lt num2	is num1 less than num2
Not Equal to	num1 -ne num2	is num1 not equal to num2c


Example:

Let's compare two numbers and find their relationship:

read x
read y

if [ $x -gt $y ]
then
echo X is greater than Y
elif [ $x -lt $y ]
then
echo X is less than Y
elif [ $x -eq $y ]
then
echo X is equal to Y
fi


The structure of conditional statements is as follows:

if...then...fi statements
if...then...else...fi statements
if..elif..else..fi
if..then..else..if..then..fi..fi.. (Nested Conditionals)


Syntax:

if [[ condition ]]
then
	statement
elif [[ condition ]]; then
	statement 
else
	do this by default
fi


To create meaningful comparisons, we can use AND -a and OR -o as well.

The below statement translates to: If a is greater than 40 and b is less than 6.

if [ $a -gt 40 -a $b -lt 6 ]


Looping with numbers:
In the example below, the loop will iterate 5 times.

#!/bin/bash

for i in {1..5}
do
    echo $i
done


Looping with strings:
We can loop through strings as well.

#!/bin/bash

for X in cyan magenta yellow  
do
	echo $X
done

