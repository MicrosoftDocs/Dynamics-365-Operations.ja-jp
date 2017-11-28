---
title: "販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。 

## <a name="template-and-tasks"></a>テンプレートおよびタスク

Finance and Operations から Sales への販売注文ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。

- [**データ統合でのテンプレートの名前**] 

    - 販売注文 (Finance and Operations から Sales)
    
- [**データ統合プロジェクトのタスク名**]

    - OrderHeader
    - OrderLine

売上請求書ヘッダーおよび明細行の同期より前に必要な同期タスク。

- 製品 (Finance and Operations から Sales)
- 勘定 (Sales から Finance and Operations) (使用されている場合)
- 顧客への連絡先 (Sales から Finance and Operations) (使用されている場合)

## <a name="entity-set"></a>エンティティ セット

| Finance and Operations |    Common Data Service (CDS)         |     売上      |
|------------------------|----------------|----------------|
| CDS 販売注文ヘッダー| SalesOrder     | SalesOrders |
| CDS 販売注文明細行  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>エンティティのフロー

販売注文が Finance and Operations で作成され Sales に同期されます。

テンプレートのフィルターは、関連する販売注文のみが同期に含まれていることを確認します。

- Sales からの販売注文で、注文と請求の両方の顧客が同期に含まれます。 Finance and Operations で、フィールドの [**OrderingCustomerIsExternallyMaintained**] および [**InvoiceCustomerIsExternallyMaintained**] は、データ エンティティの同期を追跡するために使用されます。

- Finance and Operations で [**販売注文**] を確定する必要があります。 出荷済や請求済ステータスなどの、確定済販売注文または処理ステータスの大きい販売注文のみが、Sales に同期されます。

- 販売注文を作成または変更した後、Finance and Operations でバッチ ジョブの [**販売合計の計算**] を実行する必要があります。 売上合計が計算された販売注文のみが CDS と Sales に同期されます。

> [!NOTE]
> [**販売注文ヘッダー**] での税に関連する費用は、現在 Finance and Operations から Sales への同期に含まれていません。 これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。 明細行レベルでの税に関連する費用が含まれます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

新しいフィールドが [**注文**] エンティティに追加され、ページに表示されます。

- 注文が Finance and Operations から来る場合、[**外部で管理**] - を [**はい**] に設定します。

- [**処理状態**] - Finance and Operations で注文の処理状態を表示するために使用します。 値は、

    - 使用可能
    - 確認済
    - 梱包明細
    - 請求済
    - ピッキング済
    - 一部ピック済
    - 一部ピック済
    - 出荷済
    - 一部出荷済
    - 一部請求済
    - キャンセル済

[**外部で管理される製品のみの見積**] 設定は、販売注文が完全に [**外部で管理される製品**] で構成されているかを一貫して追跡するよう、別の販売注文のシナリオ (Sales から Finance and Operation 同期) で使用されます。その場合、製品は Finance and Operations で管理されます。 これにより、Finance and Operations で不明な製品と販売注文明細行を同期しなくなります。
 
[**販売注文**] ページで、[**請求書の作成**]、[**注文のキャンセル**]、[**再計算**]、[**製品の取得**] および [**ルックアップ アドレス**] ボタンは外部で管理される注文用に非表示となります。それは Finance and Operations で請求書が作成され Sales に同期されるためです。 販売注文情報は Finance and Operations から同期されるため、注文ページは編集できません。
 
Finance and Operations からの変更が Sales での [**販売注文**] にフローするよう、[**販売注文状態**] は有効になります。 これは、データ統合プロジェクトで、既定の [**Statecode [状態]**] を [**有効**] に設定することにより制御されます。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定 

販売注文を同期する前に、次の設定でシステムを更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

- 割り当てられるユーザー (Sales [**接続設定**] から) のチームに対するアクセス許可を確保します。 デモ データを使用している場合は、通常ユーザーに管理者アクセスがあり、チームにはありません。 これがないと、データ インテグレーターからプロジェクトを実行するときに主要なチームがないという、エラー メッセージが表示されます。 

    - [**設定**] > [**セキュリティ**] > [**チーム**] で、関連チームを選択し、[**ロール管理**] をクリックして [システム管理者] などの必要なアクセス許可を持つロールを選択します。

- [**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**システム プライジング計算システムの使用**] が [**はい**] に設定されていることを確認します。 

- [**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**割引の計算方法**] が [**明細行品目**] に設定されていることを確認します。 

### <a name="setup-in-finance-and-operations"></a>Finance and Operations での設定

[**販売およびマーケティング**] > [**定期処理のタスク**] > [**販売合計の計算**] を設定してバッチ ジョブとして実行し、[**販売注文合計の計算**] を [**はい**] に設定します。 売上合計が計算された販売注文のみが CDS と Sales に同期されるため、これは重要です。 バッチ ジョブの頻度は、販売注文の同期の頻度に対応している必要があります。

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="salesheader-task"></a>SalesHeader タスク

- [**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。

    - [**Account_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。
    - [**InvoiceAccount_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。
    - [**Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。

- [**ソース**] > [**BillingAddress_Country への InvoiceCountryRegionId 用 CDS**] および [**DeliveryAddress_Country への DeliveryCountryRegionId**] 用に必要なマッピングが存在することを確認します。。

    - マップされている国の数のテンプレート値は [**ValueMap**] です。

- Sales で注文を作成するために [**価格リスト**] が必要です。 [**pricelevelid.name [価格リスト名]**] の [**CDS**] > [**出力先**] で、Sales で通貨ごとに使用される [**価格リスト**] への [**ValueMap**] を更新します。 1 つの通貨に対する既定の [**価格リスト**] を使用するか、または複数の通貨で [**価格リスト**] がある場合 [**ValueMap**] を使用するかのいずれかができます。
    
    - [**pricelevelid.name [価格リスト名]**] の既定のテンプレートの値は CRM サービス USA (サンプル) です。 

#### <a name="salesline-task"></a>SalesLine タスク

- [**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。 
    
    - [**SalesOrder_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。
    - [**Product_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。

- [**DeliveryCountryRegionId**] の [**ソース**] > [**CDS**] で、[**DeliveryAddress_Country**] に必要なマッピングが存在することを確認します。

    - マップされている国の数のテンプレート値は [**ValueMap**] です。
    
- [**ソース**] > [**CDマッピング**] に存在する Finance and Operations で、[**SalesUnitSymbol**] 用の必要な [**ValueMap**] を確認します。

    - [**Quantity_UOMにSalesUnitSymbol**] に対して [**ValueMap**] を持つテンプレート値が定義されます。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

> [!NOTE]
> [**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

### <a name="orderheader"></a>OrderHeader

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>関連トピック

[Finance and Operations の製品を売上の製品に同期する](products-template-mapping.md)

[Finance and Operations の顧客への Sales の勘定の同期](accounts-template-mapping.md)

[Finance and Operations の連絡先または顧客への Sales の連絡先の同期](contacts-template-mapping.md)

[販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期](sales-quotation-template-mapping.md)

[売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期](sales-invoice-template-mapping.md)


