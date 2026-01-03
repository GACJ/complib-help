# The Calls tab
![Calling tab example](../img/calls_tab_example.png)

The Calls tab is a table which allows you to define any custom calls which are used in a composition.

To edit any value in the table, simply click on the relevant cell, then type a new value. Multiple cells can be highlighted by clicking and dragging. Alternatively, you can click on a cell, hold <kbd>Shift</kbd>, and then click on another cell.

!!! hint 
    Unlike the [Methods tab](adding_compositions_tabs_methods.md), you do not need to enter anything into the Calls tab in order to create a valid composition. This is because Complib has a number of default calls which account for the majority of those used in actual compositions.

    It's recommended that you leave the Calls tab empty unless your composition requires explicit call definitions. Complib will **automatically remove call definitions that it considers to be unnecessary** before any composition is saved.

## Call Type & Symbol
These fields determine which of a number of standard types the call falls under, and what symbol is used to represent it in the composition's [calling](adding_compositions_tabs_calling.md). 

Complib gives you the flexibility to define calls in whatever way you want. However, most compositions tend to use one of a small number of standard call types. These types (Bob, Single, etc.) are widely used, have commonly accepted meanings, and are often represented with a set of standard symbols. Others are rarer, and may have varied uses across different methods and composers. 

The default behaviour of some call types depend on the [default calls](../methods/method_properties.md/#miscellaneous) of the method(s) currently defined for the composition. However, since there is no need to define any of the default calls explicitly (and in fact Complib will remove any such extraneous definitions), the below examples are included more as a guide as to what each call type "usually" means.

A call symbol can be **any lowercase letter [a–z], or a dash (–)**, with the constraint that **all call symbols in a composition must be unique**.

The standard call types and their default symbols are:

### Bob
*Default symbol*: **–**

The simplest, most common type of call. In single-hunt methods and principles, a bob generally replaces a place made at/after the lead- or section-end with another made elsewhere in the row.

??? note "Example: Plain Bob, 4ths place bob"
    ---
    The diagrams below show the leadend of [Plain Bob Minor](https://complib.org/method/11349) with no call (top) and with a standard "near" bob (bottom). The bob replaces 2nds over the treble with 4ths over the treble.
    <center>
    ![Plain Bob Minor, plain lead](../img/plainbob_plain.png){width="200"}
    
    ![Plain Bob Minor with 4ths place bob](../img/plainbob_bob.png){width="200"}
    </center>

??? note "Example: Double Norwich Court Bob Major, 6ths place bob"
    ---
    [Double Norwich Court Bob Major](https://complib.org/method/12470) with no call (top) and with a standard "far" bob (bottom). The bob replaces *n*ths place over the treble with (*n*–2)'s place over the treble.
    <center>
    ![DNCBM, plain lead](../img/dncbm_plain.png){width="200"}
    
    ![DNCBM, bob lead](../img/dncbm_far_bob.png){width="200"}
    </center>
    
??? note "Example: Stedman Triples, Stedman bob"
    ---
    The six-end of [Stedman Triples](https://complib.org/method/27985) with no call (top) and with a standard "Stedman" bob (bottom). The bob replaces *n*ths place over the six-end with (*n*–2)'s place over the six-end.
    <center>
    ![Stedman, plain six](../img/stedman_plain.png){width="200"}
    
    ![Stedman, bob six](../img/stedman_bob.png){width="200"}
    </center>

In twin-hunt methods, a bob generally replaces *n*ths place *before* the lead end with 3rds made *before* the lead end.

??? note "Example: Grandsire Triples, Grandsire bob"
    ---
    [Grandsire Triples](https://complib.org/method/12415) with no call and with a standard "Grandsire" bob. 
    <center>
    ![Grandsire, plain lead](../img/grandsire_plain.png){width="200"}
    
    ![Grandsire, bob lead](../img/grandsire_bob.png){width="200"}
    </center>

### Single
*Default symbol*: **s**

The second most common type of call. Singles are the counterparts to bobs, in the sense that they usually involve two extra places made in addition to the one(s) made at a standard bob.

??? note "Example: Plain Bob, 4ths place single"
    ---
    The diagram below shows the leadend of [Plain Bob Minor](https://complib.org/method/11349) with a standard "near" single. The single replaces 2nds over the treble with 2nds, 3rds and 4ths over the treble.
    <center>
    ![Plain Bob Minor with 4ths place single](../img/plainbob_single.png){width="200"}
    </center>

??? note "Example: Double Norwich Court Bob Major, 6ths place single"
    ---
    [Double Norwich Court Bob Major](https://complib.org/method/12470) with a standard "far" single. The single replaces *n*ths place over the treble with (*n*–2)'s, (*n*–1)'s and *n*ths place over the treble.
    <center>
    ![DNCBM, single lead](../img/dncbm_far_single.png){width="200"}
    </center>

??? note "Example: Stedman Triples, Stedman single"
    ---
    The six-end of [Stedman Triples](https://complib.org/method/27985) with a standard "Stedman" single. The single replaces *n*ths place over the six-end with (*n*–2)'s, (*n*–1)'s and *n*ths place over the six-end.
    <center>
    ![Stedman, single six](../img/stedman_single.png){width="200"}
    </center>

??? note "Example: Grandsire Triples, Grandsire single"
    ---
    [Grandsire Triples](https://complib.org/method/12415) with a standard "Grandsire" single. Here, 2nds and 3rds are made over the treble at the leadend, in addition to the thirds made *before* the leadend.
    <center>
    ![Grandsire, single lead](../img/grandsire_single.png){width="200"}
    </center>

### Plain
*Default symbol*: **p**

Not traditionally considered a call, a plain indicates a plain lead- or section-end. This call type is mostly only used to explicitly signal to Complib that a lead or section should not have a call made, in cases where it would otherwise attempt to insert a call there.

### Big Bob
*Default symbol*: **x**

Usually used to represent:
    
- A (*n*-4)'s place bob in single-hunt methods on more than eight bells; *or*
- A 6ths place bob on eight bells, if "near" bobs are also being used.

### Big Single
*Default symbol*: *none*

Notionally a counterpart to the big bob. This call type has no default behaviour.

### Bob Single 
*Default symbol*: **b**

This rare call type takes its name from those used by John Holt in his landmark [10-part composition of Grandsire Triples](https://complib.org/composition/29040). It is generally used to indicate a call in which 4ths, 5ths and 6ths are made over the treble at the lead-end (in addition to *n*ths, for odd-bell methods).

??? note "Example: Grandsire Triples with Holt's bob single."
    ---
    [Grandsire Triples](https://complib.org/method/12415) with a Holt's bob single. Thirds is made *before* the leadend as usual; all the bells except those in 2-3 then lie still across the leadend.
    <center>
    ![Grandsire, bob single](../img/grandsire_bobsingle.png){width="200"}
    </center>

### Double
*Default symbol*: **d**

Generally used for a call which extends the standard single with two additional places made.

??? note "Example: Plain Bob Major with a 123456 double"
    ---
    [Plain Bob Major](https://complib.org/method/12834) with a standard double: 2nds, 3rds, 4ths, 5ths and 6ths are all made over the treble at the leadend.
    <center>
    ![Plain Bob, double](../img/pb_8_double.png){width="200"}
    </center>

### Extreme 
*Default symbol*: **e**

This call type has no default behaviour. Similar to the big bob, extremes are usually used to indicate a call with a place made further to the back of the change than a standard bob. 

### Omit 
*Default symbol*: **o**

### Trim 
*Default symbol*: **t**

### Fill 
*Default symbol*: **f**

### Jump 
*Default symbol*: *none*

### Special 
*Default symbol*: *none*

## Notation
The [place notation](../methods/place_notation.md) of the call. If the call affects multiple changes, the notation will have multiple elements.

## Changes replaced

## Lead position name
The unique identifier for a Lead position at which the call can occur. This can be anything you want, so long as it exactly matches a corresponding [Methods > Lead position name](adding_compositions_tabs_methods.md/#lead-position-row-number-and-name) entry under the [Methods tab](adding_compositions_tabs_methods.md).

The Lead position name will appear in the composition's [layout](overview.md/#layout) as part of a custom call definition. However, if the call uses the **LE** Lead position name (see below), this will be omitted from the layout.

### Default Lead positions
Many of the default call types have a default Lead position name which they use. Since they correspond to common calling positions, you may wish to use them even when definining custom calls. The common ones are:

LE
:   Short for "lead end". Used by default for: 
    
    - Near/far/Grandsire bobs and singles;
    - Plains;
    - Big bobs and big singles;
    - Bob singles;
    - Doubles and extremes.

    This calling position, being by far the most commonly used, will **not** be explicitly named in the composition's layout as part of the call's definition.

SE
:   Short for "section end". This is used for Stedman-type bobs and singles by default. 

HL
:   Short for "half lead". Used for trims and fills by default.

## Mnemonic

## Heading

## Observation mask

## Further examples
For more examples of compositions using the Calls tab, [see this reference collection](https://complib.org/collection/10184/?chapter=Calls%20and%20Calling%20Positions). Click on a composition in the collection, then click ![Icon: clone](../img/icon_clone.png){width="25"}**Clone** to duplicate it in the composition editor. Navigating to the Calls tab will give you a peek at how the composer has defined the calls in their composition.