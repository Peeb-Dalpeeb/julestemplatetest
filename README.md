# Student Application Interface Template

This is a template for the Student Application Interface.

## Getting Started

### Prerequisites

- Node.js (Latest LTS version recommended)
- npm (comes with Node.js)

### Installation

1.  Clone the repository or download the source code.
2.  Open your terminal and navigate to the project directory.
3.  Install dependencies:

    ```bash
    npm install
    ```

### Development

To start the development server:

```bash
npm run dev
```

### Build

To build the project for production:

```bash
npm run build
```

## Troubleshooting Installation

If you encounter errors during `npm install` such as:

- `npm warn tar TAR_BAD_ARCHIVE: Unrecognized archive format`
- `npm warn tar TAR_ENTRY_INVALID`
- `npm warn tarball cached data for ... seems to be corrupted`
- `TAR_ENTRY_ERROR`

These errors often indicate a corrupted npm cache or file locking issues, which can happen if the project is located in a cloud-synced folder (like OneDrive, Dropbox, or Google Drive) or if there was a network interruption.

### Solution Steps

Follow these steps to resolve the issue:

1.  **Move Project Folder**: Ensure your project folder is **NOT** inside a cloud-synced directory (e.g., OneDrive, Dropbox). Move it to a local directory like `C:\Projects\` or `~/Projects/`.

2.  **Clean npm Cache**: Force clean your npm cache to remove any corrupted files.
    ```bash
    npm cache clean --force
    ```

3.  **Delete Existing Modules**: Remove the existing `node_modules` folder and `package-lock.json` file to start fresh.
    - **Windows (Command Prompt):**
        ```cmd
        rmdir /s /q node_modules
        del package-lock.json
        ```
    - **Mac/Linux/Git Bash:**
        ```bash
        rm -rf node_modules package-lock.json
        ```

4.  **Re-install Dependencies**: Run the install command again.
    ```bash
    npm install
    ```

If the problem persists, ensure you are using the latest stable version of Node.js and npm.
