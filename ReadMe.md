# Different Minds Lab: Analysis Scripts Repository

## What is this repository?
This repository acts as a database / archive of the analysis scripts used for all previously run experiments in the Different Minds Lab [https://onlineacademiccommunity.uvic.ca/differentmindslab/].

## Why does this repository exist?
1. **Resource:** These materials act as an excellent resource for current and future lab members.
2. **Accountability:** When sharing code with collaborators, there is an expectation that code will be documented to a reasonable extent (e.g., comments included throughout scripts). This same expectation applies to adding code to this repository!
   - **Some added benefits of this accountability measure include:**
      1. If you end up returning to a project at a later date, you will be able to recall the analysis protocol you implemented.
      2. To meet this accountability criteria, you may end up being more strategic and clear in how you go about writing code, which may actually save you time! :)
3. **Helpful documentation when writing a manuscript:** Sometimes, the timeline from coding up an experiment, to collecting data, to analysing data, to finally writing up a manuscript can be quite lengthy! Considering this, having clear and concise documentation detailing how you went about things will be helpful to you and other members involved in the research.

## What is NOT included in this repository?
- Participant data (participant data is not to be stored on GitHub). Lab members may access data through Jim or through OSF (if ethics approval was given to post data to OSF).
- Content used to run the experiment (e.g., HTML files, jsPsych plugins, experiment scripts, etc.)
- Results

## What IS included in this repository?
- **Arguably most importantly:** A ReadMe file to orient lab members to the experiment's submodule. This ReadMe file should detail the general procedures of the experiment: stages of the experiment, tasks completed by participants, and general trial constraints used (this can be the same ReadMe file as the one you use for your "experimental-scripts" ReadMe.
- In addition to this ReadMe, a second ReadMe that is specific to your analysis repository should be included. The contents of this second ReadMe are detailed below:
  - Detail the broad analyses that you ran (e.g., 2x2x4 ANOVA examining what?)
  - Data of interest in the analysis
  - List of key scripts used to conduct the analysis
  - All scripts used to run your analyses (i.e., scripts used for data wrangling --> plots)
  - **Bonus points for:**
      1. Subfolder ReadMe files detailing (in 1-2 sentences) what each script does (e.g., list input and output of script) and what variables may need to be adjusted.
      2. Clear comments throughout scripts highlighting what may need to be changed (e.g., folder name)
      3. Including in the ReadMe a section detailing the general workflow of the analysis (i.e., what scripts did you start with? What did they provide as output? What scripts did you need to run to get the data necessary to run basic statistical tests in R?). For example, 1) convert_raw_data.py (takes in folder holding csv files titled "raw_data". outputs concatenated csv including data from all Ps); 2) data_parsing.py (parses data from concatenated csv into a folder titled saved_data); 3) data_modelling.py (takes in populated saved_data folder, outputs convergence rate and model_inferred_1 and _2); etc...

## When should I add my experiment's materials to this repository?
- After analyses are complete (e.g., when plots are finalized and you are writing up the manuscript)


## How can I add my code to this repository?
- Each experiment's analysis will have its own _submodule_ in this repository. If you are not familiar with submodules, please review these two websites:
   - https://gist.github.com/gitaarik/8735255
   - https://www.atlassian.com/git/tutorials/git-submodule

- Please read the instructions provided below ***very*** carefully.
  
**Step 1)**
  Open your computer's command line or terminal and navigate to an easily accessible folder (e.g., Desktop or Downloads)
  ```
  cd Desktop
  ```
**Step 2)**
  Clone the repository if you have not already done so. Use the command below to do so.
  ```
  git clone https://github.com/different-minds-lab/Analysis-Scripts
  ```

**Step 3)**
   Navigate into the folder that you just cloned.
   ```
   cd Analysis-Scripts
   ```
**Step 4)**
   Add your new submodule. Please use your experiment's name when adding your submodule (follow the same naming protocol as your Experimental-Scripts submodule). An example of how to add your submodule is provided below. NOTE! Replace "name_of_experiment" (listed as the last section of the command) with the name of your experiment.
   ```
   git submodule add https://github.com/different-minds-lab/Analysis-Scripts name_of_experiment
   ```
**Step 5)**
   Open up the "Analysis-Scripts" folder you cloned using your preferred IDE (e.g., Visual Studio code). Copy and paste your analysis materials to your newly generated subcomponent. This subcomponent should appear as a folder that is nested within the "Analysis-Scripts" folder.

   
**Step 6)**
   Double-check to ensure all of your documentation and scripts are present. 

   
**Step 7)**
   Return to your terminal and navigate into the "Analysis-Scripts" folder if you are not already seated within it. Then, run the following commands. Replace "insert push message here" with "update name_of_experiment submodule".
   ```
   git add .
   git commit -m "insert push message here"
   git push
   ```
**Step 8)**
Upon confirming that your analysis materials were successfully added to the submodule, you may delete the entire "Analysis-Scripts" folder from your computer. This way, you will free up space on your computer.
