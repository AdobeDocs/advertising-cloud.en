---
title: 
description: 
feature: DSP Audiences
---
# About Activating Authenticated Segments from Audience Sources

<!-- Doesn't specifically explain what you can do in our UI -->
*Beta feature*

Advertising Cloud DSP can ingest first-party segments comprised of authenticated signals built within a customer data platform (CDP), which you can use as targets for your placements.

For advertisers with Adobe Experience Platform who use the [the [!DNL Adobe Real-time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), [destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) are connections to external platforms that allow seamless data activation. For example, you can use destinations to activate your known customer relationships (such as hashed email addresses) for targeted advertising across digital formats supported by DSP.   

<!-- need link to our page in particular -->See the Adobe Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html) for more information, including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html)and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html). 

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->
1. To XXX, you must [allow DSP to translate customer data segments into [!DNL LiveRamp RampIDs]](source-activate.md) that are recognizable in a biddable environment. This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration.

2. [Create an audience source](source-create.md).

3. [Configure a [!DNL Real-time CDP] destination connection in Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-dsp-destination.html).<!-- Verify URL once it's published. -->

For additional support, contact your [!DNL Adobe] account team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Adobe Advertising Cloud DSP Destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-dsp-destination.html)<!-- Verify URL once it's published. -->
>* [Activate Authenticated Segments from Durable ID Partners](source-activate.md)<!-- title?-->
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
