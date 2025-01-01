# Azure Virtual Machine Insights

The 'Azure Virtual Machine Insights' workbook offers a comprehensive view of your Azure Virtual Machines (VMs) resources.

It enables you to delve into and compare key metrics effortlessly, gaining insights into usage trends, optimizing performance, and guiding strategic decisions effectively.

![VMInsights](https://github.com/user-attachments/assets/9e25a32d-1afa-4e03-bc74-1ecd8e382042)



### Overview

The Monitor dashboard provides a comprehensive view of all Virtual Machine (VM) metrics, enabling you to analyze their behavior and compare metrics across different VMs.

![image](https://github.com/user-attachments/assets/d8b271ce-63d9-4ab9-9b75-3b55d3d6d74b)


### Monitor

<ins>CPU & Memory metrics</ins>

![image](https://github.com/user-attachments/assets/58a067ba-58b8-47bd-ab19-2897b1b6cc89)

<ins>Network metrics</ins>

![image](https://github.com/user-attachments/assets/3a2cf428-75af-4583-9624-7da77b4f6047)

<ins>Disks metrics</ins>

![image](https://github.com/user-attachments/assets/d812a9ae-8b16-432d-b93b-7143a3604825)

### Inventory

The Inventory dashboard offers a comprehensive overview of all Virtual Machine (VM) resources.

![image](https://github.com/user-attachments/assets/658a1bf2-fbd8-4de9-9f97-4d70c2442979)



## Introduction

Managing multiple VMs (Virtual Machines) requires effective management, performance comparison, and operational oversight — this functionalities facilitated by this workbook.

### Structure and Views

#### Structure

This workbook contains 3 main parts:
- **Overview** - Holistic view of Azure Virtual Machines resources.
- **Monitor** - Holistic view of Azure Virtual Machines Metrics
- **Inventory** - Holistic view of Azure Virtual Machines Inventory.

#### Views

Types of views this workbook provides:

##### Overview

- Virtual Machines
  - Name
  - Resource Group
  - Location
  - Size
  - Operating system
  - Status
  - Time Created
  - OS Disk
  - Tags
  - Details

> The information displayed uses [KQL](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/) queries to query the [Azure Resource Graph](https://learn.microsoft.com/en-us/azure/governance/resource-graph/overview).

##### Monitor

- Overview
  - Percentage CPU (Avg)
  - Available Memory Bytes (Avg)
- Network
  - Network In Total (Sum)
  - Network Out Total (Sum)
- Disk
  - Overview
    - Disk Read Bytes (Sum)
    - Disk Write Bytes (Sum)
    - Disk Read Operations/Sec (Avg)
    - Disk Write Operations/Sec (Avg)
  - OS Disk
    - OS Disk Read Bytes/Sec (Avg)
    - OS Disk Write Bytes/Sec (Avg)
    - OS Disk Read Operations/Sec (Avg)
    - OS Disk Write Operations/Sec (Avg)
    - OS Disk Target Bandwidth (Avg)
    - OS Disk Target IOPS (Avg)
    - OS Disk Used Burst BPS Credits Percentage (Avg)
    - OS Disk Used Burst IO Credits Percentage (Avg)
    - OS Disk Latency (Preview) (Avg)
    - OS Disk Max Burst Bandwidth (Avg)
    - OS Disk Max Burst IOPS (Avg)
    - OS Disk Queue Depth (Avg)
    - OS Disk IOPS Consumed Percentage (Avg) **
    - OS Disk Bandwidth Consumed Percentage (Avg) **
    - Premium OS Disk Cache Read Hit (Avg) **
    - Premium OS Disk Cache Read Miss (Avg) **
  - Temp Disk
    - Temp Disk Read Bytes/Sec (Avg)
    - Temp Disk Write Bytes/Sec (Avg)
    - Temp Disk Read Operations/Sec (Avg)
    - Temp Disk Write Operations/Sec (Avg)
    - Temp Disk Latency (Preview) (Avg)
    - Temp Disk Queue Depth (Avg)
  - Data Disk
    - Data Disk Read Bytes/Sec (Avg)
    - Data Disk Write Bytes/Sec (Avg)
    - Data Disk Read Operations/Sec (Avg)
    - Data Disk Write Operations/Sec (Avg)
    - Data Disk Max Burst IOPS (Avg)
    - Data Disk Queue Depth (Avg)
    - Data Disk Used Burst IO Credits Percentage (Avg)
    - Data Disk Used Burst BPS Credits Percentage (Avg)
    - Data Disk Target IOPS (Avg)
    - Data Disk Target Bandwidth (Avg)
    - Data Disk Bandwidth Consumed Percentage (Avg)
    - Data Disk IOPS Consumed Percentage (Avg)
    - Data Disk Latency (Preview) (Avg)
    - Data Disk Max Burst Bandwidth (Avg)
- Flows
  - Inbound Flows (Avg)
  - Outbound Flows (Avg)
  - Inbound Flows Maximum Creation Rate (Avg)
  - Outbound Flows Maximum Creation Rate (Avg)
- VM Cached vs Uncached
  - VM Cached Used Burst IO Credits Percentage (Avg)
  - VM Uncached Used Burst IO Credits Percentage (Avg)
  - VM Cached Used Burst BPS Credits Percentage (Avg)
  - VM Uncached Used Burst BPS Credits Percentage (Avg)
  - VM Cached IOPS Consumed Percentage (Avg) **
  - VM Uncached IOPS Consumed Percentage (Avg) **
  - VM Cached Bandwidth Consumed Percentage (Avg) **
  - VM Uncached Bandwidth Consumed Percentage (Avg) **
- CPU Credits
  - CPU Credits Consumed (Avg) ***
  - CPU Credits Remaining (Avg) ***
- Other
  - VM Availability Metric (Preview) (Avg)

> ** Only available on VM series that support premium storage.

> *** Only available on B-series burstable VMs.

##### Inventory

- Virtual Machines
  - Count by Subscription Id
  - Count by Resource Group
  - Count by Location
  - Count by VM Type
  - Count by Power State
  - Count by OS Type
  - Count by Operation System
  - Count by Publisher
  - Count by Offer
  - Count by HyperV Generation
  - Count by Hibernation Enabled

### Filters

This workbook support to filter by:

- Subscription(s)
- Resource Group(s)
- Virtual Machine(s)
- Time range

## How to use it?

Importing this Workbook to your Azure environment is quite simple.

Follow this steps to use the Workbook:

- Login to [Azure Portal](https://portal.azure.com/) <img src="https://user-images.githubusercontent.com/69309933/172941966-9e030031-6ccb-4ebf-bd2b-04bb623e5ff7.png" width="20" height="20">
- Go to _'Azure Workbooks'_

<img src="https://user-images.githubusercontent.com/69309933/172806635-14051976-328e-4623-96ab-0dd6a7bc7817.png" width="350">

- Click on _'+ Create'_

<img src="https://user-images.githubusercontent.com/69309933/172807465-cced3466-0669-423b-87b3-8fa70fdbf1d1.png" width="350">

- Click on _'+ New'_

<img src="https://user-images.githubusercontent.com/69309933/172807547-52d790ce-7852-4b4b-a81f-81e8b7fac26e.png" width="350"> 

- Open the Advanced Editor using the _'</>'_ button on the toolbar

<img src="https://user-images.githubusercontent.com/69309933/172807673-dfc63741-0c40-47c0-ab58-d39309b06e69.png" width="700"> 

- Select the _'Gallery Template'_ (step 1)
- Replace the JSON code with this JSON code [Azure Virtual Machines Insights JSON](https://github.com/dolevshor/Azure-VirtualMachines-Insights/blob/main/Workbook/Azure%20Virtual%20Machines%20Insights.workbook) (step 2)

  - We use the _Gallery Templaty type_ (step 1), so we need to use the _'Azure Virtual Machines Insights.workbook'_ and not the _'Azure Virtual Machines Insights.json'_.
- Click _'Apply'_ (step 3)

<img src="https://user-images.githubusercontent.com/69309933/172807762-17aec6f9-4a81-4d5b-9017-673a0ab6b26e.png" width="700"> 

- Click in the ‘Save’ button on the toolbar

![image](https://github.com/user-attachments/assets/6440243d-cd56-4a09-b7be-0b5dd6eb72b0)

- Select a name and where to save the Workbook:
  - Title: _'Azure Virtual Machines Insights'_
  - Subscription: <_Subscription Name_>
  - Resource group: <_Resource Group Name_>
  - Location: <_Region_>
- Click _'Save'_
  
The Workbook is ready to use!
- Click on _'Workbooks'_
- Click on _'Azure Virtual Machines Insights'_ Workbook.

Start using the Workbook and analyze your Azure Vierual Machines (VMs) resources.<br/>
