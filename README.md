# Objectives for Part 1
Get you guys a solid foundation in Python, which is useful if you want to build for the web or do any machine learning or data science.

# The Basic Data Types
What are the basic data types?
- Integers, e.g. 1, 2, 3
- Floating point numbers, e.g 2.3, 3.7
- String, e.g. "John Krasinski"
- bool, True or False
- None, which just corresponds to empty or null, if you've used other languages

Let's start with integers and floats.

Let's go into the python shell.
To do this, open up your terminal and type 'python' and then press Enter.

We can do math in the shell.
```python
>>> 2 + 2
4
>>> 2 * 3.5
7.0
>>>
```

What's the difference between 2.0 and 2?
```python
>>> 7/2
3
>>> 7/2.0
3.5
```
Practice question - try these out in the shell:
```
1. 2 * 7 * 3.5
2. 3 + 5 - (2 * 6)
3. (3 + 5 - 2) * 6
4. 4 == 5
5. 5 == 5
6. 4 < 5
7. 5 >= 4
8. 9 != 9
9. 8 != 9
```

Explanations:
```
In 1., we learned that you can chain operations
In 2 and 3, we learned that order matters and you can use parentheses to indicate the order, as part of the usual mathematical order of operations.
In 4 and 5, we learned about the equality operator.
In 6 and 7, we learned about inequality comparions like less than or greater than equal to.
In 8 and 9, we learned about the not-equal-to operator.
```

Now let's talk variables. What's a variable? It's a placeholder for a value.
```python
>>> x = 5
>>> y = 2
>>> x + y
7
>>> x = 3
>>> x + y
5
```

Practice question:
Given x=10, y=2, predict the answers to the following and then try them out in the shell:
```
1. x + y
2. x * y
3. (x + 7) / y
4. (x + 7.0) / y
5. x == y
6. x != y
```

Now let's talk about Booleans.
Simply put, a boolean variable is either True or False, and every python object or data has a boolean value.
We can find out what the true-false value is by using bool()

Let's try it out:
```python
>>> bool(False)
False
>>> bool(True)
True
>>> bool(0)
False
>>> bool(7)
True
>>> bool(None)
False
>>> bool(7 == 0)
False
>>> 7 == 0
False
```
Last stop on our journey into basic data types: Strings
A string is a sequence of characters, for example "Hello" or "My id # is 1235!"
Let's try a few in our shell:
```python
>>> "Hello World!"
Hello World!
>>> "Hello" + " World!"
>>> 1 + "world"
```

Practice problem:
```
- Set a variable called `name` equal to your full name.
- Set a variable called `first_name` equal to your first name.
- Set a variable called `last_name` equal to your last name.
- Then combine `first_name` and `last_name` so that it equals your full name, and save this in a variable called `full_name`.
- Prove using the == operator that they are equal.
```

# Lists
Lists is a super useful data type.
It's an ordered collection of items, which you can modify by adding or removing elements.

Let's learn the syntax of a list:
```python
>>> x = [1, 2, 3, 4, 5]
>>> len(x)
5
>>> # what's between the brackets is called the index
>>> x[0]
1
>>> x[1]
2
>>> x[4]
5
>>> x[6]
IndexError
>>> x.append("hello")
>>> len(x)
6
>>> x[5]
"Hello"
>>> # can remove elements, defaults to popping off the last one
>>> x.pop()
>>> print x
>>> # can specify the index
>> x.pop(2)
>>> print x
>>> # can do a boolean check if something is in the list
>>> 5 in x
False
>>> 1 in x
```

Practice problem:
```
- Create a list called `restaurants` consisting of the following elements in this order:
"Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"
- Get the third element of the list
- Add "Ootoya" to the end of the list
- Use .pop() to remove "Random String" from the list
- Print the list
- Check if 'Chipotle' is in the list
- Check if 'Random String' is in the list
- Get the length of the list
```

Let's learn about slicing:
```python
>>> y = [1, 2, 3, 4, 5, 6, 7, 8]
>>> y[2:]
>>> y[:4]
>>> y[1:3]
```

# Dictionaries
Dictionaries are also massively useful. You can think of them as maps, between as set of keys and their corresponding values.
Let's look at one in the shell to better understand how they work and how they can be useful:

