A-Maze-ing/
├── Makefile                # Automation for install, lint, test, and build
├── pyproject.toml          # Build system and dependencies (PEP 517)
├── README.md               # Documentation
├── src/
│   └── mazegen/            # YOUR SCOPE (Student 1)
│       ├── __init__.py     # Makes it a package
│       ├── main.py         # Entry point for the CLI generator
│       ├── generator.py    # The Recursive Backtracker logic
│       ├── models.py       # Maze and Cell data structures
│       ├── utils/
│       │   ├── config.py   # KEY=VALUE parser
│       │   └── validator.py# Maze integrity checks
│       └── data/           # Storing the "42" pattern template
├── tests/                  # Pytest suite (Validation)
└── scripts/                # Student 2's work (Solver/Display)