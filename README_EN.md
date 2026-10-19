# EXPLODEATT for AutoCAD

EXPLODEATT is an AutoCAD AutoLISP utility for converting attributes inside blocks, especially dynamic blocks, into ordinary editable text.

## What problem does it solve?

When you use AutoCAD's built-in `EXPLODE` or `X` command on an attribute block, the result may contain incorrect values, overlapping text, or text that cannot be edited as expected.

EXPLODEATT reads the block attributes, creates ordinary text from their values, and adjusts the text position and size so it is easier to edit, arrange, or export.

## Installation

1. Open AutoCAD.
2. Run `APPLOAD`.
3. Load `plugins/EXPLODEATT-V6.LSP`.
4. Close the load dialog after the file has loaded.

## Basic usage

1. Save a copy of your drawing first.
2. Run the `EXPLODEATT` command.
3. Select the blocks to process.
4. Press Enter when the selection is complete.
5. Wait for the completion message.
6. Check the generated ordinary text.

The `XATT` command is also available as a shortcut.

## Using it with MT2CSV

If the final goal is to export block attributes to CSV or Excel, use this order:

1. Run EXPLODEATT to release the attributes as ordinary text.
2. Check the drawing for overlapping or incorrect text.
3. Load and run MT2CSV.
4. Select the generated text and export it to CSV.

In short: **EXPLODEATT releases the text; MT2CSV organizes and exports it.**

If the drawing already contains ordinary `TEXT` or `MTEXT`, skip EXPLODEATT and use MT2CSV directly.

## Notes

- Test on a copy of the drawing first.
- The command modifies block attributes and creates new text objects.
- When processing many blocks, wait for the completion message before continuing.

## Source

Feature information is based on the original [EXPLODEATT/XATT forum post](https://www.52pojie.cn/thread-2075182-1-1.html). The source file was provided as `EXPLODEATT-V6.rar`; copyright belongs to the original author.
