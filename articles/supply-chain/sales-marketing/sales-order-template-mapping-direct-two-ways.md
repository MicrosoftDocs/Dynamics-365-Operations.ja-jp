---
title: 販売注文の Sales と Supply Chain Management の間の直接同期
description: この販売注文では、Dynamics 365 Sales と Dynamics 365 Supply Chain Management の間での販売注文の直接同期の実行に使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 63a9be9bedabe1f15ad8db583151aa7fa480473b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854155"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>販売注文の Sales と Supply Chain Management の間の直接同期

[!include [banner](../includes/banner.md)]



この販売注文では、Dynamics 365 Sales と Dynamics 365 Supply Chain Management の間での販売注文の直接同期の実行に使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー。](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://preview.admin.powerapps.com/dataintegration)を開きます。 **プロジェクト** を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Sales と Supply Chain Management との間での販売注文の直接同期の実行には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合でのテンプレートの名前:** 

    - 販売注文 (Sales から Supply Chain Management) - 直接
    - 販売注文 (Supply Chain Management から Sales) - 直接

- **データ統合プロジェクトのタスク名:**

    - OrderHeader
    - OrderLine

販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- 製品 (Supply Chain Management から Sales) - 直接
- 勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)
- 顧客への連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)

## <a name="entity-set"></a>エンティティ セット

| サプライ チェーン マネジメント  | 販売注文             |
|-------------------------|-------------------|
| Dataverse 販売注文ヘッダー | SalesOrders       |
| Dataverse 販売注文明細行   | SalesOrderDetails |

## <a name="entity-flow"></a>エンティティのフロー

**販売注文 (Sales から Supply Chain Management) - 直接** テンプレートに基づいたプロジェクトに対して **プロジェクトの実行** が発生する場合、Sales で作成された販売注文が Supply Chain Management に同期されます。 全ての **受注製品** が外部で管理される製品で構成されている場合にのみ、Sales からの販売注文を同期できます。 したがって、リスト外製品は存在しません。 注文を有効にすると、販売注文はユーザー インターフェイス (UI) で読み取り専用になります。 この時点で、更新は Supply Chain Management から行われます。 販売注文が **確認済** 状態となった後に、**販売注文 (Supply Chain Management から Sales) － 直接** テンプレートに基づいたプロジェクトは Supply Chain Management から Sales に更新またはフルフィルメントの状態を同期するために使用できます。

Sales で注文を作成する必要はありません。 代わりに、Supply Chain Management で新しい販売注文を作成することができます。 販売注文が **確認済** のステータスになった後、前の段落で説明するように Sales に同期されます。

Supply Chain Management では、テンプレートのフィルタは関連する販売注文のみが同期に含まれていることを保証します。

- 販売注文では、受注顧客と請求顧客の両方が Sales から生成されて同期に含める必要があります。 Supply Chain Management で、**OrderingCustomerIsExternallyMaintained** および **InvoiceCustomerIsExternallyMaintained** 列は、データ テーブルからの販売注文をフィルタするために使用されます。
- Supply Chain Management で販売注文を確定する必要があります。 **出荷済** や **請求済** など、確認済の販売注文または処理ステータスの高い販売注文のみが Sales に同期されます。
- 販売注文を作成または変更した後、Supply Chain Management で **販売合計の計算** のバッチ ジョブを実行する必要があります。 販売合計が計算された販売注文のみが Sales に同期されます。

## <a name="freight-tax"></a>運賃税

Sales は、明細行レベルで税が格納されるため、ヘッダー レベルでの税をサポートしていません。 運賃税など Supply Chain Management からヘッダー レベルでの税をサポートするためには、システムは **運賃税** と呼ぶリスト外製品として税を Sales に同期して、Supply Chain Management からの税額を含めます。 これにより、Sales での標準価の計算は、Supply Chain Management からヘッダー レベルで税がある場合でも合計金額として使用できます。

## <a name="discount-calculation-and-rounding"></a>割引計算と丸め

Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。 Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。 この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。 ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。 Supply Chain Management の販売ラインからの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。 したがって、Sales で **割引の計算方法** を **明細行品目** として定義する必要があります。

販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。 Supply Chain Management には、明細行の完全な割引金額を格納できるフィールドがないため、金額は数量で除算されて、**行割引** フィールドに格納されます。 この区分中に発生する丸め処理は販売注文明細行の **売上諸掛** フィールドに格納されます。

### <a name="example"></a>例

**Sales から Supply Chain Management への同期**

- **Sales:** 数量 = 3、行あたりの割引 = 10.00 USD
- **サプライ チェーン マネジメント:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01 

**Supply Chain Management から Sales への同期**

- **サプライ チェーン マネジメント:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01
- **Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

新しい列が **注文** テーブルに追加され、ページに表示されます。

- **外部で管理** - 注文が Supply Chain Management から来る場合、このオプションを **はい** に設定します。
- **処理状態** - この列には、Supply Chain Management のオーダーの処理状態が表示されます。 使用可能な値は次のとおりです。

    - **ドラフト** – Sales で受注が作成される場合の初期ステータス。 Sales では、この処理ステータスの注文のみ編集することができます。
    - **有効** – **有効** ボタンを使用すると、受注後のステータスが Sales で有効になります。
    - **確認済**
    - **梱包明細**
    - **請求済**
    - **ピッキング済**
    - **一部ピック済**
    - **一部ピック済**
    - **出荷済**
    - **一部出荷済**
    - **一部請求済**
    - **キャンセル済**

