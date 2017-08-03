Packages Included with ZetaVM
=============================

Standard Library
----------------

| Name  | Description | Example Usage |
| --- | --- | --- |
| [`std/csv/0`](/packages/std/csv/0/package)        | CSV spreadsheet parsing                            | [CSV example](/examples/csv_parsing.pls) |
| [`std/math/0`](/plush/math.pls)                   | Collection of useful constants and math functions  | [Float tests](/tests/plush/floats.pls), [audio test](/examples/audio_test.pls) |
| [`std/parsing/0`](/plush/parsing.pls)             | String parsing utilities                           | [Plush package](/plush/plush_pkg.pls) |
| [`std/peval/0`](/packages/std/peval/0/package)    | Functional-style partial evaluation                | [Package tests](/tests/plush/peval.pls), [audio render](/examples/audio_render.pls) |
| [`std/random/0`]()                                | Random number generation and utilities             | [Package tests](/tests/plush/random.pls) |

Language Packages
-----------------

Language packages are implementations of languages for ZetaVM. They implement parsing of source code and compilation
to Zeta bytecode. You can write code in one of these languages by starting your source file with `#language "language_package_name"`, eg: `#language "lang/plush/0"`.

| Name  | Description | Example Code |
| --- | --- | -- |
| [`lang/plush/0`](/plush/plush_pkg.pls) | Plush programming language | [Plush tests](/tests/plush) |


Core VM Packages
----------------

The core VM packages provide I/O functionality that is implemented directly in the VM itself, and accessible
through wrappers (host functions) written in C++. Note that references to host functions are not serializable.
As a general rule, you should avoid directly using core VM libraries if a higher-level wrapper is available.

| Name  | Description | Example Usage |
| --- | --- | --- |
| [`core/audio/0`](/vm/packages.cpp)  | Audio output                           | [Audio test](/examples/audio_test.pls) |
| [`core/io/0`](/vm/packages.cpp)     | File input/output                      | [Line count example](/examples/line_count.pls) |
| [`core/vm/0`](/vm/packages.cpp)     | Zeta image parsing and serialization   | [Serialization tests](/tests/plush/serialize.pls) |
| [`std/window/0`](/vm/packages.cpp)  | 2D graphics, pixel plotting            | [Graphics example](/examples/graphics.pls) |