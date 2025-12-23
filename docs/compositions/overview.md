# Composition Pages
As its name suggests, Complib has been designed as a library for change ringing **compositions**. In the most general terms, a composition is a specified **calling** for a change ringing performance. A composition is stored in Complib as this calling, together with specified method(s) for which it has been designed.

Complib automatically **pricks** (generates the rows of) any composition when it is entered in order to establish its **truth**. Stored compositions are then given their own dedicated page.

## Tabs overview
A composition page is subdivided into various expandable tabs (click on the name of a tab to skip to a detailed description of its contents):

[Layout](#layout)
:   The human-readable form of the composition.

[Blue Line](#blue-line)
:   The pricked rows of the composition, with (or without) an overlaid blue line.

[Music Score](#music-score)
:   The music score breakdown of the composition with respect to a specified [**music scheme**](../advanced/music_schemes.md). Users can use one of the default schemes (such as for half-muffled ringing), or specify their own.

[Handbell Positions](#handbell-positions)
:   Information about which positions each handbell pair rings during the composition, including the number of leads rung and their relative frequency.

[Properties](#properties)
:   The technical features of the composition, such as its **length**, **number of parts**, whether it is **all-the-work**, and more.

[ATW Analysis](#atw-analysis)
:   A comprehensive analysis of the all-the-work property for every method included in the composition.

[Related Compositions](#related-compositions)
:   A list of all compositions which are related to the current one, i.e., because they are related by some **transformation** such as rotation or reversal, or because they have the same calling but different specified methods.

[Performances](#performances)
:   Historical information about occasions when the composition has been performed,  with links to the relevant Bellboard page.

[References](#references)
:   A list of all accessible **collections** containing the current composition. If you own a private collection containing the composition, it will be included here.

[Library Details](#library-details)
:   Information about to the composition's Complib entry, including which **library** it is contained in, its **Composition Id**, any **Notes** included by the publisher, etc.

## Layout
This tab gives the **calling** for the composition in human-readable form. With default settings, the layout should look something like this:

![Example composition layout](../img/comp_layout_annotated.png)

Generated title
:   The composition's generated title is given automatically by Complib, and may differ from its user-defined title. The generated title        specifies, in order:

    -   the **length** of the composition;
    -   (if a single-method composition) the **title of the method** it is defined for; or
    -   (if a spliced composition) the **number of methods**, their **common class** (if it exists) and **stage(s)**;
    -   the opus number and name (if it exists).

Attribution
:   If the composition has been attributed to anyone, it will be noted here. Usually this will be the name of the composer(s) or arranger(s).

Calling
:   The **calls** which make up the composition, together with any **supplementary information**, including:

    -   **Number of parts** (for multipart compositions);
    -   **Modifications to the calling** (e.g., calls or methods which change in certain parts);
    -   **Non-standard starts** (e.g., for compositions beginning at backstroke, or at a point other than the start of a lead/division);
    -   **Non-standard or user-defined calls**: these will be defined in words (e.g. Far, Near, Grandsire) or using [place notation](../methods/place_notation.md).

Method details
:   For spliced compositions, the methods rung will be listed here. The readout will give the number of rows of each method in the composition, and their corresponding **method mnemonics** if disambiguation is needed. Clicking on a method's name will take you to its [method page](../methods/overview.md).

Music
:   A list of common **musical metrics** is given for the composition, together with **named rows** it features such as Queens or Tittums. See also: [Music score](#music-score).

Customise layout options
:   Users can adjust the form and style of the layout to suit a wide variety of needs and preferences (see [Customising composition layouts](layout_options.md)).

## Blue Line
When expanded, this tab will render all the rows of the composition in accordance with the configured **blue line options**. By default, it should look something like this:

![Example Composition Blue Line](../img/comp_blueline.png)

Much like those for methods, the blue line display for compositions is highly customisable. For an explanation of most of the available options, see [Methods > Customising the blue line](../methods/blueline_options.md). 

There are a number of blue line options which are unique to compositions. These are:

-   **Calls**: displays calls at the points where they occur. Default: **on**.
-   **Plains**: marks plain leads/divisions, similarly to leads with calls. Default: **off**.
-   **Method mnemonics**: Displays the method mnemonic of the method currently being rung at the beginning of each lead. Default: **on**.

!!! warning
    By default, the blue line tab will attempt to display the entire touch at once. For long lengths, or compositions on higher numbers, the rendering process may take some time. 
    
    The blue line display will also auto-resize to fit the width of your browser window. For longer compositions on higher numbers, this may result in bell numbers which are very small.

## Music Score
This tab calculates a numerical score for the composition based on the various metrics, or **tests**, specified in a **music scheme**. The table in the tab provides a breakdown of this score: for each applicable test, the number of rows in the composition which satisfy the test is given.

![Example Music Score table](../img/music_score_table.png)

The music scheme used to calculate the score can be changed via the dropdown menu at the top right of the tab. 

!!! warning
    If the selected music scheme has no **applicable tests** which can be scored against, then the Music Score tab will be left empty.

Clicking on a test will expand that test further:

![Expanded Music Score test](../img/music_score_table_expanded.png)

Most of the tests are self explanatory. For a full description, together with information about how to define your own tests, see [Music schemes](../advanced/music_schemes.md).

## Handbell Positions
For handbell ringers, it is often useful to know what **positions** your two bells are in relative to each other. Each handbell pair has a corresponding position (e.g 3-4 position) which is uniquely determined by what that pair does in the **plain course**.

When expanded, the tab displays a table:

![Handbell Positions Table](../img/handbell_positions_table.png)

Down the left hand side of the table is listed each handbell pair. The column headings give the corresponding positions. The table entries specify how long the given handbell pair spends in that position, both as a number of leads and as a percentage of the whole composition.

The rightmost column lists the number of distinct leads that each handbell pair rings throughout the composition. This is used to calculate the relative **simplicity** of the composition for a given handbell pair.

For spliced compositions, clicking on the name of the handbell pair will further expand the table to show a breakdown by individual method.

## Properties

## ATW Analysis

## Related Compositions

## Performances

## References

## Library Details
