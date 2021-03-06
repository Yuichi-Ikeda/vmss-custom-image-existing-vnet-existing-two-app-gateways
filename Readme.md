# VM Scale Set from a Managed Image connected to an existing Virtual Network and two Application Gateways

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FYuichi-Ikeda%2Fvmss-custom-image-existing-vnet-existing-two-app-gateways%2Fmaster%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.png"/>
</a>

This template deploys a VM Scale Set based on a specified custom image (in the form of a Managed Image), connected to an existing subnet in an existing Virtual Network, and adds the instances to a specified existing two Application Gateway Backend Pools. 

`Tags: VM Scale Set, VMSS, Managed Disks, Managed Images, Custom Image`

## Prerequisites

To deploy this template, you will need:
 * An existing Managed Image ([about Managed Images](https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-windows-capture-image-resource))
 * An existing Virtual Network and three subnets, such as VMSS subnet, AppGw1 subnet and AppGw2 subnet.
 * An existing two Application Gateways and backend pools.
 
In the parameters, you will need to take note of:
 * The name of the resource group containing the Managed Image
 * The name of the Managed Image itself
 * The name of the resource group containing the Virtual Network
 * The name of the subnet inside the Virtual Network where the create VM Scale Set will connect to
 * The name of the resource group containing the Application Gateway
 * The name of the backend pool inside the Application Gateway which will be added with instances of the VM Scale SEt

## Deployment steps

You can click the "Deploy to Azure" button at the beginning of this document or follow the instructions for command line deployment using the scripts in the root of this repo.

## Usage

#### Connect

To connect to individual instances of the VM Scale Set, utilize a jumpbox VM, that is, another VM that is located

## Notes

The OS of the VM Scale Set will follow whatever is defined in the custom image.
