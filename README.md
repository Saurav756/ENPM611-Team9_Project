# ENPM611 Project Application Template - Team9

## The three analysis features implemented in this project are:
**Analysis One:** The analysis takes user input to analyze GitHub issues based on a specific label. If a label isn't provided via the command line, it lists all available labels and prompts the user to choose one. The selected label is used to filter issues for analysis. The analysis includes several statistics, such as the average number of comments, time to close, top contributors, and the proportion of reopened issues. Visual outputs include combined bar charts (number of comments, labels, reopened issues), a pie chart (open vs closed issues), a histogram (median response times), and a bar chart for reopened issues. This user-interactive approach allows the user to explore issues dynamically based on the selected label. 
The graphs are stored in 'Output' folder

**Analysis Two:** Analysis2 provides an overview of contributor activities across all issues, highlighting top contributors based on the comments, labeling activities, and issues closed. It also includes the Top 10 labels used in the issues along with the unqiue contributers to the isssues.
- filename_contributer_activity.png: shows the top contributers to based on comments, labeling and closed issues.
- top_labels_activity.png: it shows the Top 10 labels from the issues.

**Analysis Three:** Analysis 3 provides insights into the closure times of issues. The analysis highlights average closure times for issues based on specific label types, and by both month and year.

---

This is the template for the ENPM611 class project. Use this template in conjunction with the provided data to implement an application that analyzes GitHub issues for the [poetry](https://github.com/python-poetry/poetry/issues) Open Source project and generates interesting insights.

This application template implements some of the basic functions:

- `data_loader.py`: Utility to load the issues from the provided data file and returns the issues in a runtime data structure (e.g., objects)
- `model.py`: Implements the data model into which the data file is loaded. The data can then be accessed by accessing the fields of objects.
- `config.py`: Supports configuring the application via the `config.json` file. You can add other configuration paramters to the `config.json` file.
- `run.py`: This is the module that will be invoked to run your application. Based on the `--feature` command line parameter, one of the three analyses you implemented will be run. You need to extend this module to call other analyses.

With the utility functions provided, you should focus on implementing creative analyses that generate intersting and insightful insights.

In addition to the utility functions, an example analysis has also been implemented in `example_analysis.py`. It illustrates how to use the provided utility functions and how to produce output.

## Setup

To get started, your team should create a fork of this repository. Then, every team member should clone your repository to their local computer. 


### Install dependencies

In the root directory of the application, create a virtual environment, activate that environment, and install the dependencies like so:

```
pip install -r requirements.txt
```

### Download and configure the data file

Download the data file (in `json` format) from the project assignment in Canvas and update the `config.json` with the path to the file. Note, you can also specify an environment variable by the same name as the config setting (`ENPM611_PROJECT_DATA_PATH`) to avoid committing your personal path to the repository.


### Run an analysis

With everything set up, you should be able to run the existing example analysis:

```
python run.py --feature 0
```

That will output basic information about the issues to the command line.


## VSCode run configuration

To make the application easier to debug, runtime configurations are provided to run each of the analyses you are implementing. When you click on the run button in the left-hand side toolbar, you can select to run one of the three analyses or run the file you are currently viewing. That makes debugging a little easier. This run configuration is specified in the `.vscode/launch.json` if you want to modify it.

The `.vscode/settings.json` also customizes the VSCode user interface sligthly to make navigation and debugging easier. But that is a matter of preference and can be turned off by removing the appropriate settings.
