**TODO:**

- Generate a reverse-sorted list, so files with the same suffix are
  grouped together, to minimize closing and re-opening generated files.
  Could improve performance for very large directory trees.

- Optionally index text, binary, and utf-16 files (see "classify",
  not yet released).  Note that this requires reading at least some of
  each file -- so I should also index unreadable files.  Think about
  how to generate these lists without storing them in memory.

- Optionally use iconv to generate utf-8 translations of utf-16 files.
  Remove generated utf-8 file if iconv fails (likely because of a false
  positive from "classify" or equivalent).  This is useful mostly on
  Windows; I'm not *too* likely to get around to this unless there's
  some outside demand for it.

- Add an option to continue processing after some errors (I'm actually
  not quite sure what I meant by this).

- Add an option to build the .index directory in a specified location
  outside the index tree; useful for read-only and/or shared directory
  trees.
