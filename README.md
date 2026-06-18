# Science Communication Journals — PDF Collection

Full-text PDF collection for three science communication journals, with Web of Science (WOS) metadata as the ground truth standard.

## Journals

| Journal | Abbreviation | Publisher | Period |
|---------|-------------|-----------|--------|
| Journal of Science Communication | JCOM | SISSA | 2002–2026 |
| Public Understanding of Science | PUS | SAGE | 2002–2026 |
| Science Communication | SciComm | SAGE | 2002–2026 |

## Coverage

Based on `wos_metadata_complete.csv` (downloaded = yes):

| Journal | Downloaded | WOS Total | Coverage |
|---------|-----------|-----------|----------|
| JCOM | 777 | 901 | 86.2% |
| PUS | 1,133 | 1,239 | 91.4% |
| SciComm | 585 | 672 | 87.1% |
| **Total** | **2,495** | **2,812** | **88.7%** |

## File Structure

```
Science-Communication-/
├── JCOM_pdfs.zip                  # JCOM PDFs (Git LFS)
├── PUS_pdfs.zip                   # PUS PDFs (Git LFS)
├── SciComm_pdfs.zip               # SciComm PDFs (Git LFS)
├── wos_metadata_complete.csv      # Master metadata with download status
├── missing_papers.csv             # Missing papers with reasons
└── README.md
```

Each zip contains year-based subfolders (e.g., `2002/`, `2003/`, ..., `2026/`; SciComm uses 2-digit years `02/`–`26/`).

PDF naming convention: `AuthorYY.pdf` (single author), `Author1Author2YY.pdf` (two authors), `AuthoretalYY.pdf` (three or more authors).

## Metadata

`wos_metadata_complete.csv` contains one row per WOS article/review (2002+), with all original WOS export fields preserved. Two columns are prepended/appended:

| Column | Description |
|--------|-------------|
| journal | JCOM, PUS, or SciComm (prepended) |
| PT–UT | All original WOS fields (AU, AF, TI, SO, AB, DT, DE, ID, CR, DI, PY, etc.) |
| downloaded | "yes" if PDF is in the collection, "no" otherwise (appended) |

`missing_papers.csv` has the same WOS fields, with a `reason` column instead of `downloaded`.

## Missing Papers

317 papers are missing (see `missing_papers.csv` for full list with metadata):

- **JCOM** (124 missing): Older papers (2005–2017) without DOIs — not available for DOI-based retrieval.
- **PUS** (106 missing): Not accessible.
- **SciComm** (87 missing): Not accessible.

## Data Sources

- **Ground truth**: Web of Science manual export, filtered to document types Article, Review, Article; Proceedings Paper, and Early Access variants (2002+).
- **PDFs**: Zotero bulk download, DOI-based script download, and manual download. Verified against WOS metadata via exact DOI matching.
