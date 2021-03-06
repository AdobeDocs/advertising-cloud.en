---
title: Create a Custom Goal
description: Create a Custom Goal
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
---
# Create a Custom Goal

>[!TIP]
>
>See the [best practices for creating custom goals](custom-goal-best-practices.md) for tips on how to configure your custom goals.

1. Log into Advertising Cloud Search at (U.S. companies) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) or (companies in all other countries) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Make sure the metrics you want to include in your goal have been tracked, are available in the product, and include a display name:
    1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]**.
    1. Locate the metric, and make sure that **[!UICONTROL Show in UI and Reports]** is enabled for the metric.
    1. If the metric doesn't have a value in the **[!UICONTROL Display Name]** column, click in the cell, enter the display name, and then click **[!UICONTROL Apply].**
1. Create the custom goal as an *objective*:
    1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Optimization] > [!UICONTROL Objectives]**.
    1. In the toolbar, click **[!UICONTROL Create objective].**
    1. Enter the objective settings:
        1. In the **[!UICONTROL Change Objective Name]** field, enter the objective name.

           The objective name will be shown in the [!UICONTROL Custom Goals] list in Advertising Cloud DSP package settings.

        1. Associate properties with the objective:
        
           >[!NOTE]
           >
           > All of the transaction properties tracked for the advertiser are listed by default in the [!UICONTROL Available Properties] list.

            * To import a CSV file with properties and their weights, click **[!UICONTROL Import]** and locate the file to import.
            
               The imported properties must already exist for the advertiser; the names aren't case-sensitive.
               
               The imported properties will replace any existing properties specified.
               
            * To manually specify the first property with the default weight (1), select from a list of all of the transaction properties tracked for the advertiser.
            
            * To manually add another property with the default weight (1), click **[!UICONTROL +]** .

               >[!TIP]
               >
               > To search for a property in the list, enter a string from anywhere within the property name.

            * To manually add multiple properties, click **[!UICONTROL Add Multiple Properties].** For each property you want to add, click the property name in the [!UICONTROL Available Properties] column and drag it into the [!UICONTROL Added Properties] column. When you're finished adding properties, click **[!UICONTROL Add]**.

               >[!TIP]
               >
               >* To search for a property in the list, enter a string from anywhere within the property name in the input field.
               >* To filter the list to exclude properties that are excluded in reports, select the option **[!UICONTROL Hide properties excluded from reports].**
               
            * (When the objective contains multiple properties) To change the weight of a property relative to the other properties in the objective, enter values in the **[!UICONTROL Weight]** field(s).
            
        1. At the bottom of the settings, click **[!UICONTROL Save]**.

Once you create an objective, you can assign it to an Advertising Cloud DSP package as a custom goal when the optimization goal is "[!UICONTROL Highest ROAS - Custom Goal]" or "[!UICONTROL Lowest CPA - Custom Goal]."

>[!TIP]
>
>For optimized <!-- optimum? Or optimization won't happen at all w/out it? -->performance, the combined metrics in the custom goal (objective) must total at least 10 conversions per day. When they don't, the best practice is to add additional supporting events (transaction properties), such a product pages or application starts, to the objective. See [Best Practices for Building a Custom Goal](custom-goal-best-practices.md) for guidelines.

>[!MORELIKETHIS]
>
>* [About Custom Goals](custom-goal-about.md)
>* [Best Practices for Building a Custom Goal](custom-goal-best-practices.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
