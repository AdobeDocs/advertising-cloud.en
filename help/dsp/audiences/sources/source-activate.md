---
title: 
description: 
feature: DSP Audiences
---
# TITLE? Does "Activate" belong here?

*Beta feature*




Users who want to activate authenticated audiences through a Durable ID solution within the Advertising Cloud DSP require segment translation into RampIDs recognizable in a biddable environment.  

This can be accomplished by:

•	Leveraging Adobe’s Real-Time CDP integration  and the Adobe-LiveRamp’s Retrieval API
•	Manually sending authenticated segments to the Advertising Cloud DSP from LiveRamp’s Connect dashboard for users or partners not leveraging Adobe’s Real-Time CDP

Both above options require users to reach out to adcloud-support@adobe.com to enable the following Advertising Cloud DSP settings:

1.	LiveRamp RampID campaign configuration prior to segment sharing from Real-Time CDP 
2.	“LiveRamp segments” needs to be enabled in the Advertising Cloud DSP account permissions

 
*Please Note* Failure to complete the above settings will prevent users from targeting authenticated segments on campaigns in the Advertising Cloud DSP 

Users manually sharing authenticated segments from LiveRamp and not Adobe Real-Time CDP, the below step must also be taken in LiveRamp’s Connect dashboard:

•	Ensure destination tile “AAC API 1P Onboarding” is activated 
i.	“Identifier Settings” should be set to Ramp ID only
ii.	If users are looking to still receive cookie-based identifiers, a second AAC API 1P Onboarding destination tile will need to be created that has “Cookies” IDFA” and “AAID” selected


 

Once the preferred method of sharing authenticated first or third-party segments is complete, additional best practices for testing and data validation should be followed:

1.	Target RampID-based segments and cookie-based segments in separate campaigns
•	Campaign settings only allow for one identifier to be prioritized
•	Currently, RampIDs are not retrievable during on-site events. This means certain custom goals, such as lowest CPA and ROAS, are not available with the use of authenticated segments. Leverage cookie-based segments ONLY if you have a restrictive performance KPI

2.	Create one placement in both the RampID and cookie-based campaigns
•	Target the segments that have been shared from LiveRamp using the standard segment activation process 
•	Work with your Advertising Cloud support team to validate proper data distribution

If you would like to learn more about Advertising Cloud DSP’s integration with LiveRamp, contact adcloud-support@adobe.com for more information.



After you XXX, you can [create an audience source](source-create.md).



>[!MORELIKETHIS]
>
>*[About Activating Authenticated Segments from Audience Sources](source-about.md)
>* [Create an Audience Source to Activate First-Party Audiences](source-create.md)
>* [Audience Source Settings](source-settings.md)
