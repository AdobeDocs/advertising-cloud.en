---
title: "[!DNL Analytics] Data in Advertising Cloud"
description: "[!DNL Analytics] Data in Advertising Cloud"
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
---
# [!DNL Analytics] Data in Advertising Cloud

*Advertisers with an Advertising Cloud-Adobe Analytics Integration Only*

## Analytics Segments

All segments created in [!DNL Analytics] and published to Experience Cloud.

New segments take 24-48 hours to appear in Advertising Cloud. Updates to existing segments are synchronized within about eight hours.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Site Engagement Metrics

>[!NOTE]
>
>* [!DNL Analytics] passes events for the EF ID eVar into Advertising Cloud.  The default integration doesn't support sending calculated metrics or other dimensions (eVars) into Advertising Cloud. If the calculated metric can be wholly captured in a custom event, however,then Advertising Cloud can ingest the custom event.
>* [!DNL Analytics] passes data to Advertising Cloud hourly.

* [!UICONTROL Timespent_secs_1stvisit]: The number of seconds spent on the site during the visitor's first visit.
* [!UICONTROL Timespent_secs_total]: The total number of seconds spent on the site across all visits within the click lookback window.
* [!UICONTROL Pageviews_1stvisit]: The number of page views on the site during the visitor's first visit.
* [!UICONTROL Pageviews_total]: The total number of page views on the site across all visits within the click lookback window.
* [[!UICONTROL Bounces] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: The number of times that [!DNL Analytics] collected an [!UICONTROL EF ID].

## Conversion Metrics

[!DNL Analytics] passes conversion metrics to Advertising Cloud daily.

### Standard Conversion Metrics

* [[!UICONTROL Revenue] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metric](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Custom Conversion Metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.

### Reserved Conversion Metrics

These metrics are specific to the report suite, so the available metrics vary for each customer and report suite.

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud Metrics in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
