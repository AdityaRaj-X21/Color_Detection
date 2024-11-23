# Color Detection in Images

## Overview

This project is a **Color Detection** application built using Python and OpenCV. The program allows users to click on any point in an image, and it detects the color at that point. The application displays the name of the color along with its RGB values.

## Features

- Detects colors by reading the pixel values (R, G, B) from an image.
- Matches the detected color with the most similar color name from a predefined dataset.
- Displays the color name and its RGB values on the image.
- Supports mouse double-click events to interact with the image.

## How It Works

1. **Input Image**: The application reads an image using OpenCV.
2. **Color Data**: A CSV file (`colors.csv`) is loaded containing the names and RGB values of various colors.
3. **Mouse Interaction**: When the user double-clicks on a point in the image, the application:
   - Retrieves the RGB values at that point.
   - Finds the closest matching color name using the Euclidean distance in RGB space.
4. **Output**: Displays a filled rectangle with the detected color, its name, and RGB values on the image.

## Prerequisites

Ensure you have the following installed:
- Python 3.x
- OpenCV
- pandas

Install required libraries using pip:

```bash
pip install opencv-python pandas
```

## Files Included

- `colorpic.jpg`: The input image for color detection.
- `colors.csv`: A dataset containing color names, their RGB values, and HEX codes.
- `color_detection.py`: The Python script to run the application.

## Usage

1. Place your input image (`colorpic.jpg`) in the same directory as the script.
2. Ensure the `colors.csv` file is in the same directory.
3. Run the script:

   ```bash
   python color_detection.py
   ```

4. The image will open in a new window. Double-click on any point in the image to detect the color at that point.
5. Press the **`Esc` key** to exit the application.

## Functions

### `get_color_name(R, G, B)`
- Calculates the closest color name from the dataset using the RGB values.

### `draw_function(event, x, y, flags, params)`
- A callback function to handle mouse double-click events.

### `getColorName(r, g, b)`
- Placeholder function for any additional custom logic.

## Example Output

When a user double-clicks on a point in the image:
- A rectangle is displayed with the detected color.
- The color name and its RGB values are displayed as text above the rectangle.

### Sample Output:
If the user clicks on a red area:
- Rectangle color: Red
- Text: `Red R=255 G=0 B=0`

## Notes

- The application uses a basic matching algorithm to find the nearest color. You can enhance this by using more sophisticated algorithms or machine learning models.
- The text color switches to black for light colors to ensure readability.

---

Enjoy detecting colors in your images! 😊
