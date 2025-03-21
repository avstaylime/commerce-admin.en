---
title: Transactions
description: Learn about the Transactions page and how to use it to track activity between your store and a payment system.
---
# Transactions

The _Transactions_ page lists all payment activity that has taken place between your store and a payment system, and provides access to more detailed information.

## View transactions

On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Operations]_ > **[!UICONTROL Transactions]**.

![Transactions grid](./assets/transactions.png)<!-- zoom -->

|Column|Description|
|--- |--- |
|[!UICONTROL ID]|A unique numeric identifier that is assigned to each transaction.|
|[!UICONTROL Order ID]|A unique identifier that is assigned when a customer places an order.|
|[!UICONTROL Transaction ID]|A unique numeric identifier that is assigned when a transaction happens after a customer places an order.|
|[!UICONTROL Parent Transaction ID]|The ID number of the parent transaction.|
|[!UICONTROL Payment Method]| The payment method associated with a transaction.|
|[!UICONTROL Transaction Type]|Type of transaction, which can be Order, Authorization, Capture, Void, or Refund.|
|[!UICONTROL Closed]|Whether a transaction is closed or not.|
|[!UICONTROL Created]|Time and date the transaction was created.|

{style="table-layout:auto"}

## View transaction details

Click the entry that you want to view.

On the transaction details page, you can see the transaction detail and child transactions grid.

### Transaction data

This section includes information regarding the transaction, and provides a link to the order page in the **Order ID** column.

|Column|Description|
|--- |--- |
|[!UICONTROL Transaction ID]|The transaction ID number.|
|[!UICONTROL Parent Transaction ID]|A corresponding ID number of the parent transaction, if applicable.|
|[!UICONTROL Transaction Type]|Type of transaction, which can be Order, Authorization, Capture, Void, or Refund.|
|[!UICONTROL Is Closed]|Whether a transaction is closed or not. |
|[!UICONTROL Created At]|Time and date the transaction was created.|

{style="table-layout:auto"}

### Child transactions

Child transactions are displayed in the grid after creating invoices for [orders](orders.md). This allows you to track transaction history, following a transaction hierarchy.

### [!UICONTROL Transaction Details]

This section includes the additional information for a given transaction. Information is displayed in the form of keys and values. The available keys are:

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- customer
- customerIP
- lineItems
- marketType
- order
- payment
- product
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleAmount
- solution
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>If the transaction details are not available or are outdated, click **[!UICONTROL Fetch]** in the button bar to update them.
