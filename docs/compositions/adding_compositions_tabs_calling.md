# The Calling tab

![Calling tab: Middleton/Johnson calling](../img/calling_middleton.png){width="400"}

The Calling tab is a spreadsheet in which the calling for a composition is defined. The calling specifies the sequence of calls (such as bobs and singles) which need to be made during a performance, including changes of method in Spliced.

!!! note
    In the explanation which follows, it will be assumed that you know how to read compositions. 
    
    If you are not already familiar with how compositions are typically laid out and interpreted, you should visit [How to read compositions](reading_compositions.md) before continuing.

## Editing the calling

To edit the calling, simply click on a cell in the table and type a value to enter it into that cell. 

Multiple cells can be selected by clicking and dragging. Alternatively, you can click on a cell, hold <kbd>Shift</kbd>, and then click on another cell to highlight a rectangle with those cells at opposite corners. Hold <kbd>Ctrl</kbd>/<kbd>⌘ Command</kbd> and click to select multiple individual cells.

⌫/<kbd>Backspace</kbd>/<kbd>Delete</kbd> will delete any values in selected cells.

Right-clicking on a cell will open a contextual menu, allowing you to manipulate the table by inserting or removing table rows and columns:

![Calling tab: right click menu](../img/calling_rightclick_menu.png){width="300"}

### Copy-paste from other sources
In many instances you can save time by copy-pasting a calling from another source. This might be another web page, or a file on your computer.

With the calling highlighted in the source, <kbd>Ctrl</kbd>+<kbd>C</kbd> (<kbd>⌘ Command</kbd>+<kbd>C</kbd>) will copy. Then, in the Calling tab, select **a single cell** and press <kbd>Ctrl</kbd>+<kbd>V</kbd> (<kbd>⌘ Command</kbd>+<kbd>V</kbd>) to paste. 

The calling will be pasted into the table such that the selected cell is in its top left corner.

In many instances you will have to clean up the calling after copy-pasting, as the text formatting in the source can cause problems. Copy-pasting tends to work best if the original is in **plaintext format**, such as a composition attached to a performance on BellBoard.

## Anatomy of callings
Callings are entered into the Calling tab laid out by **courses**. If a composition was originally laid out by leads, you will need to reinterpret this into a course format as you enter it into the Calling tab.

!!! note "Callings versus Layout"
    It's important to remember that **a composition is defined by its calling**, but not by its layout or style of presentation. The same composition can be represented in many different ways. Indeed, Complib gives users [a lot of control](layout_options.md) over the way that any composition appears to them. 
    
    When defining a custom composition on Complib, the most important (and pretty much only) task is to correctly define the calling.

A typical composition, when entered into the Calling tab, might look like this:

![Calling tab example: Spliced Plain Major](../img/calling_tab_annotated.png){width="550"}

