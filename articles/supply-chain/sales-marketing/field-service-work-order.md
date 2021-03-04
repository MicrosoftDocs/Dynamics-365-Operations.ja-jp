---
title: Field Service のワーク オーダーと Supply Chain Management の販売注文との同期
description: このトピックでは、Field Service の作業オーダーを Supply Chain Management の販売注文に同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d8051e21c731213e2d74ab6eeb80c239ca9932e6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528926"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Field Service のワーク オーダーと Supply Chain Management の販売注文との同期

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Field Service のワーク オーダーを Dynamics 365 Supply Chain Management の販売注文に同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>テンプレートおよびタスク

次のテンプレートと基本的なタスクは、Field Service の作業オーダーと Supply Chain Management の販売注文との同期を実行するために使用されます。

### <a name="names-of-the-templates-in-data-integration"></a>データ統合でのテンプレートの名前

**作業オーダーから販売注文 (Field Service から Supply Chain Management)** テンプレートは同期を実行するために使用します。

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>データ統合プロジェクトのタスク名

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

販売注文ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- Field Service 製品 (Supply Chain Management から Field Service)
- アカウント (Sales から Supply Chain Management) - 直接

## <a name="entity-set"></a>エンティティ セット

| **Field Service** | **サプライ チェーン マネジメント** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS 販売注文ヘッダー |
| msdyn_workorderservices | CDS 販売注文明細行   |
| msdyn_workorderproducts | CDS 販売注文明細行   |

## <a name="entity-flow"></a>エンティティのフロー

Field Service で作業オーダーが作成されます。 作業オーダーが外部で管理された製品のみを含んでおり、**ワーク オーダー ステータス** の値が **未終了－未スケジューリング** および **終了－キャンセル済** と異なる場合、作業オーダーは Common Data Service データ統合プロジェクトを通して Supply Chain Management に同期させることができます。 作業オーダーの更新は、Supply Chain Management での販売注文として同期されます。 これらの更新には、発生元のタイプやステータスに関する情報が含まれます。

## <a name="estimated-versus-used"></a>見積済と使用済

Field Service では、作業オーダーの製品およびサービスに、数量および金額に対する **見積済** 値および **使用済** 値の両方があります。 ただし、Supply Chain Management では、販売注文に **見積済** および **使用済** と同じ概念の値はありません。 Supply Chain Management の販売注文で予期される数量を使用する製品配賦をサポートし、消費および請求される使用量を維持するために、2 つのタスク セットが作業オーダー上の製品およびサービスと同期します。 1 つのタスクのセットは、**見積済** 値用であり、他のタスクのセットは **使用済** 値用です。

この動作により、Supply Chain Management の配賦または引当に使用される見積値のシナリオが有効になりますが、使用される値は消費および請求に使用されます。

### <a name="estimated"></a>見積済

製品明細行を同期するために、次の時に **見積済** 値は使用されます。**行ステータス** 値が **見積済**、**割り当て済** オプションが **はい**、および **システムの状態** の値が **終了－転記済** でない時。

サービス明細行を同期するために、次の時に **見積済** 値が使用されます。**行ステータス** 値が **見積済**、および **システムの状態** の値が **終了－転記済** でない時。

### <a name="used"></a>使用済

**使用済** 値が消費および請求に使用されます。 そのような場合、**使用済** 値が同期されます。

次の表に、製品明細行のさまざまな組み合わせの概要を示します。

| システムの状態 <br>(Field Service) | 行ステータス <br>(Field Service) | 割り当て済 <br>(Field Service) |同期値 <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| 未終了－スケジューリング済   | 見積済   | はい       | 見積済                       |
| 未終了－スケジューリング済   | 見積済   | 無        | 使用済                            |
| 未終了－スケジューリング済   | 使用済        | 有       | 使用済                            |
| 未終了－スケジューリング済   | 使用済        | 無        | 使用済                            |
| 未終了－処理中 | 見積済   | 有       | 見積済                       |
| 未終了－処理中 | 見積済   | 無        | 使用済                            |
| 未終了－処理中 | 使用済        | 有       | 使用済                            |
| 未終了－処理中 | 使用済        | 無        | 使用済                            |
| 未終了－完了   | 見積済   | 有       | 見積済                       |
| 未終了－完了   | 見積済   | 無        | 使用済                            |
| 未終了－完了   | 使用済        | 有       | 使用済                            |
| 未終了－完了   | 使用済        | 無        | 使用済                            |
| 終了－転記済    | 見積済   | 有       | 使用済                            |
| 終了－転記済    | 見積済   | 無        | 使用済                            |
| 終了－転記済    | 使用済        | 有       | 使用済                            |
| 終了－転記済    | 使用済        | 無        | 使用済                            |

次の表に、サービス明細行のさまざまな組み合わせの概要を示します。

