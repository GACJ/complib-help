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

The user-defined title can be anything you want. However, it is best practice to use a title which corresponds closely to the generated title. This makes it easier for others to identify important information about your composition at a glance.

Complib will use the user-defined title to automatically populate certain other data fields if possible. This is another good reason to match the style of generated titles. The other fields which Complib will attempt to infer from the title are:

-   [Stage](#stage)
-   [Method](adding_compositions_tabs_methods.md) (for compositions which are recognised to be for a single method)

!!! warning "Warning: Does not match pricked method."


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

## Composer details
This field allows you to list the names of people or other named entities (such as computer programs) which were involved in creating a composition.

To add an attribution to the composition, click on `Add composer`. This will create a new attribution, which has two parts: an **attribution type** and a **name**.

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

## Year, month or date composed
This field lets you specify a year, month or date when the composition was composed. Dates are given in the format [Day][Month][Year] and will appear in the composition's [properties tab](composition_properties.md/#miscellaneous).

There are a number of different ways a year, month or date can be entered. The following are all accepted ways of entering the same date:

-   1/1/10
-   1-1-2010
-   01/01/2010
-   1 Jan 2010
-   1 January 2010

!!! danger "Error: Date composed"
    Entering a date in an unaccepted format will cause a validation error. Entering a date before 1650, or that is in the future, will also cause an error.

### Year
The year can be given as either a two- or four-digit number. 

If a two-digit number is used, it is assumed represent a year in the present century, unless that date would be in the future, in which case it is assumed to be in the previous century.

### Month
The month can be entered as a one- or two-digit number, or as a short or long month name. 

If a month is specified, but no year, then the year will be assumed to be the same as the current year in Coordinated Universal Time (UTC).

### Day
The day can be entered as a one- or two-digit number.


## Parthead(s)

## Coursehead mask(s)

## Start row number

## Backstroke start

## Extents

## Default calls

## Notes

## Allow save if false