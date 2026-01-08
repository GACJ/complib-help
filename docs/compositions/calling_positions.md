# Calling positions
Named calling positions denote specific leadheads by reference to the position of an **observation bell**, which on this page is always assumed to be the heaviest working bell.

Compositions have historically used common positions whose names have become standard. When entering a calling in the [Calling tab](adding_compositions_tabs_calling.md), these named positions can be used without needing to define them explicitly elsewhere.

## Standard named positions
The table below sets out the named calling positions which Complib uses by default. 

Note that some calling positions mean different things depending on the stage, denoted here by *n*, or on what place is made at the leadend (either **12** or **1*n***). Some positions are also typically reserved for certain call types.

| Calling position | Position of obs. bell after call        | Note|
|------------------|-----------------------------------------|-----|
| **H** (Home)     | *n*                                     ||
| **W** (Wrong)    | *n*–1 (even stages); *n*–2 (odd stages) ||
| **M** (Middle)   | *n*–2 (even stages); *n*–1 (odd stages) ||
| **I** (In)       | 2                                       | Runs *in* to lead.         |
| **B** (Before)   | 2 (LE **12**) or 3 (LE **1*n***)        | Has just led *before* the treble. |
| **O** (Out)      | 3                                       | Runs *out*. Usually used for bobs. |
| **T** (Thirds)   | 3                                       | Usually used for singles. |
| **F** (Fourths)  | 4 ||
| **V** (Fifths)   | 5 ||
| **X** (Sixths)   | 6 ||
| **S** (Sevenths) | 7 ||
| **E** (Eighths)  | 8 ||
| **N** (Ninths)   | 9 ||

## Impact on default calls
Complib will attempt to guess the [default calls](adding_compositions_tabs_general.md/#default-calls) of a composition based on what standard calling positions are used in the Calling tab.

If a composition only uses calls at **H**, **W**, **M** and **B**, the composition will default to **near** calls.

*(PMD: perhaps you could clarify what the condition for defaulting to far calls is, GACJ?)*