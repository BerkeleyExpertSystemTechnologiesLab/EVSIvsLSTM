Repo for paper "Dynamic Placement of Rapidly Deployable Mobile Sensor Robots Using Machine Learning and Expected Value of Information"

# Notes
- I probably still left some absolute path in the project. When running a script, please check the paths used for loading dataset, saving models and etc.

# Repo Structure
The section contains the structure graph of this project and some simple descriptions of folders
- For more detailed description of each script, please refer to the README inside each folder.

- Every item with `.` extension is a file/script. Items without `.` extension are folders.

- Folders like `dataset`, `models`, `backup` are not actually empty. But because they usually hold fairly large files/datasets I decided to not upload the content directly to github (`.gitignore` are left in those folders as placeholders). Please contact me directly if you need those files.

```
│   env.yml: environment file (under Windows 10) for Conda. Use this to generate a working environment
│
├───evsi: scripts/data related to EVSI portion of this project
│   │   get_EVSI.ipynb
│   │   get_models.ipynb
│   │   ranking_and_correlation.ipynb
│   │   sensitivity_analysis.ipynb
│   │   training_and_evsi_fs.ipynb
│   │
│   ├───backup: results of each run of `training_and_evsi_fs.ipynb`.
│   ├───dataset: raw data of the TE dataset
│   ├───log: relevant metrics generated after the current run
│   │       acc.csv
│   │       acc_improvement.csv
│   │       sensitivity_analysis.csv
│   │       sensor_selection.csv
│   │
│   └───models: frozen LSTM models saved after the current run
│       ├───evsi: models trained for EVSI purpose
│       └───ml: models trained for forward stepwise selection purpose
|
└───ml
    │   LSTM_RandomForest.ipynb
    │   LSTM_workflow.ipynb
    │   README.md
    │   visulization.ipynb
    │
    ├───dataset: raw data of the TE dataset
    ├───models: frozen LSTM models that are used to pick the top 10 impactful features
    └───plots: plots generated to demonstrate the 10 most impactful features
            test_advantage.png
            validation_advantage.png
```
