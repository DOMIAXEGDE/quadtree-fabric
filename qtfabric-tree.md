```
quadtree-fabric/
├── .gitignore
├── LICENSE
├── pyproject.toml         # Updated with new dependencies and entry points
├── README.md              # High-level project overview
│
├── docs/                  # New: Documentation for developers and users
│   ├── development.md       # Guide for setting up the dev environment
│   └── executor_sdk.md      # How to create and distribute new executors
│
├── examples/              # New: Sample quadtree contexts
│   ├── data_science_flow.json
│   └── game_asset_pipeline.json
│
├── src/
│   └── quadtreefabric/
│       ├── __init__.py
│       ├── main.py              # New: The main application entry point
│       ├── app.py               # Renamed from nodes.py, contains the main QuadtreeApp class
│       ├── config.py            # Unchanged, for styling and configuration
│       │
│       ├── core/                # New: Core, non-UI application logic
│       │   ├── __init__.py
│       │   ├── matrix_handler.py  # Contains the QuadtreeMatrix class for data operations
│       │   └── io_handler.py      # Manages file I/O (JSON, PNG, code export) and TK dialogs
│       │
│       ├── data_models.py       # New: Centralized data classes
│       │                        # (Matrix, Layer, ExecMeta, CellPayloadV2, etc.)
│       │
│       ├── execution/           # Renamed from runtime/, focuses on code execution
│       │   ├── __init__.py
│       │   ├── engine.py          # New: The core execution engine (job queue, process pool)
│       │   ├── registry.py        # Manages discovery of executors (local and installed)
│       │   ├── session.py         # Manages state for interpreted languages
│       │   ├── constants.py       # Unchanged
│       │   │
│       │   └── executors/         # Renamed from plugins/, holds built-in language handlers
│       │       ├── __init__.py
│       │       ├── _base.py         # New: Base class or protocol for all executors
│       │       ├── python_exec.py
│       │       ├── c_exec.py
│       │       ├── cpp_exec.py
│       │       └── java_exec.py
│       │
│       └── ui/                  # New: Dedicated package for all UI components
│           ├── __init__.py
│           ├── components.py      # Basic widgets: Button, Slider, DropDown, TextInput
│           ├── modals.py          # Complex modals: CodeEditorModal, OutputModal, ExplorerModal
│           ├── context_menu.py    # The right-click context menu logic and rendering
│           └── canvas.py          # Logic for rendering the quadtree grid and its visual payloads
│
└── tests/                 # New: A dedicated test suite for ensuring stability
    ├── __init__.py
    ├── test_execution.py      # Tests for the execution engine and executors
    ├── test_matrix.py         # Tests for data manipulation in QuadtreeMatrix
    └── test_io.py             # Tests for JSON serialization and file handling

```