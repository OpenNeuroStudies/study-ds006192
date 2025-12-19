# study-ds006192

BIDS study dataset aggregating OpenNeuro dataset [ds006192](https://openneuro.org/datasets/ds006192) and its derivatives.

## Dataset Structure

This is a BIDS [DatasetType: "study"](https://bids.neuroimaging.io/extensions/beps/bep_035.html) that organizes:

- **Raw data**: Original BIDS dataset from OpenNeuro
- **Derivatives**: Processed outputs (fmriprep, mriqc, etc.) linked as submodules

## Contents

- `sourcedata/` - Link to source BIDS dataset(s) (git submodules)
- `derivatives/` - Processed data derivatives:
  - `bids-validator/` - BIDS validation results
  - Other derivatives linked as submodules
- `code/` - Analysis scripts including `run-bids-validator`
- `dataset_description.json` - BIDS dataset description

## Running BIDS Validation

To run BIDS validation with provenance tracking:

```bash
datalad run code/run-bids-validator
```

Results are stored in `derivatives/bids-validator/`:
- `version.txt` - Validator version
- `report.json` - Machine-readable results
- `report.txt` - Human-readable summary

## Links

- **OpenNeuro**: https://openneuro.org/datasets/ds006192
- **GitHub**: https://github.com/OpenNeuroStudies/study-ds006192
- **BIDS BEP035**: https://bids.neuroimaging.io/extensions/beps/bep_035.html
- **OpenNeuroStudies**: https://github.com/OpenNeuroStudies

## License

Dataset licenses vary. Check individual source datasets for license information.
