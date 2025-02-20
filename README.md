# AVL Tree For CSV Database

This is a C++ project of an AVL tree for managing CSV files. It reads information from a CSV file and stores it in a self-balancing AVL tree. In this example database it uses stocks. You can wiew a stock's name or price by its symbol, insert new stock entries, and display all stock data. 

The program demonstrates the AVL tree functionality by inserting and traversing random integer values. A self-balancing binary search tree makes sure that insertion, search, and traversal operations remain efficient even as the dataset grows. A dedicated CSV parsing function (`readStocksCSV`) reads data from a CSV file (e.g., `stocks.csv`). The CSV format can be easily extended to include additional fields such as market capitalization and trading volume.

## Example Output
```
Menu Options:
a) Display a stock's name given its symbol
b) Display a stock's price given its symbol
c) Insert a new stock
d) Display all stocks
e) Quit
Enter your choice: a

Enter stock symbol: AAPL
Stock name: Apple Inc.
```

## File Structure

- **main.cpp:**  
  Contains the main program logic, including reading the CSV file, testing the AVL tree with integers, and the interactive menu for stock operations.
- **AVLTree.h:**  
  Implements the AVL tree data structure with functions for insertion, traversals (inorder, preorder, postorder), and search.
- **node.h:**  
  Defines the `Node` struct used by the AVL tree, including fields for the stored value, height, and pointers to left/right children.
- **stock.h / stock.cpp:**  
  Define the `Stock` class and its member functions, along with overloaded comparison operators.
- **Makefile.txt:**  
  Provides build instructions to compile the project.
- **stocks.csv:**  
  Example CSV file containing stock data.

## Build Instructions (Visual Studio Code)

1. Make sure you have Microsoft's C/C++ extension installed
2. Install the compiler that Microsoft provides (MacOS has a native C++ compiler)
3. Install the Makefile Tools extension
4. Open the Makefile on the sidebar
5. Set the build and launch target to main.exe
6. Set the configuration to Deafult
7. Click Run
