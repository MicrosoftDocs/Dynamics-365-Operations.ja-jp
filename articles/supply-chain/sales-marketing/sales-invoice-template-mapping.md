---
title: "売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。 

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

Finance and Operations から Sales への売上請求書ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合でのテンプレートの名前** 

     - 売上請求書 (Finance and Operations から Sales)

- **データ統合プロジェクトのタスク名**

    - SalesInvoiceHeader
    - SalesInvoiceLine

売上請求書ヘッダーおよび明細行の同期より前に必要な同期タスク。
-   製品 (Finance and Operations から Sales)
-   勘定 (Sales から Finance and Operations) (使用されている場合)
-   連絡先 (Sales から Finance and Operations) (使用されている場合)
-   販売注文ヘッダーおよび明細行 (Finance and Operations から Sales)

## <a name="entity-set"></a>エンティティ セット

| Finance and Operations                               | Common Data Service (CDS)              | 売上          |
|------------------------------------------------------|------------------|----------------|
| 外部的に管理された顧客の売上請求書ヘッダー | SalesInvoice     | 請求書       |
| 外部的に管理された顧客の売上請求書明細行   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>エンティティのフロー

売上請求書が Finance and Operations で作成され Sales に同期されます。

> [!NOTE]
> [**売上請求書ヘッダー**] での税に関連する費用は、現在 Finance and Operations から Sales への同期に含まれていません。 これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。 明細行レベルでの税に関連する費用が含まれます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

-  [**請求書番号フィールドで**] が [**請求書**] エンティティに追加され、ページに表示されます。
 
-  請求書が Finance and Operations で作成され Sales に同期されるため、[**販売注文**] ページで [**請求書の作成**] ボタンは非表示になります。 請求書は Finance and Operations から同期されるため、[**請求書**] ページは編集できません。
 
-  Finance and Operations からの関連する請求書が Sales に同期されると、[**販売注文状態**] は自動的に [**請求済**] に変更します。 また、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。 これにより、販売注文書の所有者は、請求書を表示することができます。
 
## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

売上請求書を同期する前に、次の設定でシステムを更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

- [**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**システム プライジング計算システムの使用**] が [**はい**] に設定されていることを確認します。 

- [**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**割引の計算方法**] が [**明細行品目**] に設定されていることを確認します。 

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader タスク

- [**ソース**] > [**CDS**] で [**CDS 組織 ID**] のマッピングを更新します。 

    -  [**SalesOrder_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。
    -  [**Account_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。
    -  [**Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。

- [**ソース**] > [**InvoiceCountryRegionId 用 CDs**] で [**BillingAddress_Country**] に必要なマッピングが存在することを確認します。

    -  マップされている国の数のテンプレート値は [**ValueMap**] です。

- Sales で売上請求書を作成するために [**価格リスト**] が必要です。 [**CDS**] > [**pricelevelid.name [価格リスト名] の出力先**] で、Sales で通貨ごとに使用される [**価格リスト**] への [**ValueMap**] を更新します。 1 つの通貨に対する既定の [**価格リスト**] を使用するか、または複数の通貨で [**価格リスト**] がある場合 [**ValueMap**] を使用するかのいずれかができます。

    -  [**pricelevelid.name [価格リスト名]**] のテンプレート値は [**通貨**] に基づく [**ValueMap**] です。
    -  usd: CRM サービス USA (サンプル)。 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine タスク

- [**ソース**] > [**測定単位の CDS**] で必要なマッピングが存在することを確認します。

- [**ソース**] > [**CDマッピング**] に存在する Finance and Operations で、[**SalesUnitSymbol**] 用の必要な [**ValueMap**] を確認します。 
    
    - [**Quantity_UOMにSalesUnitSymbol**] に対して [**ValueMap**] を持つテンプレート値が定義されます。
    
-  [**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。 

    -  [**SalesInvoicer_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。
    -  [**Product_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。
 
## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターのテンプレートのマッピング

> [!NOTE]
> [**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] は、既定のマッピングの一部ではありません。 これらのフィールドのマッピングには、エンティティ間で同期される組織内のデータに固有の、設定される値マッピングが必要になります。

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-2.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>関連トピック

[Finance and Operations の製品を売上の製品に同期する](products-template-mapping.md)

[Finance and Operations の顧客への Sales の勘定の同期](accounts-template-mapping.md)

[Finance and Operations の連絡先または顧客への Sales の連絡先の同期](contacts-template-mapping.md)

[販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期](sales-quotation-template-mapping.md)

[販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-order-template-mapping.md)


