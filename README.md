# Searching Harder Looks Better

Code and research materials for *Searching Harder Looks Better: A Budget-Resolved Study of Evaluation Inflation in Evolutionary Feature Selection*.

## Supplementary material

The consolidated S1-S5 supplement is available as a [PDF](supplementary/Supplementary_Material_S1-S5.pdf) and an [editable Word document](supplementary/Supplementary_Material_S1-S5.docx). It contains the exploratory literature-excerpt audit, repeated-measurement and oversampling checks, strict-scaling analysis, implementation and protocol provenance, and validation on additional datasets with a same-size follow-up. See the [supplementary index](supplementary/README.md).

This repository accompanies the research study and does not specify a publication venue or submission status.

## Research materials

| Collection | Completed jobs used in the analyses | Contents |
|---|---:|---|
| R22 | 43,710 | Original benchmark, auxiliary controls, and strict inner-fold scaling analysis |
| X11c | 4,000 | Eight additional non-biomedical data sets, five searches, two learners, and three fixed contrasts |
| X12m | 800 | Size-matched random-search follow-up on the additional data sets |
| Total | **48,510** | Experimental records, summaries, source versions, and provenance |

## Verify and restore

Download the complete repository with **Code > Download ZIP** and extract it. From its root, use Python 3.9 or later:

```sh
python verify_repository.py
python restore_materials.py --verify-only
python restore_materials.py --output restored
```

These commands check the distributed files and extract the saved collections into `restored/R22`, `restored/X11c`, and `restored/X12m`. The merged `restored/project` applies them in that order. [REPRODUCE.md](REPRODUCE.md) lists the analysis entry points and their recorded environments.

## Files and directories

- `supplementary/`: consolidated S1-S5 supplement in PDF and editable Word formats.
- `R22_science.zip.part*`, `X11c_science.zip.part*`, and `X12m_science.zip`: experimental records and collection-specific protocols, sources, and summaries.
- `src/efsbench/`, `analysis/`, `experiments/`, `extras/`, and `tests/`: frozen implementation, analysis, experiment, and test source files for browsing. Restore the collections for execution with their version-specific records.
- `source_tree.zip`: source snapshot used by the restoration checks.
- `integrity_manifest.json` and `SHA256SUMS.txt`: provenance, file identities, and integrity checks.
- [DATA_SOURCES.md](DATA_SOURCES.md): dataset attribution, transformations, and source links.
- [RIGHTS.md](RIGHTS.md): software and data licensing status.

R22 supplies source cards and acquisition scripts for its original data; X11c includes the eight additional UCI source copies and processed matrices. The full manuscript and administrative documents are maintained separately.

Frozen records retain their original paths and identifiers for reproducibility. Historical labels are provenance information and do not describe the current publication status.

## Study design

R22 and X11c are analysed separately. X11c's three primary contrasts were fixed internally before execution; no external preregistration was completed. X12m is the exploratory size-matched follow-up.

Budget-gain discrepancy, relative-advantage discrepancy, and outer-performance advantage are distinct quantities. Rankings are assessed separately. Request-matched, distinct-mask, and size-matched random search each define a specific reference comparison; the size-matched reference conditions on the subset size selected by the corresponding algorithm.
