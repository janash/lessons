---
title: "Python Coding Style"
teaching: 15
exercises: 0
questions:
- "How should python code be styled?"
objectives:
- "Understand pep8 styling guidelines for Python."
keypoints:
- "PEP stands for Python Enhancement Proposal."
- "PEP8 gives styling guidelines for python"
- "Variable and function names should be lowercase with underscores _ separating words."
---

## Coding Style

As a developer, you will spend a lot of time thinking about writing your code. However, code is read much more often than it is written. Following a style guide will help others (and perhaps you in the future!) to read your code.

For Python, the common convention for code style is called [PEP8](https://www.python.org/dev/peps/pep-0008/). PEP8 is a document that gives guidelines for best practices in Python coding style. PEP8 is a recommendation, not rule. However, you should follow this convention when possible.

> ## Python PEP
>
> If you spend a lot of time programming in Python, you will see references to PEPs. PEP stands for "Python Enhancement Proposal". These are design documents which provide information about features. PEPs come from the Python community, meaning anyone can author a PEP (however, there is a strict review process). PEPs are classified into three categories - standards, informational, or process.
>
> You can read more about PEPs in [Python's documentation](https://www.python.org/dev/peps/pep-0001/). PEP1 outlines what a PEP is and how they work.
{: .callout}

PEP8 tells us several things about styling that will make our code easier to read. Let's consider some of these.

## Variable names
PEP8 recommends that

> Never use the characters 'l' (lowercase letter el), 'O' (uppercase letter oh), or 'I' (uppercase letter eye) as single character variable names.
 
> Function names should be lowercase, with words separated by underscores as necessary to improve readability.

Though not specifically reference in PEP8, we also recommend making all variable names descriptive so that someone reading your code can easily understand what the variable is. 

## Indentation

PEP8 indicates that indentation should be 4 spaces per indentation level. If you use Jupyter or another text editor which is made for Python development, this should be set automatically. For VSCode, you can see the indentation level on the lower right of the program (should say 'Spaces: 4')

## Whitespace

> Always surround these binary operators with a single space on either side: assignment (=), augmented assignment (+=, -= etc.), comparisons (==, <, >, !=, <>, <=, >=, in, not in, is, is not), Booleans (and, or, not).

This means that every time we have an expression assigning a variable, it should be `variable = value` instead of `variable=value`.

You can also use whitespace to separate ideas within a function or code.

> Use blank lines in functions, sparingly, to indicate logical sections.

For example, compare the two copies of the same code. The one with whitespace separating ideas is easier to read:

~~~
n_samples = 100

num_inside = 0
for i in range(n_samples):
    # Generate a random point between 0 and 1 for x.
    x = random.random()
    
    # Generate a random point between 0 and 1 for y.
    y = random.random()
    
    ## Calculate the radius of this point.
    r = math.sqrt(x ** 2 + y ** 2)
    
    # if this value is less than 1, the point is inside the circle.
    if r < 1:
        num_inside += 1
        # if inside add to plot
        ax.plot(x, y, 'ob')
    else:
        ax.plot(x, y, 'r*')

ax.set_xlim(0, 1)
ax.set_ylim(0, 1)
~~~
{: .language-python}

~~~
n_samples = 100
num_inside = 0
for i in range(n_samples):
    # Generate a random point between 0 and 1 for x.
    x = random.random()
    # Generate a random point between 0 and 1 for y.
    y = random.random()
    ## Calculate the radius of this point.
    r = math.sqrt(x ** 2 + y ** 2)
    # if this value is less than 1, the point is inside the circle.
    if r < 1:
        num_inside += 1
        # if inside add to plot
        ax.plot(x, y, 'ob')
    else:
        ax.plot(x, y, 'r*')
ax.set_xlim(0, 1)
ax.set_ylim(0, 1)
~~~
{: .language-python}
