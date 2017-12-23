# line-stickerbot
A Telegram bot for downloading Line stickers. It takes a URL sent to the bot from a user, downloads the page, and finds the relevant image links. Then, it downloads the images, rescales them to the appropriate size, and sends them all back to the user in a .zip archive.

## How do I use it?
Add [@line_stickerbot](http://telegram.me/line_stickerbot) on Telegram.

Or, if you prefer to run it yourself, replace `<token>` in `main.py` with the token the Botfather gave you, and run `main.py`.

## Dependencies

This bot uses python3. Use linux because Windows is having issues with wand. Also, in the root repo directory create a new directory called "downloads". You should also `touch updatefile`, and put a random integer (just put 1) inside it. In `main.py`, under the `resize` function, select the algorithm you want according to the documentation for wand/imagemagick.

Run `pip install` if you don't have them.

* `bs4` for parsing the HTML of the sticker page.
* `cssutils` for getting the url of the sticker image.
* `wand` for resizing the downloaded images.
* `pyopenssl` for OpenSSL.
