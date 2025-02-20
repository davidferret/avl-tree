# AVL Tree For CSV Database

This is a C++ project of an AVL tree for managing CSV files. It reads information from a CSV file and stores it in a self-balancing AVL tree. For the example database, it uses stocks. You can interact with the stock database via a command-line menu that allows you to:
- View a stock's name or price by its symbol.
- Insert new stock entries.
- Display all stock data.

In addition to stock data management, the program demonstrates the AVL tree functionality by inserting and traversing random integer values.

## Features

- **AVL Tree Implementation:**  
  A self-balancing binary search tree (AVL tree) ensures that insertion, search, and traversal operations remain efficient even as the dataset grows.
- **Stock Data Management:**  
  The `Stock` class stores company name, stock symbol, and stock price. The AVL tree is used to manage and retrieve stock information.
- **CSV File Parsing:**  
  A dedicated CSV parsing function (`readStocksCSV`) reads stock data from a CSV file (e.g., `stocks.csv`). The CSV format can be easily extended to include additional fields such as market capitalization and trading volume.
- **Interactive Menu:**  
  A command-line interface allows users to search for stocks by symbol, insert new stock records, and display all stored stock data.

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
  Example CSV file containing stock data. (If not provided, create one using the sample format below.)

## Requirements

- **C++17 Compiler:**  
  The project requires a compiler that supports C++17.
- **Make:**  
  A Makefile is provided for building the executable.
- **CSV File:**  
  A properly formatted `stocks.csv` file is needed for stock data input.

## Build Instructions

1. **Clone the Repository:**  
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Build the Project:**  
   Use the provided Makefile:
   ```bash
   make
   ```

3. **Run the Executable:**  
   ```bash
   make run
   ```

4. **Clean Build Files:**  
   ```bash
   make clean
   ```

## CSV File Format

The CSV file should be formatted as follows (include a header row):

```csv
CompanyName,StockSymbol,StockPrice,MarketCap,Volume
Apple Inc.,AAPL,150.25,2500000000000,1000000
Microsoft Corp.,MSFT,295.00,2200000000000,2000000
Alphabet Inc.,GOOGL,2800.10,1800000000000,1500000
Amazon.com Inc.,AMZN,3300.55,1700000000000,1200000
Tesla Inc.,TSLA,900.35,800000000000,3000000
...
```

Ensure that `stocks.csv` is placed in the same directory as your executable or update the file path accordingly in your code.

## Usage

When you run the program, you will see a menu with these options:

- **a:** Display a stock's name given its symbol.
- **b:** Display a stock's price given its symbol.
- **c:** Insert a new stock.
- **d:** Display all stocks.
- **e:** Quit the program.

Follow the prompts to search for stocks or insert new entries. The AVL tree ensures efficient data retrieval and maintains a balanced structure even with a large number of records.

## Enhancements and Future Work

- **Deletion Operation:**  
  Implement stock deletion from the AVL tree.
- **Extended Data Handling:**  
  Enhance the `Stock` class to include additional fields (e.g., market cap and volume) and update file parsing accordingly.
- **Improved Parsing:**  
  Consider using robust libraries for CSV or JSON parsing (e.g., using nlohmann/json for JSON support).
- **Graphical User Interface (GUI):**  
  Develop a GUI for enhanced user interaction with the stock database.
- **Batch Insertion for Balance:**  
  For very large datasets, read all data into a vector and build a balanced tree by inserting the middle element first.

## License

This project is open source and available under the MIT License.

## Acknowledgments

- Thanks to the open source community for resources and inspiration on AVL tree implementations.
- Contributions and feedback are welcome.

---

Feel free to customize this README to better fit your project's needs or to include additional instructions and information.
