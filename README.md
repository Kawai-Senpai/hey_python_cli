# Hey Python

An AI-powered CLI assistant that helps with coding and system tasks using OpenAI's language models.

## Installation

```bash
pip install hey-python
```

## API Key Configuration

Hey CLI securely manages your OpenAI API key:

1. **First-time use**: You'll be prompted to enter your API key
2. **Secure storage options**:
   - **System keyring**: Uses your OS's secure credential storage (preferred)
     - Windows: Windows Credential Locker
     - macOS: Keychain
     - Linux: Secret Service API (GNOME Keyring/KDE Wallet)
   - **Fallback storage**: When system keyring is unavailable (Docker, minimal servers)
     - Uses file-based encrypted storage in `~/.hey_config/`
     - Machine-specific encryption (keys can't be transferred between systems)

3. **Removing a saved key**: Use the `--remove-api-key` option to delete your stored key
   ```bash
   hey --remove-api-key
   ```

### Manual API Key Setup

You can also set your API key using:

- **Environment variable**: `export OPENAI_API_KEY=your_key_here`
- **.env file**: Create a `.env` file in your working directory:
  ```
  OPENAI_API_KEY=your_api_key_here
  ```

## Usage

After installation, use the `hey` command followed by your question or instruction:

```bash
# Ask for help
hey help me understand how to use this tool

# Create a simple script
hey create a hello world script in python

# Get system information
hey what files do I have in this directory?

# Create files for a project
hey create a new React component for a login form
```

## Features

- **Secure API Key Management**: Keys stored in system's secure credential manager
- **Intelligent File Operations**: Create, edit, delete, and rename files
- **Directory Management**: Create and remove directories
- **Command Execution**: Run shell commands directly
- **Context-Aware**: Maintains conversation history for better assistance
- **Syntax Highlighting**: Shows diffs and code with proper formatting
- **Streaming Responses**: See AI responses in real-time

## Examples

```bash
# Create a Python script
hey create a script that downloads images from a URL

# Fix errors in code
hey debug this file and fix the bugs: app.js

# Get explanations
hey explain how the authentication works in this project

# Execute commands
hey show me the disk usage in this directory
```

## License

MIT License - See LICENSE.rst for details.
