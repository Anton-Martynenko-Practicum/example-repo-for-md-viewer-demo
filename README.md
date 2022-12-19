# Loops

In normal life, people often have to perform series of identical operations.

For example, completing the task of “washing a pile of dirty dishes” would imply performing the following operation: take a plate — wash it — rinse it — wipe it — put it away — take another plate — wash it — ... and so on.

This process is not endless. Work continues only on the condition that there are dirty dishes left. No more dirty plates — the work is over.

![image](https://practicum-content.s3.us-west-1.amazonaws.com:443/resources/34Artboard_1_copy_591.5x_1667305135.png)

Certain things in development are very similar to washing the dishes. You have to perform the same actions with each element of a list. This is a pretty common type of operation.

Let's consider a list of the members of The Beatles.

```python
the_beatles = ['John', 'Paul', 'George', 'Ringo']
```

We need to print their names on the poster like this:

```
John
Paul
George
Ringo
```

How do you do this in Python? We can manually print each element:

```python
print(the_beatles[0])
print(the_beatles[1])
...
```

We would have to write the same code five times. But what if we're dealing with a larger list of members? Not a rock band but a large symphony orchestra with a choir?

Remember washing plates — it's all about repeating identical operations. First, you need to take the first element of `the_beatles` list, print it using `print()`, then take the next element... and continue until the last element of the list has been processed.

{{**Loops**}}[be_python_loop] were invented to perform repetitive operations like this. Loops perform certain instructions until a given condition is met.

# Syntax

##  Loop declaration

For the program to understand where a loop starts, you need to **declare a loop** — tell the program about the loop using special keywords. Python has several types of loops. The simplest loop for iterating over a list is `for … in …`. So let's start there.

This loop is declared using the keywords `for` and `in`; the loop declaration should always end with a colon.

Below the declaration you'll write the **loop body** — code that describes what needs to be done with each element of the list.

```python
for variable in item_list: # Loop declaration
   # Loop body
    
```

The name of the variable in which the elements of the processed list will be temporarily saved one by one following `for`. The name of the list to be processed follows `in`.

To continue the metaphor, if a list of elements is a pile of unwashed plates, the variable declared in the loop condition is every plate taken from a pile.

The loop will automatically terminate when it has gone through all the elements in the list.

You can give any name to the variable in the loop declaration, but traditionally the name is based on the name of the processed list in the singular form. For example, if the list is called `musicians`, the variable would be called `musician`; if the list is called `cats`, the variable would be called `cat`.

## Loop body

Once we've declared the loop, we can write **the body of the loop** Each line in the loop body should be indented with four spaces:

```python
for variable in item_list:
    # Here's the start of the loop body: this code will be executed for each element
    # You can do something with the variable declared in the loop condition,
    # like print its value: print(variable)
```

![image](https://practicum-content.s3.us-west-1.amazonaws.com:443/resources/2.2.2_1667304276.png)

Now we can write a loop that will automatically print the names of The Beatles members.

```python
the_beatles = ['John', 'Paul', 'George', 'Ringo']

for musician in the_beatles:
		# Each element of the_beatles
    # will in turn be passed to the musician variable
    # and printed
    print(musician)

# There may be some code here that will be executed
# only after the loop has finished
```

The loop takes the value of the first element from `the_beatles` list and passes it to the `musician` variable. Then the code in the body of the loop is executed and the value of the `musician` variable is printed.

After that, a new cycle of the loop begins with the next element in the list. It will continue like this until the loop has gone through the entire list.

Each cycle is called an **iteration of the loop**.

When the list ends, the program will exit the loop and continue executing any code written after the loop.

Translation:

![image](https://practicum-content.s3.us-west-1.amazonaws.com/new-markets/Python/ENG/10112022_KF_yaPers_animation_belka_EN.gif?etag=b49231e10d402aaf2ce96cb0c6df289e)

### Ready to run!

Run the code and check out the result of the execution. Add a few more musicians to the list (for example, Yoko Ono or Pete Best) and run the code again.