**外部で管理される製品のみ** 設定が注文時に使用され、販売注文が外部から管理された製品で完全に構成されているかどうかが一貫して追跡されます。 受注が外部から管理された製品で完全に構成されている場合、製品は Supply Chain Management で管理されます。 この設定は、Supply Chain Management に不明な製品を含む販売注文明細行を有効化したり、同期化しようとするのを防ぐのに役立ちます。

**販売注文** ページで、**請求書の作成**、**注文のキャンセル**、**再計算**、**製品の取得** および **ルックアップ アドレス** ボタンは外部で管理される注文用に非表示となります。それは Supply Chain Management で請求書が作成され Sales に同期されるためです。 これらの注文は、販売注文情報が有効化後に Supply Chain Management から同期されるため編集することができません。

販売発注状況は **有効** のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れることを保証します。 この動作を制御するためには、データ統合プロジェクトで、既定の **Statecode \[状態\]** を **有効** に設定します。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

販売注文を同期する前に、システムで以下の設定を更新することが重要です。

### <a name="setup-in-sales"></a>Sales での設定

- Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可として設定されていることを確認します。 デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。 データ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。

    **設定** &gt; **セキュリティ** &gt; **チーム** の順に移動し、関連チームを選択してから、**ロール管理** をクリックして **システム管理者** などの必要なアクセス許可を持つロールを選択します。

- Sales および Supply Chain Management の両方で割引の計算が正しいことを確認するには、**割引の計算方法** が **行項目** に設定される必要があります。
- **設定** &gt; **管理** &gt; **システム設定** &gt; **Sales** へと順に進み、次の設定が使用されていることを確認してください。

    - **システム プライジング計算システムの使用** オプションが、**はい** に設定されている。
    - **割引の計算方法** 列が、**明細行品目** に設定されている。

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management での設定

- **販売とマーケティング**&gt;**定期処理のタスク**&gt;**販売合計を計算する** の順に移動してから、バッチ ジョブとして実行されるようにジョブを設定します。 **販売注文合計を計算する** オプションを **はい** に設定します。 販売合計が計算された販売注文のみが Sales に同期されるため、このステップは重要です。 バッチジョブの頻度は、販売注文同期の頻度と一致させる必要があります。

ワークオーダー統合も使用する場合は、販売元を設定する必要があります。 販売元は、Field Service のワーク オーダーから作成された Supply Chain Management の販売注文を区別するために使用されます。 販売注文に **ワーク オーダー統合** タイプの販売元がある場合、**外部ワーク オーダー ステータス** フィールドが販売注文ヘッダーに表示されます。 また販売元は、Field Service のワーク オーダーから作成された販売注文が、Supply Chain Management から Field Service への販売注文同期の間に除外されることを確認します。

1. **販売とマーケティング** \> **設定** \> **販売注文** \> **販売元** に移動します。
2. **新規** を選択し、新しい販売元を作成します。
3. **販売元** 列に、**SalesOrder** のような販売元の名前を入力します。
4. **説明** 列に、**Sales からの販売注文** のような説明を入力します。
5. **発生元タイプの割り当て** チェック ボックスを選択します。
6. **販売元タイプ** 列を **販売注文統合** に設定します。
7. **保存** を選択します。

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>販売注文のセット アップ (Sales から Supply Chain Management) - ダイレクト データ統合プロジェクト

- 必要なマッピングが **Shipto\_country** から **DeliveryAddressCountryRegionISOCode** に存在することを確認します。 値マップで既定値を空白にして、国内の注文の国を入力を回避することができます。 左側を「空白」のままにして、右側を希望する国または地域に設定します。

    テンプレート値は、いくつかの国または地域がマップされている値マップで、「空白」= アメリカ合衆国です。

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>販売注文のセット アップ (Supply Chain Management から Sales) - ダイレクト データ統合プロジェクト

#### <a name="salesheader-task"></a>SalesHeader タスク

- 価格リストは、Sales で注文を作成するために必要です。 Sales で通貨ごとに使用される価格リストへの **pricelevelid.name \[価格リスト名\]** の値マップを更新します。 1つの通貨に対する既定の価格リストを使用することができます。 または、複数の通貨で価格リストがある場合、値マップを使用することもできます。

    **pricelevelid.name\[価格リスト名\]** の既定のテンプレートの値は、**CRM サービス USA (サンプル)** です。

#### <a name="salesline-task"></a>SalesLine タスク

- Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。
- Sales に必要な単位が定義されていることを確認します。

    値マップを持つテンプレート値は、**SalesUnitSymbol** から **oumid.name** に対して定義されています。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE]
> **支払条件**、**運賃条件**、**配送条件**、**送付方法**、**配送モード** 列は、既定のマッピングの一部ではありません。 これらの列をマップするには、テーブル間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ統合のテンプレート マッピングの例を示しています。

> [!NOTE]
> マッピングでは、Supply Chain Management に、または Supply Chain Management から Sales に同期する列情報を表示します。

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>販売注文 (Supply Chain Management から Sales) - 直接: OrderHeader

[![データ統合のテンプレート マッピング、販売注文 (Supply Chain Management から Sales) - 直接: OrderHeader。](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>販売注文 (Supply Chain Management から Sales) - 直接: OrderLine

[![データ統合のテンプレート マッピング、販売注文 (Supply Chain Management から Sales) - 直接: OrderLine。](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>販売注文 (Sales から Supply Chain Management) - 直接: OrderHeader

[![データ統合のテンプレート マッピング、販売注文 (Sales から Supply Chain Management) - 直接: OrderHeader。](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>販売注文 (Sales から Supply Chain Management) - 直接: OrderLine

[![データ統合のテンプレート マッピング、販売注文 (Sales から Supply Chain Management) - 直接: OrderLine。](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-articles"></a>関連記事

[見込顧客の現金化](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]