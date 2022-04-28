---
title: Adobe Advertising Cloud Support for the General Data Protection Regulation
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
---
# Adobe Advertising Cloud Support for the General Data Protection Regulation

*For Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP, and Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the General Data Protection Regulation.

The General Data Protection Regulation (GDPR), a law in effect May 25, 2018, gives all individuals (data subjects) within the borders of the European Union (EU) control of their personal data and simplifies the regulatory environment for international business. This law applies to all businesses (data controllers) that offer goods or services to, monitor the behavior of, or collect personal data from individuals within the borders of the EU at the time their personal data is processed, regardless of the data controller's business location.

Adobe Experience Cloud acts as a data processor for any personal data it receives and stores on behalf of its customers. As a data controller, you determine the personal data that Adobe Experience Cloud processes and stores on your behalf.

This document describes how Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform), and Media Optimizer DCO support your data subjects' GDPR data access and deletion rights using the Adobe Experience Platform Privacy Service API and Privacy Service UI.

For more information about what GDPR means for your business, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Supported Data Request Types for Advertising Cloud

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a data subject's cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for data subjects using a browser; or delete ID-level data stored within [!DNL DSP] for data subjects using apps on mobile devices.
* Check the status of one or all existing requests.

## Required Setup to Send Requests for Advertising Cloud

To make requests to access and delete data for Advertising Cloud, you'll need to:

1. Deploy a JavaScript library to retrieve and remove your data subject cookies. The same library, `AdobePrivacy.js`, is used for all Adobe Experience Cloud solutions.

   >[!IMPORTANT]
   >
   >Requests to some Adobe Experience Cloud solutions don't require the JavaScript library, but requests to Advertising Cloud require it.

   You should deploy the library on the web page from which your data subject s can submit access and delete requests, such as your company's privacy portal. The library helps you retrieve Adobe cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of access and delete requests via the Adobe Experience Platform Privacy Service API.

   When the data subject asks to delete personal data, the library also deletes the data subject's cookie from the data subject's browser.

   >[!NOTE]
   >
   >Deleting personal data is different than Opt-Out, which stops the targeting of an end user with audience segments. However, when a data subject asks to delete personal data from [!DNL Creative], [!DNL DSP], or [!DNL DCO], the library also sends a request to Advertising Cloud to opt out the data subject from segment targeting. For advertisers with [!DNL Search], we recommend that you provide the data subjects a link to [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), which explains how to opt out of audience segment targeting.

1. Identify your Experience Cloud organization ID and make sure it's linked to your Advertising Cloud accounts.

   An Experience Cloud organization ID is a 24-character alphanumeric string appended with "@AdobeOrg." Most Experience Cloud customers have been assigned an organization ID. If your marketing team or internal Adobe system administrator doesn't know your organization ID, or isn't sure if it's been provisioned, contact Adobe Customer Care at gdprsupport@adobe.com. You'll need the organization ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Advertising Cloud representative to confirm that all of your organization's Advertising Cloud accounts &mdash; including [!DNL DSP] accounts or advertisers, [!DNL Search] accounts, and [!DNL Creative] or [!DNL DCO] accounts &mdash; are linked to your Experience Cloud organization ID.

1. Use either the [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (for automated requests) or the [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (for ad-hoc requests) to submit access and delete requests to Advertising Cloud on behalf of the data subjects, and to check the status of existing requests.

   For advertisers who have a mobile app to interact with data subjects and launch campaigns with the DSP, you'll need to download the Privacy-ready Mobile SDKs for Experience Cloud. The Mobile SDKs allow data controllers to set opt-out status flags, retrieve the data subject's device ID (namespace ID: deviceID), and submit requests to the Privacy Service API. Your mobile app will require an SDK Version 4.15.0 or greater.

   When you submit a data subject's access request, the Privacy Service API returns a data subject's information based on the specified cookie or device ID, which you then must return to the data subject.

   When you submit a data subject's delete request, the cookie ID or device ID and all cost, click, and revenue data associated with the cookie are deleted from the server.

   >[!NOTE]
   >
   >If your company has multiple Experience Cloud organization IDs, then you must send separate API requests for each. You can, however make one API request to multiple Advertising Cloud sub-solutions ([!DNL Search], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All of these steps are necessary for Advertising Cloud. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the items you'll need, see [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Required Field Values in Advertising Cloud JSON Requests

``"company context": 

* `"namespace": **imsOrgID**`
* `"value":` <*your IMS Org ID value*>

`"users":`

* `"key":` <*usually the name of the data subject*> 

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

    * `"namespace": **411**` (which indicates the [!DNL adcloud] cookie space)

    * `"value":` <*the actual data subject’s cookie ID value as retrieved from `AdobePrivacy.js`*>

* `"include": **adCloud**` (which is the Adobe product that applies to the request)

* `"regulation": **gdpr**` (which is the privacy regulation that applies to the request)

## Example of Request Submitted by Data Subject Using an Advertising Cloud User ID Retrieved from `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## Data Fields That Are Returned for Access Requests

The following is an example of an access response for Advertising Cloud.

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
