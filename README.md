# magic-cheat-sheet

# Magic VLSI Cheatsheet

**Author:** Harald Pretl  
**Institute for Integrated Circuits, Johannes Kepler University Linz**  
**Date:** © 2021–2022  

---

This cheat sheet compiles useful commands (to be entered in the Tcl console) and bind keys (in the layout window) as well as a summary of the mouse operations for the different tool modes. This compilation relates to Magic 8.3 (see [Magic GitHub Repository](https://github.com/RTimothyEdwards/magic)).

A comprehensive Magic documentation and description of all macros can be found at [Magic User Guide](http://opencircuitdesign.com/magic/userguide.html).

The command `macro layout` in the Magic Tcl console lists all defined macros.

---

## Useful Commands

| Command                          | Description                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `addpath [path]`                 | Add search `path` of cells.                                                |
| `antennacheck`                   | Run antenna check on cell.                                                 |
| `array xsize ysize`              | Array the selection `xsize`-times in X, `ysize`-times in Y, spacing by box.|
| `box [options]`                  | Print information about the box like `b`, or manipulate it in various ways.|
| `cif [options]`                  | Powerful command with various options (e.g., generating mask layers).      |
| `contact type`                   | Create contact inside box of intersecting layers.                          |
| `copy [to x y]`                  | Copy to current cursor position or to `x`/`y`-position.                    |
| `corner dir1 dir2`               | Draws a corner inside the box, first in `dir1`, then in `dir2`.            |
| `drc find`                       | Locate DRC error.                                                          |
| `drc why`                        | Explain DRC errors in the box.                                             |
| `dump cell`                      | Copy given `cell` into the current layout cell.                            |
| `erase layers`                   | Erase comma-separated list of `layers` in the box.                         |
| `erase *`                        | Erase all layers but not labels.                                           |
| `erase $`                        | Erase everything (like `CTRL-D`).                                          |
| `erase labels`                   | Erase selected label(s) in the box.                                        |
| `fill dir`                       | Extend layers from one side of the box to the other in the given direction.|
| `findlabel label`                | Center the box on the `label`.                                             |
| `flatten cell`                   | Flatten the current edit cell incl. hierarchy into a new `cell`.           |
| `flush`                          | Revert edit cell to the last state on disk.                                |
| `get cell`                       | Instantiate `cell` into the current edit cell.                             |
| `goto nodename`                  | Move box to net `nodename`, throw an error if not existing.                |
| `help [pattern]`                 | Shows help for various commands.                                           |
| `identify cell-id`               | Name the selected cell as `cell-id`.                                       |
| `iroute`                         | Interactive point-to-point router, from cursor to the box.                 |
| `label string [position [layer]]`| Create a point, line, or box label.                                        |
| `load cell`                      | Open the `cell` in the layout window.                                      |

*(Continued on next page.)*

---

## Bind Keys

| Key Combination     | Description                                                    |
|----------------------|----------------------------------------------------------------|
| `a`                 | Select everything in the box.                                  |
| `A`                 | Select additional objects in the box.                          |
| `CTRL-A`            | Deselect objects in the box.                                   |
| `b`                 | Print information about the `box`.                             |
| `B`                 | Center the window on the box.                                  |
| `c`                 | Copy the selection.                                            |
| `d`                 | Delete the selection.                                          |
| `CTRL-D`            | Delete all layers and labels in the box selected by cursor.    |
| `e`                 | Makes the selected cell the new `edit` cell.                   |
| `F`                 | Flip the selection upside-down.                                |
| `g`                 | Toggle `grid`.                                                |
| `G`                 | Toggle `grid 2`.                                              |
| `i`                 | Select the instance under the cursor.                          |
| `I`                 | Select additional instance under the cursor.                   |
| `CTRL-I`            | Deselect the instance under the cursor.                        |
| `m`                 | Move the selection to the cursor position.                     |
| `o`                 | Open the window (with the current selection).                  |
| `r`                 | Rotate 90 degrees.                                             |
| `R`                 | Rotate -90 degrees.                                            |
| `s`                 | Select objects under the cursor.                               |
| `u`                 | Undo the last operation.                                       |
| `U`                 | Redo the last undo.                                            |
| `z`                 | Zoom out.                                                     |
| `Z`                 | Zoom in.                                                      |

*(Additional bind keys and mouse operations available in the full document.)*

---

## Mouse Operations

### Box Tool
- **Left Click:** Set the lower-left corner of the box.  
- **Right Click:** Set the upper-right corner of the box.  
- **Middle Click:** Paint layer pointed with the cursor in the box.  
- **Shift + Middle Click:** Erase layer pointed with the cursor in the box.  

### Wiring Tool
- **Left Click:** Pick wire material and size from the cursor.  
- **Middle Click:** Place wire at the cursor.  
- **Right Click:** Cancel wire.  
- **Shift + Middle Click:** Place a contact at the cursor and continue on a higher layer.

---

For detailed instructions, refer to the official [Magic Documentation](http://opencircuitdesign.com/magic/userguide.html).
