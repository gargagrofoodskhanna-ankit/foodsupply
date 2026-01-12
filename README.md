# Company Test Results Comparison Tool

A web application for comparing Excel files containing company test results by license number.

## Features

- 📊 Compare two Excel files (New Report vs Old Report) with company test results
- 🔍 Automatic column detection for License Number, Company Name, QMS Passed, and QMS Rejected
- 📈 Visual comparison with color-coded differences
- 📋 Detailed results table showing:
  - Company names and license numbers
  - Passed/Rejected counts for each report
  - Difference calculations (Old Report - New Report)
  - Companies only in one report vs both reports

## How to Use

1. Open `company-test-analysis.html` in your web browser
2. Upload **New Report** (Excel file 1)
3. Upload **Old Report** (Excel file 2)
4. Map columns (or use auto-detection)
5. Click "Compare Files" to see results
6. View summary statistics and detailed comparison table

## Excel File Format

Your Excel files should contain columns for:
- **License Number** (required) - Unique identifier for each company
- **Company Name** (optional) - Name of the company
- **QMS Passed** (optional but recommended) - Number of tests passed
- **QMS Rejected** (optional but recommended) - Number of tests rejected

## Technology

- Pure HTML, CSS, and JavaScript
- Uses SheetJS (xlsx.js) library for Excel file reading
- Works entirely in the browser (no server required)
- No data leaves your computer - all processing is done locally

## Quick Start

### Option 1: Direct Browser
Simply double-click `company-test-analysis.html` to open it in your default browser.

### Option 2: Chrome (Windows)
Double-click `run-application.bat` to open the application in Chrome.

### Option 3: Local Server
If you prefer using a local server:
```bash
# Using Python
python -m http.server 3000

# Then open http://localhost:3000/company-test-analysis.html
```

## Comparison Logic

- **License Number** is used as the unique identifier for matching companies
- Results are aggregated by license number (sums passed/rejected counts)
- Differences are calculated as: Old Report - New Report
- Positive differences indicate increases in Old Report
- Negative differences indicate decreases in Old Report

## Results Display

### Summary Statistics
- Total Companies found
- Companies in Both Reports
- Companies Only in New Report
- Companies Only in Old Report
- Companies With Differences

### Detailed Table
- Side-by-side comparison of each company
- Color-coded cells:
  - **Green**: Same values
  - **Yellow**: Different values
  - **Red/Pink**: Missing in one report

## Privacy & Security

- All processing happens in your browser
- No data is sent to any server
- Files are read locally only
- No tracking or analytics

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Edge
- Safari
- Any modern browser with JavaScript enabled

## License

Free to use and modify.

## Support

For issues or questions, please check the application's built-in instructions or create an issue in the repository.
