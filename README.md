# National Trachoma F&E Surveillance Data Repository

This repository serves as a centralized, version-controlled dataset for trachoma 'F' (Facial cleanliness) and 'E' (Environmental improvement) indicators across remote Aboriginal populations in Australia. It is part of the national trachoma elimination strategy under the SAFE framework.

## Purpose
- Standardize data collection for F&E components across regions
- Enable national-level analysis to guide infrastructure investments
- Provide transparent, versioned data for research and policy

## Data Submission Guidelines

### File Format
- Submit data as comma-separated values (`.csv`) files.
- Use UTF-8 encoding.
- Do not include extra spaces, quotes, or special characters beyond those needed.

### Column Headers (Standardized)
All submissions **must** use the following exact column names:

| Column Name | Description | Allowed Values / Format |
|-------------|-------------|-------------------------|
| `community_name` | Official name of the community as per the Australian Government Gazetteer | Text, must match official gazetteer |
| `population` | Estimated population of the community | Integer ≥ 0 |
| `households_with_working_toilets` | Number of households with functional, hygienic toilets | Integer ≥ 0 |
| `percentage_of_children_with_clean_faces` | Percentage of children (1‑9 years) observed with clean faces during assessment | Numeric 0‑100 (inclusive) |
| `date_of_assessment` | Date when the assessment was conducted | YYYY‑MM‑DD |

### Data Entry Rules
1. **Community names** must be spelled exactly as they appear in the official gazetteer (case‑sensitive). Typos or abbreviations will cause rejection.
2. **Population** and **households_with_working_toilets** must be non‑negative integers.
3. **Percentages** must be between 0 and 100 (inclusive). Decimal values are allowed (e.g., 87.5).
4. **Dates** must follow ISO 8601 (YYYY‑MM‑DD). No other formats will be accepted.
5. Missing values should be left blank (empty cell). Do not use placeholders like `NA`, `NULL`, or `-`.

### Template File
A blank template [`data_template.csv`](data_template.csv) is provided in the repository. Download it, fill in your data, and rename the file to `region_[your‑region]_data.csv` (e.g., `region_alpha_data.csv`).

### Submission Workflow
1. Fork this repository.
2. Create a new branch named `submission‑region‑[your‑region]`.
3. Place your correctly formatted CSV file in the root directory.
4. Open a pull request (PR) from your branch to the `main` branch.
5. The repository maintainers will review the data against the standards above and either request changes or approve the PR.

## Quality Assurance
All submissions undergo an automated and manual review. Inline comments will be added to the PR for any deviations from the standard. Once corrected, the data will be merged into the `main` branch and become part of the national dataset.

## Contact
For questions or assistance, contact the National Trachoma Control Programme at `trachoma.data@health.gov.au`.

## License
The data in this repository is released under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).