| システムの状態 <br>(Field Service) | 行ステータス <br>(Field Service) | 同期値 <br>(Supply Chain Management) |
|--------------------|-------------|-----------|
| 未終了－スケジューリング済   | 見積済   | 見積済 |
| 未終了－スケジューリング済   | 使用済        | 使用済      |
| 未終了－処理中 | 見積済   | 見積済 |
| 未終了－処理中 | 使用済        | 使用済      |
| 未終了－完了   | 見積済   | 見積済 |
| 未終了－完了   | 使用済        | 使用済      |
| 終了－転記済    | 見積済   | 使用済      |
| 終了－転記済    | 使用済        | 使用済      |

**使用済** 値に対する **見積済** 値の同期は、製品明細行とサービス明細行の 2 つのタスク セットによって管理されます。 定義済のフィルターによって正しいタスクがトリガーされ、基礎となるマッピングによって、**予定** と **使用済** の正しい値の同期が保証されます。

### <a name="example"></a>例

1. 作業オーダーが作成され、Field Service でスケジュールされます。

    **システムの状態** 値は **未終了－スケジューリング済** です。

    - **製品の明細行:** 見積済数量 = 5ea、使用済数量 = 0ea、行ステータス = 見積済、割り当て済 = いいえ
    - **サービス明細行:** 見積済数量 = 2h、使用済数量 = 0 h、行ステータス = 見積済

    この例では、製品の **使用済数量** 値 **0** (ゼロ)、およびサービスの **見積済数量** 値 **2h** を Supply Chain Management に同期します。

2. 製品は Field Service に割り当てられます。

    **システムの状態** 値は **未終了－スケジューリング済** です。

    - **製品明細行:** 見積済数量 = 5ea、使用済数量 = 0ea、行ステータス = 見積済、割り当て済 = はい
    - **サービス明細行:** 見積済数量 = 2h、使用済数量 = 0 h、行ステータス = 見積済

    この例では、製品の **見積済数量** 値 **5ea**、およびサービスの **見積済数量** 値 **2h** を Supply Chain Management に同期します。

3. サービス技術者は、ワーク オーダーの作業を開始し、原材料消費 6 を登録します。

    **システムの状態** 値は **未終了－処理中** です。

    - **製品明細行:** 見積済数量 = 5ea、使用済数量 = 6ea、行ステータス = 使用済、割り当て済 = はい
    - **サービス明細行:** 見積済数量 = 2h、使用済数量 = 0 h、行ステータス = 見積済

    この例では、製品の **使用済数量** 値 **6**、およびサービスの **見積済数量** 値 **2h** を Supply Chain Management に同期します。

4. サービス技術者が、ワーク オーダーを完了し、使用した時間 1.5 時間を登録します。

    **システムの状態** 値は **未終了－完了** です。

    - **製品明細行:** 見積済数量 = 5ea、使用済数量 = 6ea、行ステータス = 使用済、割り当て済 = はい
    - **サービス明細行:** 見積済数量 = 2h、使用済数量 = 1.5h、行ステータス = 使用済

    この例では、製品の **使用済数量** 値 **6**、およびサービスの **見積済数量** 値 **1.5h** を Supply Chain Management に同期します。

## <a name="sales-order-origin-and-status"></a>販売注文元および販売注文状態

### <a name="sales-origin"></a>販売元

ワーク オーダーから発生した販売注文を追跡するために、**発生元タイプの割り当て** オプションを **はい** に設定され、**販売元タイプ** フィールドが **ワーク オーダー統合** に設定された販売元を作成できます。

既定では、マッピングはワーク オーダーから作成されるすべての販売注文の、**ワーク オーダー統合** 販売元のタイプに対する販売元を選択します。 この動作は、Supply Chain Management で販売注文を処理する際に役に立ちます。 ワーク オーダーから発生した販売注文がワーク オーダーとして Field Service に同期されていないことを確認する必要があります。

Supply Chain Management で正しい販売元設定を作成する方法の詳細については、このトピックの「前提条件とマッピングの設定」を参照してください。

### <a name="status"></a>ステータス

販売注文がワーク オーダーから発生した場合、**外部ワーク オーダー ステータス** フィールドが、販売注文ヘッダー上の **設定** タブに表示されます。 このフィールドには Field Service でのワーク オーダーからのシステムのステータスが表示され、Supply Chain Management の販売注文の同期されたワーク オーダー ステータスが追跡されます。 このフィールドは、販売注文が出荷または請求される必要がある時にユーザーが決定する助けにもなります。

**外部ワーク オーダー ステータス** フィールドは、次の値を持つことができます。

- 未終了－スケジューリング済
- 未終了－処理中
- 未終了－完了
- 終了－転記済

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション

Field Service および Supply Chain Management の統合をサポートするために、Field Service CRM からの追加機能が必要です。 ソリューションには、次の変更が含まれます。

