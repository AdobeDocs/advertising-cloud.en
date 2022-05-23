---
title: 
description: 
---
# Create an Audience Source to Activate First-Party Audiences from [!DNL Adobe Real-time Customer Data Profile (CDP)]

*Beta feature*

Create a source to import audiences to your DSP account or an advertiser account.


For users looking to activate their Real-Time CDP audiences through the Advertising Cloud DSP destination within the Real-Time CDP dashboard, please refer to the Advertising Cloud DSP connections page. There you will find helpful tips on managing and activating the Advertising Cloud destination, selecting segments, as well as accessing control permissions. 

Users will need to add Real-Time CDP as a Source in their Advertising Cloud DSP account by following the below steps: 

1. In the main menu, click **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Click [!UICONTROL Add Source].

1. In the [!UICONTROL Select a Type] menu, select the source type.

     [!UICONTROL RT-CDP] (the [!DNL Adobe Real-time Customer Data Profile](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html) is the only option.

1. Specify the [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* or *[!UICONTROL Account]*.

1. Enter the remaining [source settings](source-settings.md).

     Keep a copy of the [!UICONTROL Source Key] that is generated. You'll need the value later.

1. Click **[!UICONTROL Save]**.

1.  In Experience Platform, create an [Adobe Advertising Cloud DSP destination](???) using the [!UICONTROL Source Key] that was generated in the source settings. <!-- probably just need a link to our page in particular, which should link out to instructions. For instructions on how , see the [Destinations overview](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html#steps). -->
