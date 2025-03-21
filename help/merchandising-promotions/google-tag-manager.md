---
title: "[!DNL Google Tag Manager]"
description: Learn how to use [!DNL Google Tag Manager] to manage the many tags (snippets of code) that are related to your marketing campaign events in your Adobe Commerce sites.
---
# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] helps you manage the many tags, or snippets of code, that are related to your marketing campaign events. [!DNL Google Tag Manager] gives you the ability to add tracking tags to your site to measure the audience, or to personalize, retarget, or conduct search engine marketing initiatives.

[!DNL Google Tag Manager] directly transfers data and events to [!DNL Google Analytics], Enhanced Ecommerce, and other third-party analytics solutions to produce a clear picture of how well your site, products, and promotions are performing.

You should have a [!DNL Google Analytics] and [!DNL Tag Manager] account to continue this process. The following instructions walk you through the process of configuring your Google accounts, configuring your Commerce store, and creating a tag.

>[!NOTE]
>
>If your business is subject to privacy regulations such as the [General Data Protection Regulation](../getting-started/compliance-gdpr.md) and/or the [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), see [Google Privacy Settings](google-tools.md#google-privacy-settings).

## Step 1. Configure your [!DNL Google Analytics] account

See [Set up Site Search][7] in Google Help for the basics you need to get started. Also see the Google guides for [Google Analytics][1] and [Google Tag Manager][2].

1. Sign in to your [!DNL Google Analytics] account.

1. To enable **[!UICONTROL Internal Site Search Tracking]**, do the following:

    - Navigate to **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

    - Set **[!UICONTROL Site Search Tracking]** to `On`.

    - Set **[!UICONTROL Query]** parameter to `q`.

    - When complete, **[!UICONTROL Save]** the settings.

1. To enable display features, do the following:

    - Choose **[!UICONTROL Property Settings]**.

    - Under _[!UICONTROL Advertising Features]_, set **[!UICONTROL Enable Demographics and Interest Reports]** to `On`.

    - **[!UICONTROL Save]** the settings.

1. To enable Ecommerce Tracking, do the following:

    - Navigate to **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

    - Set **[!UICONTROL Enable Ecommerce]** to `On`.

    - Set **[!UICONTROL Enable Enhanced Ecommerce Reporting]** to `On`.

    - **[!UICONTROL Save]** the settings.

1. Reload the page to verify that all the settings remain `On`.

   >[!NOTE]
   >
   >If not all settings are `On`, repeat the previous steps, save, and reload the page. Repeat this process until all settings are set to `On`.

## Step 2. Configure your [!DNL Google Tag Manager] account

The following instructions show how to configure a new container with the basic settings. A sample [Composer][4] configuration (.json) file is used to simplify the process, importing to generate a tag in a new container. For this example, we recommend that you create a container, rather than modify an existing container.

>[!NOTE]
>
>For additional information, see Google's [Container export and import][5]. These instructions walk-through importing a sample JSON to a new container.

1. Download the linked file [GTM_M2_Config_json.txt][6] and open the file in an editor, and save as `GTM_M2_Config.json`.

   The json file is uploaded directly to [!DNL Google Tag Manager].

1. Navigate to **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Click **[!UICONTROL Choose container file]** and select the json file.

1. Under **[!UICONTROL Choose workspace]**, click **[!UICONTROL New]**.

1. Enter a title and description, then click **[!UICONTROL Save]**.

1. Select one of the following actions to import the file:

    - The **[!UICONTROL Overwrite]** option should be selected for a new container.

    - The **[!UICONTROL Merge]** option should be selected if you are using an existing container.

1. Click **[!UICONTROL Preview]** to review the tags, triggers, and variables.

1. To edit the **[!UICONTROL Google Analytics ID]** that is referenced in variables, do the following:

    - Navigate to **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

    - Choose **[!UICONTROL Google Analytics]** and update the placeholder (`UA-xxxxxx-x`) with your own **[!UICONTROL GA ID]**.

1. Follow Google's instructions to add tags, triggers, and variables to the new container.

    If you have settings in another container that you want to use, they can be moved to the new container.

1. Click **[!UICONTROL Confirm]** when complete.

1. Follow Google's instructions to publish the new container.

## Step 3. Configure your store

{{gtag-api-note}}

1. Log in to the Admin of your Commerce store.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Google API]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Google Analytics]** section and configure the following:

    ![Sales configuration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png)<!-- zoom -->

    - Set **[!UICONTROL Enable]** to `Yes`.

    - Set **[!UICONTROL Account type]** to `Google Tag Manager`.

    - In the **[!UICONTROL Container ID]** field, enter your GTM ID (`GTM-xxxxxx`).

    - If you are also using Google Analytics to content experiments, set **Enable Content Experiments** to `Yes`.

    - Use the default values for the remaining fields.

1. When complete, click **[!UICONTROL Save Config]**.

1. Test your [!DNL Google Tag Manager] settings to verify that everything works correctly.

>[!NOTE]
>
>Each container is associated with one website and you only need one container per account. If you have a multi-site Commerce instance, you need separate containers.

## Step 4. Add the GTM code to your Adobe Commerce store

1. To copy the GTM code, go to **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   There are two GTM code snippets to be added to your Commerce site: the first one for the `<head>` tag and the second for the `<body>` tag.

   ![Install Google Tag Manager](./assets/install-google-tag-manager.png)<!-- zoom -->

1. In the Commerce Admin, go to **[!UICONTROL Content]** > _[!UICONTROL Design]_ > **[!UICONTROL Configuration]** and open the store view in edit mode.

1. Under _[!UICONTROL Other Settings]_, expand **[!UICONTROL HTML Head]** and paste the code you copied from GTM for the `<head>` tag in the **[!UICONTROL Scripts and Style Sheets]** field.

   ![Inserting code in the HTML Head](./assets/head-tag.png)<!-- zoom -->

