# Large Language Models Can Solve Real-World Planning Rigorously with Formal Verification Tools

Codes and Dataset for the Paper "[Large Language Models Can Solve Real-World Planning Rigorously with Formal Verification Tools](https://arxiv.org/pdf/2404.11891)".

## Framework
<img src="./imgs/fm_travelplanner_overview.png" width="800px" alt="s" />

## Setup Environment

1. Create a conda environment and install dependency:
    ```bash
    conda create -n fmtravelplanner python=3.9
    conda activate fmtravelplanner
    pip install -r requirements.txt
    ```

2. The UnsatChristmas dataset is provided in `database_small` folder. You can run interactive plan repair experiment with this database.

3. To run satisfiable plan generation experiment, refer to paper "TravelPlanner: A Benchmark for Real-World Planning with Language Agents" and their github repo to download their database and train/validation/test set.

## Running
#### Satisfiable Plan Solving 
The file for satisfiable plan generation experiment is `test_travelplanner.py`. An example command is ```python test_travelplanner.py  --set_type train --model_name gpt```
*Note: You might want to use the training set to adjust the prompts for different LLMs. You can add customized checker for steps and codes to further improve the performance.*

#### Unsatisfiable Plan Repair 

* Run test_travelplanner_interactive.py for unsatisfiable interactive plan repair experiment for TravelPlanner. Follow the instructions in file to first collect initial codes and then do the plan repair. 
* Run test_unsat.py for unsatisfiable interactive plan repair experiment for UnsatChristmas. Follow the instructions in file to first collect initial codes and then do the plan repair. 

## Prompts
The prompts we used are included in the `prompts` folder