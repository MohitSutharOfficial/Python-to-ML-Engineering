# Python Environment Setup Guide

This guide documents how I set up Python before starting my structured Python to ML engineering journey.

Before writing code, it is important to set up the environment correctly. A good setup avoids package conflicts, version issues, and confusion when working with Python, notebooks, data science libraries, and ML tools.

## What Is an Environment?

A Python environment is an isolated workspace where Python and its libraries are installed.

Example:

- One project may need Python 3.10 and NumPy 1.x.
- Another project may need Python 3.11 and newer ML libraries.

If everything is installed globally on the computer, packages can conflict with each other. Environments solve this by keeping each project separate.

## Why Environment Setup Matters

Environment setup is important because it helps me:

- Keep projects clean and organized
- Avoid dependency conflicts
- Install only the libraries needed for one project
- Reproduce the same setup later
- Work like real Python, data science, and ML projects are managed
- Build a professional habit from the beginning

## Python Setup Options

There are two common ways to manage Python environments:

| Tool | Best For |
|------|----------|
| `venv` | Lightweight Python projects |
| Conda | Data science, ML, notebooks, and package-heavy projects |

For this learning repository, I prefer Conda because it is widely used in data science and ML workflows.

## What Is Conda?

Conda is a tool used to manage:

- Python versions
- Virtual environments
- Python packages
- Data science and ML dependencies

Conda makes it easy to create a separate environment for each project.

## Anaconda vs Miniconda

| Option | Meaning |
|--------|---------|
| Anaconda | Comes with Python and many data science libraries pre-installed |
| Miniconda | Smaller version; install only what you need |

Recommended:

- Use **Anaconda** if you want an easier beginner setup.
- Use **Miniconda** if you want a lightweight setup.

## Step 1: Install Python or Conda

### Option A: Install Anaconda

1. Go to the Anaconda website.
2. Download Anaconda for your operating system.
3. Install it using the default options.
4. Open Anaconda Prompt after installation.

### Option B: Install Miniconda

1. Go to the Miniconda website.
2. Download Miniconda for your operating system.
3. Install it.
4. Open Anaconda Prompt or terminal.

## Step 2: Check Conda Installation

Open terminal or Anaconda Prompt and run:

```bash
conda --version
```

Expected output will look like:

```text
conda 24.x.x
```

If you see a version number, Conda is installed correctly.

## Step 3: Create a New Environment

Create a separate environment for this learning repo:

```bash
conda create -n python-ml-learning python=3.11
```

Here:

- `conda create` creates a new environment.
- `-n python-ml-learning` gives the environment a name.
- `python=3.11` installs Python 3.11 inside that environment.

## Step 4: Activate the Environment

```bash
conda activate python-ml-learning
```

After activation, the terminal may show:

```text
(python-ml-learning)
```

This means the environment is active.

## Step 5: Check Python Version

```bash
python --version
```

Expected output:

```text
Python 3.11.x
```

## Step 6: Install Basic Libraries

For Python fundamentals, no extra libraries are required.

For notebooks and data science practice, install these:

```bash
conda install jupyter numpy pandas matplotlib
```

You can also install packages using `pip`:

```bash
pip install notebook
```

## Conda vs Pip

| Tool | Use |
|------|-----|
| `conda` | Best for Python versions, environments, and scientific packages |
| `pip` | Best for installing Python packages from PyPI |

Simple rule:

- Use `conda` first when installing data science libraries.
- Use `pip` when a package is not available through Conda.

## Step 7: Create Your First Python Program

Create a file named:

```text
hello.py
```

Add this code:

```python
print("Hello, Python!")
print("I am starting my Python to ML Engineering journey.")
```

Run the file:

```bash
python hello.py
```

Expected output:

```text
Hello, Python!
I am starting my Python to ML Engineering journey.
```

## Step 8: Run Python in Interactive Mode

You can also run Python directly in the terminal:

```bash
python
```

Then try:

```python
2 + 3
print("Python is working")
```

To exit interactive mode:

```python
exit()
```

## Step 9: Run Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

This opens Jupyter in the browser.

In Jupyter, you can:

- Write Python code in cells
- Run one cell at a time
- Add notes with Markdown
- Practice concepts interactively
- Build learning notebooks for revision

## Step 10: Use VS Code for Python

Recommended VS Code extensions:

- Python
- Jupyter
- Pylance

Basic workflow:

1. Open the project folder in VS Code.
2. Select the Conda environment as the Python interpreter.
3. Create a `.py` file.
4. Run the file from the terminal.

To check the active Python path:

```bash
where python
```

On macOS or Linux:

```bash
which python
```

## Useful Conda Commands

| Command | Purpose |
|---------|---------|
| `conda env list` | Show all environments |
| `conda activate env_name` | Activate an environment |
| `conda deactivate` | Exit the current environment |
| `conda install package_name` | Install a package |
| `conda list` | Show installed packages |
| `conda remove -n env_name --all` | Delete an environment |

## Save Environment Dependencies

To save installed packages:

```bash
conda env export > environment.yml
```

To recreate the environment later:

```bash
conda env create -f environment.yml
```

This is useful because it helps others or future me recreate the same setup.

## Common Problems and Fixes

### Problem: `conda` is not recognized

Fix:

- Open Anaconda Prompt instead of normal terminal.
- Restart the terminal after installing Conda.
- Check if Conda was added to PATH.

### Problem: Wrong Python version is running

Fix:

```bash
conda activate python-ml-learning
python --version
```

Make sure the correct environment is active.

### Problem: Jupyter is not opening

Fix:

```bash
conda activate python-ml-learning
conda install jupyter
jupyter notebook
```

### Problem: Package import error

Example:

```text
ModuleNotFoundError: No module named 'pandas'
```

Fix:

```bash
conda install pandas
```

or:

```bash
pip install pandas
```

## My Setup Checklist

Before starting Python practice, I check:

- Python is installed
- Conda is installed
- Project environment is created
- Environment is activated
- VS Code is using the correct interpreter
- Jupyter Notebook is working
- First Python program runs successfully

## Final Note

Environment setup is the first step in learning Python professionally.

This setup helps me keep my learning organized, avoid confusion, and build good habits for future AI/ML engineering projects.
