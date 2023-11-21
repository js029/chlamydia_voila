## Chlamydia inclusion measurement tool

This repository contains a tool to estimate area of chlamydia inclusions within human cells in microscopy images. It uses edge detection from `open-cv` to locate the inclusions.

## Setup and run

1. Clone the repo
2. Make sure that you have Python 3.11 installed
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


## Deployment 

This tool can be deployed on [Render](https://render.com/) as follows:
1. Import `main` branch of the repo into Render
2. Set `Build Command` to `pip install -r requirements.txt`
3. Set `Start Command` to `voila --port=$PORT --no-browser --Voila.ip=0.0.0.0 detect_measure_inclusion.ipynb`
4. Add environmental variable `PYTHON_VERSION` and set it to 3.11.6
5. Deploy the project