1. Expand **[!UICONTROL Footer]** and paste the GTM code for `<body>` in the **[!UICONTROL Miscellaneous HTML]** field.

   ![Inserting code in the Footer](./assets/footer-tag-section.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Configuration]**.

## Field descriptions

|Field|Scope|Description|
|--- |--- |--- |
|[!UICONTROL Enable]|Store View|Determines if Google Analytics Enhanced Ecommerce can be used to analyze activity in your store. Options: `Yes` / `No`|
|[!UICONTROL Account type]|Store View|Determines the Google tracking code that is used to monitor store activity and traffic. Options: `Google Analytics` / `Google Tag Manager`|
|[!UICONTROL Anonymize IP]|Store View|Determines if identifying information is removed from IP addresses that appear in Google Analytics results.|
|[!UICONTROL Enable Content Experiments]|Store View|Activates Google Content Experiments, which can be used to test up to ten different versions of the same page. Options: `Yes` / `No`|
|[!UICONTROL Container Id]|Store View|If [!DNL Google Tag Manager] is already installed and configured for your store, the Container ID appears automatically in this field.|
|[!UICONTROL List property for the catalog page]|Store View|Identifies the Tag Manager property associated with the catalog page. Default value: `Catalog Page`|
|[!UICONTROL List property for the cross-sell block]|Store View|Identifies the Tag Manager property associated with the cross-sell block. Default value: `Cross-sell`|
|[!UICONTROL List property for the up-sell block]|Store View|Identifies the Tag Manager property associated with the up-sell block. Default value: `Up-sell`|
|[!UICONTROL List property for the related products block]|Store View|Identifies the Tag Manager property associated with the related products block. Default value: `Related Products`|
|[!UICONTROL List property for the search results page]|Store View|Identifies the Tag Manager property associated with the search results page. Default value: `Search Results`|
|[!UICONTROL "Internal Promotions" for promotions field "Label"]|Store View|Identifies the Tag Manager property associated with the labels for internal promotions. Default value: `Label`|

{style="table-layout:auto"}

## Create a tag to track conversions

If you have a Google AdWords account, you can create a tag that tracks conversions. The following example shows how to use both [!DNL Google Tag Manager] and [!DNL Google Analytics] to create a tag that fires on your store's conversion _Success_"_ page.

### Step 1. Create a tag

1. Log in to your [!DNL Google Tag Manager] account and click the link for the container that you created for your store.

1. In the **[!UICONTROL New Tag]** box, click **[!UICONTROL Add a new tag]**.

   ![Google Tag Manager - new workspace](./assets/gtm-workspace-new.png)<!-- zoom -->

1. Get the following information from your AdWords account:

    - Conversion ID
    - Conversion Label

   If you need help, visit Google's [support site][8].

1. From the [!DNL Google Tag Manager] dashboard, click **[!UICONTROL Google AdWords]** and do the following:

    - Click the title placeholder and enter a name for the new tag.

    - Under **[!UICONTROL Choose Product]**, select **[!UICONTROL Google AdWords]**.

      ![Google Tag Manager - choose Google Adwords](./assets/gtm-create-adwords-tag1.png)<!-- zoom -->

    - Under _[!UICONTROL Choose a Tag Type]_, select **[!UICONTROL AdWords Conversion Tracking]** and click **[!UICONTROL Continue]**.

      ![Google Tag Manager - Adwords conversion tracking](./assets/gtm-create-adwords-tag2.png)<!-- zoom -->

1. Enter the **[!UICONTROL Conversion ID]** and **[!UICONTROL Conversion Label]** from your AdWords account and click **[!UICONTROL Continue]**.

    ![Google Tag Manager - conversion ID and label](./assets/gtm-create-adwords-tag3.png)<!-- zoom -->

### Step 2. Create a rule

Continuing from the [!DNL Google Tag Manager] dashboard, the next step is to create a rule that fires the tag on the conversion page.

1. Under **[!UICONTROL Fire On]**, click **[!UICONTROL Some Pages]**.

   ![Google Tag Manager - fire on](./assets/gtm-create-adwords-tag4.png)<!-- zoom -->

1. In the _[!UICONTROL Choose Pages]_ section, complete the following settings:

   - **[!UICONTROL Name]** - Enter a name for the page description.

   - **[!UICONTROL Variable]** `url`

   - **Operation** - `matches RegEx`

      To learn more, see [Regex and CSS selector operators][9] in Tag Manager Help.

   - **[!UICONTROL Value]** - `checkout/success.*`

   ![Google Tag Manager - conversion page location](./assets/gtm-create-adwords-tag6.png)<!-- zoom -->

1. Select the green checkbox and click **[!UICONTROL Save]**.

   The trigger that you set up appears as a blue button in the Fire On section.

1. When complete, click **[!UICONTROL Save Tag]**.

   ![Google Tag Manager - trigger setup success](./assets/gtm-create-adwords-tag7.png)<!-- zoom -->

### Step 3. Preview and publish

The next step in the process is to preview the tag. Each time the tag is previewed, a snapshot of the version is saved. When you are satisfied with the results, go to the version that you want to use and click **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/1008015
[2]: https://support.google.com/tagmanager/answer/6102821
[3]: https://support.google.com/analytics/answer/1012264
[4]: https://developer.adobe.com/commerce/php/development/composer/
[5]: https://support.google.com/tagmanager/answer/6106997
[6]: https://docs.magento.com/m2/downloads/GTM_M2_Config_json.txt
[7]: https://support.google.com/analytics/answer/1012264
[8]: https://support.google.com/tagmanager/answer/6105160
[9]: https://support.google.com/tagmanager/answer/7679109
