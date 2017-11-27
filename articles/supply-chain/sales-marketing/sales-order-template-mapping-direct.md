---
title: "販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。 次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。 **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Finance and Operations から Sales への販売注文ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合における テンプレートの名前** 販売注文 (Sales から Finance and Operations )- 直接
- **データ統合プロジェクトのタスク名:**

    - OrderHeader
    - OrderLine

販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- 製品 (Finance and Operations から Sales) - 直接
- 勘定 (Sales から Finance and Operations) - 直接(使用されている場合)
- 顧客への連絡先 (Sales から Finance and Operations) - ダイレクト (使用されている場合)

## <a name="entity-set"></a>エンティティ セット

| Finance and Operations  | 売上             |
|-------------------------|-------------------|
| CDS 販売注文ヘッダー | SalesOrders       |
| CDS 販売注文明細行   | SalesOrderDetails |

## <a name="entity-flow"></a>エンティティのフロー

販売注文が Finance and Operations で作成され Sales に同期されます。

テンプレートのフィルタは、関連する受注のみが同期に含まれることを保証します。

- 受注では、Sales から生成される発注元の顧客と販売担当者の両方が同期に含まれます。 Finance and Operations で、[**OrderingCustomerIsExternallyMaintained**] および [**InvoiceCustomerIsExternallyMaintained**] フィールドは、データ エンティティの同期を追跡するために使用されます。
- Finance and Operations で [販売注文] を確定する必要があります。 [**出荷済**] や [**請求済**] など、確認済の販売注文または処理ステータスの高い販売注文のみが Sales に同期されます。
- 販売注文を作成または変更した後、Finance and Operations で [**販売合計の計算**] のバッチ ジョブを実行する必要があります。 販売合計が計算された販売注文のみが Sales に同期されます。

> [!NOTE]
> 現在、販売注文ヘッダの料金に関連する税金は、Finance and Operations から Sales までの同期には含まれていません。 これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。 ただし、同期の明細行レベルでの税に関連する費用が含まれます。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

新しいフィールドが [**注文**] エンティティに追加され、ページに表示されます。

- [**外部で管理**] - 注文が Finance and Operations から来る場合、このオプションを [**はい**] に設定します。
- [**処理状態**] - このフィールドには、Finance and Operations の注文の処理状態が表示されます。 使用可能な値は次のとおりです。

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

[外部で管理される製品のみ] 設定は、別の販売注文のシナリオ (例えば、Sales から Finance and Operation への同期) で使用され、販売注文が完全に外部管理製品から構成されているかどうか一貫して追跡されます。 受注が外部から管理された製品で完全に構成されている場合、製品は Finance and Operations で管理されます。 この設定は、Finance and Operations に不明な製品を含む受注明細行を同期させないことを保証するのに役立ちます。

[**販売注文**] ページで、[**請求書の作成**]、[**注文のキャンセル**]、[**再計算**]、[**製品の取得**] および [**ルックアップ アドレス**] ボタンは外部で管理される注文用に非表示となります。それは Finance and Operations で請求書が作成され Sales に同期されるためです。 注文ページは編集できません。販売注文情報は Finance and Operations から同期されるためです。

受注状況は、Finance and Operations からの変更が Sales の受注に流れることを保証するために、**有効**のままになります。 この動作を制御するためには、データ統合プロジェクトで、既定の [**Statecode\[状態\]**] を [**有効**] に設定します。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

販売注文を同期する前に、システムで以下の設定を更新することが重要です。

### <a name="setup-in-sales"></a>Sales での設定

- Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可として設定されていることを確認します。 デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。 チームがデータ統合からプロジェクトを実行するとき、管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。

    **設定** > **セキュリティ** > **チーム**で、関連チームを選択し、**ロール管理**をクリックして**システム管理者**などの必要なアクセス許可を持つロールを選択します。

- **設定** > **管理** > **システムの設定** > **Sales**の順にクリックし、次の設定を使用することを確認します。

    - [**システム プライジング計算システムの使用**] オプションが、[**はい**] に設定されている。
    - [**割引の計算方法**] フィールドが、[**明細行品目**] に設定されている。

### <a name="setup-in-finance-and-operations"></a>Finance and Operations での設定

**販売およびマーケティング** > **定期処理タスク** > **販売合計を計算する**の順にクリックし、バッチ ジョブとして実行されるようにタスクを設定します。 **販売注文合計を計算する**オプションを**はい**に設定します。 販売合計が計算された販売注文のみが Sales に同期されるため、このステップは重要です。 バッチジョブの頻度は、販売注文同期の頻度と一致させる必要があります。

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="salesheader-task"></a>SalesHeader タスク

- 必要なマッピングが **InvoiceCountryRegionId** から **BillingAddress\_Country** に、また **DeliveryCountryRegionId** から **DeliveryAddress\_Country** に存在することを確認します。

    テンプレートの値は、複数の国または地域がマップされている値マップです。

- 価格リストは、Sales で注文を作成するために必要です。 Sales で通貨ごとに使用される価格リストへの [**pricelevelid.name \[価格リスト名\]**] の値マップを更新します。 1つの通貨に対する既定の価格リストを使用することができます。 または、複数の通貨で価格リストがある場合、値マップを使用することもできます。

    **pricelevelid.name \[価格リスト名\]** の既定テンプレート値は **CRM サービス USA (サンプル)** です。

#### <a name="salesline-task"></a>SalesLine タスク

- **DeliveryCountryRegionId** から **DeliveryAddress\_Country** に必要なマッピングが存在することを確認します。

    テンプレートの値は、複数の国または地域がマップされている値マップです。

- Finance and Operation で [**SalesUnitSymbol**] 用の必要な値マップを確認します。

    [**SalesUnitSymbol**] から [**Quantity\_** UMO] に対して値マップを持つテンプレート値が定義されます。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE]
> [**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングには含まれていません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ統合のテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。

### <a name="orderheader"></a>OrderHeader

![データ インテグレーターのテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![データ インテグレーターのテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>関連トピック

[見込顧客を現金化](prospect-to-cash.md)

[Sales から Finance and Operations の顧客への勘定の直接同期](accounts-template-mapping-direct.md)

[Sales 製品への Finance and Operations 製品の直接同期](products-template-mapping-direct.md)

[Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期](contacts-template-mapping-direct.md)

[売上請求書ヘッダーおよび直接明細行の Finance and Operations から Sales への直接同期](sales-invoice-template-mapping-direct.md)




