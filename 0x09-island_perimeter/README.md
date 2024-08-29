# Island Perimeter Calculator

This project contains a Python script to calculate the perimeter of an "island" in a grid. An island is represented by `1`s (land) and `0`s (water) in a 2D grid. The perimeter is the number of edges surrounding the land.

## Files

- `island_perimeter.py`: Python script to calculate the perimeter of an island.

## Usage

1. Make sure you have Python installed on your system.
2. Run the script by using the command:

    ```bash
    python island_perimeter.py
    ```

## Example

Given a grid:
The perimeter of the island is `16`.

## Function

The script includes a function `island_perimeter(grid)` that takes a 2D list of integers (grid) and returns an integer representing the perimeter of the island(s).

## How It Works

The function calculates the perimeter by iterating over each cell in the grid. If the cell is land (`1`), it adds 4 to the perimeter. For each adjacent land cell, it subtracts 1 from the perimeter. This way, only the edges not shared with another land cell are counted.

## License

This project is licensed under the MIT License.
