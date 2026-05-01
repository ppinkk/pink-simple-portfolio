# Guide: Deploying Static HTML/CSS/JS to GitHub Pages

Deploying a static website (HTML, CSS, and JS) to GitHub Pages is a straightforward process.

## Prerequisites
*   A GitHub account.
*   Your website files, including a mandatory `index.html` file at the root of your project.

---

## Method 1: Using the GitHub Website (Easiest)
1.  **Create a Repository:** Log in to GitHub, click the **+** icon in the top right, and select **New repository**.
2.  **Name it:** Give it a name (e.g., `my-website`). Keep it **Public**.
3.  **Upload Files:** Click **Add file > Upload files**. Drag and drop your HTML, CSS, and JS files into the repository.
4.  **Commit:** Click **Commit changes**.
5.  **Enable Pages:**
    *   Go to the **Settings** tab of your repository.
    *   Click **Pages** in the left sidebar.
    *   Under **Build and deployment > Source**, ensure **Deploy from a branch** is selected.
    *   Under **Branch**, select `main` (or `master`) and the `/ (root)` folder. Click **Save**.
6.  **View Site:** Wait a minute or two. A link will appear at the top of the Pages section (e.g., `https://username.github.io/my-website/`).

---

## Method 2: Using Git (Best for Updates)
If you have Git installed locally, follow these steps in your terminal:

1.  **Initialize & Commit:**
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    ```
2.  **Push to GitHub:**
    *   Create a new repository on GitHub (don't initialize with a README).
    *   Copy the remote URL and run:
    ```bash
    git remote add origin https://github.com/username/repository-name.git
    git branch -M main
    git push -u origin main
    ```
3.  **Enable Pages:** Follow **Step 5** from Method 1 above.

---

## Pro Tips
*   **Personal URL:** If you name your repository exactly `yourusername.github.io`, your website will be available at `https://yourusername.github.io/` instead of having the repository name at the end.
*   **Custom Domains:** You can add a custom domain (like `www.yourname.com`) in the **Settings > Pages** section.
*   **Automatic Updates:** Every time you `git push` new changes to your `main` branch, GitHub will automatically rebuild and update your live site.
