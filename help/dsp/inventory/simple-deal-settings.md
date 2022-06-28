---
title: '[!UICONTROL Simple Ad Serving] Deal Settings'
description: Learn about the available settings for [!UICONTROL Simple Ad Serving] deals.
feature: DSP Simple Ad Serving
exl-id: 1a8f215c-c52b-4099-a55f-99c4232b7a22
---
# [!UICONTROL Simple Ad Serving] Deal Settings

## New [!UICONTROL Simple Ad Serving] Deals

### [!UICONTROL Select Ad Source]

| Parameter | Description |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | The media type for this deal: *[!UICONTROL Video],* *[!UICONTROL Display],* or *[!UICONTROL Audio].* |
|**[!UICONTROL Publisher Site Served On]** | The name of the publisher that is selling this inventory. Search for a publisher by entering at least the first two characters in the name. To add a publisher that isn't listed, contact your [!DNL Adobe] account team.|
|**[!UICONTROL Advertiser]** | A single advertiser in the account who can access this deal. Also select the campaign and (optionally) the package in which the deal is available. |
| **[!UICONTROL Media Quality Assessment?]** | (Some users) Enables the ad to run on another DSP for third-party verification. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | The only option is *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (New deals only) Whether to:<ul><li>*[!UICONTROL Create New]:* To create an ad for this deal.</li><li>*[!UICONTROL Select Ads]:* To use an existing ad for this deal.</li></ul> |
| **[!UICONTROL Ad Type]** | The ad type for this deal. If you're going to create ads for the deal, include the ad size or duration, as requested. The available options vary by media type. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(When you're using existing ads) The ads to include in the deal. Select the check box next to each ad to include.

### [!UICONTROL Select & Upload [Media Type]]

(New ads only) Screens to create a new [third-party ad](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parameter | Description |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | The cost per 1000 impressions (CPM), as reflected in the rate card for your contract. Contact your [!DNL Adobe] account team for this value. <br><br>Specify also the currency for the deal. All users can select USD, or, if the SSP supports additional currencies, the currency for the DSP account. |
| **[!UICONTROL Third Party Billed Fees]** | (Optional) A static third-party fee to be tracked as a non-billable cost,  and the currency for the deal.<br><br>All users can select USD, or, if the SSP supports additional currencies, the currency for the DSP account. **NOTE:** Billable fees are reflected in the [!UICONTROL Net CPM] metric.|
| **[!UICONTROL Third Party Fee Description]** | (Optional) A description of the third-party fees. |
| **[!UICONTROL Flight Dates]** | The start and end dates for traffic using this deal. The flight dates must be included within the campaign flight dates. The ad tags return a response only during the specified flight.<br><br> The best practice to create a separate simple ad serving campaign with a year-long duration and to build tracking pixels within it. |
| **[!UICONTROL Impressions]** | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
| **[!UICONTROL Deal Name]** | The deal name. Enter a name, or select *[!UICONTROL Auto Generate Deal Name]* to let DSP generate a name based on the deal details.<br><br>Example of an auto-generated name: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Read-only) The ads that are part of the deal. To edit an ad, click the ad name. To remove an ad from the deal, click **[!UICONTROL X]** next to the ad name. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [About [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Create a [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [Edit [!UICONTROL Simple Ad Serving] Deal Settings](simple-deal-edit.md)
>* [View a Detailed Report for a Deal](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
