# Brute Force PIN Tester

This script is a simple Python utility to brute force a 4-digit PIN on a server by making HTTP requests. It iterates through all possible PIN combinations (0000 to 9999) and sends them to a specified server endpoint. If the server returns a successful response with a flag, the script stops and displays the correct PIN and flag.

## Features
- Iterates through all 4-digit PINs (0000-9999).
- Sends HTTP GET requests to a server endpoint.
- Detects success based on server response.

## Requirements

This script requires:

- Python 3.7 or higher.
- The `requests` library.

To install the `requests` library, run:

```bash
pip install requests
```

## Usage

1. **Set the Target Server Details**:
   Update the following variables in the script with your server's IP and port:
   ```python
   ip = "127.0.0.1"  # Change this to your instance IP address
   port = 1234       # Change this to your instance port number
   ```

2. **Run the Script**:
   Execute the script using Python:
   ```bash
   python brute_force_pin.py
   ```

3. **Monitor the Output**:
   The script will attempt all PIN combinations and display the following if successful:
   - The correct PIN.
   - The flag returned by the server.

## Example

For a server running on `192.168.1.100` at port `8080`, update the script as follows:

```python
ip = "192.168.1.100"
port = 8080
```

Run the script:

```bash
python brute_force_pin.py
```

Output:
```text
Attempted PIN: 0000
Attempted PIN: 0001
...
Attempted PIN: 0423
Correct PIN found: 0423
Flag: FLAG{example_flag}
```

## Notes

- **Server Response**: The server must return a JSON response containing the key `flag` on successful PIN entry.
- **Security**: Use this script only in a legal and ethical manner. Ensure you have explicit permission to test the target server.

## Disclaimer

This script is intended for educational purposes and authorized testing only. Unauthorized use of this tool is illegal and unethical. The author assumes no responsibility for misuse or damages caused by this script.
