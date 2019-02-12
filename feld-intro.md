FELD-INTRO(7) - Miscellaneous Information Manual

# NAME

**feld-intro** - an introduction to feld, the pairing window manager

# SHORT DESCRIPTION

**feld**
is a simple window manager based on
**wmutils**.
It supports floating, tiling and tabbed layouts, but not in a
conventional way.
Instead, the two latter layouts are incorporated into a unique
feature called
*pairing*,
which I will explain in the following section.

# PAIRING IN THEORY

When two windows are
*paired*,
they are associated with each other in terms of behavior. It is a
way of telling
**feld**
to treat two windows as one window.  This means that an action
affecting one window will also affect the other: move one window,
and the other one will be moved too.

(Note that closing is a special case: when closing one of the windows
in a pair, the other one will remain open in its previous place,
but the pair will be dissolved.)

Because a window pair is treated as a single window,
the user can create pairs of pairs.

It is through the pairing mechanism that
**feld**
provides alternative layouts like tiling and tabbed.
Through a key binding, the two windows of a pair can be arranged
in a tiling or tabbed layout instead of the default floating.
However, as a whole, the pair still behaves as a floating window,
unless it too is a member of a tiling pair.

If a pair that is made tiling or tabbed contains an inner pair,
then that pair is automatically made tiling.
This prevents weird and unintuitive layouts.

Pairing also serves as an approximation of workspaces: minimizing
one pair and restoring another pair is equivalent to changing
workspace.

# PAIRING IN PRACTICE

When a window is created, it is floating and unpaired.
To pair it with another window, both windows must first be selected.
Indeed,
**feld**
supports multiple selections: one primary and one secondary,
distinguishable via border color.
This is achieved with key or mouse bindings.
Once selected, the windows are paired by another key binding.

# AUTHORS

**feld**
is written by
John Ankarstr&#246;m,
available {on the web|by e-mail} at john{.|@}ankarstrom.se.

OpenBSD 6.4 - February 13, 2019
