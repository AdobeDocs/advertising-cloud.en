---
title: About the [!UICONTROL Deal ID Inbox]
description: Learn about the [!UICONTROL Deal ID inbox] feature, which allows you to accept private deals you've already negotiated with publishers on [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (formerly [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
---
# About the [!UICONTROL Deal ID Inbox]

DSP's [!UICONTROL Deal ID inbox] allows you to quickly set up deals that Advertising Cloud DSP has imported from publishers through supply side platforms (SSPs) so you don't have to set up each deal manually. You can accept the guaranteed and non-guaranteed private inventory deals you've already negotiated with publishers on [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (formerly [!DNL Rubicon]) from the [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP is the first DSP to integrate with the [!DNL FreeWheel] API.

In the [!UICONTROL Deal ID inbox], you can see the details of the deal as your publisher sees them, speed up your deal setup, and avoid manual entry errors.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP automatically refreshes all deal details daily at 4:30 a.m. EST. It also refreshes all [!DNL FreeWheel] deals and updates existing deals from [!DNL Google] and [!DNL Magnite DV+] hourly. You can also manually refresh the deal details to populate new deals at any time.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>For programmatic guaranteed deals through [!DNL Google Authorized Buyers], you must deliver on at least 90% of your budget or your account will lose access to [!DNL Google] deals in the [!UICONTROL Deal ID inbox].

## Implementing the [!UICONTROL Deal ID Inbox]

To receive your deals in the [!UICONTROL Deal ID inbox], your SSP accounts must map your organization's DSP account to your SSP account. DSP will share the organization's account names with the relevant SSPs. Contact your [!DNL Adobe] account team for instructions.

During deal negotiations, tell the publisher to send the deal to your buyer instead of to the parent DSP account. The deal identifier may be a name or an ID, depending on the SSP.

## Actions You Can Take on Your Deals

* **Review deals** to verify that the SSP has sent the correct publisher, flight dates, CPM, and other deal details. If the publisher has made a mistake, contact them outside of DSP so they can correct and resend the deal.

* **Accept deals** after reviewing, and they will no longer appear in the [!UICONTROL Deal ID inbox]. Accepted deals are listed in [!UICONTROL Inventory] > [!UICONTROL Deals] and are ready to target within advertisers’ placements.

* **Ignore deals** that aren't needed or are unsolicited. Ignored deals are moved to the [!UICONTROL Ignored Deals] tab within the [!UICONTROL Deal ID inbox], which serves as an archive. DSP doesn't alert SSPs and publishers when you ignore a deal.

* **Modify details for already-accepted deals** from [!UICONTROL Inventory] > [!UICONTROL Deals] (not in the [!UICONTROL Deal ID inbox]). Similarly, when publishers send changes to deals, advertisers are responsible for implementing those changes in [!UICONTROL Inventory] > [!UICONTROL Deals] because the [!UICONTROL Deal ID inbox] doesn't sync changes from the SSPs after deals are set up.

## What Types of Deals Can't Be Accepted?

When a deal listing doesn't include a ![Accept](/help/dsp/assets/accept.png) icon or an [!UICONTROL Accept] button, you can't accept it from the [!UICONTROL Deal ID inbox]. Instead, you can [create the deal ID details manually](/help/dsp/inventory/deal-id-create.md).

You can't accept the following types of deals:

* [!DNL Google] deals that aren't in USD.

* [!DNL Magnite DV+] deals that aren't in USD

* [!DNL FreeWheel] deals that aren't in your account currency.

* Deals that have an end date before today.

* Old [!DNL Magnite DV+] deals that were labeled as "multiple media types."

The deal details include the reason that the deal isn't available to accept.

>[!MORELIKETHIS]
>
>* [Accept a Deal in the Deal ID Inbox](deal-id-inbox-accept.md)
>* [Overview of Inventory Features](inventory-overview.md)
