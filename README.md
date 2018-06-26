# Collecting/Uploading Physio Data

## Prerequsites
- Make sure the wifi is turned off.
- Make the participant/session folder in the VossLab folder under the appropriate project folder (either BETTER or EXTEND) using the [BIDS](http://bids.neuroimaging.io/) naming convention.
    - Specifically, there should be a subject folder and a session folder, with the general naming scheme `sub-<label>_ses-<label>`, where \<label\> is any combination of alphanumeric characters.
        - subject folder names
            - BETTER: 3 digit number (e.g. 001)
            - EXTEND: 4 digit number starting at 2000 (e.g. 2001)
        - session folder names
            - Even more specifically, for BETTER the session folder names are `ses-pre` & `ses-post`.
            - For BikeExtend, the session folder names are `ses-day1pre`, `ses-day1post`, `ses-day2pre`, `ses-day2post`, & `ses-postintervention`.


## Step 1: Find Standard.acq
Open Standard.acq within the VossLab folder on the desktop.


## Step 2: Save Standard.acq
- Click on MP150 along the top menu bar
- specify setup acquisition
- on the something/something tab, click on file ...
    - save the file using the [BIDS](http://bids.neuroimaging.io/) naming convention.
        - specifically, the name will follow the form: `sub-<label>_ses-label_acq-`
            - Note the trailing `-`, this is what we want since a 4 digit number will be appended to the filename.
        - after clicking okay, make sure the "incrementing number" is selected
- test the file by clicking start on the upper left hand corner
    - the file will still have the name `Standard.acq` until you hit start

## Step 3: Record the functional scans
- Start the file before the mri tech begins the scan. 
- Stop the file shortly after the scan.

## Step 4: export each file
- Open each file in acknowledge and click save as...
- name the file (using [BIDS](http://bids.neuroimaging.io/) naming conventions).
    - template: `sub-<label>_ses-<label>_task-<label>_(run-<label>)_physio`
        - the task can be rest, taskswitch, breathhold, etc.
        - the portion between the parens () is optional, that is, if there are not multiples of the same task, you do not need run as a marker.
- the default file type is `acq`, change this to `.txt, .csv`.
- when saving a window will pop up asking how you want to save the file, choose to save with:
    - tab delimiters
    - Linux line endings

## Step 5: git workflow
- Using github desktop, follow the [general instructions](https://github.com/HBClab/addGitData/blob/master/README.md) to add/commit/push the data to github.