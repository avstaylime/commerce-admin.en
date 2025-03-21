---
title: Archive orders
description: Learn how to configure the order archive to improve performance and streamline Commerce for your organization.
---
# Archive orders

{{ee-feature}}

Archiving orders regularly improves performance and keeps your workspace free of unnecessary information, so you can focus on current business. Invoices, shipments, and credit memos can be archived automatically or manually, and can be viewed at any time.

>[!NOTE]
>
>The _[!UICONTROL Archive]_ option appears in the [!UICONTROL Sales] menu only when archiving is [enabled](https://docs.magento.com/user-guide/configuration/sales/sales.html).

![Orders, Invoices, Shipments, Credit Memos Archiving](./assets/order-move-to-archive.png)<!-- zoom -->

## Configure the order archive

Your store can be configured to archive orders, invoices, shipments, and credit memos after a set number of days. You can move orders and their associated documents to the archive, or restore them to their previous state. Archived orders are not deleted and remain available from the Admin. Archived data can be exported to a CSV file and opened in a spreadsheet. When enabled, the _Archive_ action appears at the top of the workspace.

>[!NOTE]
>
>Adobe Commerce Support recommends enabling Order archiving to save MySQL disk space and improve checkout performance. See [Best practices for order placement performance ](https://support.magento.com/hc/en-us/articles/360048170772) in Adobe Commerce Support Knowledge Base.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand the **[!UICONTROL Sales]** section and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** section.

   ![Orders, Invoices, Shipments, Credit Memos Archiving](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

1. Set **[!UICONTROL Enable Archiving]** to `Yes`.

   >[!NOTE]
   >
   >If you later decide to turn archiving off, all archived orders are restored to the previous state.

1. Set **[!UICONTROL Archive Orders Purchased]** to the number of days to wait before completed orders are archived.

   By default, orders are archived 30 days after the purchase.

1. In the **[!UICONTROL Order Statuses to be Archived]** list, select each order status to use for identifying orders to archive. 

   To select multiple items, hold down the Ctrl (Windows) or Command (Mac) key as you click each item.

1. Click **[!UICONTROL Save Config]**.

1. When prompted, refresh any invalid cache.

## View archived documents

1. In the _[!UICONTROL Sales]_ menu under _[!UICONTROL Archive]_, choose any of the following:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Click any archived document in the list to view details.

## Apply an action to an archived document

Select each document to be the target of the action and choose one of the following **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Manually archive documents

1. Select the type of the document to archive from the following:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Select the checkbox of each item that you want to archive.

1. In the upper-right corner, set **[!UICONTROL Actions]** to `Move to Archive`.

1. Click **[!UICONTROL Submit]** to archive the selected documents.

## Restore archived documents

1. Choose the type of document that you want to restore.

1. Select documents using one of the following options:

   - To select all visible documents, in the upper-left corner, click **[!UICONTROL Select Visible]**.

   - Manually select the checkbox of each document that you want to restore.

1. In the upper-right, set **[!UICONTROL Action]** to `Move to Orders Management`.

1. Click **[!UICONTROL Submit]** to restore the documents.

## Export archived documents

1. Choose the type of document that you want to export.

1. In the upper-right menu, set **[!UICONTROL Export to:]** to one of the following values:

   - `CSV`
   - `Excel`

1. Click **[!UICONTROL Export]**.

Your store can be configured to archive orders, invoices, shipments, and credit memos after a set number of days. You can move orders and their associated documents to the archive, or restore them to their previous state. Archived orders are not deleted and remain available from the Admin. Archived data can be exported to a CSV file and opened in a spreadsheet. When enabled, the _[!UICONTROL Archive]_ command appears at the top of the workspace.

## Manually archive an order

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Operations]_ > **[!UICONTROL Orders]**.

1. To select the order on the grid, select the checkbox in the first column.

   ![Select the orders to archive](./assets/order-select-in-grid.png)<!-- zoom -->

1. Set the **[!UICONTROL Actions]** control to `Move to Archive` and look for the message that order has been archived.

>[!TIP]
>
>To specify a list of order statuses that can be archived, see [Configure the order archive](#configure-the-order-archive).

## View an archived order

1. Open the archive view using one of the following methods:

    - In the button bar above the _[!UICONTROL Orders]_ grid, click **[!UICONTROL Go to Archive]**.

    - On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Archive]_ > **[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Like the Orders page, the title of the archived orders page is _[!UICONTROL Orders]_. The only noticeable difference is the option in the button bar to _[!UICONTROL Return to Orders Management]_. The URL of the page also indicates that you are in the order archive.

1. In the _Action_ column, click **[!UICONTROL View]**.

   ![View Archived Order](./assets/order-archived-view.png)<!-- zoom -->

## Restore an archived order

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Operations]_ > **[!UICONTROL Orders]**.

1. In the button bar, click **[!UICONTROL Go to Archive]**.

1. Find the record to restore and click the checkbox to select it.

   ![Select Order to be Restored](./assets/order-archived-select-to-restore.png)<!-- zoom -->

1. Set the **[!UICONTROL Actions]** control value to `Move to Order Management`.

 Look for the message that the archived order has been removed from the archive.

## Export archived order

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Operations]_ > **[!UICONTROL Orders]**.

1. In the action menu, click **[!UICONTROL Export]** and select the desired format.
