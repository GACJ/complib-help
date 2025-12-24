# Adding compositions
Any registered user can add a composition to the Composition Library.

To get started, click on **Create new > New composition** in the navbar or dropdown menu:

![Navbar Create New](../img/navbar_create_new.png){ width="200" }
![Dropdown Menu Create New](../img/dropdown_menu_create_new.png){ width="200" }

## The Add composition page
![The Add composition page](../img/add_comp_page.png){ width="500"}

The Add composition page ([https://complib.org/composition/add](https://complib.org/composition/add)) has a number of fields which allow you to specify certain properties of your custom composition. Click on the name of a tab below to go to a dedicated page explaining how to use it.

[General](adding_compositions_general_info.md)
:   Specify high-level information about the composition such as its title, composer/arranger, number of parts, and so on.

Methods
:   Specify which methods are used in the composition, including custom definitions of existing methods and their method mnemonics.

Calls
:   Specify the calls used in the composition, together with their corresponding calling positions.

Calling
:   Edit the calling, or sequence of calls, which defines the composition.

Performances
:   Add performance information. Mostly used when uploading historical compositions.

References
:   Link the composition to collections within the Composition Library.

## Validating and saving compositions
If Complib is able to parse the composition as entered, then its generated title, [composition layout](#layout-display) and [blue line](#blue-line) will be displayed at the bottom of the page. Complib will automatically attempt to validate any composition it can parse. Clicking the `Validate` button will force a re-validation.

A composition which passes validation can be saved as a **private composition** by clicking the `Save` button. If the composition does not pass validation, one or more [validation errors](#validation-errors) will be displayed. The composition layout and blue line displays will highlight certain specific errors, to aid in troubleshooting. Non-critical [warnings](#warnings) may also be given.

## Validation errors
![Composition errors](../img/comp_errors.png)

If Complib encounters a critical problem when attempting to validate the composition, an error message will be displayed. **All errors must be cleared before a composition can be saved**.

There are a number of different error types. Most errors will give an indication of how to clear them. The following is a non-exhaustive list of some of the more common errors:

!!! error "Error: Composition is false and cannot be saved unless overriden in the General tab"
The composition as specified is false (that is, not true). See [Composition properties > Truth](composition_properties.md/#truth) for an explanation of what it means for a composition to be true.

Since the vast majority of compositions which ringers want to ring are true, the Composition Library will not allow false compositions to be saved and published by default. However, this behaviour can be overridden in the General tab (see [General info > Allow save if false](adding_compositions_general_info.md/#allow-save-if-false)).

A composition which is false will have an ![False icon](../img/false.svg) icon displayed next to its generated title.

!!! error "Error: Composition is not a round block."
The composition as specified does not end at the same row it started from. There are various things which can cause this to happen, but most often it is due to a mistake in the calling.

!!! error "Error: Unable to prick composition, or other errors need to be cleared."
Complib is not able to prick (generate the rows of) the composition as it has been defined. Usually this means that some other error is preventing Complib from parsing the composition.

!!! error "Error: Maximum false row limit reached."
Complib will not automatically stop pricking a composition as soon as it runs false. However, in order to prevent the pricker from entering an infinite loop, there is an upper limit on the number of false rows which will be generated. This error means that the composition has reached that upper limit, and no more rows will be pricked in the [blue line display](#blue-line).

## Validation warnings
![Composition warnings](../img/comp_warnings.png)

When validating a composition, Complib may generate one or more warnings. These contain information about the composition which you may wish to take into account before saving and/or publishing it. However, warnings by themselves do not prevent compositions from being saved.

## Tab-specific warnings and errors
A number of warnings and errors relate to specific tabs in the composition editor. In such cases, the validation readout will list the tab which is responsible for causing the warning or error.

Information on how to clear tab-specific warnings and errors can be found on the Help pages for each tab, accessible via the sidebar. [See above](adding_compositions_overview.md/#the-add-composition-page) for a brief description of the tabs.

## Layout display
A parsed composition will be laid out by Complib at the bottom of the page. For an overview of the various parts of a composition layout, see [Composition pages > Layout](overview.md/#layout). 

The appearance of the layout is determined by the current configuration of the [composition layout options](layout_options.md). The layout options can be adjusted by clicking on the **cog icon** next to the `Validate` button.

### Layout colour coding
Various elements of the composition layout will change colour when displaying a composition which is false, to aid in troubleshooting. The specific elements which change colour will depend on the format of the layout.

Course/leadheads in magenta (![False course in magenta](../img/false_course_magenta.png){ width="50" }) indicate that the course/lead contains a row which is false against another row which appears later in the composition.

Course/leadheads in red (![False course in red](../img/false_course_red.png){ width="50" }) indicate that either: 

- The course/lead contains a row which is false against another row which appears earlier in the composition; or 
- The course/lead is false against itself.

## Blue line






