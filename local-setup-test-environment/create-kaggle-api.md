### 🔑 How to Create and Use Kaggle API Key

To enable programmatic access to Kaggle datasets using the Kaggle API, follow these steps:

#### 📥 1. Generate Your Kaggle API Token

1.  Visit <https://www.kaggle.com/settings>
2.  Scroll to the "API" section.
3.  Click "Create New API Token".
4.  A file named `kaggle.json` will be downloaded automatically. This contains your username and API key.

#### 📁 2. Store the API Key Securely

Place the `kaggle.json` file in the following directory:

*   **Windows:**
    ```
    C:\Users\<YourUsername>\.kaggle\kaggle.json
    ```
*   **macOS/Linux:**
    ```
    ~/.kaggle/kaggle.json
    ```

📌 **Note:** If the `.kaggle` folder does not exist, create it manually.

#### ✅ 3. Verify Installation and Access

1.  Install the Kaggle CLI if not already present:
    ```bash
    pip install kaggle
    ```
2.  Test the API by listing datasets:
    ```bash
    kaggle datasets list
    ```

---

### 🔒 Important

*   **Never commit your `kaggle.json` to version control (e.g., GitHub).**
*   Add `.kaggle/` or `kaggle.json` to your `.gitignore` file.
