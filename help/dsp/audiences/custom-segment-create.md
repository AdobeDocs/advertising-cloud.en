---
title: Create and Implement a Custom Segment
description: Learn how to create and implement a custom segment to track users exposed to ads or users who visit your webpages.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
---
# Create and Implement a Custom Segment

You can collect your own first-party audience data by creating and implementing a custom Advertising Cloud segment. You can use the segment to track a) users exposed to ads from desktop, mobile, and CTV devices and b) users who visit specific webpages. You can later retarget users in the segment with additional ads or prevent users in the segment from receiving additional ads.

>[!NOTE]
>
>To track users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA), create a [CCPA opt-out-of-sale segment](ccpa-opt-out-segment-create.md).

1. Create the segment:

    1. In the main menu, click **[!UICONTROL Audiences] > [!UICONTROL Segments]**.

    1. Above the data table, click **[!UICONTROL Create]**.

    1. Enter a unique **[!UICONTROL Segment Name]**.

    1. For the [!UICONTROL Segment Type], select **[!UICONTROL Custom]**.

    1. Enter the Segment Window, which is the number of days a user's cookie stays in the segment.

       The default window is 45 days. Enter a value from one (1) to 365.

    1. Click **[!UICONTROL Save]**.

1. Copy and implement tags to track the segment, as needed:

    1. Return to **[!UICONTROL Audiences] > [!UICONTROL Segments]**.

    2. Hold the cursor over the segment row and click **[!UICONTROL Get pixel]**.

        * To track desktop and mobile visitors to a webpage:

            1. Copy the page view tracking tag, which is labeled "[!UICONTROL Desktop or mobile websites]."

            1. Provide the tag to the advertiser or website contact for deployment.

               The advertiser's IT department or other group may need to schedule, or be informed about, the tag deployment.

        * To track users exposed to an ad unit on desktop, mobile, or CTV devices:

            1. Copy the impression tracking tag, which is labeled "[!UICONTROL Desktop or mobile ads]."

            1. Add the tag to either the [!UICONTROL Pixel] tab for each relevant ad or to the [!UICONTROL Event Pixels] section of the [[!UICONTROL Tracking] settings for each relevant placement](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Once a tracking tag is implemented, you can use the segment in the audience targets or exclusions for any placement.

>[!TIP]
>
>Keep track of the segment size as users are tracked.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Create and Implement a [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Create a Reusable Audience](reusable-audience-create.md)
>* [Audience Settings](audience-settings.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- I'll add x-ref to ad settings later.-->
