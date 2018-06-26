# Collecting/Uploading Physio Data

## Step 1: Find Standard.acq
Open Standard.acq in the appropriate folder (either BikeExtend or BETTER) through the VossLab folder on the desktop.


## Step 2: Save Standard.acq
Save Standard.acq as a new filename using the [BIDS](http://bids.neuroimaging.io/) naming convention.
Specifically, there should be a subject folder and a session folder, with the general naming scheme `sub-<label>_ses-<label>`, where \<label\> is any combination of alphanumeric characters.
Even more specifically, for BETTER the session folder names are `ses-pre` & `ses-post`
For BikeExtend, the session folder names are `ses-day1pre`, `ses-day1post`, `ses-day2pre`, `ses-day2post`, & `ses-postintervention`
The filename will mirror the folder structure and will be `sub-<label>_ses-<label>_`.
Notice the underscore after the session label, a number will automatically be appended to this filename.

## Step 3: Record the functional scans
Start the file before the mri tech begins the scan. 
Stop the file shortly after the scan.

## Step 4: export each file
Unix file endings

## Step 5: git workflow
- `git add .`
- `git commit -m 'add subject data'`
- `git push origin master`