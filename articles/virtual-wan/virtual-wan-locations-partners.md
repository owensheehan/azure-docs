---
title: 'Azure Virtual WAN partners and locations | Microsoft Docs'
description: This article contains a list of Azure Virtual WAN partners and hub locations.
services: virtual-wan
author: cherylmc

ms.service: virtual-wan
ms.topic: conceptual
ms.date: 04/27/2021
ms.author: cherylmc
ms.custom: references_regions
# Customer intent: As someone with a networking background, I want to find a Virtual WAN partner
---
# Virtual WAN partners and virtual hub locations

This article provides information on Virtual WAN supported regions and partners for connectivity into Virtual Hub.

Azure Virtual WAN is a networking service that provides optimized and automated branch-to-branch connectivity through Azure. Virtual WAN lets you connect and configure branch devices to communicate with Azure. Connection and configuration can be done either manually, or by using provider devices through a Virtual WAN partner. Using partner devices allows you ease of use, simplification of connectivity, and configuration management.

Connectivity from the on-premises device is established in an automated way to the Virtual Hub. A virtual hub is a Microsoft-managed virtual network. The hub contains various service endpoints to enable connectivity from your on-premises network (vpnsite). 

## <a name="automation"></a>Branch IPsec connectivity automation from partners

Devices that connect to Azure Virtual WAN have built-in automation to connect. This is typically set up in the device-management UI (or equivalent), which sets up the connectivity and configuration management between the VPN branch device to an Azure Virtual Hub VPN endpoint (VPN gateway).

The following high-level automation is set up in the device console/management center:

* Appropriate permissions for the device to access Azure Virtual WAN Resource Group
* Uploading of Branch Device into Azure Virtual WAN
* Automatic download of Azure connectivity information
* Configuration of on-premises branch device 

Some connectivity partners may extend the automation to include creating the Azure Virtual Hub VNet and VPN Gateway. If you want to know more about automation, see [Automation guidelines for Virtual WAN partners](virtual-wan-configure-automation-providers.md).

## <a name="partners"></a>Branch IPsec Connectivity partners

[!INCLUDE [partners](../../includes/virtual-wan-partners-include.md)]

The following partners are slated on our roadmap based on a terms sheet signed between the companies indicating the scope of work to automate IPsec connectivity between the partner device and Azure Virtual WAN VPN Gateways: 128 Technologies, Arista, F5 Networks, Oracle SD-WAN (Talari), and SharpLink.

## Partners with integrated Virtual Hub offerings

In addition to having automated branch office IPsec connectivity, some partners offer **Network Virtual Appliances (NVAs)** that can be integrated directly into the Azure Virtual WAN hub.  This allows customers the option to terminate their branch connections into a compatible third-party appliance in the Virtual Hub.  

Partners that offer NVA in the Virtual WAN Hub must:

* Have implemented IPsec Connectivity Automation from their branch device and have on-boarded their NVA offering to Azure Virtual WAN hub.
* Have an existing Network Virtual Appliance offer available in Azure Marketplace.

If you are a partner and have questions about the Managed NVA in the Virtual Hub offering, contact us by sending email to vwannvaonboarding@microsoft.com

## Integrated Virtual Hub NVA partners

These partners have **Managed Application** offers that are available now to deploy into the Virtual WAN hub.

|Partners|Configuration/How-to/Deployment Guide|
|---|---|
|[Barracuda Networks](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/barracudanetworks.barracuda_cloudgenwan_gateway?tab=Overviewus/marketplace/apps/barracudanetworks.barracuda_cloudgenwan_gateway?tab=Overview)| [Barracuda CloudGen WAN Deployment Guide](https://campus.barracuda.com/product/cloudgenwan/doc/91980640/deployment/)|
|[Cisco Cloud Service Router(CSR) VWAN](https://aka.ms/ciscoMarketPlaceOffer)| The integration of the Cisco SD-WAN solution with Azure virtual WAN enhances Cloud OnRamp for Multi-Cloud deployments and enables configuring Cisco Catalyst 8000V Edge Software (Cisco Catalyst 8000V) as a network virtual appliance (NVA) in Azure Virtual WAN Hubs. [View  Cisco SD-WAN Cloud OnRamp, Cisco IOS XE Release 17.x Configuration Guide](https://www.cisco.com/c/en/us/td/docs/routers/sdwan/configuration/cloudonramp/ios-xe-17/cloud-onramp-book-xe/cloud-onramp-multi-cloud.html#Cisco_Concept.dita_c61e0e7a-fff8-4080-afee-47b81e8df701) 
|[VMware SD-WAN in Virtual WAN Hub](https://sdwan.vmware.com/partners/microsoft) | During the Public Preview of VMware SD-WAN into VWAN hub, VMware requires the customer to register by sending an email to vhubsupport@vmware.com. [VMware SD-WAN in Virtual WAN Hub Deployment Guide](https://kb.vmware.com/s/article/82746)|

The following partners are slated to bring NVA in the Virtual Hub offers in the near future: Aviatrix, Citrix and Versa Networks.

## <a name="locations"></a>Locations

[!INCLUDE [Virtual WAN regions file](../../includes/virtual-wan-regions-include.md)]

## Next steps

* For more information about Virtual WAN, see the [Virtual WAN FAQ](virtual-wan-faq.md).

* For more information about how to automate connectivity to Azure Virtual WAN, see [Automation guidelines for Virtual WAN partners](virtual-wan-configure-automation-providers.md).
