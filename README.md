# Quadtree Fabric

**A visual, polyglot programming lab for rapid prototyping and systems sketching.**

---

## 1. Characterization

**Quadtree Fabric** is a desktop application that re-imagines code organization through a spatially-aware, visual interface. It is characterized as a general-purpose, multi-language programming environment where each cell in a subdividable grid (a quadtree) is a fully programmable, Turing-complete unit. This allows for the intuitive arrangement of scripts, notes, and media, creating a tangible "canvas" for complex projects.

The primary function of this application is to serve as an interactive laboratory for developers, data scientists, students, and systems thinkers. It facilitates rapid prototyping, educational exploration, and the visualization of multi-component systems by breaking them down into discrete, interconnected cells.

## 2. Core Features

The Quadtree Fabric is constituted by a modular architecture that provides a robust and extensible feature set.

* **Visual Quadtree Canvas**: Organize your project by placing code, text, and images into cells on an infinitely subdividable grid. Group related logic spatially and visualize the structure of your system.
* **Polyglot Execution Engine**: Write and execute code in multiple languages within the same project. The application includes built-in, sandboxed executors for:
    * Python 3
    * C (C11)
    * C++ (C++20)
    * Java
* **Stateful Sessions**: For interpreted languages like Python, the engine maintains a persistent session, allowing cells to share state (variables, functions, imports) for building complex, multi-step workflows.
* **Extensible Plugin Architecture**: The execution engine is designed to be extended. Developers can create and distribute their own language executors as standard Python packages.
* **Comprehensive Tooling**: Includes a multi-file code editor, an output viewer that separates stdout from stderr, and a cell explorer for managing and batch-executing code across the canvas.
* **Data Persistence**: Save and load entire quadtree contexts, including all code, cell colors, and payloads, to a structured JSON format.

## 3. Installation

Ensure you have Python 3.12 or newer installed on your system.

### 3.1. Standard Installation

Install the application and its core dependencies from the Python Package Index (PyPI):

```
pip install quadtree-fabric
```

### 3.2. Full Installation (with Optional Dependencies)

For enhanced functionality, such as more robust Python session snapshotting, install the application with the `[full]` option:

```
pip install quadtree-fabric[full]
```

## 4. Usage

Once installed, run the application from your terminal:

```
quadtree-fabric
```

### Basic Workflow:

1.  **Right-click** on a cell in the main grid to open the context menu.
2.  Select **"Add Code"** to open the Code Editor.
3.  Choose your desired language from the dropdown menu, write your code, and click **"Save"**.
4.  **Right-click** the cell again and select **"Execute Code"** to run it. The Output Modal will appear with the results.
5.  Use the **Cell Explorer** to view and manage all code cells in your context.

## 5. For Developers and Contributors

We welcome contributions to the Quadtree Fabric project. Whether you are fixing a bug, improving a feature, or creating a new language executor, your input is valuable.

Please refer to our documentation for detailed guides:

* **`docs/development.md`**: For instructions on setting up a development environment and running the test suite.
* **`docs/executor_sdk.md`**: A comprehensive guide for creating and distributing your own language executor plugins.

---

The Quadtree Fabric project is built on the principle that the way we organize our code should be as flexible and powerful as the code itself. We hope you find it to be a useful and inspiring tool.
