# Day 6 Exercise 2
This is a reference of Code for Day 6 Exercise 2

## Create and Subscribe to SAP HANA Cloud
### Steps
1. Login to your `SAP BTP Trial account`. -> https://cockpit.hanatrial.ondemand.com/trial/#/home/trial
2. Go to `Services` > `Service Marketplace` and search for `SAP Hana Cloud` and click `Create`.
<kbd> ![Description](images/Day6-Exercise2-Create-SAP-HANA-Cloud.png)</kbd><br>

3. Fill-up the following:
    - Service: `SAP HANA Cloud`
    - Plan: `tools`
<kbd> ![Description](images/Day6-Exercise2-Subscribe-SAP-HANA-Cloud.png)</kbd>

4. After subscribing to SAP HANA Cloud, we need to assign the role collection to our user. Go to `Security` > `Users` > `Default Identity provider` and click `Assign Role Collection`.

    <kbd> ![Description](images/Day6-Exercise2-Open-Role-Collection.png)</kbd>

5. Search for `SAP HANA` and select all the items and click `Assign Role Collection`.

    <kbd> ![Description](images/Day6-Exercise2-Assign-Role-Collection.png)</kbd>

6. Once role assignment is completed, go back to `Instances and Subscription` > `SAP HANA Cloud` and click `Go to Application`.

    <kbd> ![Description](images/Day6-Exercise2-Open-SAP-HANA-Cloud.png)</kbd>

## Create SAP HANA Database

1. Click `Create Instance`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-1.png)</kbd>

2. Select `Configure manually` and `SAP HANA Database`. Then click `Next Step`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-2.png)</kbd>

3. Click `Sign in to the Cloud Foundry Environment`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-3-1.png)</kbd>

4. Click `Sign in with default identity provider`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-3-2.png)</kbd>

5. Click `Authorize`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-3-3.png)</kbd>

6. Sign-in successfull then click `Close`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-3-4.png)</kbd>

7. Now, Enter `Instance Name` and provide `Administrator Password`.<br>
Instance Name: **dev-hana**<br>
Administrator Password: **zb00tCamp**<br>   
Click **Next Step**.   

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-3-5.png)</kbd>

8. Leave the default settings and click `Next Step`.
    <kbd> ![Description](images/Day6-Exercise2-Create-Database-4.png)</kbd>

9. Select `All BTP IP address` and click `Next Step`.
    <kbd> ![Description](images/Day6-Exercise2-Create-Database-5.png)</kbd>

10. For SAP HANA Database:Advance Settings, Click `Next Step`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-6.png)</kbd>

11. For Data Lake: General, Click `Review and Create`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-7.png)</kbd>

12. Summary of Instance. Click `Create Instance`.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-8.png)</kbd>

13. Creating of HANA DB Instance in-progress.

    <kbd> ![Description](images/Day6-Exercise2-Create-Database-9.png)</kbd>


15. Once HANA DB Instance is created. It should change the status to `Running`.
    <kbd> ![Description](images/Day6-Exercise2-Create-Database-10.png)</kbd>