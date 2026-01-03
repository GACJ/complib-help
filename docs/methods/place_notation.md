# Place notation
There are many different ways that change ringing methods can be written down. Most often they are represented visually as a *blue line diagram*, which can aid in memorisation. Some methods can be learned according to a rule such as *"first, treble-bob, last, near, full, far..."* which expresses the blue line concisely as a short phrase.

However, in order to refer to a specific method uniquely, we need a (compact) way of expressing what exactly every bell does while ringing it. Place notation is a tool invented in order to do just that.

## The basic concept
We'll be making use of the following definitions:

Row
:   An ordering of the bells 1 to *n*, where *n* is the total number of bells being rung. A row is written in ringing order left to right. Each bell rings once and only once within a row. 

    For example:

    * **135246** is a row;
    * **987654321** is a row;
    * **113478** is *not* a row (why?).

Change
:   The action of moving from one row to another by altering the order of the bells; or, the relationship between two rows in terms of how they differ. In order to qualify as a change, the following condition must be satisfied:

    - The two rows must have the same number of bells.

    For most of change ringing history, changes were also required to satisfy a second condition:

    - In going from one row to another, no bell should move more than one position forward or backward within the row.
    
    Changes which do not satisfy this latter condition are known as **jump changes**. 
    
Methods using jump changes are still extremely rare, and so we will assume for the moment that we are dealing with changes which satisfy both of the conditions above.

Consider these two rows related by a change:

```text
A: 1 4 2 5 3 6

B: 4 1 2 3 5 6
```

How can we express the change? 

We can start by making a note of which bells do *not* change position between the two rows. In the above example, bells `2` and `6` are the only ones which remain fixed across the change. We could try writing down the numbers of the bells, but that would not be a sensible solution. To see why, consider this other pair of rows related by a change:

```text
C: 6 5 4 3 2 1

D: 5 6 4 2 3 1
```

It should be apparent that the relationship between rows C and D is the same as that between rows A and B: if we were to relabel the bells in row C so as to match row A, then the row D obtained under the same relabelling would match row B.

In other words, the change between rows A and B is *the same* as the change between rows C and D, even though the rows themselves are different. Any sensible notation should be able to express this in a way which is independent of the specific rows. Therefore, rather than the numbers of the bells which do not move between rows, we should note the *position* of those bells instead.

Here's the first example again, this time with lines drawn to show the motion of the bells between rows:

```text
A: 1 4 2 5 3 6
    x  |  x  |
B: 4 1 2 3 5 6
```

Bells 2 and 6 are the only ones which stay in the same place, those places being 3rd and 6th within the row. Similarly, going from row C to row D, the bells in positions 3 and 6 are the only ones which don't move:

```text
C: 6 5 4 3 2 1
    x  |  x  |
D: 5 6 4 2 3 1
```

In change ringing, a bell which stays in the same position between rows is said to *make a place* in that position. Place notation is so named because it expresses changes exclusively in terms of which places are made between rows.

## Place notation elements and strings
To represent a change, we list the positions of the bells which make places between two rows in numerical order. The change in the examples above would be written as **36**. This is an *element* of place notation (sometimes also called a *unit*). Each element of place notation expresses a single change.

Here are some more example changes and the place notation elements which represent them:

```text
1 3 2 5 4 6
| |  x   x
1 3 5 2 6 4
```

Place notation: **12**

```text
1 3 5 7 2 4 6 8
|  x  | |  x  |
1 5 3 7 2 6 4 8
```

Place notation: **1458**

```text
1 2 3 4 5 6 7 8 9 0
 x  |  x   x  | | |    
2 1 3 5 4 7 6 8 9 0
```

Place notation: **3890**

There is a special type of change possible on even numbers of bells in which no bell makes a place between rows. For example:

```text
1 2 3 4 5 6
 x   x   x
2 1 4 3 6 5
```

This change is sometimes called the **cross change**, and is notated using the special element **–** (or **x**).

To perform a method, several changes must be made one after the other in sequence. To use place notation to write methods, we need a way of concatenating place notation elements together.

A *string* of place notation is a series of elements written in sequence. To avoid ambiguity about the boundaries between elements, dots . are added between any two elements which are not the cross change. For example, the sequence of changes in which change **14** is followed by change **36**, which is followed by change **1458**, would be written **14.36.1458**.

It is not necessary to use dots to mark the bounds of the cross change: replacing **36** with the cross change in the former example would give **14-1458**.

This simple notation is already powerful enough to uniquely express every "conventional" method that has ever been rung. For example, here are some place notation strings corresponding to a single lead of some well known methods:

