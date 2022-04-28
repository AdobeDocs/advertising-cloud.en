---
title: FAQs
description: xxx
---
# FAQs xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214
By default, Adobe Analytics reports all captured events in every report. "[!UICONTROL Unspecified]" events represent form completion events that weren't connected to Advertising Cloud. For example, in the Ad Platform report, organic conversions or conversions driven by an email campaign would fall into "unspecified."

You can use the filter to remove unspecified events from reports by removing the check mark by “Include Unspecified (none)” option. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323
Put Analytics event tags in the same spots as the Ad Cloud pixels to make sure XXX match.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q: During our internal security audit, certain features were flagged as security concern that we enabled when we integrated Ad Cloud into our existing Adobe Analytics installation.

The integration in question is between the AdCloud and Adobe Audience Manager. This feature increases the match rate for the visitor ID between AdCloud and Adobe Audience Manager. It does this by sending network requests to pagead.l.doubleclick.net, star-mini.c10r.facebook.com and pug88000nf.pubmatic.com to determine if these services have an existing ID for the visitor that can be leveraged. These are the network requests that have been flagged as a security risk and are occurring for all site visitors.

Our auditor is asking us to disable this feature. What happens if we block those network requests?

A:  We checked with our product and they mentioned that the pixels in question are for the purpose of increasing cookie match rates between Ad Cloud, specific inventory/SSP partners (with respect to DSP), and AAM.  If they are removed, the customer may see some level of diminished match rate between AAC/AAM and the inventory partners the respective pixels are for, but they wouldn't expect it to be substantial.

For Ad Cloud Search, we do see the advertiser's Experience Cloud organization ID is setup for Mathworks but our product team don’t see Mathworks setup to activate audiences in Ad Cloud. Are you using Adobe Audience manager for sending Audiences to Ad Cloud Search? If not, removing these will not have an impact on current workflow. AAM Customer Care can assist with the removal of these pixels if you don’t want them to be fired. 

