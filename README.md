# RelationshipContinuity

## Source Schemas

The following official schema specifications are used in this research project. The version and download date are recorded to support reproducibility and provenance.

| Schema        | Version | Format | Download Date | Official Source                    |
| ------------- | ------- | ------ | ------------- | ---------------------------------- |
| DDI-Lifecycle | 3.3     | XSD    | 2026-10-05    | `https://ddialliance.org/ddi-lifecycle_v3.3` |
| DataCite      | 4.7     | XSD    | 2026-10-05    | `https://schema.datacite.org/meta/kernel-4.7/metadata.xsd`      |

### DDI-Lifecycle 3.3

* **Version:** 3.3
* **Format:** XML Schema Definition (XSD)
* **Download date:** 2026-10-05
* **Official source:** `https://ddialliance.org/ddi-lifecycle_v3.3`
* **Local directory:** `data/ddi-lifecycle-3.3/`

### DataCite 4.7

* **Version:** 4.7
* **Format:** XML Schema Definition (XSD)
* **Download date:** 2026-10-05
* **Official source:** `https://schema.datacite.org/meta/kernel-4.7/metadata.xsd`
* **Local directory:** `data/datacite-4.7/`

> **Reproducibility note:** The original schema files are retained in the `data/` directory. The version and download date are recorded here so that the analysis can be reproduced using the same schema versions.

## Python Environment

This project uses a dedicated Conda environment to keep the research dependencies isolated from other Python projects.

### Requirements

* Anaconda or Miniconda
* Python 3.12
* Git
* VS Code (recommended)

### 1. Create the Conda environment

From the Anaconda PowerShell Prompt:

```powershell
conda create -n ddi-datacite python=3.12
```

Activate the environment:

```powershell
conda activate ddi-datacite
```

Verify the Python version:

```powershell
python --version
```

The expected output is:

```text
Python 3.12.x
```

### 2. Install project dependencies

With the `ddi-datacite` environment activated, navigate to the project directory:

```powershell
cd "C:\path\to\RelationshipContinuity"
```

Install the dependencies listed in `requirements.txt`:

```powershell
python -m pip install -r requirements.txt
```

The current dependencies are:

* `pandas` — data manipulation and CSV processing
* `lxml` — XML/XSD parsing
* `openpyxl` — Excel file support

### 3. Verify the environment

Run:

```powershell
python -c "import pandas, lxml, openpyxl; print('Environment OK')"
```

If successful, the terminal should display:

```text
Environment OK
```

### 4. VS Code

In VS Code, select the project environment:

**Ctrl + Shift + P → Python: Select Interpreter**

Select:

```text
C:\Users\<username>\AppData\Local\anaconda3\envs\ddi-datacite\python.exe
```

The selected interpreter should correspond to the `ddi-datacite` Conda environment.

### 5. Recreating the environment

To recreate the project environment on another machine:

```powershell
conda create -n ddi-datacite python=3.12
conda activate ddi-datacite
python -m pip install -r requirements.txt
```

This installs the Python dependencies required by the project.

## Dependency management

The `requirements.txt` file records the Python packages required by the analysis. When a new Python dependency is introduced, it should be added to this file.

For example:

```text
pandas
lxml
openpyxl
```

The Conda environment itself is named:

```text
ddi-datacite
```

The README documents the environment creation and installation procedure so that the analysis can be reproduced.
