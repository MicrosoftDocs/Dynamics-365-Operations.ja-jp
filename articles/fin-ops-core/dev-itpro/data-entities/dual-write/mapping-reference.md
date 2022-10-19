---
title: 二重書き込みマッピングのリファレンス
description: この記事では、各二重書き込みマッピングの列マッピングを一覧表示します。
author: josaw
ms.date: 10/06/2022
ms.topic: reference
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-12-22
ms.openlocfilehash: 2bde40e2b9d7ced453036634ec46156a6b543681
ms.sourcegitcommit: c5591cda7caba17fba282ba419fd6a294e7c5453
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2022
ms.locfileid: "9636872"
---
# <a name="dual-write-mapping-reference"></a>二重書き込みマッピングのリファレンス

[!include [banner](../../includes/banner.md)]

[!include [banner](includes/dual-write-symbols.md)]

## <a name="templates"></a>テンプレート

[!include[source-destination](includes/source-destination.md)]

[!include[mapping-list](includes/mapping-tables.md)]

## <a name="transfer-order-headers"></a>移動オーダーのヘッダー

|**財務と運用フィールド** | **タイプのマッピング** | **Customer Engagement 列** | **既定値** |
|------------------------------------|-------------|----------------------------------|-----------------|
|SHIPPINGADDRESSNAME | > | msdyn_shippingaddressname |
|FORMATTEDSHIPPINGADDRESS | > | msdyn_formattedshippingaddress |
|SHIPPINGADDRESSCITY | > | msdyn_shippingaddresscity |
|SHIPPINGADDRESSCOUNTRYREGIONID | > | msdyn_shippingaddresscountryregionid |
|SHIPPINGADDRESSCOUNTYID | > | msdyn_shippingaddresscountyid |
|SHIPPINGADDRESSDESCRIPTION | > | msdyn_shippingaddressdescription |
|SHIPPINGADDRESSDISTRICTNAME | > | msdyn_shippingaddressdistrictname |
|SHIPPINGADDRESSDUNSNUMBER | > | msdyn_shippingaddressdunsnumber |
|SHIPPINGADDRESSLATITUDE | > | msdyn_shippingaddresslatitude |
|SHIPPINGADDRESSLOCATIONID | > | msdyn_shippingaddresslocationid |
|SHIPPINGADDRESSLONGITUDE | > | msdyn_shippingaddresslongitude |
|SHIPPINGADDRESSPOSTBOX | > |  msdyn_shippingaddresspostbox |
|SHIPPINGADDRESSSTATEID | > | msdyn_shippingaddressstateorprovince |
|SHIPPINGADDRESSSTREET | > | msdyn_shippingaddress1 |
|SHIPPINGADDRESSSTREETNUMBER | > | msdyn_shippingaddress2 |
|SHIPPINGADDRESSTIMEZONE | > | msdyn_shippingaddresstimezone |
|SHIPPINGADDRESSZIPCODE | > | msdyn_shippingaddresspostalcode |
|SHIPPINGCONTACTPERSONNELNUMBER | > | msdyn_shippingcontactpersonnelnumber |
|DELIVERYMODECODE | = | msdyn_shipvia |
|DELIVERYTERMSCODE | = | msdyn_deliveryterm |
|SHIPPINGWAREHOUSEID | = | msdyn_fromwarehouse.msdyn_warehouseidentifier |
|RECEIVINGWAREHOUSEID | = | msdyn_towarehouse.msdyn_warehouseidentifier |
|TRANSITWAREHOUSEID | > | msdyn_transitwarehouse.msdyn_warehouseidentifier |
|REQUESTEDRECEIPTDATE | = | msdyn_receivedate |
|REQUESTEDSHIPPINGDATE | = | msdyn_shipdate |
|RECEIVINGADDRESSNAME | > | msdyn_receivingaddressname |
|TRANSFERORDERNUMBER | = | msdyn_name |
|TRANSFERORDERSTATUS | >> | msdyn_transferstatus |
|RECEIVINGCONTACTPERSONNELNUMBER | > | msdyn_receivingcontactpersonnelnumber |
|FORMATTEDRECEIVINGADDRESS | > | msdyn_formattedreceivingaddress |
|RECEIVINGADDRESSCITY | > | msdyn_receivingaddresscity |
|RECEIVINGADDRESSCOUNTRYREGIONID | > | msdyn_receivingaddresscountryregionid |
|RECEIVINGADDRESSCOUNTYID | > | msdyn_receivingaddresscountyid |
|RECEIVINGADDRESSDESCRIPTION | > | msdyn_receivingaddressdescription |
|RECEIVINGADDRESSDISTRICTNAME | > | msdyn_receivingaddressdistrictname |
|RECEIVINGADDRESSDUNSNUMBER | > | msdyn_receivingaddressdunsnumber |
|RECEIVINGADDRESSLATITUDE | > | msdyn_receivingaddresslatitude |
|RECEIVINGADDRESSLOCATIONID | > | msdyn_receivingaddresslocationid |
|RECEIVINGADDRESSLONGITUDE | > | msdyn_receivingaddresslongitude |
|RECEIVINGADDRESSPOSTBOX | > | msdyn_receivingaddresspostbox |
|RECEIVINGADDRESSSTATEID | > | msdyn_receivingaddressstateorprovince |
|RECEIVINGADDRESSSTREET | > | msdyn_receivingaddresss1 |
|RECEIVINGADDRESSSTREETNUMBER | > | msdyn_receivingaddresss2 |
|RECEIVINGADDRESSTIMEZONE | > | msdyn_receivingaddresstimezone |
|RECEIVINGADDRESSZIPCODE | > | msdyn_receivingaddresspostalcode |

## <a name="transfer-order-products"></a>移動オーダー製品

|**財務と運用フィールド** | **タイプのマッピング** | **Customer Engagement 列** | **既定値** |
|------------------------------------|-------------|----------------------------------|-----------------|
| ITEMNUMBER | = | msdyn_product.msdyn_productnumber |
| LINENUMBER | = | msdyn_lineorder | 
| ALLOWEDOVERDELIVERYPERCENTAGE | = | msdyn_allowedoverdeliverypercentage |
| RECEIVEDCATCHWEIGHTQUANTITY | > | msdyn_catchweightquantityreceived |
| SCRAPPEDCATCHWEIGHTQUANTITY | > | msdyn_catchweightquantityscrapped |
| SHIPPEDCATCHWEIGHTQUANTITY | > | msdyn_catchweightquantityshipped |
| TRANSFERCATCHWEIGHTQUANTITY | = | msdyn_catchweightquantity |
| RECEIVEDQUANTITY | > | msdyn_quantityreceived |
| SCRAPPEDQUANTITY | > | msdyn_quantityscrapped |
| SHIPPEDQUANTITY | > | msdyn_quantityshipped |
| TRANSFERQUANTITY | > | msdyn_quantity |
| REQUESTEDRECEIPTDATE | = | msdyn_receivedate |
| LINESTATUS | >> | msdyn_linestatus |
| REQUESTEDSHIPPINGDATE | = | msdyn_shipdate | 
| TRANSFERORDERNUMBER | = | msdyn_transferorder.msdyn_name | 
| ALLOWEDUNDERDELIVERYPERCENTAGE | = | msdyn_allowedunderdeliverypercentage |
| INVENTORYUNITSYMBOL | > | msdyn_unit |
| SHIPPINGWAREHOUSEID | = | msdyn_shippingwarehouse |
| SHIPPINGSITEID | = | msdyn_shippingsite |
| SHIPPINGWAREHOUSELOCATIONID | = | msdyn_shippinglocation |
