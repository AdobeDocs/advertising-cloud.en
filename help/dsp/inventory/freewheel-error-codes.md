---
title: Error Codes for [!DNL FreeWheel] Ad Submissions
description: Reference the error codes that are returned for ad submissions to [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 2eb93971-ba82-4de8-96c5-48524d628b70
---
# Error Codes for [!DNL FreeWheel] Ad Submissions

The error messages for failed ad submissions can come from either Advertising Cloud DSP or from [!DNL FreeWheel]. Error messages are shown in the [!UICONTROL API Response] column in the [[!UICONTROL Freewheel Status] dialog](freewheel-check-status.md).

## Advertising Cloud DSP Internal Errors

|Error Message|Description|Next Steps|
|--- |--- |--- |
|[!DNL Awaiting status response from [!DNL FreeWheel]]|[!DNL FreeWheel] hasn't yet responded that the submission was successful or failed.|Check the status again in 10 minutes.|
|[!DNL The submitted ad does not have a clock number assigned.]|[!DNL FreeWheel] doesn't accept UK ads without assigned clock numbers.|Assign a clock number to the ad, and then resubmit the ad.|
|[!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.]|The transcoder hadn't finished transcoding the ad when you attempted to submit the ad.|Wait ten minutes, and then resubmit the ad.|
|[!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.]|The submitted deal is not set up as a programmatic guaranteed deal. [!DNL FreeWheel] accepts only guaranteed deals.|Set up the deal ID as a programmatic guaranteed deal. The ad is automatically submitted to [!DNL FreeWheel] when you save the programmatic guaranteed default placement at the end of deal ID workflow.|
|[!DNL Invalid external_deal_id:] \<deal_id\>|The submitted deal ID either doesn't exist or isn't active on the Adobe end.|Make sure that the deal is active, and then resubmit the ad.|
|[!DNL \[public_id=]\<deal\>] does not exist|The submitted deal id doesn't exist on the [!DNL FreeWheel] end.|Contact your [!DNL FreeWheel] representative to confirm the deal ID.|
|[!DNL Ad with identifier] \<*ad name*\> [!DNL was not found.]|The submitted ad key either doesn't exist or isn't active on the Adobe end.|Find the correct ad key, and then resubmit the ad.|
|[!DNL Pending Submission]|The submission is still pending.|Refresh the page.|

{style="table-layout:auto"}

## [!DNL Freewheel] API Errors

|Code|Meaning|Description|Next Steps|
|--- |--- |--- |--- |
|401|Unauthorized|Incorrect, missing, or invalid access credentials.|Contact your [!DNL Adobe] account team.|
|403|Forbidden|The server understood the request but refuses to authorize it.|Contact your [!DNL Adobe] account team.|
|404|Not Found|The resource you requested is not available. If the Creative ID is not found in the PUT operation, a 404 is returned.|Contact your [!DNL Adobe] account team.|
|405|Method Not Allowed|A request was made of a resource using a request method not supported by that resource (for example, using GET on a method that requires data to be sent by POST, or using PUT on a read-only resource).|Contact your [!DNL Adobe] account team.|
|408|Request Timeout|A timeout occurred while this request was processing. Timeouts usually are caused by concurrent requests of exclusive access to certain resources.|Resubmit the request when you receive this status. If the issue persists, contact your [!DNL Adobe] account team.|
|422|Unprocessable Entity|Invalid resource. This error happens when the request body is invalid or the created/updated resource is invalid (for example, if the Deal ID was not found). See [FreeWheel API 422 Errors](#freewheel-422-errors) for more information.|Contact your [!DNL Adobe] account team.|
|500|Internal Server Error|API system error.|Contact your [!DNL Adobe] account team.|

{style="table-layout:auto"}

## [!DNL Freewheel] API 422 Errors {#freewheel-422-errors}

|Code|HTTP Code|Description|
|--- |--- |--- |
|DATA_UNMARSHALL_FAILURE|422|The request data is invalid json format. Check the error message for details.|
|DATA_VALIDATION_FAILURE|422|The request data is missing required fields or has an invalid data type. Check the error message for details.|
|DATA_DEAL_INVALID|422|The deal is configured incorrectly or doesn't exist. Check the error message for details.|
|DATA_DEAL_GET_FAILURE|422|The deal wasn't found or its configuration has an issue. Check the error message for details.|
|DATA_CREATIVE_INGEST_FAILURE|422|The creative URL is invalid. Check the error message for details.|
|DATA_CREATIVE_LINK_FAILURE|422|The creative wasn't linked to the ad unit nodes of the deal. Check the error message for details.|
|DATA_CREATIVE_UPDATE_FAILURE|422|The creative wasn't updated. Check the error message for details.|
|DATA_DSP_GET_FAILURE|422|The DSP doesn't exist within the system.|
|DATA_CREATIVE_UNLINK_FAILURE|422|The creative wasn't unlinked from ad units.|
|DATA_CREATIVE_DELETE_FAILURE|422|The creative wasn't deleted.|
|DATA_CREATIVE_DETECTION_FAILURE|422|The URL wasn't detected.|
|DATA_ENTITY_NOT_FOUND|422|The creative doesn't exist.|

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Overview of Setting up Programmatic Guaranteed Deals in [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Accept a Deal in the Deal ID Inbox](deal-id-inbox-accept.md)
>* [Submit an Ad for a Programmatic Guaranteed Deal to [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Check the Status of Ads for [!DNL FreeWheel] Programmatic Guaranteed Deals](/help/dsp/inventory/freewheel-check-status.md)
