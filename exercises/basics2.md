1. Without using a PHP program to evaluate them, determine whether each of
these expressions is true or false :
a. 100.00 - 100
b. "zero"
c. "false"
d. 0 + "true"
e. 0.000
f. "0.0"
g. strcmp("false","False")
h. 0 <=> "0"
2. Without running it through the PHP engine, figure out what this program prints:
```
$age = 12;
$shoe_size = 13;

if ($age > $shoe_size) {
    print "Message 1.";
} elseif (($shoe_size++) && ($age > 20)) {
    print "Message 2.";
} else {
    print "Message 3.";
}
print "Age: $age. Shoe Size: $shoe_size";
```
3. Use while() to print a table of Fahrenheit and Celsius temperature equivalents
from –50 degrees F to 50 degrees F in 5-degree increments. On the Fahrenheit
temperature scale, water freezes at 32 degrees and boils at 212 degrees. On the
Celsius scale, water freezes at 0 degrees and boils at 100 degrees. So, to convert
from Fahrenheit to Celsius, you subtract 32 from the temperature, multiply by 5,
and divide by 9. To convert from Celsius to Fahrenheit, you multiply by 9, divide
by 5, and then add 32.
4. Modify your answer to Exercise 3 to use for() instead of while() .