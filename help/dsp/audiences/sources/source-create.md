---
title: Create an Audience Source to Activate First-Party Audiences
description: 
feature: DSP Audiences
---
# Create an Audience Source to Activate First-Party Audiences

*Beta feature*

<!-- Will this remain for admin users/Adobe account teams only? -->

Create a source to import audiences to your DSP account or an advertiser account. Currently, you can import audiences from [!DNL Adobe Real-time Customer Data Profile (CDP)].

After you create a source for [the [!DNL Adobe Real-time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), you'll need to activate your [!DNL Real-Time CDP] audiences through the Adobe Advertising Cloud DSP destination within [!DNL Real-Time CDP] to begin importing them. 

1. In the main menu, click **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Click [!UICONTROL Add Source].

1. In the [!UICONTROL Select a Type] menu, select the source type.

   [!UICONTROL RT-CDP] (the [!DNL Adobe Real-time Customer Data Profile](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html) is the only option.

1. Specify the [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* or *[!UICONTROL Account]*.

1. Enter the remaining [source settings](source-settings.md).

   Keep a copy of the [!UICONTROL Source Key] that is generated. You'll need the value later.

1. Click **[!UICONTROL Save]**.

1.  In Experience Platform, create an Adobe Advertising Cloud DSP destination connection using the [!UICONTROL Source Key] that was generated in the DSP source settings.

   For instructions for activating the Advertising Cloud destination connection, selecting segments, and accessing control permissions, see "[Adobe Advertising Cloud DSP Destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-dsp-destination.html)."

>[!MORELIKETHIS]
>
>*[About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Audience Source Settings](source-settings.md)
>* [Activate Authenticated Segments from Durable ID Partners](source-activate.md)<!-- title?-->
