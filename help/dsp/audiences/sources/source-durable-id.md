---
title: Activate Authenticated Segments from Durable ID partners
description: Learn about activating authenticated audiences through a durable ID solution.
feature: DSP Audiences
exl-id: 44635b74-1874-4781-bd1a-a4dadae049e0
---
# Activate Authenticated Segments from Durable ID partners 

*Beta feature*

To activate authenticated audiences through a durable ID solution within Advertising Cloud DSP, your segments must be translated into [!DNL RampIDs], which are recognizable in a biddable environment. You can accomplished this by either:

* Leveraging the DSP integration with the [!DNL Adobe Real-Time Customer Data Profile (CDP)] and the [!DNL Adobe-LiveRamp Retrieval API].

* Manually sending authenticated segments to DSP from the [!DNL LiveRamp] [!DNL Connect] dashboard.

## Tasks

1. For either option, contact `adcloud-support@adobe.com` to enable the following settings in DSP, which will allow you to target authenticated segments in DSP campaigns once [all steps in the activation workflow are completed](source-about.md#workflow-sources):

    1. [!DNL LiveRamp] [!DNL RampID] campaign configuration prior to segment sharing from [!DNL Real-Time CDP].
    
    1. The account-level “[!UICONTROL LiveRamp segments]” option.

1. (Users manually sharing authenticated segments from [!DNL LiveRamp]) Complete the following steps in the [!DNL LiveRamp] [!DNL Connect] dashboard:

    1. Activate the destination tile **[!DNL AAC API 1P Onboarding]**.
    
    1. Set [!DNL Identifier Settings] to **[!DNL Ramp ID]** only.

       ![Identifier settings](/help/dsp/assets/liveramp-tile-settings.png)
    
    1. (Optional) If you want to still receive cookie-based identifiers, create a second [!DNL AAC API 1P Onboarding] destination tile with “[!DNL Cookies],” "[!DNL IDFA],” and “[!DNL AAID]” selected.

## Best Practices for Testing and Data Validation

* **Target [!DNL RampID]-based segments and cookie-based segments in separate campaigns.**

  * Campaign settings allow for only one identifier to be prioritized.
  
  * Currently, [!DNL RampIDs] aren't retrievable during on-site events. This means that certain custom goals, such as Lowest CPA and ROAS, aren't available with the use of authenticated segments. Use cookie-based segments only if you have a restrictive performance KPI.

* **Create one placement in both the [!DNL RampID] and cookie-based campaigns.**

  * Target the segments that are shared from [!DNL LiveRamp] using the standard segment activation process.
  
  * Work with your Advertising Cloud support team to validate proper data distribution.

To learn more about the DSP integration with [!DNL LiveRamp], contact `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
>* [Adobe Advertising Cloud DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
