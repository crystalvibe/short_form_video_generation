# Short Form Video Generator (Telegram Bot)

This project is a Jupyter Notebook based Telegram bot that creates short-form videos.

The main code is in:
- `video_genereator.ipynb`

## What this project does

- Accepts user input through Telegram.
- Generates short video content.
- Uses Python libraries like `moviepy`, `pydub`, `yt-dlp`, and `python-telegram-bot`.

## Requirements

- Python 3.10+ (recommended)
- Jupyter Notebook or Google Colab
- A Telegram Bot Token (from [@BotFather](https://t.me/BotFather))

## Install dependencies

Run this in a notebook cell or terminal:

```bash
pip install moviepy==1.0.3 python-telegram-bot pydub yt-dlp librosa scipy numpy requests fonttools nest_asyncio beautifulsoup4 httpx selenium
```

## Telegram token setup (important)

You need to add your own Telegram bot token.

In `video_genereator.ipynb`, near the bot startup code, you will find:

```python
token = 'YOUR_TELEGRAM_BOT_TOKEN'
```

Replace it with your token from BotFather.

## Recommended secure way (better than hardcoding)

Instead of writing the token directly in code, use an environment variable:

```python
import os
token = os.getenv("TELEGRAM_BOT_TOKEN")
if not token:
    raise ValueError("Please set TELEGRAM_BOT_TOKEN")
```

Then set the variable before running:

- Windows PowerShell:
```powershell
$env:TELEGRAM_BOT_TOKEN="your_real_bot_token_here"
```

- Linux/macOS:
```bash
export TELEGRAM_BOT_TOKEN="your_real_bot_token_here"
```

## How to run

1. Open `video_genereator.ipynb`.
2. Run cells from top to bottom.
3. Make sure your Telegram token is configured.
4. Run the final bot startup cell.
5. Open Telegram and message your bot to test.

## Quick checks if it is not working

- Token is valid and from the correct bot.
- Required packages are installed without errors.
- Internet is available.
- Notebook cells were executed in order.
- No error in the last startup cell output.

## Notes

- Do not commit real bot tokens to GitHub.
- If a token was exposed, regenerate it in BotFather immediately.
