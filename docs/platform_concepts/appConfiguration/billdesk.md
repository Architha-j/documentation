---
title : Billdesk
sidebar_label : Billdesk UPI
---


## Scope of Integration

Yellow.ai Integration with Billdesk Payment Gateway allows you to create UPI Intent for WA Pay, view payment status and Send UPI notification with the yellow.ai platform. 

## Configuration

Configuring the integration with Billdesk is straightforward. Follow the steps defined below to start integrating:

1. Get the KeyId, Client Id, Merchant Id, Public Key File and API Base URL from Billdesk Team.

2. Upload your Public Key file in some bucket or server like (AWS-S3, SFTP, etc) and Get the public CDN Url . Note:(CDN URL should be public readable).

3. Now Go to Integration page and Enter the right value in Billdesk's form to connect the billdesk Integration.

![alt_text](https://cdn.yellowmessenger.com/NsZFcYu9H3md1666156528149.png "image_tooltip")

If you have multiple accounts, follow the above mentioned steps to add each of them.

:::note
1. Enter a unique name for each account to easily identify them within the yellow.ai platform. It is recommended to use a name that aligns with its purpose for better usability. 
2. You can add a maximum of 5 merchant accounts.
3. In a two-tier environment, such as bots with only Development/Live environments, you can add account names only in the development mode. Once added and flows have been built, in the Live mode, you can only choose the account names and not edit them.
4. In a three-tier environment, such as bots with Staging/Sandbox/Production modes, in Staging and Sandbox modes, you can add and edit new accounts. However, in Production, only the account details added in Staging will be available. You can only map in the production environment.
:::

### Event for receving payment confirmation on bot
Following are the events which are currently accommodated in the Integration:

Event | Description
----- | -----------
Billdesk Payment Status | In case of payments the status can be checked with these details.
Please Activate the Billdesk Payment Status after configuring instamojo credentials at integration page.

:::info
If you have added multiple accounts in your platform, enable events for each of those accounts.
:::


## Use-cases 

Following are the use-cases which are currently accommodated in the Integration:

:::note
When multiple accounts are added, select the appropriate account for each node, allowing you to leverage the unique functionalities of each account for their intended purposes.
:::

### 1. Generate UPI Intent

Get the final amount from your cart total and call the Generate UPI Intent action node of integration, get the transaction Id and Intent URI for whatsapp pay api.


_ Node Input Params:-_ 

|Field Name|Sample Input|Description|
|--- |--- |--- |
|Amount*|200|The amount for the request.|
|Additional Parameters|any varchar|additional_info values that can be attached to the transaction.|
|Additional Parameters|John@test.com|additional_info values that can be attached to the transaction.|
|Additional Parameters|Some value|additional_info values that can be attached to the transaction.|

![alt_text](https://cdn.yellowmessenger.com/kWOnZfYtuAMB1666156690035.png "image_tooltip")

##### Note: To use in app.ym's bot use below function
```
app.executeIntegrationAction({
    "integrationName": "billdesk",
    "action": "Generate UPI Intent",
    "dynamicParams": {
        "amount": 100
    }
}).then((res)=>{
    console.log("response from action node", res);
    app.log(res, '||Response from action node||')
}).catch((err)=>{
    console.log("Error in action node",err);
    app.log(err, '||Error in action node||')
})
```
##### Sample Success Response:
```
{
  "objectid": "transaction",
  "transactionid": "X7890477676443",
  "orderid": "UPIODR00000004",
  "mercid": "BDMERCID",
  "transaction_date": "2022-03- 18T11:50:27+05:30",
  "amount": "2.00",
  "surcharge": "0.00",
  "txn_process_type": "collect",
  "bankid": "789",
  "itemcode": "DIRECT",
  "auth_status": "0002",
  "transaction_error_code": "TRP0000",
  "transaction_error_desc": "Transaction Pending",
  "transaction_error_type": "pending",
  "payment_method_type": "upi"
```

### 2. Generate UPI Collect

The end customer will authorize the transaction via the UPI PSP mobile app. On successful authorisation, BillDesk will receive a callback from the acquirer, and in turn BillDesk will notify the merchant via webhook notification.

_ Node Input Params:-_ 

|Field Name|Sample Input|Description|
|--- |--- |--- |
|Amount*|200|The amount for the request.|
|VPA*|billdesk@upi|UPI Id of customer|
|Additional Parameters|any varchar|additional_info values that can be attached to the transaction.|
|Additional Parameters|John@test.com|additional_info values that can be attached to the transaction.|
|Additional Parameters|Some value|additional_info values that can be attached to the transaction.|

##### Note: To use in app.ym's bot use below function
```
app.executeIntegrationAction({
    "integrationName": "billdesk",
    "action": "Generate UPI Collect",
    "dynamicParams": {
        "amount": 100,
        "vpa":"billdesk@upi",
        "additionalParameters4":"anything"
        "additionalParameters5":"anything"
        "additionalParameters6":"anything"
    }
}).then((res)=>{
    console.log("response from action node", res);
    app.log(res, '||Response from action node||')
}).catch((err)=>{
    console.log("Error in action node",err);
    app.log(err, '||Error in action node||')
})
```
##### Sample Success Response:
```
{
  "objectid": "transaction",
  "transactionid": "X7890477676443",
  "orderid": "UPIODR00000004",
  "mercid": "BDMERCID",
  "transaction_date": "2022-03- 18T11:50:27+05:30",
  "amount": "2.00",
  "surcharge": "0.00",
  "txn_process_type": "collect",
  "bankid": "789",
  "itemcode": "DIRECT",
  "auth_status": "0002",
  "transaction_error_code": "TRP0000",
  "transaction_error_desc": "Transaction Pending",
  "transaction_error_type": "pending",
  "payment_method_type": "upi"
```






