---
title: Syntax for Audience Segment Logic
description: Reference the syntax you can use to define the logic for audience segments.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
---
# Syntax for Audience Segment Logic

When you create reusable audiences, you can manually define segment logic using alphanumeric segment IDs and the following syntax:

* () to indicate a group
* `||` for [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* && for [!DNL AND]
* ! for [!DNL NOT] (exclude)

>[!NOTE]
>
>* All specified segment groups are included unless they're preceded by ! (which excludes them).

For example, the following logic:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

means (in plain English)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>In placement settings, you can use saved audiences either as audiences to explicitly target or as separate audiences to exclude from targeting. Make sure your segment logic reflects the purpose for which you will be using the audience.

>[!MORELIKETHIS]
>
>* [About Audience Management](audience-about.md)
>* [Create a Reusable Audience](reusable-audience-create.md)
>* [Audience Settings](audience-settings.md)
>* [Available Third-party Data Providers](third-party-data-providers.md)
