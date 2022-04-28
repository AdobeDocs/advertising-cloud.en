---
title: Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags
description: Learn why and how to add [!DNL Analytics for Advertising Cloud] macros to your [!DNL Google Campaign Manager 360] ad tags
feature: Integration with Adobe Analytics
exl-id: 05084a85-5890-4a82-b3eb-4520f44f9d66
---
# Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags

*Advertisers with an Advertising Cloud-Adobe Analytics Integration Only*

*Applicable to Advertising Cloud DSP only*

If you use ad tags from [!DNL Google Campaign Manager 360] for your Advertising Cloud DSP ads, append Analytics for Advertising Cloud parameters to your landing page URLs using the [`%p` macro](https://support.google.com/campaignmanager/table/6096962). The parameters record `s_kwcid` and `ef_id` query string parameters in the landing page URL, allowing Advertising Cloud to send click data for the ads to Adobe Analytics.

Use macros for [!DNL Campaign Manager 360] display and video ads for the following types of [!DNL Analytics for Advertising Cloud] implementations:

* **Advertisers with the [!DNL Adobe] [!DNL Analytics for Advertising Cloud] JavaScript code implemented on their websites**: The JavaScript code already records the `s_kwcid` and `ef_id` query string parameters. However, using macros extends tracking to include click-based conversions when third-party cookies aren't supported. The best practice is to add the macros in the following sections to your ad tags to capture additional click-through data that isn't captured through the JavaScript code.

>[!NOTE]
>
>The JavaScript code is a solution for click tracking only while cookies are still available. Once cookies are discontinued, implementing the following macros will be necessary.

* **Advertisers whose websites don't use the [!DNL Analytics for Advertising Cloud] JavaScript code and instead rely on [!DNL Analytics] server-side forwarding for click-through data only** (without any view-through data): The following macros are required to report onsite click activity driven from ads you buy through Advertising Cloud.

## Append the Macros to Your [!DNL Google Campaign Manager 360] Ads

Within [!DNL Google Campaign Manager 360], append to the following parameter to the landing page URL for each of your display and video ads: `%pamo=!;`

You can specify the landing page URL in several ways. Instructions for each option are included in the following subsections.

The following is an example of the landing page URL formatted with the suffix.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* If the landing page URL includes a hash symbol (#), which is not common, then place the `amo` parameter before the hash symbol.
>* If no other parameters are included after the `amo` parameter, then add a parameter (for example, &a=b) after it. Example:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configure the Advertiser-Level Landing Page URL Suffix

1. In the main menu, click the [!UICONTROL Advertisers] tab.
1. Click the advertiser name.
1. In the [!UICONTROL Landing page URL suffix] settings, include `%pamo!;` in the [!UICONTROL URL suffix] field.

![advertiser-level settings](/help/integrations/assets/macro-ggl360-advertiser.png)

### Configure the Campaign-Level Landing Page URL Suffix

1. In the main menu, click the [!UICONTROL Campaigns] tab.
1. Click the campaign name.
1. Click [!UICONTROL Properties].
1. In the [!UICONTROL Landing page URL suffix] settings, include `%pamo!;` in the [!UICONTROL URL suffix] field.

![campaign-level settings](/help/integrations/assets/macro-ggl360-campaign.png)

### Configure the Creative-Level Landing Page URL Suffix

1. In the main menu, click the [!UICONTROL Campaigns] tab.
1. Click the campaign name.
1. In the [!UICONTROL Views] menu, select [!UICONTROL Creatives].
1. Click the creative name.
1. In the [!UICONTROL Click tags] setting, include `%pamo!;` in the [!UICONTROL Landing page] column for the click tag.

![creative-level settings](/help/integrations/assets/macro-ggl360-creative.png)

## How [!DNL Analytics for Advertising Cloud] Macros Are Expanded in DSP

In DSP, when you create an ad that includes the [!DNL Analytics for Advertising Cloud] parameter (`amo`), the `ef_id` and `s_kwcid` macros are automatically appended to the click URL. The best practice is to check the tag in DSP to ensure that the `ef_id` and `s_kwcid` macros are present.

The following is an example of a [!DNL Google Campaign Manager 360] [ins tag](https://support.google.com/campaignmanager/answer/6080468) as it appears in DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

When a user clicks the ad, [!DNL Google Campaign Manager 360] sees `%pamo` in the URL suffix and dynamically inserts the value of the `amo` parameter into the URL.


>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Flashtalking] Ad Tags](macros-flashtalking.md)
