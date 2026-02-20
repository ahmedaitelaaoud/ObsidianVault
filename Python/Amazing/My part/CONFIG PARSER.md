> [!IMPORTANT] Phase 2: Config Parser Architecture
> **Input:** A plain text file with `KEY=VALUE` pairs.
> **Expected Keys:** `WIDTH` (int), `HEIGHT` (int), `ENTRY` (str/tuple), `EXIT` (str/tuple), `OUTPUT_FILE` (str), `PERFECT` (bool).
> **Error Handling Rule:** NEVER show a raw Python traceback to the user. Always catch `FileNotFoundError` and `ValueError`, print an error to `sys.stderr`, and exit cleanly.


> [!TIP] String Splitting & Error Outputs
> **Splitting Limits:** Always use `.split("=", 1)` when parsing `KEY=VALUE`. This protects the program from crashing if the `VALUE` string accidentally contains an `=` character.
> **Standard Error:** In 42 projects, error messages must never be printed normally. Always use `print("Error msg", file=sys.stderr)` so other programs can filter out the errors from the real output.
> **Reserved Words:** Never name variables `list`, `dict`, `str`, or `int`. It shadows the built-in Python functions!

> [!NOTE] Defensive Splitting (`maxsplit`)
> **Code:** `string.split("=", 1)`
> **Why:** The `1` represents `maxsplit=1`. It forces Python to only cut the string at the *first* occurrence of the separator.
> **42 Defense:** Evaluators will maliciously test config files with values like `FILE=maze=final.txt`. Using `maxsplit=1` ensures the program splits the string into exactly `['FILE', 'maze=final.txt']` without crashing or losing data.


> [!NOTE] Validating Configurations (Mandatory vs Optional)
> **Mandatory Data** (`WIDTH`, `HEIGHT`, `ENTRY`, `EXIT`): > - Must be strictly checked for existence using `if key not in dict:`.
> - Must be type-cast safely inside `try...except ValueError` to catch malicious inputs like `WIDTH=apple`.
> - Coordinates must be split by `,` and cast to `Tuple[int, int]`.
>
> **Optional Data** (`OUTPUT_FILE`, `PERFECT`):
> - Never crash if they are missing.
> - Use the dictionary `.get(key, default_value)` method to provide safe fallback values.

> [!WARNING] Minimum Maze Dimensions
> **Rule:** `WIDTH >= 3` and `HEIGHT >= 3`
> **The Geometry:** A maze requires an external boundary. The smallest possible enclosed space requires 1 cell for the left wall, 1 cell for the path, and 1 cell for the right wall (Total = 3).
> **Defense Context:** Catching impossible dimensions (like 2x2 or negative numbers) during the *Parsing phase* protects the *Generation algorithm* from fatal `IndexError` crashes later on.

> [!TIP] Dictionary `.get()` and Boolean Parsing
> **Safe Lookups:** Never use `dict["KEY"]` for optional settings. Always use `dict.get("KEY", "default_value")` to prevent `KeyError` crashes if the user forgets a setting.
> **The Boolean Trap:** `bool("False")` equals `True` in Python. To safely convert a string to a boolean, force it to lowercase and compare: `string_val.lower() == "true"`.

> [!SUCCESS] Phase 2: Configuration Parser Completed
> - **Modularity Maintained:** Kept in `src/mazegen/utils/config.py`.
> - **42 Compliance:** Handled file closure safely with `with open()`, routed all errors to `sys.stderr`, and strictly avoided tracebacks with `sys.exit(1)`.
> - **Type Safety:** Used `Dict[str, Any]` to cast strings into `int`, `bool`, and `tuple`.
> - **Defensive Logic:** Prevented the "Boolean Trap", prevented impossible dimensions (2x2), and handled optional missing values safely via `dict.get()`.
