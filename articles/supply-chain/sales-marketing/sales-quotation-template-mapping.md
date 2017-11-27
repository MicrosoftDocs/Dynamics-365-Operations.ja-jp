---
title: "販売見積のヘッダーおよび明細行を Sales から Finance and Operations に同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、販売見積ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>販売見積のヘッダーおよび明細行を Sales から Finance and Operations に同期する

[!include[banner](../includes/banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。 

このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に対して、販売見積ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。 

## <a name="template-and-tasks"></a>テンプレートおよびタスク

Sales から Finance and Operations への販売見積ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。

- [**テンプレートの名前:**] 販売見積もり (Sales から Finance and Operations)
- **プロジェクトのタスク名:**

    - QuoteHeader
    - QuoteLine

販売見積ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- 製品 (Finance and Operations から Sales)
- 勘定 (Sales から Finance and Operations) (使用されている場合)
- 顧客への連絡先 (Sales から Finance and Operations) (使用されている場合)

## <a name="entity-set"></a>エンティティ セット

| 売上        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| 引用       | 見積書     | 販売見積ヘッダー   |
| QuoteDetails | QuotationLine | CDS 販売見積明細行 |

## <a name="entity-flow"></a>エンティティのフロー

販売見積が Sales で作成され Finance and Operations に同期されます。

Sales からの販売見積は、次の条件が満たされた場合にのみに同期されます。

- 販売見積明細行のすべての製品は、外部から管理されます。
- 販売見積は、有効または有効化されています。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

[**外部で管理される製品のみあり**] フィールドが見積エンティティに追加され、販売見積が外部管理製品から完全に構成されているかどうかが一貫して追跡されます。 販売見積に外部で管理された製品のみがある場合、製品は Finance and Operations で管理されます。 この動作は、Finance and Operations で不明な製品と販売見積明細行を同期させないことを保証するのに役立ちます。

見積書のすべての製品と明細行は、見積書ヘッダーからの [**外部で管理される製品のみあり**] 情報で更新されます。 この情報は、見積明細行エンティティの [**外部で管理される製品のみの見積**] フィールドに記載されています。

[**割引**]、[**請求**]、および [**税**] フィールドは、Finance and Operations の複雑な設定によって制御されます。 この設定では現在、統合マッピングはサポートされていません。 現在の設計では、[**価格**]、[**割引**]、[**請求金額**]、および [**税**] の各フィールドは、Finance and Operations によって習得され、処理されます。

Sales では、値が Finance and Operations に同期されていないため、このソリューションでは次のフィールドを読み取り専用にします。

- [**販売見積ヘッダーの読み取り専用フィールド:**] 割引率、割引、貨物量
- [**販売見積明細行の読み取り専用のフィールド:**] 税

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

販売注文を同期する前に、次の設定でシステムを更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

- Sales で [**設定**] &gt; [**管理**] &gt; [**システム設定**] &gt; [**販売**] に移動し、[**割引の計算方法**] フィールドが [**単位あたり**] に設定されていることを確認します。 この設定を使用すると、Sales からの明細行品目割引が Finance and Operations の設定と一致することが保証されます。 それ以外の場合、Finance and Operations では、売上高の 1 ラインあたりの割引であっても、割引を単価単位で読み取るため、割引は Finance and Operations では正しく行われません

### <a name="setup-in-finance-and-operations"></a>Finance and Operations での設定

- [**売掛金勘定**] &gt; [**設定**] &gt; [**売掛金勘定パラメーター**] の順に移動します。 [**番号順序**] タブで、販売見積の番号順序を選択し、[**詳細を表示**] をクリックします。 その後 [**全般設定**] で、[**手動**] フィールドを [**はい**] に設定します。
- [**売掛金勘定**] &gt; [**設定**] &gt; [**売掛金勘定パラメーター**] の順に移動します。 その後、[**出荷**] タブで、[**配送日管理**] フィールドを [**なし**] に設定します。 この設定は、販売見積の同期が失敗するのを防ぐのに役立ちます。

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="quoteheader"></a>QuoteHeader

- [**要求された納期日**] フィールドは Finance and Operations で必要です。このフィールドが空白の場合、同期は失敗します。 この問題を防ぐために、このフィールドが空白の場合、既定の日付が [**ソース &gt; CDS**] から取得されます。 日付は優先値に更新する必要があります。 現在、今日の日付を表す [**今日**] などの値を入力することはできません。 固有の期日を入力してください。 [**配送指定日**] の既定のテンプレート値は [**1/1/2020**] です。
- [**住所/国の地域コード**] フィールドが Finance and Operations では必要です。 同期エラーを防ぐために、Sales でフィールドが空白のままである場合に使用されるデフォルト値を指定できます。 この既定値は、ローカル アドレスの場合は [**国地域**] フィールドに値を手動で入力する必要がないため便利です。 [**DeliveryAddressCountryRegionISOCode**] には既定のテンプレート値はありません。
- [**ソース &gt; CDS**] の [**CDS 組織 ID**] のマッピングを更新して、組織エンティティの [**CDS 組織**] に一致させます。

    - [**Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。
    - [**Account_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。
    - [**InvoiceAccount_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。

#### <a name="quoteline"></a>QuoteLine

- [**ソース &gt; CDS**] の [**CDS 組織 ID**] のマッピングを更新して、組織エンティティの [**CDS 組織**] に一致させます。

    - [**Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。
    - [**Product_Organization_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。
    - [**Quotation_Organization_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。

- [**要求された納期日**] フィールドは Finance and Operations で必要です。このフィールドが空白の場合、同期は失敗します。 この問題を防ぐために、このフィールドが空白の場合、既定の日付が [**ソース &gt; CDS**] から取得されます。 日付は優先値に更新する必要があります。 現在、今日の日付を表す [**今日**] などの値を入力することはできません。 固有の期日を入力してください。 [**配送指定日**] の既定のテンプレート値は [**1/1/2020**] です。
- [**CDS &gt; 出力先**] から次のマッピングを追加して、顧客または製品からの既定の情報がない場合、見積書明細行を Finance and Operations にインポートすることができます。

    - **SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。 [**SiteId**] に対する既定のテンプレート値はありません。
    - **WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。 [**WarehouseId**] に対する既定のテンプレート値はありません。

- [**Quantity_UOM**] から [**SALESUNITSYMBOL**] の [**CDS &gt; Destination**] マッピングに、Finance and Operations における販売量測定単位 (UOM) の必要な値マップが存在することを確認してください。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

> [!NOTE]
> - [**割引**]、[**請求**]、および [**税**] フィールドは、Finance and Operations の複雑な設定によって制御されます。 この設定では現在、統合マッピングはサポートされていません。 現在の設計では、[**価格**]、[**割引**]、[**請求金額**]、および [**税**] の各フィールドは、Finance and Operations によって処理されます。
> - [**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

### <a name="quoteheader"></a>QuoteHeader

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>関連トピック

[Finance and Operations の製品を売上の製品に同期する](products-template-mapping.md)

[Finance and Operations の顧客への Sales の勘定の同期](accounts-template-mapping.md)

[売上の連絡先を Finance and Operations の連絡先または顧客に同期させる](contacts-template-mapping.md)