### <a name="work-order-entity"></a>ワーク オーダー エンティティ

**ワーク オーダー** エンティティに **外部で管理される製品のみの見積** フィールドが追加され、ページに表示されます。 外部から管理された製品で完全に構成されているかどうかを一貫して追跡するために使用されます。 すべての関連する製品が Supply Chain Management で管理されている場合、ワーク オーダーは外部から管理された製品で完全に構成されます。 このフィールドは、ユーザーが不明な製品を含むワーク オーダーを同期させないことを保証するのに役立ちます。

### <a name="work-order-product-entity"></a>ワーク オーダー製品エンティティ

- **ワーク オーダー製品** エンティティに **外部で管理される製品のみの注文** フィールドが追加され、ページに表示されます。 ワーク オーダー製品が Supply Chain Management で管理されているかどうかを一貫して追跡するために使用されます。 このフィールドは、ユーザーが Supply Chain Management に不明なワーク オーダー製品を同期させないことを保証するのに役立ちます。
- **ワーク オーダー製品** エンティティに **ヘッダー システムの状態** フィールドが追加され、ページに表示されます。 ワーク オーダーのシステムの状態を一貫して追跡するために使用され、ワーク オーダー製品が Supply Chain Management に同期されている時の正しいフィルター処理を保証するのに役立ちます。 統合作業にフィルターが設定されている場合、**ヘッダー システムの状態** 情報は、見積、または使用される値を同期するかどうかを決定するためにも使用します。
- **請求の単位量** フィールドは、使用される実際の単位あたりの請求された金額を表示します。 値は、**実数量** 値で割った **合計金額** 値として計算されます。 このフィールドは、使用量と請求量の値が異なることをサポートしていないシステムへの統合に使用されます。 このフィールドは、ユーザー インターフェイス (UI) には表示されません。 
- **請求済割引金額** フィールドは、**割引金額** 値に **請求の単位量** 値の計算からの丸めを足したものとして計算されます。 このフィールドは統合のために使用され、UI には表示されません。
- **小数数量** フィールドは、**数量** フィールドからの値を小数として格納します。 このフィールドは統合のために使用され、UI には表示されません。 
- ワーク オーダー製品の **行ステータス** 値が **使用済** から **見積済** に変更されると、**使用済** フィールドの値が **0** (ゼロ) にリセットされます。 この変更は、**行ステータス** 値が **見積済**、また **割り当て済** オプションが **いいえ** に設定された時に、間違って入力された使用量が同期に使用される状況を防ぐのに役立ちます

### <a name="work-order-service-entity"></a>ワーク オーダー サービス エンティティ

- **ワーク オーダー サービス** エンティティに **外部で管理される製品のみの注文** フィールドが追加され、ページに表示されます。 ワーク オーダーのサービスが Supply Chain Management で管理されているかどうかを一貫して追跡するために使用されます。 このフィールドは、ユーザーが Supply Chain Management に不明なワーク オーダーのサービスを同期させないことを保証するのに役立ちます。
- **ワーク オーダー サービス** エンティティに **ヘッダー システムの状態** フィールドが追加され、ページに表示されます。 ワーク オーダーのシステムの状態を一貫して追跡するために使用され、ワーク オーダーのサービスが Supply Chain Management に同期されている時の正しいフィルター処理を保証するのに役立ちます。 統合作業にフィルターが設定されている場合、**ヘッダー システムの状態** 情報は、見積、または使用される値を同期するかどうかを決定するためにも使用します。
- **期間 (時)** フィールドは、値を分から時間に変換した後、 **期間** フィールドからの値を格納します。 このフィールドは統合のために使用され、UI には表示されません。
- **見積期間 (時)** フィールドは、値を分から時間に変換した後、 **見積期間** フィールドからの値を格納します。 このフィールドは統合のために使用され、UI には表示されません。
- **請求の単位量** フィールドは、使用される実際の単位あたりの請求された金額を格納します。 値は、**実数量** 値で割った **合計金額** 値として計算されます。 このフィールドは、使用量と請求量の値が異なることをサポートしていないシステムへの統合に使用されます。 フィールドは、UI には表示されません。
- **請求済割引金額** フィールドは、**割引金額** 値に **請求の単位量** 値の計算からの丸めを足したものとして計算されます。 このフィールドは統合のために使用され、UI には表示されません。
- **外部明細行の注文** フィールドは、ワーク オーダ製品とサービス明細行が結合されている外部システムで使用できる、計算された負の明細行注文番号です。 このフィールドは、正の行番号とワーク オーダー サービスを持つために挿入されたワーク オーダー製品が、負の行番号を持つことができるようにします。 このフィールドの値は、**明細行の注文** 値に -1 を掛けたものとして計算されます。 このフィールドは、UI には表示されません。
- ワーク オーダー サービスの **行ステータス** 値が、何らかの理由で **使用済** から **見積済** に変更されると、**使用済** フィールドの値が **0** (ゼロ) にリセットされます。 この変更は、**行ステータス** 値が **見積済**、また **ヘッダー システムの状態** 値が **終了－転記済** に設定された時に、間違って入力された使用量が同期に使用される状況を防ぐのに役立ちます

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

