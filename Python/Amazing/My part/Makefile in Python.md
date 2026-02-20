
>[!abstract] Makefile is a contract proves you can automate your workflow, manage environments, and enforce code quality


>In Python projects, a Makefile isn't for compiling C; it's for **Task Orchestration**.

## 1. Goal

To provide a single entry point for:
- **Installing** the project and its development dependencies.
- **Linting** the code to ensure `flake8` compliance.
- **Type Checking** via `mypy`.
- **Testing** via `pytest`.
- **Building** the `.whl` and `.tar.gz` packages.

> [!INFO] Project Tools Summary
| Tool | Role | Analogy |
| :--- | :--- | :--- |
> | **flake8** | Style & Syntax | The strict grammar proofreader (PEP 8). |
> | **mypy** | Static Type Checker | The inspector ensuring data shapes match (PEP 484). |
> | **pytest** | Testing Framework | The test track to prove small units of code work. |
> | **build** | Packager | The factory machine that boxes up the code. |
> | **wheel** | Distribution Format | The final `.whl` box that Student 2 will install. |
### 2. Design Decisions

- **Virtual Environment (`venv`):** We never install packages globally. The Makefile should handle the creation of a local environment.
    
- **PHONY Targets:** Since `clean`, `test`, a nd `lint` aren't files being built, we mark them as `.PHONY` to prevent conflicts if a folder with that name exists.
    
- **Standard 42 Rules:** We include `all`, `clean`, and `fclean`.

> [!NOTE] Lightweight Makefile Strategy
> **Pros:** Bypasses complex `venv` setup, uses strict `mypy` typing rules, and includes a handy `pdb` debugger target.
> **Cluster Safety:** Added `--user` to `pip install` commands to prevent "Permission Denied" errors on 42 Linux machines without root access.
> **42 Compliance:** Ensured `all`, `clean`, `fclean`, and `re` are present to meet standard evaluation rubrics.
> **Student 1 Warning:** Ensure `mlx` (display library) is NOT imported in the core maze generation logic!

`

