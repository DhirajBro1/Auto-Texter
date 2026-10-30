# Auto-Spam

Auto-Spam is a terminal-based Python tool that types and sends messages in
WhatsApp using keyboard automation.

> **Disclaimer:** Use this project only for messages that you are authorized to
> send. Do not use it to harass, abuse, or send unsolicited messages.

## Features

- Send one or more user-provided messages repeatedly.
- Send numbered messages, such as `Hello 1`, `Hello 2`, and `Hello 3`.
- Generate messages from random words.
- Generate meaningless messages from random characters.
- Set a delay in seconds between message batches.
- Move the cursor to WhatsApp manually before sending starts.

## Requirements

- Python 3.x
- WhatsApp Web or the WhatsApp desktop application
- A working keyboard and mouse
- Python packages listed in [requirements.txt](./requirements.txt)

## Installation

Clone the repository and install its dependencies:

```bash
git clone https://github.com/dhirajbro1/Auto-Texter.git
cd Auto-Texter
```

### Create and activate a virtual environment

Using a virtual environment keeps this project's packages separate from your
system Python installation.

**Linux/macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**Windows PowerShell:**

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
```

**Windows Command Prompt:**

```bat
py -m venv .venv
.venv\Scripts\activate.bat
```

After activation, install the dependencies:

```bash
pip install -r requirements.txt
```

To leave the virtual environment later, run:

```bash
deactivate
```

If PowerShell blocks activation, allow local scripts for your user and try
again:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## Usage

Start the tool with:

```bash
python auto-spam.py
```

The main menu contains:

```text
[1] User typed message
[2] Auto typed message
[4] Help
[0] Quit
```

### Terminal interface

Auto-Spam displays its interface in the terminal. The startup banner looks
like this:

```text
    _         _             ____
   / \  _   _| |_ ___      / ___| _ __   __ _ _ __ ___
  / _ \| | | | __/ _ \ ____\___ \| '_ \ / _` | '_ ` _ \
 / ___ \ |_| | || (_) |_____|__) | |_) | (_| | | | | | |
/_/   \_\__,_|\__\___/     |____/| .__/ \__,_|_| |_| |_|
                                 |_|
```

The main menu lets you choose user-entered messages, automatically generated
messages, the help screen, or quit:

```text
Choose an option from the following:
[1] User typed message
[2] Auto typed message
[4] Help
[0] Quit
[+] Enter Option ->
```

### User typed message

Choose option `1` to:

1. Enter the messages that should be sent.
2. Enter how many times the complete message list should be repeated.
3. Enter a delay in seconds.
4. Open WhatsApp and place the cursor in the message box.
5. Press Enter or choose `1` when ready.

For example, with these messages:

```text
owo h
owo b
```

and a repeat count of `3`, the tool sends:

```text
owo h
owo b
<delay>
owo h
owo b
<delay>
owo h
owo b
```

The delay is applied only after the complete list of messages has been sent.
Messages in the same list are sent consecutively. A blank delay or `0` sends
the batches without an additional pause.

### Auto typed message

Choose option `2`, then select one of these modes:

```text
[1] Message with counting
[2] Random Message Generator
[3] Meaningless Message Generator
[0] Quit
```

Each mode asks for its message count or message size, followed by the delay
between messages. The tool then gives you 10 seconds to place the cursor in
the WhatsApp message box.

### Stopping or cancelling

- Enter `0` at an available quit prompt to exit.
- Choose `0` at the ready prompt to cancel before sending.
- Keep the WhatsApp message box focused while the tool is running.

## Contributing

Bug reports and improvements are welcome. Please keep changes focused and
update this README when the command-line interface changes.

## License

This project is licensed under the [MIT License](./LICENSE).