```python
>>> # Here's the syntax, {} with key:value, with key being a string.
>>> person = {"name": "John Jameson", "age": 31, "hobbies": ["tennis", "python", "piano"]}
>>> person["name"]
>>> # like a string, we use the brackets but instead of the index, we provide the key name
>>> person["age"]
>>> hobbies = person["hobbies"]
>>> len(hobbies)
>>> hobbies[1]
>>> person["random"]
KeyError
>>> person["location"] = "New York"
>>> person["deepest_darkest_secret"] = "Loves Vampire Diaries"
print person
>>> del person["deepest_darkest_secret"]
print person
>>> person.keys()
>>> person.values()
>>> person.items()
>>> # check if a key exists in the dictionary
>>> "name" in person
>>> "secret" in person
```
Practice problem:
```
Create a dictionary called `class_data` with the following keys:
- "course_name", which should correspond to "Intro to Python"
- "student_count", which should correspond to number of students, say 20
- "instructor", which should itself be a dictionary with the following keys
    - "name" ("Suneel")
    - "gender" ("M")
    - "can_program" (True)
- get the student count from the dictionary
- get the instructor name from the dictionary
```

# If/Else
If/else statements are blocks of our code that allow us to do different things based on some logical condition
Let's learn the syntax, note INDENTATION is important:
```python
>>> x = 5
>>> if x > 4:
        print "Hello"
    else:
        print "World"
Hello
>>> if x < 5:
        print "Less than five"
    else:
        print "Greater than or equal to five"
>>> if x == 1 or x == 2:
        print "Ha"
    elif x == 3:
        print "Hey"
    else:
        print "Hi"
```

Practice problem:
```
Given x = "John Jameson",
- Construct an if else statement according to this logic: if "John" is in x, print "John is in x", otherwise print "John is not in x"
- Construct an if/elif/else statement according to this logic: if "roger" is in x, print "Hi Roger!", elif the length of x is greater than 20, print "thats a long string", else print "Oh well!"
```

# Loops
Loops let us pass through a set of values and do some operation on each.
There are different kinds of loops, for loops and while loops. They're quite similar, but let's look at the canonical loop, the for loop.

```python
>>> numbers = [1, 2, 8, 7, 9, 10]
>>> odds = []
>>> for cat in numbers:
        if cat % 2 == 1:
            odds.append(cat)

print odds
```
- the `number` in the for loop syntax is a dummy variable that refers to the element in the list that we're passing through. The first time around, number refers to 1, the last time it refers to 10.
- we are going through this list and if the number is odd, we add it to the odds list that we initialized before the for loop.

Before we move on to some practice problems, here is a useful function:
```python
>>> range(10)
```

Practice problems:
```
- Construct a list of numbers between 0 and 1000 that are divisible by 33
- Given the following list
["Donald Duck", "Mickey Mouse", "Daffy Duck", "Goofy", "Minnie Mouse", "Pluto"]
Get the sum of all of the lengths of these strings.
- Given the above list, create a list of all of the elements that have the letter "d" or the letter "m" in them
```

# Functions
Functions are the heart and soul of python. Functions are blocks of code that take an input and based on some rules produce an output.

Let's learn the syntax of functions:

```python
>>> def add(a, b):
        return a + b
>>> z = add(3, 4)
>>> print z
```
a and b are variables that the function `add` takes

Practice problems:
```
- create function `multiply` that takes two variables and returns their product
- create function `subtract` that takes two variables and returns their difference
```

Let's write a function that takes a variable, which is a list of numbers, and then returns just the ones that are divisible by 33.

```python
def div_by_33(numbers):
    by_33 = []
    for number in numbers:
        if number % 33 == 0:
            by_33.append(number)
    return by_33
```

Practice problem: Write a function that takes a list of numbers and retursn True if the sum of the numbers is even and False otherwise.

# Try/Except Statement
What happens when we try to cast a string like "Hello" to an integer?

## Exercise
Write a division function `divide(a, b)` that catch exceptions and return an error string if the arguments do not make sense.

