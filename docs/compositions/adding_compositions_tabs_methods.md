# The Methods tab
![Methods tab example](../img/methods_tab_example.png)

The Methods tab is a table which allows you to define the methods which are used in a custom composition. Every composition must have at least one method definition. 

To edit any value in the table, simply click on the relevant cell, then type a new value. Multiple cells can be highlighted by clicking and dragging. Alternatively, you can click on a cell, hold <kbd>Shift</kbd>, and then click on another cell.

If you have filled out the [Title](adding_compositions_tabs_general.md/#title) field under the [General tab](adding_compositions_tabs_general.md), then the Methods tab may already be populated with one or more entries.

## Method title
To manually add methods to the table, begin typing its title in the [Method title](#method-title) column. As you type, Complib will attempt to auto-complete with the titles of any matching public methods, or private methods which you own. 

Once a recognised method title has been entered, the rest of the cells in the row will auto-populate with default values appropriate to that method.

### Deleting methods
Deleting a method's name in the table will delete all its associated information as well.

### Adding methods from a collection
You can add methods directly from an existing method collection. This can be useful if you need to add a large number of methods to the tab.

To add methods from a collection, click on the dropdown menu above the methods table, then click on a method collection. The table will be populated with all the methods in that collection.

It's possible to add methods from multiple collections in this way, though the methods must all be at the same stage for this to work.

Methods already in the table will not be duplicated if they are added again via collection. **If you want multiple copies of a method, you must add them manually.**

## Mnemonic
A method mnemonic is a one- or two-character code which is used to represent the method in the composition's [layout](overview.md/#layout). Mnemonics are displayed by default in compositions of spliced, but they can be enabled for any composition by selecting **Columns > Method mnemonics** in the [composition layout options](layout_options.md).

![Mnemonics example](../img/mnemonics_annotated.png){width="400"}

!!! warning "Mnemonic restrictions"
    Method mnemonics must have an uppercase letter [A–Z] as their first character. This may be optionally followed by a lowercase letter [a–z] or number [0–9].

    Method mnemonics must be unique. If two methods used in a composition have the same mnemonic, it will cause an error.

### Default mnemonics
When a method is added to the Methods tab, its mnemonic will be the **first letter in its title** by default. Any numbers and special characters at the beginning of the title will be ignored. For example, ['ogwash Delight Minor](https://complib.org/method/30148) has a default mnemonic of "O".

Deleting a method's mnemonic from the table will reset the mnemonic to its default value.

If a method is given a mnemonic which is different from its default in a composition of spliced, then the mnemonic will be appended to the method's name at the bottom of the composition layout.

## Starting place
This field defines the row position above which the changes of the method will be applied. In effect, this defines where the "front" of the change is when ringing the specified method. 

Bells in positions which fall outside the bounds of the method will remain stationary whenever the method is rung in the composition.

??? note "Example"
    ---
    
    ![Bristol Major on 10 with starting place of 1](../img/starting_place_1.png){width="150"} &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    ![Bristol Major on 10 with starting place of 3](../img/starting_place_3.png){width="150"}

    These examples show the first half-lead of [Bristol Surprise Major](https://complib.org/method/19048) being rung on 10 bells, but with different starting places. Since the method's stage has 8 bells, there are two stationary bells.

!!! warning "Starting place restrictions"
    The starting place cannot cause the method to go outside the bounds of the composition's stage. 
    
    The minimum starting place is 1. The maximum starting place is (*N* – *M* + 1), where *N* is the stage of the composition and *M* is the stage of the method.

    This means that it is only possible for a method to have a starting place greater than 1 when used in a composition whose stage is greater than its own, such as in **mixed-stage compositions**.

## Rotate by
This field specifies an amount by which the method's [place notation](../methods/place_notation.md) will be rotated. 

When Complib pricks (generates the rows of) a composition, it does so by applying the elements of the current method's place notation in sequence. By default, the pricker will begin from the first element of the method's place notation. When it reaches the end, it will start the place notation again from the beginning, provided there is no change of method.

When a **Rotate by** value is specified, that many elements will be removed from the front of the method's place notation and reinserted at the end. This modified place notation then becomes the place notation for the method within the composition, and its final element is the new leadend change.

??? note "Example"
    ---

    Below are the plain courses of two different rotations of [Double Court Bob Minor](https://complib.org/method/11118), together with their place notations. Lines are drawn through bell number 2, as well as the hunt bell in each case.

    **Rotate by = 0**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`-14-36-16-36-14-16`

    ![Double Court Bob Minor, unrotated](../img/double_court_unrotated.png)

    ---

    **Rotate by = 5**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`16-36-14-16-14-36-`

    ![Double Court Bob Minor, rotated by 5](../img/double_court_rotated.png)

!!! warning "Rotate by: restrictions"
    The **Rotate by** value must be between 0 and (*L* – 1), where *L* is the **lead length** of the method. Attempting to specify a **Rotate by** value that falls outside this range will cause an error.

    The lead length of a method is listed under the Properties tab on its Method page (see [Method properties > Miscellaneous](../methods/method_properties.md/#miscellaneous)).

## Start row number
This field specifies which row of the method it should be started from. The default value is 0. Almost all methods are rung with a starting row of 0.

When a Start row number is specified, that many elements will be removed from the method's [place notation](../methods/place_notation.md). The removed elements are **not** reinserted elsewhere, and the leadend change remains the same. The place notation of subsequent (consecutive) leads of the method is not affected. 

Whenenever a change-of-method results in this method being rung, this operation is applied again.

??? note "Example"
    ---

    ![Double Norwich Court Bob Major, starting at row 5](../img/dncbm_startrow_5.png){width="300"}

    The above diagram shows part of a composition of [Double Norwich Court Bob Major](https://complib.org/method/12470) in which the method's Start row number has been set to 4. Four elements have been removed from the place notation of the first lead, resulting in a lead which is four rows shorter.  

### Rotate by vs. Start row number
The effects of a method's Start row number on the actual rows of the composition are, in some cases, identical to that of the [Rotate by](#rotate-by) field. The main difference is in which rows of the method will be treated as **leadheads and courseheads** when laying out the composition.

??? note "Example"
    ---

    In this example, a plain course of Grandsire Triples is being rung with a Start row number of 4.

    ![Grandsire Triples starting at row 4, blue line](../img/grandsire_startrow_4.png)

    In a blue line diagram, the rows which Complib considers leadheads have horizontal lines drawn above them by default. For coursehead rows, the lines are blue.

    When laid out by leads, the layout for this composition looks like this:

    ![Grandsire Triples starting at row 4, layout](../img/grandsire_startrow_4_layout.png){width="300"}

    ---

    A touch containing identical rows can be defined using a rotation instead. However, the appearance of the composition will be different. If instead the **Rotate by** value is set to 4, the blue line diagram becomes:

    ![Grandsire Triples rotated 4 changes, blue line](../img/grandsire_rotated.png)

    And the corresponding layout:

    ![Grandsire Triples rotated 4 changes, layout](../img/grandsire_rotated_layout.png){width="300"}

!!! warning 
    A method's Start row number should not be confused with the [composition's Start row number](adding_compositions_tabs_general.md/#start-row-number), which is set under the General tab. 
    
    The difference is that a method's Start row number is part of its definition, and will combine with other parts of the method's definition (such as [Length](#length) and [Lead position row number](#lead-position-row-number)) to determine how every lead of it in the composition is rung. 
    
    By contrast, a composition's Start row number affects only the first lead of the composition, and has no bearing on a method's definition.

    If **both** a method and the composition's Start row numbers are non-zero, then their effects may be combined. This can have unintended consequences. In almost all cases, it is only necessary to set one of them.

## Length

## Lead position row number

## Lead position name