*Example: [5000 2-Spliced Bob Major](https://complib.org/composition/21029) by Edward W Martin*

Since you know [how to read compositions](reading_compositions.md), it should be clear from the above example that there is a direct correspondence between the way the calling is entered into the table and how it would normally be written when laid out by courses.

Some composition callings may not have all the features labelled here, while others may have more. The following sections contain information on all the calling features Complib supports and how to use them correctly.

## Calling positions
Calling positions are column headers which signal to Complib when a [call](#calls) in the table should occur.

**A calling position must be a single uppercase or lowercase letter [A–Z, a–z] or a positive whole number**.

**A calling position should be entered in the top row of a column, with nothing in any cell above it.** Failing to do this will cause the calling positions to be incorrectly identified as other objects, such as calls or named blocks.

Compositions generally use one of two types of calling position: [named positions](#named-calling-positions) (represented with letters), or [numbered positions](#numbered-calling-positions). A special kind of named position, unique to Stedman Triples, is used in [twin-bob compositions](#twin-bob-calling-positions).

### Named calling positions
Named calling positions indicate that a call should be made when an **observation bell** reaches a specific part of the course. By default, the observation bell is the heaviest working bell.

Most compositions use a small number of well-known calling positions with special names, such as **H** (Home) and **W** (Wrong). Complib also uses these named calling positions by default. [See the dedicated page on calling positions](calling_positions.md) for a full list of the default positions and their names.

Custom named positions can be created by defining a new [Mnemonic](adding_compositions_tabs_calls.md/#mnemonic) and [Heading](adding_compositions_tabs_calls.md/#heading) in the [Calls tab](adding_compositions_tabs_calls.md). A different observation bell can also be specified using [observation masks](adding_compositions_tabs_calls.md/#observation-mask).

### Numbered calling positions
Numbered calling positions indicate a number of leads/divisions since the last **coursehead**.

When using numbered calling positions, you must provide additional information to Complib to allow it to count the leads/divisions correctly. If possible, you should specify appropriate [coursehead masks](adding_compositions_tabs_general.md/#coursehead-masks) in the General tab. You can also directly [control the length of courses](#manipulating-course-length) in the Calling tab itself.

Since a course can be arbitrarily long, a numbered calling position can be any positive whole number. However, in practice it is very unusual to have courses requiring numbered calling positions with more than two digits. Bear in mind that anyone calling the composition has to count up to that number!

### Twin-bob calling positions
For historical reasons, many compositions of Stedman Triples use a special type of calling position which indicates **pairs of calls**. Such "twin-bob" compositions use four named calling positions, each of which is usually shortened to its initial letter:

> **S**low, **H**alf turn, **L**ast whole turn and **Q**uick.

The twin-bob calling positions correspond to numbered positions as follows:

|Position|Bobs at...|
|-----|--------|
|**S**| 3 and 4|
|**H**| 5 and 6|
|**L**| 7 and 8|
|**Q**| 12 and 13|

**When entering a twin-bob composition in the Calling tab, you should use numbered calling positions**. Complib will automatically recognise the twin-bob calling positions and display them appropriately in the composition layout (provided the user viewing it has [Layout Options > Rows > Expand twin bobs](layout_options.md/#rows) disabled in the [composition layout options](layout_options.md)).

## Calls
Calls such as bobs and singles are indicated by symbols and numbers in columns which are headed by [calling positions](#calling-positions).

The majority of compositions use a small set of standard call symbols. Accordingly, Complib has a standard set of [default call symbols](adding_compositions_tabs_calls.md/#bob) which it will interpret automatically. Any other symbols must be explicitly defined in the [Calls tab](adding_compositions_tabs_calls.md).

!!! warning "Defining custom calls"
    When defining a custom call in the Calls tab, remember that you must specify an [observation mask](adding_compositions_tabs_calls.md/#observation-mask), [Mnemonic](adding_compositions_tabs_calls.md/#mnemonic) and [Heading](adding_compositions_tabs_calls.md/#heading) for every **named calling position** at which that call occurs. 
    
    Symbols and calling position headings in the Calls tab should exactly match those in the calling, otherwise you will get a validation error.

### Multiple bobs
The [default bob](adding_compositions_tabs_calls.md/#bob) call is unique: it can be represented in the calling using numbers as well as the standard dash (–) symbol.

A positive whole number in a cell beneath a calling position will be interpreted to mean that many **consecutive** bobs at that calling position. In particular, the number 1 can be used as an alternative to the dash (–) symbol.

## Call alterations
Some multipart compositions will indicate that alterations should be made to the calling in specific parts. The Calling tab has a robust syntax which allows you to specify these alterations, such as additional bobs, omitted calls, and even method substitutions in Spliced.

### Insertion and deletion
A basic call alteration looks something like this:

![Call insertion deletion](../img/calling_insertion_deletion.png){width="400"}

Calls
:   The call or sequence of calls affected by an alteration is always enclosed in [square brackets]. 

    The opening and closing brackets do not have to be in the same cell, or even the same row. The only requirement is that a left [ bracket is followed at some point by a corresponding right ] bracket.

Part number(s)
:   Directly in front of the opening bracket are the numbers of any parts in which the alteration takes place. When multiple part numbers are listed, they should be separated by a pipe character ( **|** ).

Insertion/deletion indicator
:   Directly in front of the part number(s) is a symbol which indicates whether the calls in brackets are to be inserted (+) or deleted (-) in the numbered parts.

If entered correctly, the call alteration will be marked with a superscript number in the generated layout, with a corresponding footnote of the form:

> [*#*] Include/omit in part(s)...

### Call substitution
A more complex form of call alteration is a **call substitution**. This is when a call (or sequence of calls) is replaced with a different call (or sequence of calls) in a particular part.

A call substitution has the following form:

![Call substitution](../img/calling_substitution.png){width="400"}

Original calling
:   The call or sequence of calls to be replaced in the numbered parts. Separated from the substituted calling by a **comma**.

Substituted calling
:   The call or sequence of calls to be substituted in place of the original calling in the numbered parts.

Substitution indicator
:   A combination of the insertion and deletion indicators. Can be entered by typing both + and - (in either order) in front of the part number(s).

The original and substituted calling can be in the same cell, or spread across multiple cells and rows:

![Call substitution with line breaks](../img/calling_substitution_long.png){width="400"}

The only requirement is that the parts of the syntax appear in their proper order when read left-to-right, top-to-bottom.

If entered correctly, the original calling will be marked with a superscript number in the generated layout, with a corresponding footnote of the form:

> [*#*] Replace bracketed calls with (substituted calling) in part(s)...

### Alterations affecting methods
The same alteration syntax for calls also applies to any [methods](#methods) specified in the calling, allowing you to add, omit, or replace sequences of methods in certain parts.

## Courseheads

### Manipulating course length

## Methods

### Method alterations and substitutions

## Named blocks

## Troubleshooting