# 'Real-life' problem: Restaurant Recommendation Engine (for after-class practice)
- figuring out where to eat lunch everyday is annoying
- let's automate it
- First version is going to be given a list of restaurants, randomly pop out a recommendation until the list is depleted

Let's learn about the random library, a pretty useful builtin python library:
```python
>>> import random # this is how we make accessible the random library code
>>> numbers = [1, 3, 5, 6, 7]
>>> shuffled = random.shuffle(numbers)
>>> for number in shuffled:
        print number.pop()
```

Problem 1:
```
Given a list of restaurants,
["Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"]

Write a function that takes the list of restaurants, shuffles the list,
and one by one pops out a restaurant as a recommendation.
```

What happens when we deplete the list and need to recommend again, let's go by the following algorithm:
- Each time, randomly recommend a restaurant from the list that has not been recommended in the last 4 tries

We're going to create a file called recommender.py and type the below in there.

```python
import random

# Keep track of the recommendations
recommendation_history = []
restaurants = ["Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"]

def recommend(restaurants):
    random.shuffle(restaurants)
    for choice in restaurants:
        if choice not in recommendation_history[-1: -4]:
            return choice
```

# Useful python libraries to know
- random
- math
- datetime
- collections
- csv

---

# Objectives for Part 2
The primary goal is to get the students comfortable enough with `pandas` to apply it to their data processing and analysis tasks.

Students will be able to use `pandas` to
- perform data analysis
- read in CSV data
- perform data munging and cleaning on dirty data
- apply advanced pandas techniques such as grouping, aggregation and pivot tables

# Agenda
1. Python Warm Up
2. Using Documentation
3. Go Deep into Pandas
4. Wrap Up & Next Steps

# Python Warm-Up / Review (20)
This problem will give us a review of lists, for loops and lambda functions

Given the following list,

```
names = ["Michael Fassbender", "Karlie Kloss", "Taylor Swift", "Justin Bieber"]

```
1. print out the names that contain the letter "l"
2. turn all of the names lowercase
3. sort the list of names alphabetically using the built-in `sorted` function (HINT: Use Google)
4. sort the list of names by length using the built-in `sorted` function


# Warming Up to Documentation (20)
What is a library? A reusable, collection of code that someone else (or you) has already written. Some great built-in libraries:
- `random`
- `csv`
- `collections`
- `datetime`

To use other libraries, we need to be able to:
- understand the documentation of that library
- understand what the inputs and outputs of their functions are
- how to call those functions correctly

Let's start with the random library.

