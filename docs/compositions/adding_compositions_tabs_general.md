# The General tab
The General tab allows you to specify various high-level properties of a custom composition. When creating a new custom composition, this is usually the tab that you will use first.

Several fields in the General tab will **automatically update** other tabs when populated. This can save a lot of time when defining a custom composition.

!!! warning "Required fields"
    Many fields in the General tab are optional. However, a composition cannot be saved without an entry in any **required fields**. The required fields in the General tab are:

    -   [Title](#title)
    -   [Stage](#stage)

    Once a custom composition has been parsed by Complib, it will automatically repopulate these required fields if you delete them.

The sections on this page describe the entry fields on the General tab in detail. If you are encountering [validation errors](adding_compositions_overview.md/#validation-errors) specific to fields in the General tab, they will usually be listed at the end of the section pertaining to that field.

## Title
This field specifies the user-defined title of the composition. This is different from the **generated title**, which is provided automatically by Complib upon validation. The user-defined title is how the composition will be referred to elsewhere in the Composition Library once it is published, such as on the home page or in search results. 

The user-defined title can be anything you want: Complib has full Unicode support, so there's nothing to stop you from using titles like "❤️❤️❤️❤️" or "五千四十 B̶͇̊̈́̈r̸̰̈́ī̵̙s̵͈̙̰͆͆͘ť̵̝̉o̶̦͔͌͆͝l̶̜̊ ̸̻͕̰͋̃́Ş̷͛̅u̶̞͚̞̇̽͠r̶̹͉͉̈́͛̈́p̶͉̆r̸͙̼̰̐͆͝i̴̛͕͒s̷̪̻̈́͝e̴͔͗̓͜ ̵̨̛̻̀M̸̧̜͕͐̃a̷̠̼̞̓̀j̸̱̀̏͛ö̴͙̝́͂r̶̨̮̲̎"  if you really want to. However, if you intend to publish the composition, it is best practice to use a title which corresponds closely to the generated title. This makes it easier for others to identify important information about your composition at a glance. 

The generated title formats are:

- **Length + Method name + Class + Stage**, for single-method compositions;
- **Length + (# of methods)-Spliced + Class + Stage**, for spliced-compositions at a single stage;
- **Length + (# of methods)-Spliced + Stage 1 and Stage 2**, for mixed-stage compositions.

Complib will use the user-defined title to automatically populate certain other data fields if possible. This is another good reason to match the style of generated titles. The other fields which Complib will attempt to infer from the title are:

-   [Stage](#stage)
-   [Method](adding_compositions_tabs_methods.md) (for compositions which are recognised to be for a single method)

### Title warnings and errors

!!! warning "Warning: Does not start with the pricked length."
    The title provided does not start with a number which matches the length of the composition as pricked by Complib. With rare exceptions, composition titles begin with their length.

!!! warning "Warning: Does not match pricked method."
    The title provided does not contain the full name of the method which is being used to generate the composition's rows. With rare exceptions, you should aim for these to match.

## Opus
This field allows you to specify an Opus for the composition. Some composers use an Opus to help distinguish between compositions which might otherwise have the same title, or to highlight a notable feature of the composition. Some example compositions using an Opus are: 

-   [5088 Bristol Surprise Major Op. 4](https://complib.org/composition/11538) by Donald F Morrison;
-   [5016 6-Spliced Maximus Op. Classic](https://complib.org/composition/12496) by David J Pipe;
-   [5014 Stedman Cinques Op. Bobs only](https://complib.org/composition/75325) by Mark R Eccleston.

Text entered in the Opus field will be automatically appended to the end of the composition's title whenever it is referenced elsewhere in the Composition Library. For this reason, there is no need to include it in the [Title](#title). The Opus text will be listed in the form **Op. [text]**.

## Stage
This field is a drop-down menu which allows you to select the stage the composition is designed for. For mixed-stage compositions, this should be the highest numbered stage (also called the **effective stage**).

The stage of a composition indicates how many working (non-stationary) bells there are. Many stages have historical names which must be learned. The table below gives the stage names for every stage at which Complib can accept compositions.

| *N* | Stage name |   | *N* | Stage name |   | *N* | Stage name | 
|-----|------------|---|-----|------------|---|-----|------------|
| 2   | Two        |   | 13  | Sextuples  |   | 24  |Twenty-four |
| 3   | Singles    |   | 14  | Fourteen   |   | 25  |Twenty-five |
| 4   | Minimus    |   | 15  | Septuples  |   | 26  |Twenty-six  |
| 5   | Doubles    |   | 16  | Sixteen    |   | 27  |Twenty-seven|
| 6   | Minor      |   | 17  | Octuples   |   | 28  |Twenty-eight|
| 7   | Triples    |   | 18  | Eighteen   |   |
| 8   | Major      |   | 19  | Nonuples   |   |
| 9   | Caters     |   | 20  | Twenty     |   |
| 10  | Royal      |   | 21  | Decuples   |   |
| 11  | Cinques    |   | 22  | Twenty-two |   |
| 12  | Maximus    |   | 23  | Twenty-three | |

### Stage warnings and errors

!!! warning "Warning: is not the same as stage in Title"
    The stage specified does not match the stage name in the [Title](#title) field. In almost all cases these should be the same. 
    
    The warning will also be displayed if: 

    - No stage name is included in the Title field; or
    - The Title field contains **multiple stage names**, even if one of them matches the stage specified. 
    
    An exception to this last point is where **exactly two** stage names are used with the word "and" in between, and one of these matches the stage specified. In this case the composition is interpreted as being **mixed-stage**.

## Composer details
This field allows you to list the names of people or other named entities (such as computer programs) which were involved in creating a composition.

To add an attribution to the composition, click on `Add composer`. This will create a new attribution, which has two parts: an **attribution type** and a **name field**.

![Add composer details](../img/add_composer.png){width="500"}

To delete an attribution, click the ![Icon: cross](../img/icon_x.png){width="20"} cross to the right of the name field.

!!! note "Note: adding multiple attributions"
    You can add multiple attributions to the same composition. 
    
    However, you should generally avoid attributing a composition to the same person in multiple different ways (see [Attributions in search results, etc.](#attributions-in-search-results-etc)).

### Attribution type
This field is a drop-down menu which allows you to further specify the kind of attribution you want to make. These attribution types do not have set definitions, and to some extent they are open to interpretation. However, most have commonly accepted meanings. 

When submitting a composition which was produced by someone else, you should use an attribution type which corresponds with their wishes whenever possible.

The types of attribution are:

Composed by
:   The most common type of attribution. Used to identify the person or entity primarily responsible for creating the composition. 

Jointly composed by
:   For cases in which a team of people were jointly responsible for creating the composition. You should add one attribution of this type for each person you wish to jointly attribute the composition to.

Arranged by
:   Generally used in cases where the composer considers the composition to be an arrangement of one previously published.

Generated by
:   Used to identify a computer program which was responsible for producing the composition.

Selected by
:   Generally used to identify someone who chose the composition from a set generated by a computer program.

After
:   Used to identify another composer who inspired the composition. As opposed to **Inspired by**, this usually means that a particular stylistic feature or prior composition is being imitated in some way.

Inspired by
:   Used to identify another composer who inspired the composition.

Also attributed to
:   Generally used to identify other composers who have previously been credited with producing the composition.

### Name
This is a text field in which you can enter the name of the person or entity which you wish to attribute. Complib will attempt to auto-complete the name using all the registered composer names in its database.

If the name you enter does not match an existing composer, then saving the composition will create a new composer page under that name. You should make sure that the name is listed correctly before saving or publishing a composition attributed to a new composer.

### Attribution ordering
There is an implicit order of priority between the attribute types, given by the order in which they appear in the drop-down menu. This determines the order in which attributions are listed on the composition's page as part of its [layout](overview.md/#layout).

If multiple names have the same attribution type, they will be listed on the same line in lexicographical order.

### Attributions in search results, etc.
When a composition appears in search results, or in certain other places such as the Recently Published section, all its attributions will be listed after the composition's title in the format: 

[Title] by [Name 1], [Name 2], ... , and [Name *N*]. 

Complib will **not** identify if any of the listed names are identical, which means that the same name may appear multiple times. For this reason, you should generally avoid attributing a composition to the same person in multiple different ways.

### Attribution warnings and errors
!!! warning "Warning: [Name] will be added as a new composer."
    The entered name does not match any existing composer in Complib's database. Saving the composition will create a new composer page with the same name as the attribution. 

    You should make sure that the name is listed correctly before saving or publishing a composition attributed to a new composer.

## Year, month or date composed
This field lets you specify a year, month or date when the composition was composed. Dates are given in the format [Day][Month][Year] and will appear in the composition's [properties tab](composition_properties.md/#miscellaneous).

There are a number of different ways a year, month or date can be entered. The following are all accepted ways of entering the same date:

-   1/1/10
-   1-1-2010
-   01/01/2010
-   1 Jan 2010
-   1 January 2010

### Year
The year can be given as either a two- or four-digit number. 

If a two-digit number is used, it is assumed represent a year in the present century, unless that date would be in the future, in which case it is assumed to be in the previous century.

### Month
The month can be entered as a one- or two-digit number, or as a short or long month name. 

If a month is specified, but no year, then the year will be assumed to be the same as the current year in Coordinated Universal Time (UTC).

### Day
The day can be entered as a one- or two-digit number.

### Date warnings and errors
!!! danger "Error: `____` is invalid."
    The text entered in the date field does not match any accepted date format. You should use one of the formats described above.

!!! danger "Error: `____` is before 1650."
    Composition dates must fall after 1650, as the earliest known method, Grandsire, dates to around then. 
    
    If you have good reason to believe you are in possession of a composition dating from before 1650, you should immediately notify the Central Council (as well as anyone else who will listen).

!!! danger "Error: `____` is in the future."
    Composition dates must be in the past with respect to the present date in Coordinated Universal Time (UTC).

    If you have good reason to believe you are in possession of a composition originating from the future, you should immediately seek medical attention.

## Parthead(s)
This field allows you to specify one or more partheads. In a composition that has multiple parts, a parthead is the **first row** of one of the parts. 

The parthead(s) must be valid rows, must match the currently specified [Stage](#stage). If more than one parthead is entered, they must be separated by commas (`,`).

Complib will use any entered parthead(s) to generate a closed set of partheads. The number of partheads in this set depends on the parthead(s) themselves. The generated parthead(s) will be listed in the validation readout, with the user-specified parthead(s) highlighted in grey.

### Parthead warnings and errors

!!! danger "Error: must be a valid row of the same length as the stage"
    This error is encountered if any parthead is an **invalid row**, or if the stage of the composition and the stage of the specified parthead(s) do not match.

    Valid row
    :   A valid row contains the numbers 1 to *N*, where *N* is determined by the [specified stage](#stage). It must contain each number **exactly once**.

    Too many/too few commas
    :   If the stages match and the partheads are all valid rows, but you are still seeing the error, it may be because the Parthead(s) field contains too many or too few commas. 
        
        Specified partheads must be separated by commas, or Complib will interpret them as being part of the same row. 
        
        Extra commas will prompt Complib to expect additional parthead(s): if it cannot find any, it will interpret this as a parthead of stage zero, which will not match the specified stage.


!!! danger "Error: The number of partheads specified is `___` but the composition as pricked only contains `___` of them."
    Complib will check whether all generated parthead(s) are included among the pricked rows of the composition. If any are missing, then there is a mismatch between the implied multi-part structure and the actual composition. There are two main causes for this error:
    
    Incorrect calling
    :   There is a mistake in the specified [calling](adding_compositions_tabs_calling.md) which is preventing the composition from reaching the desired parthead(s);

    Incorrect parthead(s)
    :   The parthead(s) are all valid rows, but one or more of them have been entered incorrectly. As a consequence, the generated parthead(s) do not match the intended ones. You should check that the parthead(s) entered in this field exactly match the expected parthead(s) of the composition.

        If the number of generated parthead(s) in the validation readout does not match the number of parts you expect the composition to have, then this is a sign that the parthead(s) have been entered incorrectly.

## Coursehead mask(s)

## Start row number

## Backstroke start

## Extents

## Default calls

## Notes

## Allow save if false