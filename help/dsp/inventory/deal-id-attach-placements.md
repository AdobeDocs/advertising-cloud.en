---
title: Specify Placements and Ads for a Private Deal
description: Learn how to use a private deal with additional placements and ads.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 669cadcf-021b-4129-95d5-3d24af4a4b88
---
# Specify Placements and Ads for a Private Deal

For non-guaranteed deals, you can specify the deal as an inventory target for new placements from the [!UICONTROL Placements] view.

For programmatic guaranteed (PG) deals, you can create placements with specified ads from the [!UICONTROL Deals] view.

You can also [attach new ads to existing placements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) associated with PG and non-guaranteed deals at any time.

## Specify a Non-Guaranteed Deal as an Inventory Target for a Placement

* [Create a placement from the [!UICONTROL Placements] view](/help/dsp/campaign-management/placements/placement-create.md). In the [!UICONTROL Inventory Targeting] settings, select the private deal.

## Attach Placements and Ads to a PG Deal

1. In the main menu, click **[!UICONTROL Inventory] > [!UICONTROL Deals].**

1. In the deal row, click  **[!UICONTROL ...] > [!UICONTROL Attach New Placement]**.

1. In the [!UICONTROL Ad & Campaign Selection] settings, select the ads to use for the placement:

       1. Select the advertiser, campaign, and ad type. Optionally select an ad status by which to filter the ads.
        
       1. From the list of available ads, select the check box next to each ad that will be used for the deal.

       1. Click **[!UICONTROL Apply]**.

    1. In the placement settings screen:
    
       1. Enter the placement name.
        
       1. (Optional) Edit the [placement settings](/help/dsp/campaign-management/placements/placement-settings.md), including overwriting the default bid, which is automatically populated with the CPM value from the deal; changing the date range; or attaching more ads.
       
         The deal is automatically targeted in the Inventory Targets section. All other targeting options are inapplicable.

       1. Click **[!UICONTROL Create placement]**.

The placement will begin running after the publisher activates your PG deal ID.

>[!NOTE]
>
> You don't need to send the deal tag to the publisher for verification.

>[!MORELIKETHIS]
>
>* [About Private Inventory](private-inventory-about.md)
>* [List the Placements and Ads for a Private Deal](/help/dsp/inventory/private-deal-view-placements.md)
>* [Manually Create Deal ID Details](deal-id-create.md)
>* [Manual Deal ID Settings](deal-id-settings.md)
>* [Set up a Programmatic Guaranteed Deal](programmatic-guaranteed-set-up.md)
