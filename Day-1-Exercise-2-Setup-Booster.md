# Day 1 Exercise 2 - Setup Cloud Identity Provider and Subscribe to Build Work Zone.
This is a reference of Code for Day 1 Exercise 2.

## Setup Cloud Identity Provider

### Steps:

1. In your `BTB Cockpit`, navigate to  `Services` -> `Instances & Subscription`, and click the `Create` button. 

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-1.png) </kbd>

2. Select the following and click `Create`.
    - Service: `Cloud Identity Services`
    - Plan: `default`

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-2.png) </kbd>

3. After creating the instance, an email will be sent to activate your account. Please check your email and activate the account.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-3.png) </kbd>

4. Click `Skip`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-4.png) </kbd>


5. Set `Password`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-5.png) </kbd>

6. Account Activated.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-6.png) </kbd>

7. Go to `BTP Cockpit` and click `Security` -> `Trust Configuration` and click button `Establish Trust`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-7.png) </kbd>

8. Select the `tenant`. It will only show 1 tenant.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-8.png) </kbd>

9. Details are auto populated. No need for modification. Click `Next`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-9.png) </kbd>

10. Details are auto populated. No need for modification. Click `Next`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-10.png) </kbd>

11. Click `Finish`.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-11.png) </kbd>

12. Summary.

    <kbd> ![Description](images/Day1-Exercise2-Cloud-Identity-12.png) </kbd>


## Subscribe to SAP Build Work Zone

### Steps

1. Go to `BTP Cockpit` and click `Services` -> `Instances and Subscription` and click the button `Create`. Fill-up the following details:
    - Service: `SAP Build Zone, standard edition`
    - Plan: `standard`
    <kbd> ![Description](images/Day1-Exercise2-Build-WorkZone-1.png) </kbd>

2. Once subscribed to SAP Build Work Zone, a new entry should be added in the `Instances & Subscription`.

    <kbd> ![Description](images/Day1-Exercise2-Build-WorkZone-2.png) </kbd>

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