## The `random` library.
Our first step is to locate the documentation. Google "python random". It should take you [here](https://docs.python.org/2/library/random.html)

Let's import the library
```python
>>> import random
>>> dir(random)
```

How does python know what `random` is and how to find the code? Because it comes built-in to the Python language. Other libraries such as `pandas` will have to be installed prior to use.

### Exercises
1. Find the `randint` function in the documentation and explain to your neighbor what it does and how to use it.
2. Again, with your partner, use the `randint` function to generate a random number between 1 and 125.

## What is `as`?

Let's see what happens:
```python
>>> import random as rd
>>> random.randint
>>> rd.randint
```

# Pandas (65)
*Question* What is [`pandas`](http://pandas.pydata.org/pandas-docs/stable/)?

[Here](https://s3.amazonaws.com/python-level-2/sales-funnel.csv) is our first data set. Let's download it and upload it to the datasets folder within the notebook.

## Preliminary Exercise
With your partner
0. Download and open the dataset
1. What is this dataset about?
2. What are some questions you might ask about the data?

## Basic Manipulation (75)
0. Let's read in the data.
0. How do we see what columns are available?
1. How do we look at just the head or tail of the dataset?
2. How do we look at only a few rows?
3. How do we only look at certain columns?
4. How do we pull out a column and look at it as a series?

## Filtering DataFrames (80)
0. How do we look at only those rows that have Status = won
1. Exercise: How many accounts have a price greater than $12,000?
2. How do we get the maximum value of a certain column?
3. Exercise: What is the minimum account price? The mean? The sum? The standard deviation?

## Aggregating data (120)
What is the total dollar amount pending?

0. How do we add columns?
1. Let's add a column called Amount that is equal to Quantity * Price
2. Exercise: Let's select just those rows where status is pending and sum up those amounts.

## Pivot tables (130)
*Question*: What are pivot tables? Why are they useful?

Let's take a look at the documentation [here](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.pivot_table.html).

0. Let's pivot using one index.
1. Let's pivot on multiple indexes
2. Let's reverse those indexes
3. Let's specify which values we care about
4. Let's specify which columns we want broken down
5. Let's specify how we want the values to be aggregated (`aggfunc`)
6. Let's fill N/A values
7. Let's get subtotals

(Creative) Exercise: with a partner, use pivot tables to play around with the data. What pivots do you find particularly interesting or useful for this dataset?

## Plots from the dataframe
Let's see documentation on DataFrame.plot

1. Let's pivot and sum up Amount by Account Name
2. Reset index so we get a normal pivot table again
3. Make a clean bar chart.


# More Pandas (120)
Let's expand our Pandas knowledge and practice it with another dataset.

Download [this dataset](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/rock.csv)

## Preliminary Exercise
1. Take 2 minutes to download this dataset and examine it.
2. Take 4 minutes to talk with a partner about the dataset and what kinds of insights you might extract from the data.
3. Share with the class.

## Exercises (125)
1. Read in the dataset from the url
2. Solo: How many songs were released in 1981
3. What is the earliest release year in the data (Hint: there might be dirty data...)

## Data munging (135)
### Using `.apply()` to clean up the year.
Let's create a new column that contains the clean year

### lambda functions (150)
Sometimes the data manipulation we'll want to do on a column will be pretty simple, so we can apply it in place. Say for example we wanted to lowercase an entire column

```python
>>> df["lowercase_title"] = df["Song Clean"].apply(lambda val: val.lower())
```

#### lambda function exercises
1. Create a new column called "contains_Rock" and the value should be True if the title contains the word "Rock" and False otherwise
2. Create a new column called "contains_rock" and the value should be True if the title contains "rock" regardless of case (so it could contain "Rock", "ROCK", "roCK", etc) and False otherwise

## Using `value_counts` (175)
Pull up the pandas value_counts documentation.
We'll answer the following: What are the top 20 songs by play count?

```python
>>> df["ARTIST CLEAN"].value_counts()[:20]
```
## Using `groupby` (180)
Pull up the Pandas `groupby` documentation.
We'll look at play count grouped by artist.

```python
>>> df.groupby("ARTIST CLEAN")["PlayCount"].mean()
```

# Even More Pandas (190)
Let's look at [this dataset](https://raw.githubusercontent.com/suneel0101/lesson-plan/master/crunchbase_monthly_export.csv) from Crunchbase

## Preliminary Exercises
1. Solo: Read in the data. What is this data about? What are some questions you want to answer about the data?
2. What is the max funding total?
3. Partner: Anything interesting/strange about the column names?
4. Class altogether: Let's rename the column names accordingly.

## Using `.describe()` to get some descriptive statistics
Pull up the pandas DataFrame `describe` documentation.

## Exercises (200)
1. Construct a pivot table that indexes on region and shows the total funding amounts by region
2. What is the average number of funding rounds for companies in NYC? How does that compare to SF?
3. What are the top 3 markets with the highest average funding total per company?
4. How many companies have Games as a category? What's their average funding total? Using a pivot table, what's the average funding total of those companies that have Games as a category, broken down by Region?
5. What is the most popular category of company?

## Practice on revenue schedules data

Notes: df.dtypes; Parsing datetimes

1. How much money won YTD? lost?
2. What's the close rate by Account Owner?
3. What's the total number of accounts broken down by Account Owner
4. What's the average opportunity amount per closed account broken down by Account Owner
5. Create a pivot table indexing on Account Name that shows the total amount in each stage, YTD and then separately since the beginning of the data set
6. What plots would be useful?

## Practice on leads data
1. What pivot tables would you care about? Create them.
2. What are the top original referrer domains of leads that have converted in 2015?

# Sharing Our Analysis
1. Download the iPython notebook
2. Paste it into a [GitHub gist](http://gist.github.com)
3. Copy the URL of the gist and paste it [here](http://nbviewer.ipython.org)
4. Voilà, now you have a shareable analysis!