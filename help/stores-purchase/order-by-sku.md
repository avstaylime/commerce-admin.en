---
title: Order by SKU
description: Learn how to configure your store to support ordering by SKU as a convenience for your customers.
---
# Order by SKU

{{ee-feature}}

Order by SKU is a [widget](../content-design/widgets.md) that can be displayed in the store as a convenience for all shoppers, or made available to only those in specific customer groups. Shoppers can either enter the SKU and quantity information directly into the Order by SKU block, or upload a csv file from their customer account. Regardless of the configuration, order by SKU is always available to store administrators.

![Order by SKU in the Storefront](./assets/storefront-order-by-sku.png)<!-- zoom -->

## Configure order by SKU

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand the **[!UICONTROL Sales]** section and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Order by SKU Settings]** section.

1. Set **[!UICONTROL Enable Order by SKU on my Account in Storefront]** to one of the following:

    - `Yes, for Everyone` – The Order by SKU block is available in the store for every shopper.
    - `Yes, for Specified Customer Groups` – Order by SKU is available only to members of a specific customer group, such as `Wholesale`.
    - `No` – The Order by SKU block does not appear in the storefront, and the Order by SKU page is not available in the  customer account.

      ![Order by SKU Settings](../configuration-reference/sales/assets/sales-order-by-sku-settings.png)<!-- zoom -->

1. Click **[!UICONTROL Save Config]**.

![B2B for Adobe Commerce](../assets/b2b.svg) (B2B for Adobe Commerce only) _**To enable the Order by SKU function, disable the Quick Order function:**_

1. Go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL General]_, choose **[!UICONTROL B2B Features]**

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL B2B Features]** section.

1. Set **[!UICONTROL Enable Quick Order]** to `No`.

   The [Quick Order feature](../b2b/quick-order.md) allows customers and guests to quickly place orders based on SKU or product name.

## Order by SKU storefront experience

When the functionality is configured for the store, customers can order by SKU from any page that includes the _Order by SKU_ widget or from their account dashboard.

### Order by SKU from the page block

1. In the _Order by SKU_ block, the customer enters the **[!UICONTROL SKU]** and **[!UICONTROL Qty]** of the item to be ordered.

1. To add another item, clicks **[!UICONTROL Add Row]** and repeat the process.

1. Clicks **[!UICONTROL Add to Cart]**.

### Order by SKU from a customer account

1. From the storefront, the customer logs in to their account.

1. In the panel on the left, chooses **[!UICONTROL Order by SKU]**.

1. Adds individual items according to preference:

   _**Adds each item by SKU:**_

      - Enters the **[!UICONTROL SKU]** and **[!UICONTROL Qty]** of the item to be ordered.

      - To add additional items as needed, clicks _Add Row_ ![Plus sign button](../assets/button-add-item.png) and repeats for as many items as necessary.

   _**Uploads a CSV file of multiple items:**_

      - Prepares a CSV file that includes columns for SKU and Qty.

      - To upload the CSV file, clicks **[!UICONTROL Choose File]** and select the file to upload.

      - Clicks **[!UICONTROL Add to Cart]**.
