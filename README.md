## Chlamydia inclusion measurement tool

This repository contains a tool to estimate area of chlamydia inclusions within human cells in microscopy images.

## Setup and run

1. Clone the repo
2. Make sure that you have python installed
3. (Recommended) Create a virtual environment using e.g. venv
4. Run `pip install -r .\requirements.txt` in the root directory
5. Run `voila .\detect_measure_inclusion.ipynb` in the root directory

Your browser should automatically open a tab with the tool.

## Use

To use the tool you simply need to upload your images and click `Measure chlamydia!` button.

Take note of the following:
- the tool assumes that there will be a scale bar in the top left corner and will use it's width as a reference for calculating areas. You can change this scale using the `Width` parameter
- you can discard results below certain area size using `Minimum inclusion size` parameter
- you can toggle visualisation of your results using the `Visualisation` tickbox
