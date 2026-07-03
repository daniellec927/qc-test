# QC Test Parser (C++)

An interactive C++ program that parses quality-control batch strings and reports
statistics. A results string encodes one or more batches in the form
`Q<total>p<pass>d<defect>` (for example `Q10p7d3`), which the program validates
and totals.

## Functions
- `isValidQC` — validates the batch-string format (each batch's total must equal
  pass + defect, with no leading zeros).
- `passQC`, `defectQC`, `totalQC` — sum the pass, defect, and total counts.
- `batches` — counts the number of batches.

## Build & Run
```bash
g++ -std=c++17 qctest.cpp -o qctest
./qctest
```
Enter a results string when prompted, e.g. `Q10p7d3`.
