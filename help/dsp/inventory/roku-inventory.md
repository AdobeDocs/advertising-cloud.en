---
title: Using [!DNL Roku] Inventory
description: Learn about DSP's partnership with [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]-specific placements. 
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
---
# Using [!DNL Roku] Inventory

Advertising Cloud DSP provides unique features for advertising on [!DNL Roku].

## The Advertising Cloud DSP and [!DNL Roku] Partnership

Roku and Advertising Cloud DSP have a unique partnership that matches your [!DNL DSP] audiences to [!DNL Roku] IDs for 1:1 deterministic audience targeting on [!DNL Roku] inventory.

Outside of Roku’s own DSP (OneView), Advertising Cloud DSP has sole access to these targeting capabilities. Advertising Cloud DSP is also the only DSP with permission to measure [!DNL Roku] supply next to all other connected TV (CTV) inventory. Because [!DNL Roku] doesn't share all standard RTB and impression pixel signals, no other DSP can target or measure across Roku-sold CTV supply.

## [!DNL Roku] Inventory Options

You can either a) set up private deal IDs directly with [!DNL Roku] and then enter the deal ID data into DSP or b) visit the [!DNL On Demand] Gallery to subscribe to [!DNL Roku] profiles:

>[!NOTE]
>
>[!DNL Roku] inventory isn't available in open marketplaces and exchanges.

* For your private deals, [set up information about the deal IDs in DSP](/help/dsp/inventory/deal-id-create.md) and then target “[!UICONTROL Roku Network – Audience]” and “[!UICONTROL The Roku Channel – Audience]” within [!DNL Roku] placements.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* You can [subscribe to the following [!DNL Roku] inventory within the [!DNL On Demand] Gallery](/help/dsp/inventory/on-demand-inventory-subscribe.md), and then target any of the approved deals within [!DNL Roku] placements:

    * “[!UICONTROL Roku Network – Audience]” for inventory across the [!DNL Roku] ecosystem with premium content partners, such as [!DNL The CW], [!DNL ABC], and [!DNL ESPN].
    * “[!UICONTROL The Roku Channel – Audience]” for [!DNL Roku] owned-and-operated (O&O) app content.

### Advantages of Customizing Private Marketplaces with [!DNL Roku]

Private deals allow you to customize the deal parameters according to your needs.

* **Negotiated pricing:** Work with the [!DNL Roku] sales team to negotiate and structure a deal that meets your campaign needs.

* **Scale Priority:** Private marketplaces (PMPs) receive higher priority than always-on deals (such as [!DNL On Demand] deals).

* **Frequency Management:** The [!DNL Roku] default frequency cap is one (1) ad per 30 minutes per user, but you can customize the cap by hour, day, week, month, or entire flight period.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku] Data Targeting:** [!DNL Roku] audiences are built from [!DNL Roku] device and TV signals, data tracked by [!DNL The Roku Channel] (such as TV genre affinity, streaming TV behavior, and cable subscription status), and additional data from the [!DNL Roku] customer relationship management (CRM) system.

* **[!DNL Roku] Content Targeting:** Private deals can target apps by genre, application of app blocklist, seasonal and tentpole events, and shows within [!DNL The Roku Channel] only.

## [!DNL Roku] Placements

In DSP campaigns, [create [!DNL Roku]-specific placements](/help/dsp/campaign-management/placements/placement-create.md) using the placement type "[!UICONTROL Connected TV (Roku)]." Include [!DNL Roku] placements in [!DNL Roku]-specific packages with defined goals.

Each [!DNL Roku] placement must target at least one [!DNL Roku] deal or source. To use DSP’s unique audience matching with [!DNL Roku], include one or more one audience segments that can be matched against the [!DNL Roku] (opted-in) deterministic dataset.

### [!DNL Roku]-Approved Third-Party Tracking Vendors

[!DNL Roku] placements can include third-party event pixels and conversion pixels from the following vendors:  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], and [!DNL Research Now].

### Best Practices by Placement Strategy

 The following are the recommended practices for [!DNL Roku]-specific placements.

To maximize incremental reach:

* Suppress exposed audiences on [!DNL Roku O&O] by excluding audiences that you've already reached using [!DNL The Roku Channel].

* Suppress exposed audiences on [!DNL All Roku] by excluding audiences that you've already reached across the [!DNL Roku] platform.

For the fastest setup:

* Target existing, always-on deals for [!DNL The Roku Channel] in [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) to quickly access [!DNL Roku] owned-and-operated inventory.
* Target existing, always-on deals for [!DNL Roku Network] in [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) to quickly achieve scale across the [!DNL Roku] platform.

To maximum scale:

* Customize a [!DNL Roku] private marketplace for prioritized access to [!DNL Roku] supply at a negotiated price.

>[!MORELIKETHIS]
>
>* [Manually Create Deal ID Details](/help/dsp/inventory/deal-id-create.md)
> * [Subscribe and Request Access to [!DNL On Demand] Premium Inventory Deals](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Create a Placement](/help/dsp/campaign-management/placements/placement-create.md)
