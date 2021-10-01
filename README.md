<!-- SPDX-License-Identifier: MIT OR Apache-2.0 -->
<!-- SPDX-FileCopyrightText: Ferrous Systems GmbH -->

# REUSE demo

This is a small demo of a project using [REUSE] to track its licensing status.
To run the demo you need to [install REUSE][install] and then run this command:

```
reuse lint
```

REUSE will analyze all the files in the current directory and its
subdirectories, and it will report a summary of what it found. You can also run
this command to get a SPDX report:

```
reuse spdx
```

## Structure

There are two directories in this demo:

* `src`: contains files individually licensed, either through comments at the
  start of each source file (`main.rs`) or with a separate `.license` file
  (`bunnies.jpg`).

* `bulk`: contains files without individual annotations, which are
  bulk-annotated through the `.reuse/dep5` file.

There is also the `LICENSES` directory containing the text of all the included
licenses (including a custom one), and `.reuse` containing the bulk
annotations.

[REUSE]: https://reuse.software
[install]: https://github.com/fsfe/reuse-tool#install
