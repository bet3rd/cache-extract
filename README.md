# Cache Extract - Web Edition

A web tool for extracting JWT tokens and credentials from binary files. Upload `.exe` or `.txt` files, extract credentials in bulk, and download as a combined list.

## 🌐 Live Version

Use the tool directly in your browser (no installation required):
**[Launch Cache Extract](https://bet3rd.github.io/cache-extract)**

## 💻 Local Installation

If you prefer to run the tool locally on your machine:

1. **Install**
   ```bash
   pip install flask
   ```

2. **Run**
   ```bash
   python app.py
   ```

3. **Access** `http://localhost:4444`

## Usage

- **Upload**: Drag-and-drop or click to select files
- **Extract**: Automatically parses binary data for JWT tokens
- **Export**: Download all credentials as `.txt`
- **Manage**: Copy or delete individual entries

## How It Works

1. Reads file as binary
2. Extracts ASCII strings (4+ chars)
3. Detects JWT tokens (start with "ey", 50+ chars)
4. Associates nearby usernames
5. Stores in browser IndexedDB (no server upload)

## Features

- Bulk file processing
- Real-time progress updates
- Local browser storage (IndexedDB)
- Dark theme UI
- Export deduplicated credentials

## File Structure

```
├── app.py              # Flask server
├── templates/index.html # Web UI + JS logic
└── README.md
```

## Notes

- All data stored locally (not uploaded)
- Clearing browser cache deletes data
- Requires modern browser with IndexedDB support