[Plain Bob Minor](https://complib.org/method/11349)
:   -16-16-16-16-16-12

[Cambridge Surprise Minor](https://complib.org/method/14568)
:   -36-14-12-36-14-56-14-36-12-14-36-12

[Bristol Surprise Major](https://complib.org/method/19048)
:   -58-14.58-58.36.14-14.58-14-18-14-58.14-14.36.58-58.14-58-18

## Condensed place notation
Strings of place notation can become rather cumbersome when written out in full. However, for many methods we may leverage their inherent symmetry to produce a *condensed form* of the place notation.

The very significant majority of named methods are **palindromic**, which means that their sequence of changes is the same when reversed. Looking at the three examples above, if we ignore the final elements in each case, the remaining strings are all symmetrical about their central elements. For example, take Cambridge Surprise Minor:

-36-14-12-36-14-**56**-14-36-12-14-36-(12)

The lead has a symmetry point at the change **56** (and also at the final change, if you want to be picky). This means that this place notation string is about twice as long as it needs to be, because all the changes in the second half are already expressed in the first half in reverse order.

We can now introduce the convention that a comma `,` within a place notation string separates any palindromic substrings. With this convention, the place notation for Cambridge becomes

-36-14-12-36-14-56,12


The full place notation can be obtained from the condensed form by way of the following steps:

1. List the elements before the comma from left to right;
2. List the elements before the comma from right to left;
3. Join the strings obtained from steps 1 and 2 together at the repeated element;
4. Repeat steps 1 and 2 for the section after the comma;
5. Concatenate the strings obtained from steps 3 and 5.

Writing these steps out for our example, we have:

Step 1: List the elements before the comma from left to right.

-36-14-12-36-14-56

Step 2: List the elements before the comma from right to left.

56-14-36-12-14-36-

Step 3: Join the strings obtained from steps 1 and 2 together at the repeated element.

-36-14-12-36-14-56-14-36-12-14-36-

Step 4: Repeat steps 1 and 2 for the section after the comma.

12

Step 5: Concatenate the strings obtained from steps 3 and 5.

-36-14-12-36-14-56-14-36-12-14-36-12

And we are done.

Step 4 seems somewhat trivial in this example because the substring after the comma in the condensed place notation has only a single element. However, it is crucial that both substrings be treated as palindromic for this convention to work. This is because there are many palindromic methods which have their points of symmetry in a different place. 

The best example of this is Grandsire, in which the point of palindromic symmetry is offset from the midpoint of the lead. The full place notation for a lead of [Grandsire Doubles](https://complib.org/method/10587) is

3.1.5.1.5.1.5.1.5.1

which condenses to

3,1.5.1.5.1

## Alternative conventions
When [creating a custom method](adding_methods.md) on Complib, you may use either the full or condensed form of the notation as specified above. You can use either **–** or **x** to represent the cross change. Complib will automatically condense the notation when validating the method, provided that the place notation itself is valid.

While they can't be used for defining methods on Complib, there are other conventions for writing place notation, many of which are still very common. For the sake of convenience, here are a few you are likely to encounter elsewhere.

### MicroSIRIL notation
MicroSIRIL notation consists of three parts: a method group indicator, a symmetry indicator, and the place notation itself. 

Method group indicator
:   This is the alphanumeric code which specifies the first leadhead of the method, as well as what change is made at the leadend (see [Leadhead codes](../advanced/leadhead_codes.md)).

    A code of **z** indicates that the method does not have a standard leadhead code. In such cases, the place notation will be given in full.

Symmetry indicator
:   An ampersand **&** at the start of a place notation string is used to indicate that the string which follows is palindromic about its last element. This is similar to the comma notation.

    For example, **&-16-14** represents the same string as **-16-14,**

    A plus symbol **+** is used to indicate that the following string is non-palindromic, and should be read verbatim.

??? note "Example: Cambridge Surprise Minor"
    ---
    In the MicroSIRIL format, Cambridge Surprise Minor is written:

    > b &-36-14-12-36-14-56

    From this we can read off that the method is in group **b**, meaning the leadend change is **12**, and that the method is palindromic.

??? note "Example: Scientific Triples"
    ---
    In MicroSIRIL format, [Scientific Triples](https://complib.org/method/27989) is written:

    > z +3.1.7.1.5.1.7.1.7.5.1.7.1.7.1.7.1.7.1.5.1.5.1.7.1.7.1.7.1.7

    The method group indicator is z, meaning that it does not have a standard leadhead code. **+** indicates the place notation should be read as-is, and should not be interpreted as palindromic.

Leadhead change
:   A place notation element prefixed with **lh** or **le**, or sometimes simply separated from the main string by a space, is used to denote the leadhead (or leadend) change. This is most often used as an alternative to the method group indicator in MicroSIRIL format.

    Sometimes the actual leadhead row will be given rather than the place notation element. In order to obtain the terminal element, you will need to work out what change must be made at the end of the lead to get to the specified row.

## Jump changes
Coming soon!