---
title: Adobe Advertising Cloud support for the California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale Support
description: Learn about support for capturing consumer opt-out-of-sale requests.
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
---
# Adobe Advertising Cloud Support for the California Consumer Privacy Act: Consumer Opt-Out of Sale Support

*For Adobe Advertising Cloud Demand Side Platform*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their data as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe Experience Cloud processes and stores on your behalf.

As your service provider, Adobe Advertising Cloud provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Advertising Cloud products and services, including managing consumer requests to access and delete personal information and managing consumer requests to opt out of the sale of personal information.

This document describes how Adobe Advertising Cloud Demand Side Platform (DSP), as a service provider, supports the consumer right to opt out of the "sale" of "personal information," as each term is defined by the CCPA. It includes information on how to communicate opt-out-of-sale requests to Advertising Cloud and how to retrieve reports of your organization's opt-out-of-sale requests.

For information about how Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform), and Media Optimizer DCO support consumers' personal information access and deletion rights, see [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ad-cloud-ccpa-access-delete.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Communicating Consumer Opt-Out-of-Sale Requests to Advertising Cloud

You can communicate consumer opt-out-of-sale requests by using either:

* a CCPA opt-out-of-sale segment created in Advertising Cloud DSP
* the Adobe Experience Platform Privacy Service API

### Method 1: Communicate CCPA Opt-Out-of-Sale Requests Using a [!UICONTROL CCPA Opt-Out-of-Sale] Segment in Advertising Cloud DSP

>[!NOTE]
>
>Users remain in CCPA opt-out-of-sale segments indefinitely.

1. Log into the advertiser's account in Advertising Cloud DSP at [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Create a CCPA opt-out-of-sale segment, and implement the segment pixel to capture the opt-out requests](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Method 2: Communicate CCPA Opt-Out-of-Sale Requests Using the Adobe Experience Platform Privacy Service API

*Advertisers assigned an Adobe Experience Cloud ID only*

1. Deploy a JavaScript library to retrieve your customer's cookies. The same library, `AdobePrivacy.js`, is used for all Adobe Experience Cloud solutions.

   >[!IMPORTANT]
   >
   >Requests to some Adobe Experience Cloud solutions don't require the JavaScript library, but requests to Advertising Cloud require it.

   You should deploy the library on the web page from which your customers can submit opt-out-of-sale requests, such as your company's privacy portal. The library helps you retrieve Adobe cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of opt-out-of-sale requests via the Adobe Experience Platform Privacy Service API.

1. Identify your Experience Cloud ID and make sure it's linked to your Advertising Cloud accounts.

   An Experience Cloud ID is a 24-character alphanumeric string appended with "@AdobeOrg." Most Experience Cloud customers have been assigned an ID. If your marketing team or internal Adobe system administrator doesn't know your organization's ID, or isn't sure if it's been provisioned, contact Adobe Customer Care at gdprsupport@adobe.com. You'll need the ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Advertising Cloud representative to confirm that all of your organization's Advertising Cloud accounts &mdash; including [!DNL DSP] accounts or advertisers, [!DNL Search] accounts, and [!DNL Creative] or [!DNL DCO] accounts &mdash; are linked to your Experience Cloud ID.

1. Use the Adobe Experience Platform Privacy Service API to [submit opt-out-of-sale requests](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) to Advertising Cloud on behalf of consumers, and to check the status of existing requests.

   See the Appendix below for an example of an opt-out-of-sale request.

   >[!NOTE]
   >
   >If your business has multiple Experience Cloud IDs, then you must send separate API requests for each. You can, however make one API request to multiple Advertising Cloud sub-solutions ([!DNL Search], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All of these steps are necessary to receive support from Advertising Cloud. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the items you'll need, see [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Retrieving Reports of Consumers Who Submitted Opt-Out-of-Sale Requests

Advertising Cloud generates monthly reports of IDs that customers have submitted for opt-out-of-sale requests for the account. Each report is available as a tab-separated text file compressed into GZIP format. The data consolidates requests captured using CCPA opt-out-of-sale segments that were created in Advertising Cloud DSP and any submissions made via the Privacy Service API. User IDs captured in CCPA opt-out-of-sale segments are identified by segment and by advertiser. Reports are generated on the first of each month for the previous month. For example, the monthly user list for June is available on July 1.

You can retrieve links to the monthly reports that were created in the previous three months, either from within Advertising Cloud DSP or by using the Advertising Cloud [!DNL Trafficking API]. Each link is valid for seven days but refreshes each time a customer attempts to retrieve one.

### Method 1: Retrieve Consumer Opt-Out-of-Sale Reports Within Advertising Cloud DSP

1. Log into the advertiser's account in Advertising Cloud DSP at [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Retrieve the reports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Method 2: Retrieve Consumer Opt-Out-of-Sale Reports Using the Advertising Cloud [!DNL Trafficking API]

This feature is available to organizations that use the [!DNL Trafficking API]. See the documentation for the [!DNL Trafficking API] for more information.

If your organization doesn't use the [!DNL Trafficking API] but is interested in more information, contact your [!DNL Adobe] account team.

## Appendix: Example [!UICONTROL CCPA Opt-Out-of-Sale] Request for Privacy Service API Users

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

where:

* `"namespace": "AdCloud"` indicates the `AdCloud` cookie space, and the corresponding value is the customer’s cookie ID as retrieved from `AdobePrivacy.js`
* `"include": ["AdCloud"]` indicates that the request applies to Advertising Cloud
