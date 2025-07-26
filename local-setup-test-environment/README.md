## 🛠️ Local Setup Instructions

This guide walks you through setting up the `data-processing-automation` project locally, including creating the required folder and virtual environment.

---

### 📁 1. Navigate to Your Project Directory

Open your terminal (Command Prompt, PowerShell, or your preferred terminal) and navigate to the directory where your project will reside:

```bash
cd C:/Users/loydt/OneDrive/文档/Project/data-processing-automation
```

```bash
Make sure this directory exists. If not, create it first using:


mkdir C:/Users/loydt/OneDrive/文档/Project/data-processing-automation
cd C:/Users/loydt/OneDrive/文档/Project/data-processing-automation
```

### 🐍 2. Create a Virtual Environment

Create a virtual environment in the project directory using Python’s built-in `venv` module:

```bash
python -m venv .venv
```

This command creates a `.venv` folder that contains an isolated Python environment for this project.

### ⚡ 3. Activate the Virtual Environment

Activate the virtual environment to begin installing and managing project-specific packages.

**For Windows (PowerShell):**

```bash
.\.venv\Scripts\Activate.ps1
```

**For Windows (Command Prompt):**

```bash
.venv\Scripts\activate
```

**For macOS/Linux:**

```bash
source .venv/bin/activate
```

Once activated, your terminal should show a prefix like `(.venv)` indicating the environment is active.

### ✅ 4. Verify Python Version

Check that you're using the correct Python version (e.g., Python 3.12+):

```bash
python --version
```
```
