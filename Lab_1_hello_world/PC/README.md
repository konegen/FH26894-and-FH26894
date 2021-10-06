upyter Notebooks in VS Code
Jupyter (formerly IPython Notebook) is an open-source project that lets you easily combine Markdown text and executable Python source code on one canvas called a notebook. Visual Studio Code supports working with Jupyter Notebooks natively, and through Python code files. This topic covers the native support available for Jupyter Notebooks and demonstrates how to:

Create, open, and save Jupyter Notebooks
Work with Jupyter code cells
View, inspect, and filter variables using the Variable Explorer and Data Viewer
Connect to a remote Jupyter server
Debug a Jupyter Notebook
Setting up your environment#
To work with Python in Jupyter Notebooks, you must activate an Anaconda environment in VS Code, or another Python environment in which you've installed the Jupyter package. To select an environment, use the Python: Select Interpreter command from the Command Palette (Ctrl+Shift+P).

Once the appropriate environment is activated, you can create and open a Jupyter Notebook, connect to a remote Jupyter server for running code cells, and export a Jupyter Notebook as a Python file.

Workspace Trust#
When getting started with Notebooks, you'll want to make sure that you are working in a trusted workspace. Harmful code can be embedded in notebooks and the Workspace Trust feature allows you to indicate which folders and their contents should allow or restrict automatic code execution.

If you attempt to open a notebook when VS Code is in an untrusted workspace running Restricted Mode, you will not be able to execute cells and rich outputs will be hidden.

Create or open a Jupyter Notebook#
You can create a Jupyter Notebook by running the Jupyter: Create Blank New Jupyter Notebook command from the Command Palette (Ctrl+Shift+P) or by creating a new .ipynb file in your workspace.

Blank Jupyter Notebook

Next, select a kernel using the kernel picker in the top right.

Kernel Picker

After selecting a kernel, the language picker located in the bottom right of each code cell will automatically update to the language supported by the kernel.

Language Picker

If you have an existing Jupyter Notebook, you can open it by right-clicking on the file and opening with VS Code, or through the VS Code File Explorer.

Running cells#
