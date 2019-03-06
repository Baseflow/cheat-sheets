# Docker Cheat Sheet

## Login

| Command | Description |
| ------- | ----------- |
| `az login` | Sign-in interactively (this will open a browser window which will ask for your Azure Credentials). |
| `az login -u <username> -p <password>` | Sign-in to Azure using the supplied username and password. Note: this approach doesn't work for Microsoft Accounts or accounts that have two-factor authentication enabled. |
| `az account show --output table` | Show the account details for the current user. |

## Azure Kubernetes Service (AKS)

| Command | Description |
| ------- | ----------- |
| `az aks get-credentials --resource-group <resource_group_name> --name <cluster_name>` | Get the credentials for the cluster matching the  supplied resource group and cluster name. |
| `az aks browse --resource-group <resrouce_group_name> --name <cluster_name>` | Open the Kubernetes dashboard for the supplied resource group and cluster name. |

## Useful links

- Azure Portal: https://portal.azure.com
