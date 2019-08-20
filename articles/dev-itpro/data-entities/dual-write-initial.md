---
title: Finance and Operations と Common Data Service の初期同期に対する執行命令
description: このトピックでは、初期データを作成するために従う必要がある同期の順序を指定します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797301"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operations と Common Data Service の初期同期に対する執行命令

データ統合を使用する前に、顧客、仕入先、および取引先担当者に必要な初期データを作成する必要があります。 たとえば、新しい**仕入先グループ**品目を作成し、その**支払条件**を **Net30** として設定する場合、**仕入先グループ**品目の作成を試みる前に、**Net30** が Finance and Operations と Common Data Service 両方に存在しすることを確認します。 (将来的には、**初期同期**と呼ばれるデュアル書き込みプラットフォーム機能をリリースする予定です。デュアル書き込みセットアップの一部として Finance and Operations と Common Data Service 間で 1 回限りのデータ同期が行われます)

ヒント: **支払条件** (支払条件) を含むすべての参照データのデュアル書き込みマップをリリースします。 1 つのシステムに初期データが既に含まれる場合は、レコードの小さな更新操作によって、そのレコードのデュアル書き込みをトリガーできます。 

次の優先順位に従い、初期データが Finance and Operations と Common Data Service の両方で使用できるようにする必要があります。   

## <a name="vendor"></a>仕入先

仕入先の実行順序は次のとおりです。

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>顧客 (組織)

顧客の実行順序は次のとおりです。

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>連絡先 (名前)

連絡先の実行順序は次のとおりです。

```
Customer
Vendor               
```
