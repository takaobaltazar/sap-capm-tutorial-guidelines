# Day 1 Exercise 2 - Setup Booster
This is a reference of Code for Day 1 Exercise 2.

## Create initial project via Wizard
### Steps:
1. Open your `BTP Cockpit` and navigate to `Global Account (e.g. cccc1e09trial)`.
2. Then go to `Booster` and search for `Get Started with SAP Build Apps` and click it. 
<kbd> ![Description](images/Day1-Exercise2-Select-Booster.png) </kbd>

3. Click `Start`. It automatically establishes the necessary trust without requiring access to the Security → Trust Configuration.
<kbd> ![Description](images/Day1-Exercise2-Start-Booster.png) </kbd>

4. Click `Next`.
<kbd> ![Description](images/Day1-Exercise2-Check-Prerequisite.png) </kbd>

5. Select `Subaccount` and click `Next`.
<kbd> ![Description](images/Day1-Exercise2-Select-Scenario.png) </kbd>

6. These are the Services will be created and Click `Next`.
<kbd> ![Description](images/Day1-Exercise2-Configure-Subaccount.png) </kbd>

7. Click `Next`.
<kbd> ![Description](images/Day1-Exercise2-Add-User.png) </kbd>

8. Click `Finish`.
<kbd> ![Description](images/Day1-Exercise2-Review.png) </kbd>

## De-activate Custom IDP
### Steps

1. Go to your subaccount system thru `trial` > `Security` > `Trust Configuration`.
<kbd> ![Description](images/Day1-Exercise2-Trust-Config.png) </kbd>

2. Select `Default identity Provider` and click `Edit`.
<kbd> ![Description](images/Day1-Exercise2-Edit-Default.png) </kbd>

3. In the `Parameters` tab, select `Available for User Logon` and click `Save`.
<kbd> ![Description](images/Day1-Exercise2-Edit-Available-User-Logon.png) </kbd>

4. Now, from the `Trust Configuration` menu, click the `Custom IAS tenant` and click `Edit`.
<kbd> ![Description](images/Day1-Exercise2-Edit-Custom-IAS-Tenant.png) </kbd>

5. In the `Main Information` tab, set the `Status` to **Inactive** and click `Save`.
<kbd> ![Description](images/Day1-Exercise2-Edit-Inactive-Custom-IAS-Tenant.png) </kbd>

6. Now, this is the final result after modifying the trust configuration.
<kbd> ![Description](images/Day1-Exercise2-Final-Trust-Config.png) </kbd>

## Assign Role Collection
### Steps

1. In your BTP Cockpit, go to `Security` > `Users` and click the user with `Default Identity provider`.
<kbd> ![Description](images/Day1-Exercise2-Go-to-Users.png) </kbd>

2. Click the button `Assign Role Collection`.
<kbd> ![Description](images/Day1-Exercise2-Click-Assign-Role-Collection-1.png) </kbd>

3. Search for `Launchpad_Admin` and click `Assign Role Collection`.
<kbd> ![Description](images/Day1-Exercise2-Click-Assign-Role-Collection-2.png) </kbd>