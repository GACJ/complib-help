# Dynamic methods
Most methods are **static**: every lead is rung with the same fixed sequence of changes, unless a call is made. A **Dynamic method** is one whose changes are not fixed, but are chosen as the method is rung according to the rows reached. The best known example is Dixon's Bob Minor (in Complib, *Dixon's Minor*), which is Plain Bob Minor except that 4ths are made at backstroke whenever the 2nd or 4th is leading. Methods of this kind are often called **Dixonoids**.

Complib defines Dynamic methods using the **conditional notation** of the CCCBR Framework for Method Ringing, Edition 3. A method is Dynamic if, and only if, its place notation uses conditional notation.

## Conditional notation
Conditional notation is ordinary [place notation](place_notation.md) divided into **clauses**, each of which may have a **condition** in braces `{}` after it. For example, Dixon's Minor is:

> `-{h}12{1}|14{2,4}16`

This has four clauses:

| Clause | Meaning |
|--------|---------|
| `-{h}` | Cross, if the row produced is a handstroke row. |
| `12{1}\|` | 12, if the treble is leading in the row produced. The `\|` marks this clause as the lead end. |
| `14{2,4}` | 14, if the 2nd or the 4th is leading in the row produced. |
| `16` | 16 (no condition). |

### How the clauses are applied
At each step, Complib applies the clauses in order:

1. Apply the clause's changes and test its condition on the **last row it produces**.
2. If the condition is satisfied (or the clause has no condition), keep the rows and start again from the first clause.
3. If not, discard the rows and try the next clause.

If no clause is satisfied, the method cannot be rung, and an error ("no alternative satisfied") is reported. There is no need for a final clause without a condition, as long as one of the clauses is always satisfied.

A clause may contain several changes separated by dots, including [jump changes](place_notation.md/#jump-changes), e.g. `14.36{xxxxx6}`. The condensed forms of place notation (the comma for palindromic symmetry, and the MicroSIRIL `&` and `+` prefixes) cannot be used in conditional notation.

### Conditions
A condition is one or more **masks**, separated by commas, and is satisfied if any one of them matches the row:

Masks
:   A mask gives the bells required in particular places, using `x` as a wildcard for any bell. Masks refer to actual bells, not to positions relative to the treble. For example, on six bells `1` (or `1xxxxx`) means the treble is leading, `xxxxx6` means the 6th is in 6ths place, and `x2` means the 2nd is in 2nds place. Trailing `x`s may be omitted.

Stroke
:   `h` or `b` after a mask requires the row to be a handstroke or backstroke row. A mask consisting only of `h` or `b` matches any row at that stroke. Strokes are actual strokes, so they take account of a [backstroke start](../compositions/adding_compositions_tabs_general.md).

Parity
:   `+` or `-` after a mask requires the row to be [even or odd](../advanced/row_parity.md).

For example, `{xxxxx6h,xxxx6b}` is satisfied by a handstroke row with the 6th in 6ths place, or by a backstroke row with the 6th in 5ths place.

### Lead ends
A `|` after a clause marks it as a lead end clause: when it is satisfied, the last row it produces is a **leadhead**. Any number of clauses may be marked, and they need not have the same number of changes.

If no clause is marked, the whole plain course is treated as a single lead, which ends when the row that the lead started from recurs.

## The plain course
The plain course of a Dynamic method is pricked from rounds. If lead ends are marked, it ends at the first lead end which produces rounds (rounds reached in the middle of a lead makes the method false). Otherwise it ends when rounds first recurs. A method whose plain course does not come round within a reasonable limit (the extent, for stages up to Major) cannot be saved.

Leads of a Dynamic method may have different lengths. Where they do, the lead length is shown as **Variable**.

## Adding a Dynamic method
Dynamic methods are added in the same way as other methods (see [Adding methods](adding_methods.md)), entering the conditional notation in the **Place Notation** field. In addition:

- A **Conditional Description** is required. It should describe the rule of the method in words (for example "Plain Bob, but 4ths are made at backstroke when the 2nd or 4th leads"). It is shown on the method page. It must be left blank for a static method.
- **Division Ends** cannot be specified.
- **Transforms** cannot be applied.
- The method's title is its name and stage, without any class, e.g. *Dixon's Minor*.
- Complib warns if another method has the same plain course.

## Method properties
A Dynamic method is classified as **Dynamic** (see [Method properties](method_properties.md/#changes)), and has no class (such as Bob, Surprise or Treble Place). Properties which make sense for a Dynamic method are derived from its plain course, such as truth, the types of change it contains, its leadheads, the number of leads and the lead lengths. Other properties, such as symmetry, the leadhead code, hunt bells, falseness (FCH groups) and extensions, are not determined.

On the method page:

- The blue line shows the whole plain course, with the lead ends marked. The grid and place bells options are not available.
- The Related methods and Trivial variations sections are not shown.
- A Dynamic method cannot be used as the starting point for the [Method Designer](method_designer.md).

## Dynamic methods in compositions
Dynamic methods can be used in compositions, either alone or spliced with static methods (changes of method happen at leadheads). In the [Methods tab](../compositions/adding_compositions_tabs_methods.md):

- **Starting place** may be used.
- **Rotate by**, **Start row number** and **Length** cannot be used.
- Lead positions are counted relative to the lead end, and only the lead end (row number 0) may be used, e.g. the default **LE**.

### Calls at the lead end
Calls with a lead position at the lead end (including the default calls) are made when a lead end clause is satisfied: the rows of that clause are replaced by the call, and the last row of the call is the leadhead. The number of changes in the clause must equal the call's [Changes replaced](../compositions/adding_compositions_tabs_calls.md/#changes-replaced) (one change by default). Calls cannot themselves use conditional notation.

Calling positions are determined in the same way as for static methods, from the position of the observation bell at the leadhead after the call.

### Dynamic calls
Because the leads of a Dynamic method can vary in length, a call is not always best described by its position in the lead. A **dynamic call** has no fixed position: instead it is made as soon as its condition is satisfied, in the same way as a clause of the method. See [Dynamic calls](../compositions/adding_compositions_tabs_calls.md/#dynamic-calls) in the Calls tab.

### Leadheads, courseheads and partheads
The leadheads of a composition using a Dynamic method are the rows produced by lead end clauses and by calls. Courseheads are the leadheads which match the [coursehead masks](../compositions/adding_compositions_tabs_general.md), and partheads are found in the usual way. Compositions are laid out by leads or courses as usual; the leads may be of different lengths.

Compositions which use one or more Dynamic methods have the **Dynamic method** property (see [Composition properties](../compositions/composition_properties.md/#methods)), which can also be used in composition searches.

## Searching and the API
Dynamic methods can be found in method searches using the **Dynamic** flag. Searching by place notation uses the conditional notation as Complib displays it.

In the [Complib API](../advanced/complib_api.md), a Dynamic method has its conditional notation as its place notation, the `dynamic` flag set, its conditional description, and null values for the properties which are not determined.