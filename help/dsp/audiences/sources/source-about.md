---
title: About Activating Authenticated Segments from Audience Sources
description: Learn about ingesting first-party segments from a customer data platform.
feature: DSP Audiences
---
# About Activating Authenticated Segments from Audience Sources

<!-- Doesn't specifically explain what you can do in our UI -->
*Beta feature*

Advertising Cloud DSP can ingest first-party segments comprised of authenticated signals built within a customer data platform (CDP). You can use the ingested segments as targets for your placements.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP is integrated with the [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), which is part of the Adobe Experience Platform.

In [!DNL Real-time CDP], *destinations* are connections to external data platforms that allow seamless data activation. For example, you can use destinations to activate your known customer relationships (such as hashed email addresses) for targeted advertising across digital formats supported by DSP.

For more information about destinations, see the Experience Platform [Destinations Guide](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), including an overview of the product, instructions for [creating destination workspaces](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) and [creating destination connections](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), and [activating data to destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html). 

### Workflow for Using the DSP Integration with [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Allow DSP to translate customer data segments into [!DNL LiveRamp RampIDs]](source-durable-id.md) that are recognizable in a biddable environment.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Create an audience source](source-create.md) to import audiences to your DSP account or an advertiser account.

1. [Configure a [!DNL Real-Time CDP] destination connection in Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).<!-- Verify URL once it's published. -->

For additional support, contact your [!DNL Adobe] account team or `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Activate Authenticated Segments from Durable ID Partners](source-durable-id.md)<!-- title?-->
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Destinations catalog overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [About Audience Management](audience-about.md)
