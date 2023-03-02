---
title: Upgrade site customizations for SharePoint
description: Learn about potential issues and get recommendations for upgrading SharePoint 2010 site customizations to SharePoint.
ms.date: 06/07/2022
ms.assetid: 4b515860-69ae-4af8-8013-cd071c0ddca6
ms.localizationpriority: medium
---


# Upgrade site customizations for SharePoint
Learn about potential issues and get recommendations for upgrading your SharePoint 2010 site customizations to SharePoint.
SharePoint introduces significant changes to the user interface (UI) that let you customize sites using faster, more agile components. But when you upgrade from SharePoint 2010, you might encounter some issues with the new components that have been built into SharePoint to handle the improvements to the UI.
  
    
    

This article will help SharePoint developers and those responsible for administering the upgrade process from SharePoint 2010 to identify potential problems after upgrading.
## General recommendations for upgrading

In general, we recommend that you create a new "evaluation" site where you can test your customizations and redesign them for a SharePoint environment. For more information about creating an evaluation site collection, see  [Upgrade a site collection](/sharepoint/upgrade-and-update/upgrade-a-site-collection-to-sharepoint-2013).
  
    
    

### Upgrading custom components

Table 1 lists the possible after-upgrade problems for custom components and information about how to address them.
  
    
    

**Table 1. Custom components affected by upgrading to SharePoint**


|**If you have customized**|**You might encounter**|
|:-----|:-----|
|CSS styles  <br/> |During upgrade, your site will revert to the CSS files referred to in the default.master page. As a result, any customizations you have made to the appearance of your pages will change, and pages will render with the default styles found in a default installation.  <br/> |
|Themes  <br/> |For SharePoint 2010, you may have created custom themes that define a corporate branding for an entire site. You create these as .thmx files that can be uploaded to the site collection and applied by the administrator.  <br/> In SharePoint, the theming engine has been completely redesigned to be more flexible and powerful and to provide for easier future upgrades. As a result of this redesign, upgrading from SharePoint 2010 to SharePoint themes is not supported and will require you to re-create them for SharePoint.  <br/> |
|Web templates  <br/> |Web templates were introduced in SharePoint 2010 to provide a way to package features, layouts, styles, and other components that you can then use to create new webs. They are similar in function to creating site definitions, but with web templates, you can add publishing features.  <br/> Due to the changes made in SharePoint, your customized web templates will not work immediately after upgrade.  <br/> To see what changes have been made to web templates and to fix issues resulting from this, see  [Upgrade web templates for SharePoint](upgrade-web-templates-for-sharepoint.md) for recommendations and best practices. <br/> |
|Master pages  <br/> |During upgrade, any references to custom master pages you have created are reverted back to the default.master page. This may cause errors in SharePoint due to references on the custom page to missing components.  <br/> To fix this, you have to change the references to any custom master pages.  <br/> |
   

## See also
<a name="bk_addresources"> </a>


-  [Plan to upgrade a site collection](https://technet.microsoft.com/library/ff191199.aspx)
    
  
-  [Branding issues that may occur when upgrading to SharePoint](/SharePoint/upgrade-and-update/branding-issues-that-may-occur-when-upgrading-to-sharepoint-2013)
    
  
-  [Upgrade a site collection](/sharepoint/upgrade-and-update/upgrade-a-site-collection-to-sharepoint-2013)
    
  
-  [Troubleshoot site collection upgrade issues](/sharepoint/troubleshoot/administration/troubleshoot-site-collection-upgrade-issue)
    
  

