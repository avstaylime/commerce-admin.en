---
title: Checks and money orders
description: Learn how to set up check and money order as an offline method of payment on your store.
---
# Checks and money orders

Adobe Commerce and Magento Open Source allow you to accept payments by check or money order. The _Check / Money Order_ payment method is enabled for your store by default. You can accept checks and money orders only from specific countries, and you can fine tune the configuration with minimum and maximum order total limits.

**_To configure payment by check or money order:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Check / Money Order]** section.

   ![Check / Money Order](../configuration-reference/sales/assets/payment-methods-check-money-order.png)<!-- zoom -->

   For a detailed description of each of these configuration settings, see [Check / Money Order](https://docs.magento.com/user-guide/configuration/sales/payment-methods.html#check--money-order) in the _Configuration Reference Guide_.

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To accept payment by check or money order, set **[!UICONTROL Enabled]** to `Yes`.

1. Enter a **[!UICONTROL Title]** to identify the Check / Money Order payment method during checkout.

1. If orders typically wait for approval, accept the default **[!UICONTROL New Order Status]** as `Pending"` until it is approved.

   If you prefer, you can use the `Processing` or `Suspected Fraud` status for new orders with this payment method.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. For **[!UICONTROL Make Check Payable To]**, enter the name of the party to whom the check must be payable.

1. For **[!UICONTROL Send Check To]**, enter the street address or PO Box where the checks are mailed.

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the order amounts required to qualify for this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. Enter a **[!UICONTROL Sort Order]** number to determine the position of this item in the list of payment methods that is displayed during checkout.

   This is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
