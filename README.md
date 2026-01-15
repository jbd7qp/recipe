## 1. Create a GitHub Repository

1. Go to GitHub → **New repository**.
2. Name the repo, choose **Public** or **Private**.
3. Initialize with a **README.md**.
4. Create the repository.

---

## 2. Create a Codespace

**Option A: In-browser**

1. In the repo, click **Code** → **Codespaces** → **Create codespace on main**.

**Option B: From VS Code (application)**

1. Open VS Code.
2. Install the **GitHub Codespaces** extension.
3. Click **Connect to…** → **Create New Codespace**.
4. Sign in to GitHub and select your repo.

---

## 3. Open Codespace in Local VS Code

1. Open VS Code locally.
2. Use the **Codespaces** extension to connect to your Codespace.
3. Explore the file tree and terminal layout.
4. Create a new Python file (e.g., `main.py`).
5. Add cell breaks to make it interactive:

   ```python
   # %%
   ```
6. If cells do not run, reload the **Jupyter** extension and ensure `ipykernel` is installed.

---

## 4. Create and Activate a Virtual Environment

1. Open a **bash** terminal.
2. Create a virtual environment:

   ```bash
   python3 -m venv venv
   ```
3. Activate it:

   ```bash
   source venv/bin/activate
   ```
4. Confirm activation (your terminal path now shows `(venv)`).
5. **Do not commit** the virtual environment. Add it to `.gitignore`.

---

## 5. Install and Manage Packages

1. Install required packages:

   ```bash
   pip install plotly
   ```
2. Check the installed version:

   ```bash
   pip show plotly
   ```
3. Freeze dependencies into `requirements.txt`:

   ```bash
   pip freeze > requirements.txt
   ```
4. Update the file anytime packages change using the same command.

**Why `requirements.txt`?**

* Ensures reproducibility.
* Allows others (and future you) to recreate the same environment.
* Simplifies deployment and collaboration.

---

## 6. View and Explore Data

1. Load a dataset in your Python file using pandas.
2. Install **Data Wrangler** from the Extensions menu.
3. Open the Data Viewer to inspect, filter, and clean data visually.

**Useful Data Wrangler features:**

* Interactive table preview
* Automated data cleaning suggestions
* One-click export to pandas code

---

## 7. Extension Management

1. Open the **Extensions** panel in VS Code.
2. Note that extensions can be **local**, **remote (Codespace)**, or **disabled**.
3. Extensions installed locally do **not** automatically install in a Codespace.
4. Each new Codespace is a fresh remote environment, so extensions like **Data Wrangler must be reinstalled** unless configured otherwise.

---

## 8. Commit and Push to GitHub

1. Check changes:

   ```bash
   git status
   ```
2. Stage files:

   ```bash
   git add .
   ```
3. Commit:

   ```bash
   git commit -m "Initial project setup"
   ```
4. Push to GitHub:

   ```bash
   git push
   ```

---

## Sample `requirements.txt`

```
plotly
ipykernel
pandas
```