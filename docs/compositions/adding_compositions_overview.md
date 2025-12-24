# Adding compositions
Any registered user can add a composition to the Composition Library

To get started, click on **Create new > New composition** in the navbar or dropdown menu:

![Navbar Create New](../img/navbar_create_new.png){ width="300" }
![Dropdown Menu Create New](../img/dropdown_menu_create_new.png){ width="300" }

## The Add composition page
![The Add composition page](../img/add_comp_page.png)

The [Add composition page](https://complib.org/composition/add) has a number of fields which allow you to specify certain properties of your custom composition. Click on the name of a tab below to go to a dedicated page explaining how to use it.

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

A composition which passes validation can be saved as a **private composition** by clicking the `Save` button. Non-critical [warnings](#warnings) may also be displayed. If the composition does not pass validation, one or more [validation errors](#validation-errors) will be given. The composition layout and blue line displays will also highlight specific errors, to aid in troubleshooting.

### Layout display

### Blue line

## Warnings
![Composition warnings](../img/comp_warnings.png)

## Validation errors
![Composition errors](../img/comp_errors.png)

If Complib encounters a critical problem when attempting to validate the composition, an error message will be displayed. **All errors must be cleared before a composition can be saved**.

There are a number of different error types. Most errors will give an indication of how to clear them. The following is a non-exhaustive list of some of the more common errors:

!!! error "Error: Composition is false and cannot be saved unless overriden in the General tab"
The composition as specified is false (that is, not **true**). See [Composition properties > Truth](composition_properties.md/#truth) for an explanation of what it means for a composition to be true.

Since the vast majority of compositions which ringers want to ring are true, the Composition Library will not allow false compositions to be saved and published by default. However, this behaviour can be overridden in the General tab (see [General info > Allow save if false](adding_compositions_general_info.md/#allow-save-if-false)).

!!! error "Error: Composition is not a round block."
The composition as specified does not end at the same row it started from. There are various things which can cause this to happen, but most often it is due to a mistake in the calling.

!!! error "Error: Unable to prick composition, or other errors need to be cleared."
Complib is not able to prick (generate the rows of) the composition as it has been defined. Usually this means that some other error is preventing Complib from parsing the composition.

!!! error "Error: Maximum false row limit reached."
Complib will not automatically stop pricking a composition as soon as it runs false. However, in order to prevent the pricker from entering an infinite loop, there is an upper limit on the number of false rows which will be generated. This error means that the composition has reached that upper limit, and no more rows will be pricked in the [blue line display](#blue-line).

### Tab specific-errors
The above are examples of general validation errors. However, a number of errors relate to specific tabs in the composition editor. In such cases, the validation readout will list the tab which is responsible for causing the error.

Information on how to clear tab-specific errors can be found in the Help sections for each tab. [See above](adding_compositions_overview.md/#the-add-composition-page) for a brief description of the tabs.







