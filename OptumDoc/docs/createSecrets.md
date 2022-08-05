# Create Secrets on Hashicorp Vault Web UI
---
## Step 1: Sign in to Vault

Access [pam-dev.uhc.com](http://pam-dev.uhc.com) on a web browser (the follwing browsers are supported: Chrome, Firefox, Safari, and Microsoft Edge) and sign in to Vault.  
**Note:**  It is important to provide a correct **Namespace**  
![Screenshot](img/Vault1.jpg)

1. Fill out **Namespace** with **"/OPTUM/APP/AIRFLOW"**
2. Choose **LDAP** method
3. Fill out your **Username** and **Password**
4. Click on **Sign In** button

## Step 2: Switch to your target Namespace

After signing in to Vault, you will see the following main page of the Vault Web UI:  
![Screenshot](img/Vault2.png)  

1. Click on the arrow down icon next to **AIRFLOW**, then a drop-down menu will appear. Click on **Manage namespaces**
![Screenshot](img/Vault3.png)
2. After clicking on **Manage namespaces**, a list of Namespaces will show up
![Screenshot](img/Vault4.png)
3. Click on **...** (three horizontal dots icon) next to your target Namespace and choose **Switch to Namespace**
![Screenshot](img/Vault5.png)

## Step 3: Choose your engine
After switching to your target Namespace, a list of engines will show up
![Screenshot](img/Vault6.png)
Click on your target engine
![Screenshot](img/Vault7.png)


## Step 4: Create a secret
1. Click on **Create secret** to create a new secret
![Screenshot](img/Vault8.png)
2. Fill out **secret path** and **Secret data**
![Screenshot](img/Vault9.png)
3. Click on **Save** button

## Step 5: Continue creating remaining secrets

## Examples of results

