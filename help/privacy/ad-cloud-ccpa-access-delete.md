---
title: Adobe Advertising Cloud support for the California Consumer Privacy Act &#58; Consumer Data Access and Delete Support
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
---
# Adobe Advertising Cloud Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support

*For Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP, and Adobe [!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their personal information as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe Experience Cloud processes and stores on your behalf.

As your service provider, Adobe Advertising Cloud provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Advertising Cloud products and services, including managing requests to access and delete personal information and managing requests to opt out of the sale of personal information.

This document describes how Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform), and [!DNL Media Optimizer DCO] &mdash; as service providers &mdash; support consumers' rights to access and delete personal information using the Adobe [!DNL Experience Platform Privacy Service API] and [!DNL Privacy Service UI].

For information about how Advertising Cloud DSP supports the consumer right to opt-out of the sale of personal information, see [Adobe Advertising Cloud Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Supported Data Request Types for Advertising Cloud

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a consumer's cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for consumers using a browser; or delete ID-level data stored within [!DNL DSP] for consumers using apps on mobile devices.
* Check the status of one or all existing requests.

## Required Setup to Send Requests for Advertising Cloud

To make requests to access and delete consumer personal information from Advertising Cloud, you'll need to:

1. Deploy a JavaScript library to retrieve and remove your customer's cookies. The same library, `AdobePrivacy.js`, is used for all Adobe Experience Cloud solutions.

   >[!IMPORTANT]
   >
   >Requests to some Experience Cloud solutions don't require the JavaScript library, but requests to Advertising Cloud require it.

   You should deploy the library on the web page from which your customers can submit access and delete requests, such as your company's privacy portal. The library helps you retrieve Adobe cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of access and delete requests via the [!DNL  Adobe Experience Platform Privacy Service API].

   When the customer asks to delete personal data, the library also deletes the customer's cookie from the customer's browser.

   >[!NOTE]
   >
   >Deleting personal data is different than opting out, which stops the targeting of an end user with audience segments. However, when a consumer asks to delete personal data from [!DNL Creative], [!DNL DSP], or [!DNL DCO], the library also sends a request to Advertising Cloud to opt out the customer from segment targeting. For advertisers with [!DNL Search], we recommend that you provide your customers a link to [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), which explains how to opt out of audience segment targeting. 

1. Identify your Experience Cloud organization ID and make sure it is linked to your Advertising Cloud accounts.

   An Experience Cloud organization ID is a 24-character alphanumeric string appended with "@AdobeOrg." Most Experience Cloud customers have been assigned an organization ID. If your marketing team or internal Adobe system administrator doesn't know your organization ID, or isn't sure if it's been provisioned, contact Adobe Customer Care at gdprsupport@adobe.com. You'll need the organization ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Advertising Cloud representative to confirm that all of your organization's Advertising Cloud accounts &mdash; including [!DNL DSP] accounts or advertisers, [!DNL Search] accounts, and [!DNL Creative] or [!DNL DCO] accounts &mdash; are linked to your Experience Cloud organization ID.

1. Use either the [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (for automated requests) or the [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (for ad-hoc requests) to submit requests to access and delete personal information to Advertising Cloud on behalf of consumers, and to check the status of existing requests.

   For advertisers who have a mobile app to interact with customers and launch campaigns with [!DNL DSP], you'll need to download the Privacy-ready Mobile SDKs for Experience Cloud. The Mobile SDKs allow businesses to set opt-out status flags, retrieve the consumer's device ID (namespace ID: `deviceID`), and submit requests to the Privacy Service API. Your mobile app will require an SDK Version 4.15.0 or greater.

   When you submit a consumer access request, the Privacy Service API returns a consumer's information based on the specified cookie or device ID, which you then must return to the consumer.

   When you submit a consumer delete request, the cookie ID or device ID and all cost, click, and revenue data associated with the cookie are deleted from the server.

   >[!NOTE]
   >
   >If your business has multiple Experience Cloud organization IDs, then you must send separate API requests for each. You can, however make one API request to multiple Advertising Cloud sub-solutions ([!DNL Search], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All of these steps are necessary to receive support from Advertising Cloud. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the items you'll need, see [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Required Field Values in Advertising Cloud JSON Requests

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` <*your Experience Cloud organization ID*>

"users": 

* `"key":` <*usually the name of the customer*> 

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

    * `"namespace": **411**` (which indicates the adcloud cookie space)

    * `"value":` <*the actual customer’s cookie ID value as retrieved from `AdobePrivacy.js`*>

* `"include": **adCloud**` (which is the Adobe product that applies to the request)

* `"regulation": **ccpa**` (which is the privacy regulation that applies to the request)

## Example of Request Submitted by a Consumer Using an Advertising Cloud User ID Retrieved from AdobePrivacy.js

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## Data Fields That Are Returned for Access Requests

The following is an example of a personal information access response for Advertising Cloud.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
