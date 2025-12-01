# **GIF Maker — Simple Python Script**

A small command-line utility to create an animated GIF from a list of image files using `imageio`.

---

## **Features**

* Interactive prompt to add image filenames
* Configurable output filename and frame duration
* Saves an animated GIF that loops indefinitely

---

## **Requirements**

* Python 3.7+
* `imageio` library

Install dependency:

```bash
pip install imageio
```

---

## **Usage**

Run the script:

```bash
python gif_maker.py
```

The script will prompt you to enter image filenames (one per line). Press Enter without typing anything to finish the list.

Next it asks for an output GIF name (default: `Output.gif`) and the frame duration in milliseconds (default: `500`).

Example interactive session:

```
Image file: img1.jpg
File appended
Image file: img2.png
File appended
Image file:            <-- press Enter to finish
Enter the output Gif name(default:Output.gif): my_animation
Enter frame duration in milliseconds (default: 500): 400
```

The created file will be written to the current working directory.

---

## **Notes & Tips**

* Provide at least two images — the script requires a minimum of two frames to create a GIF.
* Frame duration is in **milliseconds** (e.g. `1000` = 1 second per frame).
* Accepted input formats depend on `imageio` and Pillow support (common: JPG, PNG).

---

## **Troubleshooting**

* `file not found`: Make sure you enter the correct relative or absolute file path.
* GIF not created: Check that at least two images were successfully loaded.
* If `imageio` raises format errors, try converting images to a common format (e.g., PNG).

---

## **Possible Improvements**

* Add command-line arguments (using `argparse`) to skip the interactive prompts.
* Validate image file extensions and order before processing.
* Provide an option to resize images to a common dimension.
* Fix minor input-handling bugs in the current script (e.g. `str.lower()` call and retry logic).

---

## **License**

MIT — free to use and modify.
