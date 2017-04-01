This is an in-progress port of [seatgeek's fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy/) Python library to C++.
When done, this library will have the same interface and behavior.

The underlaying C-library ([python-Levenshtein](https://github.com/miohtama/python-Levenshtein), mirrored [here](https://github.com/Tmplt/python-Levenshtein)) has been stripped of its Python interfacing
and been wrapped around some C++ code.

| files | Python/C-lib equivalent |
| ----- | ----------------------- |
| `fuzzywuzzy.{c,h}pp` and `string_matcher.{c,h}pp` | Line-by-line Python-to-C++ translations of the Python library and python-Levenshtein's `StringMatcher.py`. |
| `diffutils.{c,h}pp` | (Python-interfaced-)C-to-C++ wrapper of `ratio_py`, `get_opcodes_py`, `get_matching_blocks_py`, etc. from python-Levenshtein. |
| `utils.{c,h}pp` | Utility functions, translated from the Python library's `utils.py`. |
| `levenshtein.{c,h}` | The underlaying C functions, copied verbatim. |
