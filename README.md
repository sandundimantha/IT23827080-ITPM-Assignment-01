# ITPM Assignment 1 - Transliteration Testing

This repository contains the Playwright test automation scripts for testing the accuracy of the Singlish-to-Sinhala chat translator.

## Prerequisites
- Python 3.11 or 3.12 installed
- Google Chrome installed

## Installation

1. Clone this repository or extract the project folder.
2. Open a Command Prompt or Terminal in the project root directory.
3. Install the required Python packages by running:
   ```bash
   pip install -U pip
   pip install playwright openpyxl
   ```
4. Install the required Playwright browsers:
   ```bash
   playwright install
   ```

## Running the Tests

To execute the test automation script, run the following command in the terminal from the `IT23827080_Playwright_Project` folder:

```bash
python test_automation.py --excel "IT23827080_Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### What this script does:
1. It reads the test cases from `IT23827080_Assignment 1 - Test cases.xlsx`.
2. It launches a browser using Playwright and navigates to the Chat Translator.
3. It iterates through the 50 identified negative test cases.
4. For each test case, it inputs the Singlish phrase, waits for the result, and extracts the actual output.
5. It compares the actual output with the expected output and records the "Actual Output" and "Status" (PASS/FAIL) directly in the Excel file.

## Expected Results
Since these are negative test cases designed to test the limitations of the transliteration system, the script will record the actual outputs and mark the statuses. Because the inputs intentionally trigger failure cases, the expected output (perfect translation) will likely not match the actual output, resulting in a FAIL status for most or all cases, highlighting areas for improvement in the transliteration model.
