VA NON-DISABILITY BENEFITS · Burial benefits MVP redesign

# Burial benefits 21P-530EZ review page issues

Designer: [Fiorella](https://github.com/fiorella-io)

<img src="https://github.com/department-of-veterans-affairs/va.gov-team/assets/91498500/bc5bf2b8-dcf4-44db-a707-a7ed8ef7ebae" width="35%" align="right">

## Issue 1 - Severe
A claimant can submit blank required information


#### Steps to replicate
- On step 2, get to the "Previous name" section, and select "No" to the "Did the Veteran serve under another name?" question
- Get to the Review page
- Expand the "Military history" section
- Click "Edit" on the "Previous name" section, and select "Yes" to the "Did the Veteran serve under another name?" question
- Click "Submit application" at the bottom of the form
- You can also choose to click "Update page" and then click "Submit application"

#### Possible Solution
1) Automatically trigger an error when "Yes" is selected to the "Did the Veteran serve under another name?" question. [Designs for this solution](https://www.sketch.com/s/de782a35-e147-4c32-a2a8-ba53071ec8e7/a/mP0x9bg)
2) Trigger errors when "Submit application" is clicked
<br><br><br><br>


## Issue 2 
When updating the "Date of death" and "Date of burial" of the deceased Veteran, the claimant does not get informed if these dates are more than 2 years from our current date.

#### Steps to replicate
- On step 2, enter any day in 2023 for the "Date of death" and "Date of burial" of the deceased Veteran
- Get to the review page
- Expand the "Veteran information"
- Change the year to 2019 or less
- No warning note gets triggered here like it does in Step 2
<img src="https://github.com/department-of-veterans-affairs/va.gov-team/assets/91498500/8bb88a1d-44a1-4846-9143-93e2b0df6a1d" width="60%">

#### Possible Solution
Add the existing note on step 2 to the corresponding section on the Review page. [Design for this solution](https://www.sketch.com/s/de782a35-e147-4c32-a2a8-ba53071ec8e7/a/OeYMxak)


<img width="20%" align="right" alt="image" src="https://github.com/department-of-veterans-affairs/va.gov-team/assets/91498500/80d7d2ed-6daf-4c9c-ba5d-ce585173b011">

## Issue 3
A claimant can add multiple blank previous names the deceased Veteran served under without having to enter a name first. This behavior is different than the same section in Step 3. On Step 3 you are not allowed to add additional names unless you add a name first.

#### Steps to replicate
- On step 2, get to the "Previous name" section, and select "No" to the "Did the Veteran serve under another name?" question
- Get to the Review page
- Expand the "Military history" section
- Click "Edit" on the "Previous name" section, and select "Yes" to the "Did the Veteran serve under another name?" question
- Click "Add another name" multiple times
As mentioned in Issue 1, the claimant is allowed to submit this application with multiple empty previous names

#### Possible Solution
1) Once "Yes" is selected for the "Did the Veteran serve under another name?" question and new fields appear, delete the "Add another name" until "Update" has been clicked. Designs for this solution: [Editable](https://www.sketch.com/s/de782a35-e147-4c32-a2a8-ba53071ec8e7/a/mP0x9bg) | [Updated/Saved](https://www.sketch.com/s/de782a35-e147-4c32-a2a8-ba53071ec8e7/a/j4D2yVW)
2) Once "Add another name" is clicked, trigger inline errors

<br><br>

## Issue 4



