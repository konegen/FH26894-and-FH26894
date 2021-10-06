Jupyter Notebooks in VS Code

[[Jupyter]{.ul}](https://jupyter-notebook.readthedocs.io/en/latest/) (formerly
IPython Notebook) is an open-source project that lets you easily combine
Markdown text and executable Python source code on one canvas called
a **notebook**. Visual Studio Code supports working with Jupyter
Notebooks natively, and through [[Python code
files]{.ul}](https://code.visualstudio.com/docs/python/jupyter-support-py).
This topic covers the native support available for Jupyter Notebooks and
demonstrates how to:

-   Create, open, and save Jupyter Notebooks

-   Work with Jupyter code cells

-   View, inspect, and filter variables using the Variable Explorer and
    Data Viewer

-   Connect to a remote Jupyter server

-   Debug a Jupyter Notebook

Setting up your
environment[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_setting-up-your-environment)

To work with Python in Jupyter Notebooks, you must activate an Anaconda
environment in VS Code, or another Python environment in which you\'ve
installed the [Jupyter package]{.ul}. To select an environment, use
the **Python: Select Interpreter** command from the Command Palette
(Ctrl+Shift+P).

Once the appropriate environment is activated, you can create and open a
Jupyter Notebook, connect to a remote Jupyter server for running code
cells, and export a Jupyter Notebook as a Python file.

Workspace
Trust[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_workspace-trust)

When getting started with Notebooks, you\'ll want to make sure that you
are working in a trusted workspace. Harmful code can be embedded in
notebooks and the [[Workspace
Trust]{.ul}](https://code.visualstudio.com/docs/editor/workspace-trust) feature
allows you to indicate which folders and their contents should allow or
restrict automatic code execution.

If you attempt to open a notebook when VS Code is in an untrusted
workspace running [[Restricted
Mode]{.ul}](https://code.visualstudio.com/docs/editor/workspace-trust#_restricted-mode),
you will not be able to execute cells and rich outputs will be hidden.

Create or open a Jupyter
Notebook[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_create-or-open-a-jupyter-notebook)

You can create a Jupyter Notebook by running the **Jupyter: Create Blank
New Jupyter Notebook** command from the Command Palette (Ctrl+Shift+P)
or by creating a new .ipynb file in your workspace.

![Blank Jupyter Notebook](.//media/image1.png){width="6.3in"
height="1.1104166666666666in"}

Next, select a kernel using the kernel picker in the top right.

![Kernel Picker](.//media/image2.png){width="6.3in"
height="1.1104166666666666in"}

After selecting a kernel, the language picker located in the bottom
right of each code cell will automatically update to the language
supported by the kernel.

![Language Picker](.//media/image3.png){width="6.3in"
height="0.8909722222222223in"}

If you have an existing Jupyter Notebook, you can open it by
right-clicking on the file and opening with VS Code, or through the VS
Code File Explorer.

Running
cells[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_running-cells)

Once you have a Notebook, you can run a code cell using the **Run** icon
to the left of the cell and the output will appear directly below the
code cell.

You can also use keyboard shortcuts to run code. When in command or edit
mode, use Ctrl+Enter to run the current cell or Shift+Enter to run the
current cell and advance to the next.

![Run Jupyter code cell](.//media/image4.png){width="6.3in"
height="1.1055555555555556in"}

You can run multiple cells by using **Run All**, **Run All Above**,
or **Run All Below**.

![Run Jupyter code cells](.//media/image5.png){width="6.3in"
height="2.283333333333333in"}

Save your Jupyter
Notebook[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_save-your-jupyter-notebook)

You can save your Jupyter Notebook using the keyboard
shortcut Ctrl+S or **File** \> **Save**.

Export your Jupyter
Notebook[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_export-your-jupyter-notebook)

You can export a Jupyter Notebook as a Python file (.py), a PDF, or an
HTML file. To export, select the **Export** action on the main toolbar.
You\'ll then be presented with a dropdown of file format options.

![Convert Jupyter Notebook to Python
file](.//media/image6.png){width="6.3in" height="0.9020833333333333in"}

**Note:** For PDF export, you must have [[TeX
installed]{.ul}](https://nbconvert.readthedocs.io/en/latest/install.html#installing-tex).
If you don\'t, you will be notified that you need to install it when you
select the PDF option. Also, be aware that if you have SVG-only output
in your Notebook, they will not be displayed in the PDF. To have SVG
graphics in a PDF, either ensure that your output includes a non-SVG
image format or else you can first export to HTML and then save as PDF
using your browser.

Work with code cells in the Notebook
Editor[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_work-with-code-cells-in-the-notebook-editor)

The Notebook Editor makes it easy to create, edit, and run code cells
within your Jupyter Notebook.

Create a code
cell[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_create-a-code-cell)

By default, a blank Notebook will have an empty code cell for you to
start with.

msg = \"Hello world\"

print(msg)

![Simple Jupyter code cell](.//media/image7.png){width="6.3in"
height="2.5993055555555555in"}

Code cell
modes[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_code-cell-modes)

While working with code cells, a cell can be in three states:
unselected, command mode, and edit mode. The current state of a cell is
indicated by a vertical bar to the left of a code cell and editor
border. When no bar is visible, the cell is unselected.

![Unselected Jupyter code cell](.//media/image8.png){width="6.3in"
height="2.2875in"}

When a cell is selected, it can be in two different modes. It can be in
command mode or in edit mode. When the cell is in command mode, it can
be operated on and accept keyboard commands. When the cell is in edit
mode, the cell\'s contents (code or Markdown) can be modified.

When a cell is in command mode, a solid vertical bar will appear to the
left of the cell.

![Code cell in command mode](.//media/image7.png){width="6.3in"
height="2.5993055555555555in"}

When you\'re in edit mode, the solid vertical bar is joined by a border
around the cell editor.

![Code cell in edit mode](.//media/image9.png){width="6.3in"
height="2.5972222222222223in"}

To move from edit mode to command mode, press the Esc key. To move from
command mode to edit mode, press the Enter key. You can also use the
mouse to **change the mode** by clicking the vertical bar to the left of
the cell or out of the code/Markdown region in the code cell.

Add additional code
cells[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_add-additional-code-cells)

Code cells can be added to a Notebook using the main toolbar, a cell\'s
add cell toolbar (visible with hover), and through keyboard commands.

![Add code cells](.//media/image10.png){width="6.3in"
height="1.2215277777777778in"}

Using the plus icons in the main toolbar and a cell\'s hover toolbar
will add a new cell directly below the currently selected cell.

When a code cell is in command mode, the A key can be used to add a cell
above and the B can be used to add a cell below the selected cell.

Select a code
cell[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_select-a-code-cell)

The selected code cell can be changed using the mouse, the up/down arrow
keys on the keyboard, and the J (down) and K (up) keys. To use the
keyboard, the cell must be in command mode.

Select multiple code
cells[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_select-multiple-code-cells)

To select multiple cells, start with one cell in selected mode. If you
want to select consecutive cells, hold down Shift and click the last
cell you want to select. If you want to select any group of cells, hold
down Ctrl and click the cells you\'d like to add to your selection.

Selected cells will be indicated by the filled background.

![Multiselected cells](.//media/image11.png){width="6.3in"
height="3.6909722222222223in"}

Run a single code
cell[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_run-a-single-code-cell)

Once your code is added, you can run a cell using the **Run** icon to
the left of the cell and the output will be displayed below the code
cell.

![Run Jupyter code cell](.//media/image12.png){width="6.3in"
height="2.5701388888888888in"}

You can also use keyboard shortcuts to run a selected code
cell. Ctrl+Enter runs the currently selected cell, Shift+Enter runs the
currently selected cell and inserts a new cell immediately below (focus
moves to new cell), and Alt+Enter runs the currently selected cell and
inserts a new cell immediately below (focus remains on current cell).
These keyboard shortcuts can be used in both command and edit modes.

Run multiple code
cells[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_run-multiple-code-cells)

Running multiple code cells can be accomplished in many ways. You can
use the double arrow in the main toolbar of the Notebook Editor to run
all cells within the Notebook or the **Run** icons with directional
arrows in the cell toolbar to run all cells above or below the current
code cell.

![Run multiple code cells](.//media/image5.png){width="6.3in"
height="2.283333333333333in"}

Move a code
cell[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_move-a-code-cell)

Moving cells up or down within a Notebook can be accomplished via
dragging and dropping. For code cells, the drag and drop area is to the
left of the cell editor as indicated below. For rendered Markdown cells,
you may click anywhere to drag and drop cells.

![Move a code cell](.//media/image13.png){width="6.3in"
height="2.8625in"}

To move multiple cells, you can use the same drag and drop areas in any
cell included in the selection.

You can also use the keyboard shortcuts Alt+Arrow to move one or
multiple selected cells.

Delete a code
cell[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_delete-a-code-cell)

Deleting a code cell can be accomplished by using the **Delete** icon in
the code cell toolbar or through the keyboard shortcut dd when the
selected code cell is in command mode.

![Delete a code cell](.//media/image14.png){width="6.3in"
height="2.5791666666666666in"}

Undo your last
change[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_undo-your-last-change)

You can use the z key to undo your previous change, for example, if
you\'ve made an accidental edit, you can undo it to the previous correct
state, or if you\'ve deleted a cell accidentally, you can recover it.

Switch between code and
Markdown[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_switch-between-code-and-markdown)

The Notebook Editor allows you to easily change code cells between
Markdown and code. Clicking the language picker in the bottom right of a
cell will allow you to switch between Markdown and, if applicable, any
other language supported by the selected kernel.

![Change language](.//media/image3.png){width="6.3in"
height="0.8909722222222223in"}

You can also use the keyboard to change the cell type. When a cell is
selected and in command mode, the M key switches the cell type to
Markdown and the Y key switches the cell type to code.

Once Markdown is set, you can enter Markdown formatted content to the
code cell.

![Raw Markdown displayed in code
cell](.//media/image15.png){width="6.3in" height="1.551388888888889in"}

To render Markdown cells, you can select the check mark in the cell
toolbar, or use the Ctrl+Enter and Shift+Enter keyboard shortcuts.

![How to render Markdown](.//media/image16.png){width="6.3in"
height="1.445138888888889in"}

![Rendered Markdown displayed in code
cell](.//media/image17.png){width="6.3in" height="1.4506944444444445in"}

Clear output or restart/interrupt the
kernel[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_clear-output-or-restartinterrupt-the-kernel)

If you\'d like to clear all code cell outputs or restart/interrupt the
kernel, you can accomplish that using the main Notebook Editor toolbar.

![Notebook Toolbar](.//media/image18.png){width="6.3in"
height="0.3076388888888889in"}

Enable/disable line
numbers[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_enabledisable-line-numbers)

When you are in command mode, you can enable or disable line numbering
within a single code cell by using the L key.

![Line numbers enabled in code cell](.//media/image19.png){width="6.3in"
height="2.7583333333333333in"}

To toggle line numbering for the entire notebook, use Shift+L when in
command mode on any cell.

![Line numbers enabled for notebook](.//media/image20.png){width="6.3in"
height="3.703472222222222in"}

Table of
Contents[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_table-of-contents)

To navigate through your notebook, open the File Explorer in the
Activity bar. Then open the **Outline** tab in the Side bar.

![Table of contents](.//media/image21.png){width="6.3in"
height="3.720138888888889in"}

**Note:** By default, the outline will only show Markdown. To show code
cells, enable the following setting: **Notebook \> Outline: Show Code
Cells**.

IntelliSense support in the Jupyter Notebook
Editor[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_intellisense-support-in-the-jupyter-notebook-editor)

The Python Jupyter Notebook Editor window has full IntelliSense -- code
completions, member lists, quick info for methods, and parameter hints.
You can be just as productive typing in the Notebook Editor window as
you are in the code editor.

![IntelliSense support](.//media/image22.png){width="6.3in"
height="4.700694444444444in"}

Variable Explorer and Data
Viewer[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_variable-explorer-and-data-viewer)

Within a Python Notebook, it\'s possible to view, inspect, sort, and
filter the variables within your current Jupyter session. By selecting
the **Variables** icon in the main toolbar after running code and cells,
you\'ll see a list of the current variables, which will automatically
update as variables are used in code. The variables pane will open at
the bottom of the notebook.

![Variable Explorer](.//media/image23.png){width="6.3in"
height="4.276388888888889in"}

![Variable Explorer](.//media/image24.png){width="6.3in"
height="4.541666666666667in"}

For additional information about your variables, you can also
double-click on a row or use the **Show variable in data viewer** button
next to the variable for a more detailed view of a variable in the Data
Viewer. Once open, you can filter the values by searching over the rows.

![Data Viewer](.//media/image25.png){width="4.841666666666667in"
height="3.908333333333333in"}

Saving
plots[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_saving-plots)

To save a plot from your notebook, simply hover over the output and
select the **Save** icon in the top right.

![Save output](.//media/image26.png){width="6.3in"
height="3.7909722222222224in"}

**Note:** There is support for rendering plots created
with [[matplotlib]{.ul}](https://matplotlib.org/) and [[Altair]{.ul}](https://altair-viz.github.io/index.html).

Custom notebook
diffing[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_custom-notebook-diffing)

Under the hood, Jupyter Notebooks are JSON files. The segments in a JSON
file are rendered as cells that are comprised of three components:
input, output, and metadata. Comparing changes made in a notebook using
lined-based diffing is difficult and hard to parse. The rich diffing
editor for notebooks allows you to easily see changes for each component
of a cell.

You can even customize what types of changes you want displayed within
your diffing view. In the top right, select the overflow menu item in
the toolbar to customize what cell components you want included. Input
differences will always be shown.

![Custom notebook diffing](.//media/image27.png){width="6.3in"
height="4.445833333333334in"}

To learn more about Git integration within VS Code, visit [[Version
Control in VS
Code]{.ul}](https://code.visualstudio.com/docs/editor/versioncontrol).

Debug a Jupyter
Notebook[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_debug-a-jupyter-notebook)

If you need additional debug support in order to diagnose an issue in
your code cells, you can export it as a Python file. Once exported as a
Python file, the VS Code debugger lets you step through your code, set
breakpoints, examine state, and analyze problems. Using the debugger is
a helpful way to find and correct issues in notebook code. To debug your
Python file:

1.  In VS Code, if you haven\'t already, activate a Python environment
    in which Jupyter is installed.

2.  From your Jupyter Notebook (.ipynb), select the **Export** button in
    the main toolbar.

> ![Convert Jupyter Notebook to Python
> file](.//media/image6.png){width="6.3in"
> height="0.9020833333333333in"}
>
> Once exported, you\'ll have a .py file with your code that you can use
> for debugging.

3.  After saving the .py file, to start the debugger, use one of the
    following options:

    -   For the whole Notebook, open the Command Palette (Ctrl+Shift+P)
        and run the **Python: Debug Current File in Python Interactive
        Window** command.

    -   For an individual cell, use the **Debug Cell** action that
        appears above the cell. The debugger specifically starts on the
        code in that cell. By default, **Debug Cell** steps into user
        code. If you want to step into non-user code, you need to
        uncheck **Data Science: Debug Just My Code** in the Python
        extension settings (Ctrl+,).

4.  To familiarize yourself with the general debugging features of VS
    Code, such as inspecting variables, setting breakpoints, and other
    activities, review [[VS Code
    debugging]{.ul}](https://code.visualstudio.com/docs/editor/debugging).

5.  As you find issues, stop the debugger, correct your code, save the
    file, and start the debugger again.

6.  When you\'re satisfied that all your code is correct, use the Python
    Interactive window to export the Python file as a Jupyter Notebook
    (.ipynb).

Connect to a remote Jupyter
server[[\#]{.ul}](https://code.visualstudio.com/docs/datascience/jupyter-notebooks#_connect-to-a-remote-jupyter-server)

You can offload intensive computation in a Jupyter Notebook to other
computers by connecting to a remote Jupyter server. Once connected, code
cells run on the remote server rather than the local computer.

To connect to a remote Jupyter server:

1.  Select the **Jupyter Server: local** button in the global Status bar
    or run the **Jupyter: Specify local or remote Jupyter server for
    connections** command from the Command Palette (Ctrl+Shift+P).

> ![Specify remote Jupyter server](.//media/image28.png){width="6.3in"
> height="1.1604166666666667in"}

2.  When prompted to **Pick how to connect to Jupyter**,
    select **Existing: Specify the URI of an existing server**.

> ![Choose to connect to an existing
> server](.//media/image29.png){width="6.3in"
> height="1.6569444444444446in"}

3.  When prompted to **Enter the URI of a Jupyter server**, provide the
    server\'s URI (hostname) with the authentication token included with
    a ?token= URL parameter. (If you start the server in the VS Code
    terminal with an authentication token enabled, the URL with the
    token typically appears in the terminal output from where you can
    copy it.) Alternatively, you can specify a username and password
    after providing the URI.

> ![Prompt to supply a Jupyter server
> URI](.//media/image30.png){width="6.3in"
> height="0.7402777777777778in"}

**Note:** For added security, Microsoft recommends configuring your
Jupyter server with security precautions such as SSL and token support.
This helps ensure that requests sent to the Jupyter server are
authenticated and connections to the remote server are encrypted. For
guidance about securing a notebook server, refer to the [[Jupyter
documentation]{.ul}](https://jupyter-notebook.readthedocs.io/en/stable/public_server.html#securing-a-notebook-server).
