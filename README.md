# Email Sender

Email Sender is a Python-based application designed to send emails using credentials specified in a `.env` file.

## Features

- Send emails through an SMTP server.
- Configure email credentials via a `.env` file.

## Prerequisites

- Python 3.x
- `python-dotenv`

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/devluxor/email-sender.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd email-sender
   ```

3. **Create a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install `python-dotenv`:**

   ```bash
   pip install python-dotenv
   ```

5. **Create a `.env` file in the project root with the following variables:**

   ```env
   EMAIL=your_email@example.com
   PASSWORD=your_password
   HOST=smtp.example.com
   PORT=587
   ```

   Replace the placeholder values with your actual email server credentials. Note that the values will depend on your email server provider.

## Usage

1. **Run the email sender script:**

   ```bash
   python send_email.py
   ```

   The script will read the credentials from the `.env` file and send an email as configured within the script.

## Configuration

- **EMAIL:** Your email address.
- **PASSWORD:** Your email account password.
- **HOST:** The SMTP server address (e.g., `smtp.gmail.com`).
- **PORT:** The SMTP server port (e.g., `587` for TLS or `465` for SSL).

Ensure that your email provider allows SMTP access and that the credentials are correct.

## Troubleshooting

- **Environment Variables Not Loading:**

  If the email credentials are not being read correctly from the `.env` file, ensure that the file is properly formatted and that there are no conflicting environment variables set in your system.

- **Authentication Issues:**

  Make sure your email server supports SMTP access and that the username and password provided are correct. Some services may require you to enable "less secure app access" or generate an app-specific password.

## License

This project is licensed under the MIT License.

## Acknowledgments

This project utilizes the `python-dotenv` package for managing environment variables.
