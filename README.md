# physics-qp-combiner

This repository contains a script that downloads a Google Drive folder and merges all Physics QP/MS PDFs into a single PDF in the required order:

- QP 1
- MS 1
- QP 2
- MS 2
- ...

The final output file is named:

- `20_qp_techinteractive.pdf`

## Files

- `combine_papers.py` — downloads the folder and merges PDFs
- `requirements.txt` — Python dependencies

## Usage

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Run the script:

```bash
python combine_papers.py "https://drive.google.com/drive/folders/1sBtHQla4ht-miCmuAnFUIFCYkPLrHTvy?usp=drive_link"
```

3. The script will create:

```bash
20_qp_techinteractive.pdf
```

## Notes

- The Google Drive folder must be publicly accessible or viewable without login.
- The script scans all nested PDF files in the downloaded folder and keeps only Physics paper files containing `QP` or `MS`.
- It sorts by paper number and writes `QP` before `MS` for the same paper number.
