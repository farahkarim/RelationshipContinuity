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

This project uses a dedicated Conda environment named `ddi-datacite`. The environment specification is stored in `environment.yml`, while Python package dependencies are listed in `requirements.txt`.

### Requirements

* Anaconda or Miniconda
* Git
* VS Code (recommended)

### 1. Create the environment

From the Anaconda PowerShell Prompt, navigate to the project directory:

```powershell
cd "C:\path\to\RelationshipContinuity"
```

Create the environment from `environment.yml`:

```powershell
conda env create -f environment.yml
```

This creates the `ddi-datacite` environment using Python 3.12 and installs the dependencies listed in `requirements.txt`.

### 2. Activate the environment

```powershell
conda activate ddi-datacite
```

Verify that the environment is active:

```powershell
conda info --envs
```

The active environment should be marked with `*`:

```text
ddi-datacite    *    C:\Users\<username>\AppData\Local\anaconda3\envs\ddi-datacite
```

Check the Python version:

```powershell
python --version
```

Expected:

```text
Python 3.12.x
```

### 3. Verify the dependencies

Run:

```powershell
python -c "import pandas, lxml, openpyxl; print('Environment OK')"
```

If successful:

```text
Environment OK
```

### 4. VS Code

Open the project in VS Code and select the `ddi-datacite` Python interpreter:

**Ctrl + Shift + P → Python: Select Interpreter**

Select the interpreter associated with:

```text
ddi-datacite
```

Typically:

```text
C:\Users\<username>\AppData\Local\anaconda3\envs\ddi-datacite\python.exe
```

### 5. Dependency files

The project uses two files for environment reproducibility:

#### `environment.yml`

Defines the Conda environment, including:

* Environment name
* Python version
* Conda channels
* Installation of `requirements.txt`

#### `requirements.txt`

Lists the Python packages required by the project.

Current dependencies:

```text
pandas
lxml
openpyxl
```

### 6. Recreating the environment

On another machine, clone the repository and run:

```powershell
conda env create -f environment.yml
conda activate ddi-datacite
```

This recreates the project environment and installs the Python dependencies.

### 7. Updating the environment

If `requirements.txt` is changed, update the environment with:

```powershell
conda activate ddi-datacite
python -m pip install -r requirements.txt
```

If the Python version or Conda configuration in `environment.yml` changes, the environment can be updated with:

```powershell
conda env update -f environment.yml --prune
```

---

## Reproducibility

The following files are maintained in the repository to support reproducible research:

```text
environment.yml
requirements.txt
README.md
```

`environment.yml` specifies the Conda environment, `requirements.txt` specifies the Python dependencies, and this README documents the setup and analysis workflow.
