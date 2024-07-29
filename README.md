# Malakai-Bot

Malakai-Bot is a WhatsApp bot built using the WPPConnect library. It listens for specific messages, processes them, and responds with appropriate actions such as sending text messages, images, PDFs, and more.

## Features

- Converts Arabic numerals in messages to English numerals.
- Normalizes keys in incoming messages for easier processing.
- Responds to specific commands such as `!ping` and `!ping reply`.
- Sends various types of files based on the content of the received message.
- Logs all received messages and errors, and sends these logs to specified recipients.

## Setup

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/malaki-bot.git
    cd malaki-bot
    ```

2. **Install dependencies:**
    ```bash
    npm install
    ```

3. **Create and configure `db.json`:**
    - Create a `db.json` file in the root directory.
    - Add the file mappings and content as per your requirements.
    ```json
    {
      "exampleKey": {
        "path": "files/example.pdf",
        "caption": "Example PDF"
      }
    }
    ```

4. **Run the bot:**
    ```bash
    node index.js
    ```

## Usage

1. **Send a message to the bot:**
    - The bot listens for messages and normalizes the text. For example, it will convert Arabic numerals to English numerals and remove spaces.

2. **Respond to specific commands:**
    - `!ping`: The bot responds with "pong".
    - `!ping reply`: The bot replies to the message with "pong".

3. **Send files:**
    - The bot checks the normalized message against the keys in `db.json` and sends the corresponding file or text.

## Logging

- The bot logs all received messages and errors.
- Logs are sent to the specified recipients in the `logRecipients` array.

## Example `db.json`

```json
{
  "hello": {
    "text": "Hello, world!",
    "caption": "A simple greeting"
  },
  "example": {
    "path": "files/example.pdf",
    "caption": "Example PDF"
  }
}
```

## Example Messages

- Sending "hello" will make the bot send the text "Hello, world!" with the caption "A simple greeting".
- Sending "example" will make the bot send the `example.pdf` file with the caption "Example PDF".

## Contributing

Feel free to contribute to this project by submitting issues or pull requests.

## License

This project is licensed under the MIT License.
