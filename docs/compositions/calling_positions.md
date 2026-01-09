# Calling positions
Named calling positions denote specific leadheads by reference to the position of an **observation bell**, which on this page is always assumed to be the heaviest working bell.

Compositions have historically used common positions whose names have become standard. When entering a calling in the [Calling tab](adding_compositions_tabs_calling.md), these named positions can be used without needing to define them explicitly elsewhere.

## Standard named positions
The table below sets out the named calling positions which Complib uses by default. 

Note that some calling positions mean different things depending on the stage, denoted here by *n*, or on what places are made at the call. Some positions are also typically reserved for certain call types.

| Calling position | Position of obs. bell after call        | Note|
|------------------|-----------------------------------------|-----|
| **H** (Home)     | *n*                                     ||
| **W** (Wrong)    | *n*–1 (even stages); *n*–2 (odd stages) ||
| **M** (Middle)   | *n*–2 (even stages); *n*–1 (odd stages) ||
| **I** (In)       | 2                                       | Runs *in* to lead.         |
| **B** (Before)   | 2 if 2nds made at call, 3 otherwise     | Has just led *before* the treble. |
| **O** (Out)      | 3                                       | Runs *out*. Usually used for bobs. |
| **T** (Thirds)   | 3                                       | Usually used for singles. |
| **F** (Fourths)  | 4 ||
| **V** (Fifths)   | 5 ||
| **X** (Sixths)   | 6 ||
| **S** (Sevenths) | 7 ||
| **E** (Eighths)  | 8 ||
| **N** (Ninths)   | 9 ||

## Impact on default calls
If you have not specified any under the General tab, Complib will attempt to guess the [default calls](adding_compositions_tabs_general.md/#default-calls) of a composition based on what named positions are present in the Calling tab.

If calling positions **H**, **W**, **M** and **B** are in the majority, then **near** calls will be used by default. 

If calling positions **I**, **O** and **V** are in the majority, then **far** calls will be used by default.

This generally works well, but it is always a good idea to make sure the default calls have been set correctly.