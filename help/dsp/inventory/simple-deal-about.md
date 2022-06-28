---
title: About [!UICONTROL Simple Ad Serving]
description: Learn about [!UICONTROL Simple Ad Serving] deals using event-tracking pixels.
feature: DSP Simple Ad Serving
exl-id: d65d1d8e-4d10-4d1d-86d3-f4457c29ae8d
---
# About [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] provides guaranteed, non-decisioned ad delivery and reporting for a specified publisher and a single ad type using a single, dedicated placement. Use [!DNL Simple Ad Serving] when your publisher can't execute your deal via deal IDs. All targeting, budget pacing and capping, and frequency capping is handled by the publisher. Execute these deals via event-tracking pixels.

With [!UICONTROL Simple Ad Serving], each ad is served directly by the publisher (site serve), and DSP provides an event-tracking pixel to send to the publisher, who must implement the pixel and traffic the DSP ads. Depending on the inventory type, the event pixels measure impression, click-through, and video played events.

The following ad types are available:

* desktop standard pre-roll
* tablet and mobile standard pre-roll
* connected TV standard pre-roll
* display
* audio

You can create a [!UICONTROL Simple Ad Serving] deal in the [!UICONTROL Inventory] > [!UICONTROL Deals] view. DSP automatically generates a placement with the subtype "[!DNL Simple ad serving]" for the ad. The placement targets the deal but doesn't allow additional targeting, budget, or frequency capping. You can edit only some of the deal settings, such as the deal name, CPM, impressions, and flight dates.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] placements don't comply with the account's usable funds or the campaign and package budgets. However, spend is tracked and counted toward those budgets. Even when the CPM is $0, event data is always tracked.

>[!MORELIKETHIS]
>
>* [Create a [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [Edit [!UICONTROL Simple Ad Serving] Deal Settings](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Settings](simple-deal-settings.md)
>* [View a Detailed Report for a Deal](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
