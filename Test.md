# Deploying a VNET in Azure

## Prerequisites
- Azure subscription
- Azure CLI installed

## Steps

1. Open a terminal or command prompt.

2. Log in to your Azure account by running the following command:
    ```
    az login
    ```

3. Create a resource group for your VNET by running the following command:
    ```
    az group create --name myResourceGroup --location eastus
    ```

    Replace `myResourceGroup` with the desired name for your resource group and `eastus` with the desired location.

4. Create a VNET by running the following command:
    ```
    az network vnet create --name myVnet --resource-group myResourceGroup --address-prefixes 10.0.0.0/16 --subnet-name mySubnet --subnet-prefixes 10.0.0.0/24
    ```

    Replace `myVnet` with the desired name for your VNET, `myResourceGroup` with the name of your resource group, and `mySubnet` with the desired name for your subnet.

5. Verify the VNET creation by running the following command:
    ```
    az network vnet show --name myVnet --resource-group myResourceGroup --output table
    ```

    This command will display the details of your VNET.

6. You have successfully deployed a VNET in Azure!
