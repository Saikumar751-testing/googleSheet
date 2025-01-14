# React Spreadsheet Clone

A modern web-based spreadsheet application built with React, inspired by Google Sheets. This project implements core spreadsheet functionality with a focus on mathematical operations, data quality functions, and a responsive user interface.

![Spreadsheet Demo](http://127.0.0.1:5500/app.html)

## 🚀 Features

### Core Functionality
- Interactive spreadsheet grid (50 rows × 26 columns)
- Cell selection and editing
- Formula bar with real-time updates
- Cell reference support (e.g., A1, B2)
- Formula evaluation engine

### Mathematical Functions
- SUM(): Calculate the sum of a range
- AVERAGE(): Calculate the average of a range
- MAX(): Find the maximum value in a range
- MIN(): Find the minimum value in a range
- COUNT(): Count numerical values in a range

### Data Quality Functions
- TRIM(): Remove leading/trailing whitespace
- UPPER(): Convert text to uppercase
- LOWER(): Convert text to lowercase

### UI Features
- Responsive grid layout
- Visual feedback for selected cells
- Column and row headers
- Basic formatting toolbar

## 🛠 Technical Stack

### Core Technologies
- *React*: Frontend framework for building the user interface
- *Tailwind CSS*: Utility-first CSS framework for styling
- *shadcn/ui*: React components built on top of Tailwind
- *Lucide React*: Icon library

### Data Structure
The application uses a two-dimensional array as its primary data structure for the spreadsheet grid. This choice was made for:
- Direct cell access using row and column indices
- Efficient updates and renders
- Simple serialization for future save/load functionality

### State Management
- React's useState for managing cell data and selections
- useRef for maintaining cell references and handling DOM interactions

### Formula Evaluation
- Custom formula parser using regular expressions
- Cell dependency tracking for formula updates
- Support for range references (e.g., A1:B3)

## 🏗 Architecture

### Component Structure

SpreadsheetApp
├── Toolbar
│   ├── Font Selection
│   ├── Font Size Selection
│   └── Format Controls
├── Formula Bar
└── Grid
    ├── Column Headers
    ├── Row Headers
    └── Cell Grid


### Data Flow
1. User interacts with a cell
2. Cell selection state updates
3. Formula bar updates to reflect cell content
4. On cell edit:
   - Data array updates
   - Dependent cells recalculate
   - UI refreshes to show new values

## 🚀 Getting Started

### Prerequisites
- Node.js 16.x or higher
- npm or yarn

### Installation
bash
# Clone the repository
git clone https://github.com/yourusername/react-spreadsheet-clone.git

# Navigate to project directory
cd react-spreadsheet-clone

# Install dependencies
npm install

# Start development server
npm run dev


### Usage
1. Open the application in your browser
2. Click any cell to select it
3. Enter values or formulas (starting with =)
4. Use the formula bar for longer entries
5. Reference other cells in formulas using their coordinates (e.g., =SUM(A1:A5))

## 🔜 Future Enhancements

### Planned Features
- Save/Load functionality
- Data validation
- More mathematical and statistical functions
- Cell formatting options
- Data visualization (charts)
- Undo/Redo functionality
- Collaborative editing
- Custom formula support

### Performance Optimizations
- Virtual scrolling for large datasets
- Memoization of formula results
- Batch updates for multiple cell changes

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Inspired by Google Sheets
- Built with shadcn/ui components
- Icons from Lucide React
