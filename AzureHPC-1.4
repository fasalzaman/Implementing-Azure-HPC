![Microsoft Cloud Workshops](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/main/Media/ms-cloud-workshop.png "Microsoft Cloud Workshops")

<div class="MCWHeader1">
Azure HPC OnDemand Platform
</div>

<div class="MCWHeader2">
Hands-on lab guide
</div>

<div class="MCWHeader3">
January 2022
</div>

<!-- TOC -->

- [Azure HPC OnDemand Platform lab guide](#azure-hpc-on-demand-platform-lab-guide)
  - [Requirements](#requirements)
  - [Before the hands-on lab](#before-the-hands-on-lab)
    - [Task 1: Validate the owner role assignment in the Azure subscription](#task-1-validate-the-owner-role-assignment-in-the-azure-subscription)
    - [Task 2: Validate a sufficient number of vCPU cores](#task-2-validate-a-sufficient-number-of-vcpu-cores)
  - [Exercise 1: Prepare for implementing the Azure HPC OnDemand Platform environment](#exercise-1-prepare-for-implementing-the-azure-hpc-ondemand-platform-environment)
    - [Task 1: Provision an Azure VM running Linux](#task-1-provision-an-azure-vm-running-linux)
    - [Task 2: Deploy Azure Bastion](#task-2-deploy-azure-bastion)
    - [Task 3: Install the az-hop toolset](#task-3-install-the-az-hop-toolset)
    - [Task 4: Prepare the Azure subscription for deployment](#task-4-prepare-the-azure-subscription-for-deployment)
  - [Exercise 2: Implement Azure HPC OnDemand Platform cloud infrastructure](#exercise-2-implement-azure-hpc-ondemand-platform-cloud-infrastructure)
    - [Task 1: Customize infrastructure components](#task-1-customize-infrastructure-components)
    - [Task 2: Deploy Azure HPC OnDemand Platform infrastructure](#task-2-deploy-azure-hpc-ondemand-platform-infrastructure)
    - [Task 3: Build images](#task-3-build-images)
    - [Task 4: Review deployment results](#task-4-review-deployment-results)
    - [Task 5: Generate passwords for user and admin accounts](#task-5-generate-passwords-for-user-and-admin-accounts)
  - [Exercise 3: Install and configure Azure HPC OnDemand Platform software components](#exercise-3-install-and-configure-azure-hpc-ondemand-platform-software-components)
    - [Task 1: Install and configure Azure HPC OnDemand Platform software components](#task-1-install-and-configure-azure-hpc-ondemand-platform-software-components)
    - [Task 2: Review installation results](#task-2-review-installation-results)
  - [Exercise 4: Validate functionality of Azure HPC OnDemand Platform](#exercise-4-validate-functionality-of-azure-hpc-ondemand-platform)
    - [Task 1: Create jobs based on the default Azure HPC OnDemand Platform template](#task-1-create-jobs-based-on-the-default-azure-hpc-ondemand-platform-template)
    - [Task 2: Create jobs based on a non-default Azure HPC OnDemand Platform template](#task-2-create-jobs-based-on-a-non-default-azure-hpc-ondemand-platform-template)
  - [Exercise 5: Deprovision Azure HPC OnDemand Platform environment](#exercise-5-deprovision-azure-hpc-ondemand-platform-environment)
    - [Task 1: Terminate the cluster](#task-1-terminate-the-cluster)
    - [Task 2: Deprovision the Azure resources](#task-2-deprovision-the-azure-resources)

<!-- /TOC -->

# Azure HPC OnDemand Platform lab guide

## Requirements

- A Microsoft Azure subscription
- A work or school account with the Owner role in the Azure subscription
- A lab computer with:
  - Access to Azure
  - A web browser supported by the Azure portal (Microsoft Edge, Google Chrome, or Mozilla Firefox)

## Before the hands-on lab

Duration: 15 minutes

To complete this lab, you must verify that your account has sufficient permissions to the Azure subscription that you intend to use to deploy all required Azure resources. The Azure subscription must have a sufficient number of available virtual CPUs (vCPUs).

### Task 1: Validate the owner role assignment in the Azure subscription

1. From the lab computer, start a web browser, navigate to [the Azure portal](http://portal.azure.com), and, if needed, sign in with the credentials of the user account with the Owner role in the Azure subscription you'll be using in this lab.
1. In the Azure portal, use the **Search resources, services, and docs** text box to search for **Subscriptions**, and from the list of results, select **Subscriptions**.
1. On the **Subscriptions** blade, select the name of the subscription you intend to use for this lab.
1. On the subscription blade, select **Access control (IAM)**.
1. On the **Check access** tab, select the **View my access** button, and in the listing of role assignments, verify that your user account has the Owner role assigned to it.

### Task 2: Validate a sufficient number of vCPU cores

1. In the Azure portal, on the subscription blade, in the **Settings** section of the resource menu, select **Usage + quota**.
1. On the **Usage + quotas** blade, in the **Search** filters drop-down boxes, select the Azure region you intend to use for this lab, and then the **Microsoft.Compute** provider entry.

   > ![Note]: We recommend that you use the **South Central US** or the **West Europe** regions because these currently are more likely to increase the possibility of successfully raising quota limits for the Azure virtual machine (VM) SKUs required for this lab.

1. Review the listing of existing quotas and determine whether you have sufficient capacity to accommodate a deployment of the following vCPUs:

   - Standard BS Family vCPUs: **12**
   - Standard DDv4 Family vCPUs: **80**
   - Standard DSv3 Family vCPUs: **8**
   - Standard DSv5 Family vCPUs: **4**
   - Standard HBrsv2 Family vCPUs: **480**
   - Standard HBv3 Family vCPUs: **480**
   - Standard NV Family vCPUs: **6**
   - Total Regional Spot vCPUs: **960**
   - Total Regional vCPUs: **590**

1. If the number of vCPUs isn't sufficient, on the subscription's **Usage + quotas** blade, select **Request Increase**.
1. On the **Basic** tab of the **New support request** blade, specify the following settings, and then select **Next: Solutions >**:

   - Summary: **Insufficient compute quotas**
   - Issue type: **Service and subscription limits (quotas)**
   - Subscription: Enter the name of the Azure subscription you'll be using in this lab.
   - Quota type: **Compute-VM (cores-vCPUs) subscription limit increases**
   - Support plan: Enter the name of the support plan associated with the target subscription.

1. On the **Details** tab of the **New support request** blade, select the **Enter details** link.
1. On the **Quota details** tab of the **New support request** blade, specify the following settings, and then select **Save and continue**:

   - Deployment model: **Resource Manager**
   - Location: Enter the name of the target Azure region you intend to use in this lab.
   - Quotas: Enter the VM series and the new vCPU limit.

1. On the **Details** tab of the **New support request** blade, specify the following settings, and then select **Next: Review + create >**:

   - Advanced diagnostic information: **Yes**
   - Severity: **C - Minimal impact**
   - Preferred contact method: Choose your preferred option and provide your contact details.

1. On the **Review + create** tab of the **New support request** blade, select **Create**.

   > ![Note]: Typically, requests for quota increases are completed within a few hours. However, processing sometimes can take up to a few days.

## Exercise 1: Prepare for implementing the Azure HPC OnDemand Platform environment

Duration: 40 minutes

In this exercise you'll set up an Azure VM that you'll use for the lab environment deployment.

### Task 1: Provision an Azure VM running Linux

1. From the lab computer, start a web browser, navigate to [the Azure portal](http://portal.azure.com), and, if needed, sign in with credentials of the account with the Owner role in the Azure subscription you'll be using in this lab.
1. In the Azure portal, start a Bash session in **Cloud Shell**.

   > ![Note]: If prompted, in the **Welcome to Azure Cloud Shell** window, select **Bash (Linux)**. In the **You have no storage mounted** window, select **Create storage**.

1. In the **Bash** session, on the **Cloud Shell** pane, run the following command to select the Azure subscription in which you'll provision the Azure resources in this lab. In the following command, replace the `<subscription_ID>` placeholder with the value of the **subscriptionID** property of the Azure subscription you are using in this lab:

   > ![Note]: To list the subscription ID properties of all subscriptions associated with your account, run `az account list -otable --query '[].{subscriptionId: id, name: name, isDefault: isDefault}'`.

   ```bash
   az account set --subscription '<subscription_ID>'
   ```

1. In the **Bash** session, on the **Cloud Shell** pane, run the following command to select the Azure subscription in which you'll provision the Azure resources in this lab:

   ```bash
   az account set --subscription '<subscription_ID>'
   ```

1. Run the following commands to create an Azure resource group that will contain the Azure VM hosting the lab deployment tools. In the following commands, replace the `<Azure_region>` placeholder with the name of the Azure region you intend to use in this lab:

   > ![Note]: You can use the `az account list-locations -o table` command to list the names of Azure regions available in your Azure subscription:

   ```bash
   LOCATION='<Azure_region>'
   RGNAME='azhop-cli-RG'
   az group create --location $LOCATION --name $RGNAME
   ```

1. Run the following commands to download into the Cloud Shell home directory the Azure Resource Manager template and the corresponding parameters file. You'll use these to provision the Azure VM that will host the lab deployment tools:

   ```bash
   rm ubuntu_azurecli_vm_template.json -f
   rm ubuntu_azurecli_vm_template.parameters.json -f

   wget https://raw.githubusercontent.com/polichtm/az-hop/main/templates/ubuntu_azurecli_vm_template.json
   wget https://raw.githubusercontent.com/polichtm/az-hop/main/templates/ubuntu_azurecli_vm_template.parameters.json
   ```

1. Run the following command to provision the Azure VM that will host the lab deployment tools:

   ```bash
   az deployment group create \
   --resource-group $RGNAME \
   --template-file ubuntu_azurecli_vm_template.json \
   --parameters @ubuntu_azurecli_vm_template.parameters.json
   ```

   > ![Note]: When prompted, enter an arbitrary password that will be assigned to the **azureadm** user, which you'll use to sign in to the operating system of the Azure VM.
   > ![Note]: Wait until the provisioning completes. This should take about 3 minutes.

### Task 2: Deploy Azure Bastion

> ![Note]: Azure Bastion allows users to connect to Azure VMs without relying on public endpoints. It also provides protection against brute force exploits that target operating-system level credentials.

1. On the lab computer, in the browser window with the Azure portal, from the Bash session on the **Cloud Shell** pane, run the following commands to add a subnet named **AzureBastionSubnet** to the virtual network that you created in the previous task:

   ```bash
   RGNAME='azhop-cli-RG'
   VNETNAME='azcli-vnet'
   az network vnet subnet create --resource-group $RGNAME --vnet-name $VNETNAME --name AzureBastionSubnet --address-prefixes 192.168.3.0/24
   ```

1. Close the **Cloud Shell** pane.
1. In the Azure portal, use the **Search resources, services, and docs** text box to search for **Bastions** and from the list of results select **Bastions**.
1. On the **Bastions** blade, select **+ Create**.
1. On the **Create a Bastion** blade, on the **Basics** tab, specify the following settings, and then select **Review + create**.

   |Setting|Value|
   |---|---|
   |Subscription|Enter the name of the Azure subscription you are using in this lab.|
   |Resource group|**azhop-cli-RG**|
   |Name|**azhop-cli-bastion**|
   |Region|Enter the same Azure region that you used for deployment in the previous task of this exercise.|
   |Tier|**Basic**|
   |Virtual network|**azcli-vnet**|
   |Subnet|**AzureBastionSubnet (192.168.3.0/24)**|
   |Public IP address|**Create new**|
   |Public IP name|**azhop-cli-pip**|

1. On the **Review + create** tab of the **Create a Bastion** blade, select **Create**.

   > ![Note]: Wait for the deployment to complete before you proceed to the next exercise. The deployment could take up to 5 minutes to complete.

### Task 3: Install the az-hop toolset

> ![Note]: Ensure that your browser has the pop-up functionality enabled before you attempt to connect through Azure Bastion.

1. On the lab computer, in the browser window displaying the Azure portal, use the **Search resources, services, and docs** text box to search for **Virtual machines** and, from the **Virtual machines** blade, select **azcli-vm0**.
1. On the **azcli-vm0** blade, select **Connect**, from the drop-down menu, select **Bastion**, on the **azcli-vm0 \| Bastion** blade, enter **azureadm** as the user name, enter the password you set during the Azure VM deployment in the first task of this exercise, and then select **Connect**.
1. Within the SSH session to the Azure VM, run the following command to update the package manager list of available packages and their versions:

   ```bash
   sudo apt-get update
   ```

1. Run the following command to upgrade the local packages' versions, and confirm when prompted whether to proceed:

   ```bash
   sudo apt-get upgrade -y
   ```

1. Run the following command to install Git:

   ```bash
   sudo apt-get install git
   ```

1. Run the following commands to clone the **az-hop** repository:

   ```bash
   rm ~/az-hop -rf
   git clone --recursive https://github.com/Azure/az-hop.git -b v1.0.14
   ```

1. Run the following commands to install all the tools required to provision the **az-hop** environment:

   ```bash
   cd ~/az-hop/
   sudo ./toolset/scripts/install.sh
   ```

   > ![Note]: Wait until the script completes running, which could take up to 5 minutes.

### Task 4: Prepare the Azure subscription for deployment

1. Within the SSH session to the Azure VM, run the following command to sign in to the Azure subscription you are using in this lab:

   ```bash
   az login
   ```

1. Note the code displayed in the output of the command. Switch to your lab computer, open another tab in the browser window with the Azure portal, navigate to [the Microsoft Device Login page](https://microsoft.com/devicelogin), enter the code, and then select **Next**.
1. If prompted, sign in with the credentials of the user account with the Owner role in the Azure subscription you are using in this lab, select **Continue**, and then close the newly opened browser tab.
1. In the browser window with the Azure portal, within the SSH session to the Azure VM, run the following command to identify the Azure subscription you are connected to:

   ```bash
   az account show
   ```

1. Verify that the Azure subscription you are connected to is the one you want to use for this lab. If it isn't, run the following command to change the subscription, replacing the `<subscription_ID>` placeholder with the subscriptionID parameter value from the Azure subscription you want to use:

   ```bash
   az account set --subscription '<subscription_ID>'
   ```

1. Within the SSH session to the Azure VM, run the following command to ensure that the CycleCloud marketplace image is available in your Azure subscription:

   ```bash
   az vm image terms accept --offer azure-cyclecloud --publisher azurecyclecloud --plan cyclecloud-81
   ```

1. Run the following command to ensure that the Azure HPC Lustre marketplace image is available in your Azure subscription:

   ```bash
   az vm image terms accept --offer azurehpc-lustre --publisher azhpc --plan azurehpc-lustre-2_12
   ```

1. Run the following command to register the Azure NetApp Resource Provider:

   ```bash
   az provider register --namespace Microsoft.NetApp --wait
   ```

1. Run the following command to verify that the Azure Resource Provider has been registered:

   ```bash
   az provider list --query "[?namespace=='Microsoft.NetApp']" --output table
   ```

   > ![Note]: In the command output, verify that the value of **RegistrationState** is listed as **Registered**.

## Exercise 2: Implement Azure HPC OnDemand Platform cloud infrastructure

Duration: 90 minutes

In this exercise, you'll deploy the Azure HPC OnDemand Platform infrastructure.

### Task 1: Customize infrastructure components

You define an az-hop environment by using a configuration file named **config.yml**, which needs to reside in the root of the repository. The simplest way to create the environment is to clone the template file **config.tpl.yml**, and then modify the copied file's content. In this task, you'll review the file's content, and if needed set the target Azure region for deploying the Azure HPC OnDemand Platform infrastructure.

1. On the lab computer, in the browser window with the Azure portal, within the SSH session to the Azure VM, run the following commands to copy **config.tpl.yml** to **config.yml**:

   ```bash
   cp config.tpl.yml config.yml
   ```

1. Open the **config.yml** file using your preferred editor, such as Nano or vi:

   ```bash
   vi config.yml
   ```

1. Review the **config.yml** file content, and observe that it includes the following settings:

   - **location**: The name of the target Azure region.
   - **resource_group**: The name of the target resource group. You do have the option of using an existing resource group by setting **use_existing_rg** to **true**.
   - **anf**: Configuration properties of Azure NetApp Files resources.
   - **admin_user**: The name of the admin user account. (Its random password is autogenerated and stored in the Azure Key vault provisioned as part of the deployment.)
   - **network**: Configuration properties of the Azure virtual network into which the Azure resources hosting the infrastructure resources are deployed.
   - **jumpbox**, **ad**, **ondemand**, **grafana**, **scheduler**, **cyclecloud**, **winviz**, and **lustre**: Configuration properties of Azure VMs hosting the infrastructure components.
   - **users**: User accounts autoprovisioned as part of the deployment.
   - **queue_manager**: The name of the scheduler to be installed and configured, which is **openpbs** by default.
   - **authentication**: The authentication method, which is **basic** by default. You also have the option of using **OpenID Connect** instead.
   - **images**: The list of images that will be available for deployment of compute cluster nodes and their respective configuration.
   - **queues**: The list of node arrays of CycleCloud and their respective configuration.

1. If needed, change the name of the target Azure region set in the **config.yml** file to the one you are using in this lab, save the change, and then close the file.

### Task 2: Deploy Azure HPC OnDemand Platform infrastructure

1. Within the SSH session to the Azure VM, run the following command to generate a Terraform deployment plan that includes a list of all resources to be provisioned:

   ```bash
   ./build.sh -a plan
   ```

1. Review the generated list of resources, and then run the following command to trigger the Azure HPC OnDemand Platform infrastructure deployment:

   ```bash
   ./build.sh -a apply
   ```

   > ![Note]: Wait for deployment to complete, which should take about 20 minutes. Deployment is complete when the message **Apply complete! Resources: 124 added, 0 changed, 0 destroyed** displays.

### Task 3: Build images

The az-hop solution provides pre-configured Packer configuration files that can be used to build custom images. The utility script **./packer/build_image.sh** performs the build process and stores the resulting images in the Shared Image Gallery included in the deployed infrastructure.

1. On the lab computer, in the browser window displaying the Azure portal, within the SSH session to the Azure VM, run the following commands to build a custom image based on the **azhop-centos79-v2-rdma-gpgpu.json** configuration file.

   > ![Note]: The image creation process based on the **azhop-centos79-v2-rdma-gpgpu.json** configuration file relies on a **Standard_d8s_v3** SKU Azure VM.

   ```bash
   cd packer/
   ./build_image.sh -i azhop-centos79-v2-rdma-gpgpu.json
   ```

   > ![Note]: Disregard any warning messages.

   > ![Note]: Wait for the process to complete. This could take about 20 minutes.

   > ![Note]: The image creation process based on the **centos-7.8-desktop-3d.json** configuration file relies on a **Standard_NV6** SKU Azure VM. If you manage to obtain a sufficient number of quotas to provision a **Standard_NV6**-based Azure VM, you can proceed directly to the next step. Otherwise, open the file **centos-7.8-desktop-3d.json**, replace the entry **Standard_NV6** with **Standard_D8s_v3**, save the change, and then close the file. While such a step is likely to affect the functionality of compute resources based on this image, it's meant strictly as a workaround that facilitates the next step in the process of implementing the Azure HPC OnDemand Platform lab environment.

1. Within the SSH session to the Azure VM, run the following command to build a custom image based on the **centos-7.8-desktop-3d.json** configuration file:

   ```bash
   ./build_image.sh -i centos-7.8-desktop-3d.json
   ```

   > ![Note]: Wait for the process to complete. This could take up to 40 minutes.

### Task 4: Review deployment results

1. On the lab computer, in the browser window displaying the Azure portal, open another tab, and then navigate to the Azure portal.
1. On the Azure portal, use the **Search resources, services, and docs** text box to search for **Azure compute galleries**, and then select **Azure compute galleries** from the list of results.
1. On the **Azure compute galleries** blade, select the entry whose name starts with the prefix **azhop**, and then, on the compute gallery blade, verify that the gallery includes two VM image definitions.
1. In the Azure portal, use the **Search resources, services, and docs** text box to search for **Azure virtual machines**, and then select **Virtual machines** from the list of results.
1. On the **Virtual machines** blade, review the listing of the provisioned virtual machines.

   > ![Note]: If needed, filter the VM listings by setting the resource group criterion to **azhop**.

1. Close the newly opened browser tab displaying the **Virtual machines** blade in the Azure portal.

### Task 5: Generate passwords for user and admin accounts

1. On the lab computer, in the browser window displaying the Azure portal, within the SSH session to the Azure VM, run the following command to generate the password for the **clusteradmin** and **clusteruser** accounts defined in the **config.yml** configuration file:

   ```bash
   cd ~/az-hop/
   ./create_passwords.sh
   ```

1. Run the following command to display the newly generated password for the **clusteradmin** account:

   ```bash
   ./bin/get_secret clusteradmin
   ```

   > ![Note]: Record the password because you'll need it later in this lab.

   > ![Note]: The **./bin/get_secret utility script** retrieves the password of the user you specify as its parameter from the Azure Key vault, which is part of the Azure HPC OnDemand Platform infrastructure you deployed in the previous exercise.

## Exercise 3: Install and configure Azure HPC OnDemand Platform software components

Duration: 50 minutes

In this exercise, you'll install and configure software components that form the Azure HPC OnDemand Platform solution.

> ![Note]: You'll perform this installation by using Ansible playbooks, which supports the setup of individual components as well as the setup of the entire solution. In either case, it's necessary to account for dependencies between components. The setup script **install.sh** in the repository's root directory performs the installation in the intended order. The components include: **ad**, **linux**, **add_users**, **lustre**, **ccportal**, **cccluster** (this component requires that custom images be present in the compute gallery), **scheduler**, **ood**, **grafana**, **telegraf**, and **chrony**.

### Task 1: Install and configure Azure HPC OnDemand Platform software components

1. On the lab computer, in the browser window displaying the Azure portal, within the SSH session to the Azure VM, run the following command to invoke the Azure HPC OnDemand Platform software components installation:

   ```bash
   cd ~/az-hop/
   ./install.sh
   ```

   > ![Note]: "Wait for the process to complete, which could take up to 30 minutes."

   > ![Note]: In case of a transient failure, you can rerun the install script because most of the settings are idempotent. In addition, the script has a checkpointing mechanism that creates component-specific files with the **.ok** extension in the playbooks directory and checks for their presence during subsequent runs. If you want to reapply the configuration to an existing component, delete the corresponding **.ok** file, and then rerun the install script.

### Task 2: Review installation results

1. Once the installation completes, on the lab computer, in the browser window displaying the Azure portal, within the SSH session to the Azure VM, run the following command to display the Azure HPC On-Demand Platform portal's URL:

   ```bash
   grep ondemand_fqdn playbooks/group_vars/all.yml
   ```

   > ![Note]: Record this value. You'll need it later in this lab.

1. From the lab computer, start a web browser, navigate to the URL of the Azure HPC On-Demand Platform portal you identified earlier in this task and, when prompted, sign in with the **clusteradmin** user account and its password you identified in the previous step.
   > ![Note]: You'll be presented with the **Azure HPC On-Demand Platform** dashboard. Review its interface, starting with the top-level menu, which provides access to **Apps**, **Files**, **Jobs**, **Clusters**, **Interactive Apps**, **Monitoring**, and **My Interactive Sessions** menu items.

1. From the **Monitoring** menu, select **Azure CycleCloud** and, when presented with the page titled **App has not been initialized or does not exist**, select **Initialize App**.

   > ![Note]: This prompt is a reflection of the OnDemand component's architecture, which the Azure HPC OnDemand Platform solution relies on to implement its portal. The shared frontend creates Per User NGINX (PUN) processes to provide connectivity to such components as **Azure CycleCloud**, **Grafana**, or **Robinhood Dashboard**.

1. On the **Azure CycleCloud for Azure HPC On-Demand Platform** page, note the presence of a configuration of a cluster named **pbs1**.
1. On the **pbs1** page, select the **Arrays** tab, and note that it contains six entries, representing queue definitions you reviewed earlier in the **config.yml** file.

## Exercise 4: Validate functionality of Azure HPC OnDemand Platform

Duration: 55 minutes

In this exercise, you'll validate Azure HPC OnDemand Platform functionality.

### Task 1: Create jobs based on the default Azure HPC OnDemand Platform template

1. On the lab computer, in the browser window displaying the Azure HPC On-Demand Platform portal, navigate to the Dashboard page.
1. From this page, select the **Jobs** menu, and then from the drop-down menu, select **Job Composer**.
1. On the **Jobs** page, select **+ New job**, and then from the drop-down menu, select **From Default Template**.

   > ![Note]: This will automatically create a job named **(default) Sample Sequential Job** that targets the **execute** CycleCloud array. To identify the content of the job script, ensure that the newly created job is selected, and then review the **Script contents** pane.

1. Repeat the previous step twice to create two additional jobs based on the default template.

   > ![Note]: The default job template contains a trivial script that runs `echo "Hello World"`.

1. Verify that all three jobs are currently in the **Not Submitted** state. To submit them, select each one of them, and then select **Submit**.

   > ![Note]: The status of the jobs should change to **Queued**.

1. On the lab computer, in the browser window displaying the Azure HPC On-Demand Platform portal, select the **Azure HPC On-Demand Platform** header, select the **Monitoring** menu, and from the drop-down list, select **Azure CycleCloud**.
1. On the **Azure CycleCloud for Azure HPC On-Demand Platform** portal, monitor the status of the cluster. Note that the number of nodes increases to **3**, which initially are listed in the **acquiring** state.
1. On the **Nodes** tab, verify that **execute** appears in the **Template** column, the **Nodes** column contains the entry **3**, and the **Last status** column displays the **Creating VM** message.
1. In the **Azure CycleCloud for Azure HPC On-Demand Platform** portal, on the **pbs1** page, select the **Scalesets** tab. Note the presence of a scaleset that hosts the cluster nodes, and has its size set to **3**.
1. Select the entry on the **Nodes** tab, and then review the details of the cluster nodes in the lower section of the page, including the name of each node, their status, the number of cores, and the placement group.
1. Navigate to the **Azure HPC On-Demand Platform** portal, select the **Jobs** menu, and from the drop-down menu, select **Active jobs**.
1. On the **Active jobs** page, verify that three active jobs are listed in the **Queued** status.
1. Navigate to the **Azure CycleCloud for Azure HPC On-Demand Platform** portal, and then monitor the progress of node provisioning.

   > ![Note]: Wait until the status of nodes changes to **Ready**, which should take about 5 minutes.

1. After the nodes are listed with the **Ready** status, switch to the **Active jobs** page, refresh it, and then note that the jobs are no longer listed.

   > ![Note]: If the jobs are still listed as queued, wait for a few more minutes, and then refresh the page again.

1. Navigate back to the **Azure CycleCloud for Azure HPC On-Demand Platform** portal and monitor the node status until it changes to terminating, which will eventually result in their deletion.
1. On the **Azure CycleCloud for Azure HPC On-Demand Platform** portal, on the **pbs1** page, select the **Scalesets** tab.
1. Note that the scaleset hosting the cluster nodes persists, but its size is set to **0**.

### Task 2: Create jobs based on a non-default Azure HPC OnDemand Platform template

1. On the lab computer, in the browser window, switch back to the **Azure HPC On-Demand Platform** portal.
1. Select the **Jobs** menu, and then from the drop-down menu, select **Job Composer**.
1. On the **Jobs** page, select **Templates**.
1. On the **Templates** page, in the list of predefined templates, select the **Intel MPI PingPong** entry, and then select **Copy Template**.

   > ![Note]: The Message Passing Interface (MPI) ping-pong tests measure network *latency* and throughput between nodes on the cluster by sending packets of data back and forth between paired nodes repeatedly. The latency is the average of half of the time that it takes for a packet to make a round trip between a pair of nodes, in microseconds. The *throughput* is the average rate of data transfer between a pair of nodes, in megabytes per second.

1. On the **New Template** page, specify the following settings, and then select **Save**.

   |Setting|Value|
   |---|---|
   |Name|**Intel MPI PingPong v2**|
   |Cluster|**AZHOP - Cluster**|
   |Name|**<p>A very basic template for running Intel MPI ping pong on hb120v2</p>**|

1. On the **Templates** page, select the newly created template, and then select **View Files**.
1. On the page listing the files that are part of the template, in the **pingpong.sh** row, select the square icon containing the vertical ellipsis symbol, and then from the drop-down menu, select **Edit**.
1. On the page displaying the content of the **pingpong.sh** script, in the third line, replace `slot_type=hb120v3` with `slot_type=hb120v2`, and then select **Save**.
1. Navigate to the **Jobs** page, select **+ New job**, from the drop-down menu, select **From Template**, on the **Templates** page, ensure that the **Intel MPI PingPong v2** entry is selected, and then select **Create New Job**."

   > ![Note]: This will automatically create a job named **Intel MPI PingPong v2** that targets the **hb120v2** CycleCloud array.

1. Repeat the previous step twice to create two additional jobs based on the **Intel MPI PingPong v2** template.
1. Note that, as before, all three jobs are currently in the **Not Submitted** state. To submit them, select each one of them, and then select **Submit**.

   > ![Note]: The status of the jobs should change to **Queued**.

1. Navigate to the **Azure CycleCloud for Azure HPC On-Demand Platform** portal and monitor the progress of node provisioning.

   > ![Note]: Wait until the status of nodes changes to **Ready**. This should take about 5 minutes.

1. When the nodes are listed with the **Ready** status, switch back to the **Active jobs** page, refresh it, and note that the jobs are no longer listed there.

   > ![Note]: If the jobs are still listed as queued, wait for a few minutes, and then refresh the page again.

1. Navigate to the **Azure CycleCloud for Azure HPC On-Demand Platform** portal and monitor the node status until it changes to terminating, which will eventually result in their deletion.
1. On the **Azure CycleCloud for Azure HPC On-Demand Platform** portal, on the **pbs1** page, select the **Scalesets** tab, and note that the scaleset hosting the cluster nodes persists but its size is set to **0**.
1. To review the job output, switch to the **Azure HPC On-Demand Platform** portal. Select the **Jobs** menu, and from the drop-down menu, select **Job Composer**.
1. On the **Jobs** page, select any of the **Intel MPI PingPong v2** job entries, and then in the **Folder Contents** section, select **PingPong.o3**.

   > ![Note]: This will automatically open another web browser tab displaying the output of the job.

## Exercise 5: Deprovision Azure HPC OnDemand Platform environment

Duration: 30 minutes

In this exercise, you'll deprovision the Azure HPC OnDemand Platform lab environment.

### Task 1: Terminate the cluster

1. On the lab computer, in the browser window, navigate to the **Azure CycleCloud for Azure HPC On-Demand Platform** portal.
1. On the **pbs1** page, select **Terminate**, and when prompted for confirmation, select **OK**.
1. Monitor the progress of terminating the cluster.

   > ![Note]: Ensure that all nodes and scaleset are deleted before you proceed to the next step.

### Task 2: Deprovision the Azure resources

1. On the lab computer, switch to the browser window displaying the Azure portal, and then start a Bash session in **Cloud Shell**.
1. From the Bash session in the **Cloud Shell** pane, run the following command to initiate the deprovisioning of the Azure HPC OnDemand Platform infrastructure you created and evaluated in this lab:

   ```bash
   az group delete --name azhop --yes
   ```

   > ![Note]: Wait for the resource deprovisioning to complete. This should take about 20 minutes.
