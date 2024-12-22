# Map Coloring Constraint Satisfaction Problem

This repository contains an implementation of the Map Coloring Constraint Satisfaction Problem (CSP) in Python. The program uses a backtracking algorithm to assign colors to regions on a map while ensuring that no adjacent regions share the same color. Additionally, this project includes utility functions for constraints and visualizations.

## Features

- **Constraint Satisfaction Problem**: Solves the map coloring problem using a backtracking algorithm.
- **Visualization**: Utilities to display solutions visually, including a chessboard display function.
- **Extensibility**: Easily adaptable for other CSP problems with similar constraints.

## Project Structure

- `main.py`: Core implementation of the backtracking algorithm for solving the CSP.
- `util.py`: Contains utility functions for handling constraints and displaying the board.

## Prerequisites

Ensure you have the following installed:

- Python 3.6+
- Required Python packages (see below)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/map-coloring-csp.git
   cd map-coloring-csp
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the main program:
   ```bash
   python main.py
   ```

2. Modify the `main.py` file to adjust the map regions, colors, or constraints.

## Utility Functions

### Constraint Function

The `constraint` function in `util.py` helps augment the `sympy.Function` class by attaching symbolic expressions for constraints.

#### Example:
```python
from sympy import symbols
from util import constraint

x, y = symbols('x y')
expr = (x + y > 5)
custom_constraint = constraint('ExampleConstraint', expr)
```

### Display Board Function

The `displayBoard` function visualizes a chessboard with specific placements.

#### Example:
```python
from util import displayBoard

locations = [(0, 0), (1, 1)]  # Coordinates of queens
shape = 3  # 3x3 board
displayBoard(locations, shape)
```

## Dependencies

The project requires the following Python libraries:

- `matplotlib`
- `numpy`
- `sympy`

## File Descriptions

### `util.py`

#### Functions:

1. `constraint(name, expr)`:
   - Augments the `sympy.Function` class.
   - Attaches a symbolic expression and makes the function evaluatable.

2. `displayBoard(locations, shape)`:
   - Draws a chessboard with queens placed at specified positions.
   - Parameters:
     - `locations`: List of `(row, column)` tuples for placement.
     - `shape`: Dimensions of the board (e.g., `shape=3` for a 3x3 board).

## Example Output

Here is an example of a Map Coloring CSP output:
![image](https://github.com/user-attachments/assets/afde62cb-df0d-4f4f-8d43-6e075a09842f)

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

Feel free to contribute or raise issues for improvements. Happy coding!
