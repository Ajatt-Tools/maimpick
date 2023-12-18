# Maimpick

> https://tatsumoto.neocities.org/blog/mining-from-manga.html

[![Chat](https://img.shields.io/badge/chat-join-green)](https://tatsumoto-ren.github.io/blog/join-our-community.html)
![GitHub](https://img.shields.io/github/license/Ajatt-Tools/maimpick)

A simple program to create manga cards in real-time.
Maimpick allows you to capture screenshots and perform various actions with them,
such as copying to the clipboard,
saving to a file,
or integrating with Anki.

[demonstration](https://www.youtube.com/watch?v=VkqkpDxF78Y)

## Prerequisites

Maim Pick requires the following dependencies to be installed:

- `maim`: A screenshot utility.
- `dmenu`: A dynamic menu for selecting options.
- `xdotool`: A command-line tool for automation.
- `xclip`: A command-line interface to X selections.
- `cwebp`: A tool for converting images.

## Usage

Simply run the `maimpick` script with the desired command as the first argument.
If no arguments are provided, `maimpick` will ask you.
The available commands are:

- `selected area`: Capture a screenshot of a selected area save it to disk.
- `selected area ⇒ clipboard`: Capture a screenshot of a selected area and copy it to the clipboard.
- `selected area ⇒ gimp`: Capture a screenshot of a selected area and open it with GIMP.
- `selected area ⇒ Anki`: Capture a screenshot of a selected area and add it to the last Anki card.
- `selected ⇒ Tesseract OCR`: Capture a screenshot of a selected area and perform OCR using maimocr.
- `current window`: Capture a screenshot of the current window and save it to disk.
- `current window ⇒ clipboard`: Capture a screenshot of the current window and copy it to the clipboard.
- `full screen`: Capture a screenshot of the entire screen and save it to disk.
- `full screen ⇒ clipboard`: Capture a screenshot of the entire screen and copy it to the clipboard.

## Tips
Create a keybinding for `maimpick area-Anki` in your WM to create a card of the current manga on the screen.
<br></br>i3wm example:
 ```
 bindsym Mod4+p exec --no-startup-id maimpick area-Anki
 ```


## Configuration

Maim Pick supports the following environment variables for configuration:

- `MAIMPICK_ANKI_FIELD`: The name of the Anki field to store the screenshots (default: `Image`).
- `MAIM_SCREENSHOTS`: The directory to store the captured screenshots (default: `$HOME/Pictures/Screenshots`).