ワーク オーダーを同期する前に、システムで以下の設定を更新することが重要です。

### <a name="setup-in-field-service"></a>Field Service での設定

- Field Service のワーク オーダーに使用されている番号シリーズが、Supply Chain Management の販売注文に使用されている番号順序と重ならないようにしてください。 それ以外の場合は、Field Service または Supply Chain Management の既存の販売注文は 正しく更新されません。
- Supply Chain Management から請求が行われるので、**ワーク オーダーの請求書の作成** フィールドを **なし** に設定する必要があります。 **Field Service** \> **設定** \> **管理** \> **Field Service の設定** に移動し、**ワーク オーダーの請求書の作成** フィールドを **なし** に設定します。

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management での設定

ワーク オーダー統合では、販売元を設定する必要があります。 販売元は、Field Service のワーク オーダーから作成された Supply Chain Management の販売注文を区別するために使用されます。 販売注文に **ワーク オーダー統合** タイプの販売元がある場合、**外部ワーク オーダー ステータス** フィールドが販売注文ヘッダーに表示されます。 また販売元は、Field Service のワーク オーダーから作成された販売注文が、Supply Chain Management から Field Service への販売注文同期の間に除外されることを保証します。

1. **販売とマーケティング** \> **設定** \> **販売注文** \> **販売元** に移動します。
2. **新規** を選択し、新しい販売元を作成します。
3. **販売元** フィールドに、**WorkOrder** のような販売元の名前を入力します。
4. **説明** フィールドに、**Field Service ワーク オーダー** のような説明を入力します。
5. **発生元タイプの割り当て** チェック ボックスを選択します。
6. **販売元タイプ** フィールドを **ワーク オーダー統合** に設定します。
7. **保存** を選択します。


### <a name="setup-in-data-integration"></a>データ統合の設定

**統合キー** が **msdyn_workorders** に存在することを確認
1. データ統合に移動
2. **接続設定** タブを選択
3. ワーク オーダー同期に使用される接続設定を選択します。
4. **統合キー** タブを選択
5. Msdyn_workorders を検索し、キーの **msdyn_name (ワーク オーダー番号)** が追加されていることを確認します。 表示されていない場合は、**キーの追加** をクリックして追加し、ページの上部にある **保存** をクリックします

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>ワーク オーダーから販売注文 (Field Service から Supply Chain Management) : WorkOrderHeader

フィルター: (msdyn_systemstatus ne 690970005) および (msdyn_systemstatus ne 690970000) および (msdynce_hasexternallymaintainedproductsonly eq true)

[![データ統合のテンプレートのマッピング](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>ワーク オーダーから販売注文 (Field Service から Supply Chain Management) : WorkOrderServiceLineEstimate

フィルター: (msdynce_headersystemstatus ne 690970005) および (msdynce_headersystemstatus ne 690970000) および (msdynce_orderhasexternalmaintainedproductsonly eq true) および (msdyn_linestatus eq 690970000) および (msdynce_headersystemstatus ne 690970004)

[![データ統合のテンプレートのマッピング](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>ワーク オーダーから販売注文 (Field Service から Supply Chain Management) : WorkOrderServiceLineUsed

フィルター: (msdynce_headersystemstatus ne 690970005) および (msdynce_headersystemstatus ne 690970000) および (msdynce_orderhasexternalmaintainedproductsonly eq true) および ((msdyn_linestatus eq 690970001) または(msdynce_headersystemstatus eq 690970004))

[![データ統合のテンプレートのマッピング](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>ワーク オーダーから販売注文 (Field Service から Supply Chain Management) : WorkOrderProductLineEstimate

フィルター: (msdynce_headersystemstatus ne 690970005) および (msdynce_headersystemstatus ne 690970000) および (msdynce_orderhasexternalmaintainedproductsonly eq true) および (msdyn_linestatus eq 690970000) および (msdynce_headersystemstatus ne 690970004) および (msdyn_allocated eq true)

[![データ統合のテンプレートのマッピング](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>ワーク オーダーから販売注文 (Field Service から Supply Chain Management) : WorkOrderProductLineUsed

フィルター: (msdynce_headersystemstatus ne 690970005) および (msdynce_headersystemstatus ne 690970000) および (msdynce_orderhasexternalmaintainedproductsonly eq true) および ((msdyn_linestatus eq 690970001) または (msdynce_headersystemstatus eq 690970004) または (msdyn_allocated ne true))

[![データ統合のテンプレートのマッピング](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]