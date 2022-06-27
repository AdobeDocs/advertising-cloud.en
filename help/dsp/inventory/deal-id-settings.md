---
title: Manual Deal ID Settings
description: See descriptions of the settings for manually-entered Deal IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
---
# Manual Deal ID Settings

| Section | Parameter | Description | Required | Editable |
|---------|-----------|-------------|----------|----------|
| [Deal Details] | [!UICONTROL Deal name] | The name to identify your [!UICONTROL Deal ID] in Advertising Cloud DSP. Enter a name or select **[!UICONTROL Auto-name]** to let Advertising Cloud generate a name based on the deal details.<br><br>Example of an auto-generated name: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Yes | Yes |
| | [!UICONTROL External deal ID] | The ID used by your publisher and the SSP to identify this deal. | Yes | No |
| | [!UICONTROL Publisher] | The name of the publisher that is selling this inventory.| Yes | No |
| | [!UICONTROL SSP] | The supply side platform (SSP) through which this deal runs. | Yes | No |
| | [!UICONTROL Media type] | The type of media bought through this deal: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, or *[!UICONTROL Audio]*. The options vary by SSP.<br><br> If the deal allows multiple media types, select the media type for the default placement when you create the deal. Later, you can change the value, or you can just [attach a new placement with the additional media type](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Yes  | No |
| | [!UICONTROL Deal type] | The deal commitment and pricing structure:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: You and the publisher haven't committed to a fixed number of impression deliveries. The deal specifies the minimum price for the inventory, although the CPM may fluctuate and increase depending on market conditions.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: You and the publisher haven't committed to a fixed number of impression deliveries. Pricing is at a negotiated fixed rate.</li><li>*[!UICONTROL Guaranteed (fixed)]*: You and the publisher have agreed on a pre-defined number of impressions, targeting, flight dates, and fixed price.<br><br><b>Note:</b> Guaranteed deals require flight dates and a specified number of impressions in the [!UICONTROL Tracking] section. You also must create a default programmatic guaranteed (PG) placement for the deal, and you can optionally use the deal for other placements instead.</li></ul>   | Yes  | No |
| | [!UICONTROL CPM] | The negotiated cost per 1000 impressions (CPM). | Yes | Yes |
| | [Currency] | The currency for the deal.<br><br>All SSPs accept deals in USD. When the SSP accepts the currency for your DSP account, that currency is also available. | Yes | No |
| | [!UICONTROL Billing method] | All deal IDs are [!DNL Adobe]-financed and -invoiced. Advertising Cloud pays all available media vendors based on usage, manage discrepancies with the vendors, and send one consolidated invoice to the account. This option incurs additional fees as outlined in the account's rate card. | Yes | No |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | The email address for the user account that can access the deal. | No  | Yes |
| | [!UICONTROL Advertisers that can access this deal] | The specific advertisers in the account who can access this deal.<br><br><b>Note:</b> You can share the deal with advertisers in additional accounts from the [!UICONTROL Deals] view. In the deal row, click **[!UICONTROL #]**, click **[!UICONTROL share]**, and then share the deal with an email address. | Yes | Yes |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | The start and end dates for traffic using this deal. These dates are for tracking purposes only and don't impact ad delivery.<br><br><b>Tip:</b> In the [!UICONTROL Inventory] > [!UICONTROL Deals] view, the [!UICONTROL Pacing & Budget] column shows how the deal is pacing to the specified flight date and impression goal. If delivery is under- or over-pacing, contact your publisher to adjust how much volume it is sending through the deal. | Guaranteed deals: Yes<br>Non-guaranteed deals: No | Yes |
| | [!UICONTROL Impressions] | (Optional for non-guaranteed deals) The estimated number of impressions you expect to run using this deal. This value is for tracking purposes only; the publisher controls ad delivery. | Guaranteed deals: Yes<br>Non-guaranteed deals: No | Yes |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Manually Create Deal ID Details](deal-id-create.md)
>* [SSP Partners](ssp-partners.md)
>* [About Private Inventory](private-inventory-about.md)
