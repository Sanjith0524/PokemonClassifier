# Dominant Color Extraction for Pokémon Images

## Overview
This project extracts the dominant color from Pokémon images using K-Means clustering. The extracted dominant color is then converted to a human-readable color name and added to a Pokémon dataset.

## Features
- Uses K-Means clustering to identify the dominant colors in an image.
- Converts the extracted colors from RGB to named colors.
- Processes a dataset of Pokémon images and updates the CSV file with the detected colors.
- Supports visualization of dominant color extraction.

## Installation
To use this project, ensure you have the following dependencies installed:

```bash
pip install pandas numpy matplotlib scikit-learn pillow webcolors
```

## Usage
### 1. Running the Color Extraction
Ensure you have a CSV file containing Pokémon data and an image folder with Pokémon images.

Modify the script to point to your dataset:
```python
csv_file = "path/to/PokemonData.csv"
img_folder = "path/to/PokemonImages"
```
Then, run the script:
```python
result_df = process_img(
    file_name=csv_file,
    img_folder=img_folder,
    ncol=3,
    show_samples=1
)
```

## Output
- The updated Pokémon dataset will be saved as `PokemonData_with_colors.csv` with an added "Colour" column.
- The script will print detected colors for a sample of images.

## Notes
- The hex values of colors are accurately extracted, but named colors might not always match human perception perfectly.
- Ensure images are named correctly to match Pokémon numbers in the dataset.

## License
This project is for educational purposes. Modify and use as needed :) !
