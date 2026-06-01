# MeshLibTestData

Input data for [MeshLib](https://github.com/MeshInspector/MeshLib) Python regression
tests (the `test_regression/` suite).

This repository is consumed by MeshLib as a git submodule mounted at `test_data/`.
The regression-test CI job initializes the submodule to obtain these files; the test
suite reads them through `test_files_path = "../test_data"` (see
`test_regression/constants.py` in MeshLib).

## Origin

Imported from `s3://data-autotest/test_data_2025-05-13`.

## Versioning

The data version consumed by MeshLib is pinned by the submodule commit. To update the
test data, commit the changes here and bump the submodule pointer in MeshLib in the
same pull request.

## Layout

- `algorithms/` — inputs and reference results for algorithm regression tests
- `conversion/` — mesh / point-cloud format conversion fixtures
- `cuda/` — CUDA test inputs
- `doc_samples/` — expected outputs for documentation samples
- `issues/` — regression fixtures for specific tracked issues
- `old_files/` — legacy-format fixtures
