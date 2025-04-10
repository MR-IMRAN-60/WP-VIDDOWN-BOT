![Imran Bot Logo](images/imran-bot-logo.png)



# Imran Bot - WhatsApp Downloader Bot

A WhatsApp bot that can download videos from various platforms, interact with users, and respond with random emojis and messages. This bot uses WhatsApp Web's Baileys library to connect and handle requests.

## Features

- QR code-based WhatsApp login.
- Auto-respond to messages with random emojis.
- Responds to the command `ping` with `Pong!`.
- Downloads videos from URLs sent by the user and sends them back.
- Uses SimSimi API to respond with predefined messages.
- Customizable to include more commands or features.

## Requirements

- Node.js (v14+ recommended)
- npm (Node Package Manager)
- WhatsApp account

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/imran-bot.git
    cd imran-bot
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Create a `session` folder in the root directory for storing authentication credentials.

4. Ensure you have the `nayan-videos-downloader` and other required dependencies in your `package.json` file.

5. Customize the `OWNER_NUMBER` variable with your WhatsApp number (in E.164 format without `+`).

## Usage

1. Run the bot:
    ```bash
    node index.js
    ```

2. The bot will generate a QR code in the terminal. Scan it with your WhatsApp mobile app.

3. Once logged in, the bot will listen for incoming messages and respond accordingly.

4. Open the web app in your browser:
    - Navigate to `http://localhost:3000`
    - You will see a basic interface where the bot will provide information about its status.

## Commands

- **ping**: Responds with `Pong!`.
- **URLs (Video URLs)**: If a video URL is sent, the bot will attempt to download and send the video back.

## Files Structure

- `index.js`: Main bot logic.
- `public/`: Contains the front-end files (HTML, CSS, JS).
- `temp/`: Temporary directory to store downloaded videos.
- `session/`: Directory to store session files for WhatsApp Web.

## Known Issues

- Some video download URLs might not be supported.
- The bot relies on the SimSimi API, which may sometimes be unavailable or return errors.

## License

This project is open-source and free to use. Feel free to contribute, report issues, or fork this repository.
