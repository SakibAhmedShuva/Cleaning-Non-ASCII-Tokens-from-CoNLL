# CoNLL-Non-ASCII-Tokens-Cleaner

A Jupyter notebook implementation to clean CoNLL files by removing lines containing non-ASCII characters while preserving empty lines for maintaining the original file structure.

## Description

This tool is designed to process CoNLL (Conference on Natural Language Learning) format files by:
- Removing lines containing non-ASCII characters
- Preserving empty lines to maintain sentence boundaries and file structure
- Keeping lines that contain only ASCII characters
- Creating a new cleaned file with the filtered content

## Requirements

- Python 3.x
- Jupyter Notebook
- No additional dependencies required (uses only built-in Python libraries)

## Installation

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/CoNLL-Non-ASCII-Tokens-Cleaner.git
cd CoNLL-Non-ASCII-Tokens-Cleaner
```

## Usage

1. Launch Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `conll_cleaner.ipynb`

3. Update the file path in the second cell to point to your CoNLL file:
```python
clean_lines_with_gaps('path/to/your/file.conll')
```

4. Run all cells (or run them one by one)

The notebook will create a new file named `cleaned_file_with_gaps.conll` in the same directory.

## Function Parameters

- `file_path` (str): Path to the input CoNLL file

## Output

- Creates a new file named `cleaned_file_with_gaps.conll`
- Preserves the original file structure with empty lines
- Removes lines containing non-ASCII characters
- Prints "Non-ASCII tokens removed successfully" upon completion

## Example

Input file (`example.conll`):
```
1    The    DET    _
2    cat    NOUN   _

1    Les    DET    _
2    café   NOUN   _

1    The    DET    _
2    dog    NOUN   _
```

Output file (`cleaned_file_with_gaps.conll`):
```
1    The    DET    _
2    cat    NOUN   _

1    The    DET    _
2    dog    NOUN   _
```

Note: The middle sentence containing "café" (non-ASCII character) is removed while maintaining the empty line structure.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Screenshot:
![image](https://github.com/user-attachments/assets/94cc6615-1e6d-4957-b866-4678132ef82a)

