# TempMails 📧🔒

**TempMails** is a Python tool that allows you to generate and manage temporary email addresses using Tor and proxies. The tool supports various functionalities and is designed to be run from the terminal.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Features 🚀

- Generate temporary email addresses
- Check email inbox for new messages
- Support for Tor and proxies
- Save emails to a file or CSV
- Customizable user-agent and HTTP headers

## Requirements 📦

- Python 3.6 or higher
- Tor (for routing through Tor network)
- Dependencies listed in `requirements.txt`

## Installation 🛠️

### 1. Clone the Repository

```bash
git clone https://github.com/lalaio1/TempMails.git
cd TempMails
```

### 2. Install Dependencies

Ensure you have Python 3 and `pip` installed. Then, install the required Python packages:

```bash
pip install -r requirements.txt
```

### 3. Install Tor

#### On Linux (Debian/Ubuntu-based)

```bash
sudo apt update
sudo apt install tor
```

#### On macOS

Install Tor using Homebrew:

```bash
brew install tor
```

#### On Windows

Download and install Tor from the [official Tor Project website](https://www.torproject.org/download/).

## Configuration ⚙️

### Tor Setup

**Ensure Tor is installed and running**. The default configuration uses the standard Tor port (9050) and control port (9051). Adjust the configuration if you have customized ports.

#### Start Tor Service

**On Linux/macOS:**

```bash
sudo service tor start
```

**On Windows:**

Launch the Tor service from the Tor Browser or from the Tor installation directory.

### Configuration File

The script uses command-line arguments for configuration. You can customize the script's behavior using these arguments:

- `-d`, `--domain`: Specify a domain for the email.
- `-ci`, `--check_interval`: Set the interval (in seconds) for checking the inbox.
- `-o`, `--output`: Specify the output file name for saving emails.
- `-b`, `--no-box`: Show only email headers.
- `-a`, `--assunto`: Show only email subjects.
- `-id`, `--only-id`: Show only email IDs.
- `-nr`, `--no-router`: Skip Tor route change.
- `-ag`, `--agent`: Set a custom User-Agent.
- `-p`, `--proxy`: Set a custom proxy.
- `-tport`, `--tor-port`: Specify the Tor control port.
- `-tpwd`, `--tor-password`: Set the Tor control port password.
- `-ch`, `--custom-headers`: Provide custom HTTP headers in `key1=value1;key2=value2` format.
- `-ici`, `--initial-check-interval`: Set an initial delay before starting the check.
- `-le`, `--log-errors`: Enable error logging.
- `-st`, `--storage-type`: Specify storage type (`file` or `csv`).

## Usage 🏃‍♂️

Run the script using the following command:

```bash
python3 tempmails.py [options]
```

**Example:**

```bash
python3 tempmails.py -d example.com -ci 1 -o emails.txt -b -le -st csv
```

This example will:
- Use `example.com` as the domain
- Check the inbox every 1 second
- Save output to `emails.txt`
- Only show email headers
- Log errors to `error_log.txt`
- Save emails in CSV format

## Screenshots 📸

![Imagem.pgn](https://github.com/lalaio1/TempMails/blob/main/Imagem.png)

## Troubleshooting 🛠️

- **Tor Not Running:** Ensure Tor is installed and running. Check if the Tor service is active.
- **Proxy Issues:** Verify proxy settings and ensure the proxy server is reachable.
- **Dependencies:** Ensure all dependencies are installed. Check `requirements.txt` for required packages.

For additional help, refer to the [Issues page](https://github.com/lalaio1/TempMails/issues) on GitHub.

## License 📜

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
