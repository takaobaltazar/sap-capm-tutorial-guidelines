# Day 7 Exercise 1
This is a reference of Code for Day 7 Exercise 1

## Check HANA Database
### Steps
1. Ensure that **HANA Database** is up and running to avoid any issue during deployment.
2. Go to `BTP Cockpit` > `trial` > `Services` > `Instances and Subscription`. Under `Subscription` tab, click **SAP HANA Cloud** > **Go to Application**.  
<kbd> ![Description](images/Day7-Exercise1-Select-SAP-HANA-Cloud.png)</kbd>

3. Start the **database**.
<kbd> ![Description](images/Day7-Exercise1-Start-SAP-HANA-DB.png)</kbd>

4. Once started, the status should change to `Running`.
<kbd> ![Description](images/Day7-Exercise1-Running-HANA-DB.png)</kbd>

## Prepare for Production
### Setup Approuter
#### Steps
1. Open your project in SAP BTP and right click `mta.yaml` > `Create MTA Module from Template`.<br>   
2. Select `Approuter Configuration` and click `Start`.<br>   
<kbd> ![Description](images/Day7-Exercise1-Approuter-Config.png)</kbd>

3. Fill-up required fields for the Approuter Configuration. Click **Next**.
    - HTML5 application runtime: **Managed Approuter**
    - Unique name of project: **com.approuter.bootcamp**
    - Do you plan to add a UI? **Yes**<br>   
    <kbd> ![Description](images/Day7-Exercise1-Approuter-Config-2.png)</kbd>

4. Select `overwrite`. This will overwrite the content of xs-security.json
<kbd> ![Description](images/Day7-Exercise1-Approuter-Config-3.png)</kbd>

5. It will now add approuter configuration to your **mta.yaml** file. Also, it will generate a new file `xs-security.json`<br>   
<kbd> ![Description](images/Day7-Exercise1-Approuter-Config-4.png)</kbd>  

### Add Hana
#### Steps
1. Open **terminal** and execute the command to add hana configuration. This is `one time setup only` together with the approuter configuration.
    ```cds
    cds add hana --for production
    ```

2. The **package.json** will be modified and will include configuration for production database which is Hana Cloud. Also, the **yaml** file will be modified. <br>   
<kbd> ![Description](images/Day7-Exercise1-HANA-Config.png)</kbd>  

### Install Modules
### Steps
1. Open again **terminal** and execute the command below:
    ```cds
    npm i @sap/xssec
    ```

### Configure Destination
#### Steps
1. **Right click** your root Fiori folder `(app/report)` > **Open Application Info**. <br>   
<kbd> ![Description](images/Day7-Exercise1-open-application-info.png)</kbd> 

2. Click **Add for Deploy**.<br>   
<kbd> ![Description](images/Day7-Exercise1-open-application-info-2.png)</kbd> 

3. Fill-up required fields and click `Finish`.
    - Target: **Cloud Foundry**
    - Destination Name: **Local CAP Project API (Instance Based Destination).**<br>   
    <kbd> ![Description](images/Day7-Exercise1-open-application-info-3.png)</kbd> 
    
4. After you configure the destination, the **mta.yaml** and `xs-app.json` file will be modified.
    - `xs-app.json`<br>   
    <kbd> ![Description](images/Day7-Exercise1-Configure-Destination-1.png)</kbd>  
    
    - `mta.yaml`<br>   
    <kbd> ![Description](images/Day7-Exercise1-Configure-Destination-2.png)</kbd>  

5. This is to allow the Fiori Application to access the OData Service of NodeJS.

## Deploy to Production
### Steps
1. Right click **mta.yaml** then click **Build MTA Project**.<br>   
    <kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-1.png)</kbd>

    <kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-2.png)</kbd>

2. Go to **mta_archives folder**. Right click the **.mtar file** > **Deploy MTA Archive.**<br>   
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-3.png)</kbd>

3. A window will appear to login into Cloud Foundry. Please click the link `Open a new browser page to generate your SSO passcode`.<br>   
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-4.png)</kbd>

4. A new window will open in your browser. Select `Sign in with default identity Provider`.
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-5.png)</kbd>

5. Copy the `code` and paste it to the `Enter your SSO Passcode` field. Then click `Sign in`.
    <kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-6.png)</kbd>

    <kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-7.png)</kbd>

6. After you login, Set the **organization** and **dev space** and click `Apply`.<br>   
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-8.png)</kbd>

7. It will now deploy the application to SAP BTP.
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-9.png)</kbd>

### Successful Deployment - UI and Node Service
1. **Fiori application** is deployed under **HTML5 Applications** residing in trial > HTML5 Applications.<br>   
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-10.png)</kbd>

2. **Node Service** is deployed under our **cloud foundry spaces**. It is residing in `trial` > `Cloud Foundry` > `Spaces` > `dev` > `Applications`. <br>   
<kbd> ![Description](images/Day7-Exercise1-Deploy-To-Production-11.png)</kbd>