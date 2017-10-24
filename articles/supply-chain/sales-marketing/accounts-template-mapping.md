---
title: "Finance and Operations で売上勘定を顧客に同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise edition に勘定を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Finance and Operations で売上勘定を顧客に同期する

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。 

このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に勘定を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="template-and-task"></a>テンプレートおよびタスク

売上から Finance and Operations への勘定同期には、以下のテンプレートと基本的なタスクが使用されます。

- **テンプレートの名前:** 勘定 (売上から Finance and Operations)
- **プロジェクトのタスクの名前:** - 勘定 - 勘定 - 顧客

勘定/顧客を同期する前に必要なタスクの同期: なし

## <a name="entity-set"></a>エンティティ セット

| 売上    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| アカウント | アカウント | 顧客              |

## <a name="entity-flow"></a>エンティティのフロー

勘定は売上で管理され、Finance and Operations に顧客として同期されます。 この顧客の**外部管理**プロパティを**はい**に設定し、売上から生成される顧客を追跡します。 請求時に、この情報は、売上に同期される請求書のフィルター処理に使用されます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

**勘定番号**フィールドは、**勘定**ページで利用できます。 統合をサポートするための自然で固有のキーとなっています。 顧客関係管理 (CRM) ソリューションのナチュラル キー機能は、すでに **勘定番号** フィールドを使用しているが、勘定ごとに一意の **勘定番号** 値を使用していない顧客に影響する可能性があります。 現時点では、統合ソリューションは、このケースをサポートしていません。

新しいアカウントが作成され、**勘定番号**値が存在しない場合、番号順序を使用して自動的に生成されます。 その値は**勘定**で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。 次に例を示します: **ACC-01000-BVRCPS**

売上の統合ソリューションが適用されている場合、アップグレード スクリプトにより、売上の既存のアカウントの、**勘定番号**フィールドが設定されます。 **勘定番号**値がない場合は、前述した番号順序を使用します。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

- [**CDS &gt; 出力先**] からの **CustomerGroupId** マッピングは Finance and Operations で有効な値に更新する必要があります。 既定値を指定するか、値マップを使用して値を設定できます。 既定のテンプレートの値は **10** です。
- **住所/国の地域コード** フィールドが Finance and Operations では必要です。 同期エラーを回避するために、[**CDS &gt; 出力先**] からのマッピングで既定値を指定できます。 販売でこのフィールドが空白の場合、既定値が使用されます。

    - [**AddressCountryRegionISOCode**] の既定のテンプレート値は **USA** です。
    - **DeliveryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。

- 次のマッピングを **CD&gt;出力先** から追加することによって、Finance and Operations で必要な手動更新の数を減らすことができます。 たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。

    - **SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。 デフォルトのサイトは、製品から、または注文ヘッダーの顧客から取得できます。 **SiteId** の既定のテンプレート値は **1** です。
    - **WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。 デフォルト倉庫は、製品から、または Finance and Operations の受注ヘッダーの顧客から取得できます。 **WarehouseId** の既定のテンプレート値は **13** です。
    - **LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。 既定では、顧客からの注文ヘッダの言語が使用されます。 **LanguageId** の既定のテンプレート値は **en-us** です。

- **ソース &gt; CD** マッピングの順に移動し、CD の組織 ID (**Organization_OrganizationId**) を更新します。 既定のテンプレートの値は **ORG001** です。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

> [!NOTE]
> [**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングには含まれていません。 これらのフィールドをマップするには、値マッピングを設定する必要があります。 値マッピングは、エンティティ間で同期される組織内のデータ固有です。

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

![データ インテグレーターでテンプレートのマッピング](./media/accounts-template-mapping-data-integrator-1.png)

![データ インテグレーターの勘定のテンプレート マッピング](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>関連トピック

[Finance and Operations の製品を売上の製品に同期する](products-template-mapping.md)

[売上の連絡先を Finance and Operations の連絡先または顧客に同期させる](contacts-template-mapping.md)

[販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期](sales-quotation-template-mapping.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-order-template-mapping.md)

[売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-invoice-template-mapping.md)




