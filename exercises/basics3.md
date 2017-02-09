## Arrays

1. The 10 largest American cities (by population) in 2010 were as follows:
  * New York, NY (8,175,133 people)
  * Los Angeles, CA (3,792,621)
  * Chicago, IL (2,695,598)
  * Houston, TX (2,100,263)
  * Philadelphia, PA (1,526,006)
  * Phoenix, AZ (1,445,632)
  * San Antonio, TX (1,327,407)
  * San Diego, CA (1,307,402)
  * Dallas, TX (1,197,816)
  * San Jose, CA (945,942)

Define an array (or arrays) that holds this information about locations and popu‐
lations. Print a table of locations and population information that includes the
total population in all 10 cities.

2. Modify your solution to the previous exercise so that the rows in the result table
are ordered by population. Then modify your solution so that the rows are
ordered by city name.

Tip: For the tasks 1 and 2 you can use simple assoc. arrays:
```
    [
        'New York, NY' => 8175133,
        'Los Angeles, CA' => 3792621,
        ...
    ]
```

3. Modify your solution to the first exercise so that the table also contains rows that
hold state population totals for each state represented in the list of cities.

Tip: To complete this task (3) you can structure the array's elements as a three-element arrays
containing city name, state, and population:
```
    [
        ['New York', 'NY', 8175133],
        ['Los Angeles', 'CA' , 3792621],
        ...
    ]
```

## Functions

1. Write a function to return an HTML <img /> tag. The function should accept a
mandatory argument of the image URL and optional arguments for alt text,
height, and width .

2. Modify the function in the previous exercise so that only the filename is passed
to the function in the URL argument. Inside the function, prepend a global vari‐
able to the filename to make the full URL. For example, if you pass photo.png to
the function, and the global variable contains /images/ , then the src attribute of
the returned <img> tag would be /images/photo.png . A function like this is an
easy way to keep your image tags correct, even if the images move to a new path
or server. Just change the global variable—for example, from /images/ to
http://images.example.com/ .

3. Put your function from the previous exercise in one file. Then make another file
that loads the first file and uses it to print out some <img /> tags.

4. What does the following code print out?
```
<?php
function restaurant_check($meal, $tax, $tip) {
    $tax_amount = $meal * ($tax / 100);
    $tip_amount = $meal * ($tip / 100);
    return $meal + $tax_amount + $tip_amount;
}

$cash_on_hand = 31;
$meal = 25;
$tax = 10;
$tip = 10;

while(($cost = restaurant_check($meal,$tax,$tip)) < $cash_on_hand) {
    $tip++;
    print "I can afford a tip of $tip% ($cost)\n";
}
