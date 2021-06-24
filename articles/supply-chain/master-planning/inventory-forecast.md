---
title: 在庫予測
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management で在庫予測を作成するために使用できる供給と需要の予測機能について説明します。
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a7ed310ebdef130b0fb09c5db19397398dc5042
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216845"
---
# <a name="inventory-forecasts"></a>在庫予測

[!include [banner](../includes/banner.md)]

このトピックでは、在庫予測を表示および作成する方法について説明します。 品目、品目グループ、品目配賦キー、顧客勘定、顧客グループ、仕入先勘定、仕入先グループの供給予測明細行と需要予測明細行を作成、表示できます。

各予測行に対して、使用する予測モデルを選択できます。 その後、品目または品目グループに、数量やトランザクション金額を指定できます。 予測数量を割り当てるためのタイム スケジュールを設定することもできます。

供給予測明細行と需要予測明細行により、品目とモデルの同じ組み合わせに対して在庫予測が生成されます。 この在庫予測は、同じ品目に対して入力された供給と需要の残高を表します。 この値は編集できません。 在庫予測を使用すると、在庫管理チームは、予測される次の期間に品目の在庫に対して予想される変更を確認するのに役立ちます。

需要や供給を入力した後、予測計画を実行して材料および能力の総必要量を計算し、計画オーダーを生成することができます。

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>予測明細行の表示と手動入力

手動で製品の予測明細行を作成するには、この手順を使用してください。

他に予測明細行を作成する方法があります。

- [統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)。
- [需要予測の履歴データのインポート](import-historical-data.md)。
- [Microsoft Azure Machine Learning Web サービスを使って予測を生成します](demand-forecasting-setup.md)。
- [データ管理フレームワーク (ForecastDemandForecastEntryStaging および ForecastSupplyForecastEntryStaging データ エンティティ) を使用して、需要または供給予測明細行をインポートする](../../dev-itpro/data-entities/data-entities-data-packages.md)。

手順1. のテーブルの通り、使用されるページにはさまざまな方法でアクセスできます。

1. 次の表に示したように、予測を作成するエンティティのタイプと、作成する予測のタイプ、供給、需要、または在庫予測ページに応じて異なります。

    | エンティティ | 指示 |
    |---|---|
    | リリースされた製品 | <ol><li>**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</li><li>予測を作成する製品を選択します。</li><li>アクション ペインの **予測** グループの **計画** タブで、使用する予測のタイプに応じて、**需要予測**、**供給予測**、または **在庫予測** を選択 します。</li></ol> |
    | リリース済製品バリアント | <ol><li>**製品情報管理 \> 製品 \> リリース済製品バリアント** の順に移動します。</li><li>予測を作成するバリアントを選択します。</li><li>アクション ペインの **予測** グループの **計画** タブで、使用する予測のタイプに応じて、**需要予測**、**供給予測**、または **在庫予測** を選択 します。</li></ol> |
    | 品目グループ | <ol><li>**在庫管理 \> 設定 \> 在庫 \> 品目グループ** の順に移動します。</li><li>予測を作成する品目グループを選択します。</li><li>アクション ペインで、使用する予測のタイプに応じて、**予測 \> 需要**、**予測 \> 供給**、または **予測 \> 在庫予測** を選択します。</li></ol> |
    | 品目配賦キー | <ol><li>**在庫管理 \> 設定 \> 予測** の順に移動します。</li><li>予測を作成する品目配賦キーを選択します。</li><li>アクション ペインで、**需要予測** を選択します。</li></ol> |
    | 顧客 | <ol><li>**マスター プラン \> 予測 \> 手動予測入入力 \> 顧客** の順に移動します。</li><li>予測を作成する顧客を選択します。</li><li>アクション ペインで、**需要予測の定義** を選択します。</li></ol> |
    | 顧客グループ | <ol><li>**マスター プラン \> 予測 \> 手動予測入入力 \> 顧客グループ** の順に移動します。</li><li>予測を作成する顧客グループを選択します。</li><li>アクション ペインで、**需要予測の定義** を選択します。</li></ol> |
    | 仕入先 | <ol><li>**マスター プラン \> 予測 \> 手動予測入入力 \> ベンダー** の順に移動します。</li><li>予測を作成するベンダーを選択します。</li><li>アクション ペインで、**エントリ** を選択して **供給予測** ページを開きます。</li></ol> |
    | 仕入先グループ | <ol><li>**マスター プラン \> 予測 \> 手動予測入入力 \> ベンダーグループ** の順に移動します。</li><li>予測を作成するベンダー グループを選択します。</li><li>アクション ペインで、**エントリ** を選択して **供給予測** ページを開きます。</li></ol> | 
    | すべての行 | <ul><li>作業する予測のタイプに応じて、**マスター プラン \> 予測 \> 需要予測明細行** または **マスター プラン \> 予測 \> 供給予測明細行** に移動します。</li></ul> |

    選択に応じて、**供給予測** ページまたは **需要予測** ページが表示されます。 ページを開く前に選択したレコードの既存の予測行が表示されます。

1. アクション ペインで **新規** を選択して、ページ上部のグリッドに予測明細行を追加します。
1. 新しい明細行の **モデル** フィールド で、使用する予測モデルを選択します。 その後、必要に応じて、品目、品目グループ、顧客か仕入先の勘定、またはグループ、品目の数量、またはトランザクションの合計金額などのその他の詳細を入力します。 **供給予測** ページと **需要予測** ページで使用できるフィールドの詳細については、このトピックの後のセクションを参照してください。
1. 予測を期間に配賦するには、**概要** タブでツール バーの **予測の配賦** を選択します。
1. **配賦** グリッドで、予測数量を配分するための計画対象期間と時間間隔をレビューします。

## <a name="supply-forecast-lines"></a>供給予測の明細行

供給予測を使用すると、購入する必要がある品目の計画を作成できます。 調達係が注文する予定を伝える情報です。

供給予測は、品目、品目グループ、品目配賦キー、仕入先、および仕入先グループ別に入力できます。 さまざまなエンティティやレコードの **供給予測** ページを開く方法の詳細については、このトピックの [予測行の表示と手動入力](#manual-entry) を参照してください。

**供給予測** ページの上部には、供給予測明細行のグリッドと一連のタブが表示され、選択した予測明細行に関する詳細を表示および 設定できます。 ページの下部には配賦グリッド **配賦** が表示されます。

次のサブセクションでは、各タブで使用できるすべてのフィールドと、ページのアクション ペインと **概要** タブのツール バーで使用できるすべてのコマンドについて 説明 します。

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>アクション ペインの [供給予測] ページ上のコマンド

次の表で、アクション ペインの **供給予測** ページで使用可能なコマンドについて示します。

| コマンド | 説明 |
|---|---|
| 保存 | 現在の設定を保存します。 |
| 編集 | ページの設定を編集する場合に有効にします。 |
| 新規 | 予測明細行を上のグリッドに追加します。 |
| 消去 | 選択した予測行を上部グリッドから削除します。 |
| 予測残高 | 現在の会計年度に対して選択した行のモデル ID に対して計算された予測残高を表示します。 残高は期間 (月) 別に分割されます。 |
| キャッシュ フロー予測 | 総勘定元帳に割り当てられている予測トランザクションを表示します。 詳細については、「[キャッシュ フロー予測](../../finance/cash-bank-management/cash-flow-forecasting.md)」を参照してください。 |
| 在庫 \> 分析コードの表示 | **概要** タブのグリッドに表示する在庫分析コードを選択します。 |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>[供給予測] ページの [概要] タブのツール バー コマンド

次の表は、**供給予測** ページの **概要** タブ上のツールバーで使用可能なコマンドについて示します。

| コマンド | 説明 |
|---|---|
| 予測の配賦 | 配賦方法を使用する場合は、予測トランザクションの個々のスケジュール行を生成します。 行の数量は、選択した時間間隔、数量、および期間全体の金額に従って、日付別に分配されます。 |
| 一括更新 | **予測トランザクションの編集** ページを開きます。 (このトピックの後の [予測トランザクションの一括更新](#bulk-update) セクションをご覧ください。) |
| 在庫予測 | 選択した品目/モデルの組み合わせに対してフィルター処理される **在庫予測** ページのビューを開きます。 (このトピックの後の [在庫予測](#inventory-forecast) セクションをご覧ください。) |
| 在庫品目要求の作成 | プロジェクト関連の予測トランザクションの品目要求、および販売注文または品目仕訳帳明細行を作成するダイアログ ボックスを開きます。 このコマンドは、供給予測明細行と需要予測明細行の両方で使用できますが、**供給予測** ページでは使用できません。 |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>[供給予測] ページの [概要] タブ

次の表は、**供給予測** ページの **概要** タブにあるフィールドを示します。

| フィールド | 説明 |
|---|---|
| **モデル** | トランザクションが関連付けられている予測モデル。 |
| **日** | トランザクションの開始日。 |
| **仕入先** | トランザクションが関連付けられている仕入先。 |
| **仕入先グループ** | トランザクションが関連付けられているベンダー グループ。 |
| **品目番号** | 品目の識別子。 |
| **品目グループ** | トランザクションが関連付けられている品目グループ。 |
| **品目配賦キー** | 予測が関連付けられる品目配賦キー。 |
| **CW 数量** | 特定の Catch Weight 単位の予測数量。 |
| **CW 単位** | 品目の購買に使用する Catch Weight 単位。 この値は、品目設定から自動的に取得されます。 |
| **件数** | 特定の購買単位の予測数量。 |
| **単位** | 品目を購入する単位。 この値は、品目設定から自動的に取得されます。 ただし、単位換算が設定されている場合は変更できます。 |
| **金額** | 予測トランザクションが予測に占める総額 (総額から割引を差し引いた額)。 |
| **通貨** | 予測トランザクションに使用される通貨。 既定の通貨は自動的に入力されますが、別のテンプレートを選択できます。 |
| (他の分析コード) | 追加の分析コードをグリッド内で列として表示できます。 表示されたその他の分析を選択するには、アクション ペインで **分析コードの表示** を選択します。 |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>[供給予測] ページの [概要] タブ

**一般** タブには、**概要** タブで現在選択されている明細行に関する詳細な情報が表示されます。この情報の一部は、**概要** タブから繰り返されます。次の表では、**一般** タブに固有のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| レポート  | このオプションを *はい* に設定して、トランザクションをレポートに含めます。 |
| 備考 | 予測トランザクションに関するコメントを入力します。 |
| 有効 | このチェック ボックスをオンにすると、トランザクションが予算レポートに含まれます。 |
| キャッシュ フロー予測に含める | 予測トランザクションを一般会計に割り当てるには、このチェックボックスを選択します。 このチェック ボックスの設定は、トランザクション報告時に変更できません。 |
| 売上税グループ | 予測トランザクションの税を指定する場合に使用される税グループ。 |
| 品目消費税グループ | 予測トランザクションの税を指定する場合に使用される品目税グループ。 |
| メソッド | <p>予測トランザクションの割り当て方法を選択します。</p><ul><li>**なし** - 配賦は行われません。</li><li>**期間** - 各期間で同じ数量を予測します。 この値を選択した場合は、**単位あたり** フィールドに数量を指定し、**単位** フィールドに時間の単位を指定します。</li><li>**キー** - 予測数量は、**期間キー** フィールドで指定した期間割り当てキーに基づいて割り当てられます。 この方法は、季節変動を考慮する場合に使用できます。</li></ol>|
| 間隔 | <p>予測の対象となる期間を示す時間間隔の数値を入力します。 このフィールドは、**メソッド** フィールドで、*期間* を選択した場合にのみ使用できます。</p><p>たとえば、**メソッド** フィールドで *期間* を選択し、**単位あたり** フィールドに *1* を入力し、**単位** フィールドで *月* を選択します。 **終了** フィールドで、1 年先となる終了日を指定します。 この場合、ヘッダー行で指定された品目および数量に基づき、翌年の各月に対する予測明細行を 1 行ずつ作成します。</p> |
| 単位 | 時間間隔の単位を *日*、*月* または *年* から選択します。 その後割り当ては、**単位あたり** フィールドで指定した日数、月数、または年数に対応します。|
| 期間キー | 期間配賦キーを指定します。 |
| 終了 | **単位あたり** フィールドと **単位** フィールドを使用する場合の終了日を指定します。 |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>[供給予測] ページの [品目] タブ

**概要** タブを選択して、**品目** タブで現在選択されている明細行の詳細を表示します。

**品目** タブの上部にあるグリッドには、**概要** タブにも表示される品目情報が繰り返されます。さらに、**単位価格** フィールドには、**単位** フィールドに指定された単位数の購買価格が表示されます。 この単価は品目設定から自動的に取得されますが、変更することができます。

グリッドの下にあるフィールドにより、品目の詳細が表示されます。 この情報の一部は、**概要** タブから繰り返されます。次の表では、**品目** タブに固有のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| 価格単位 | 数量に適用される購買価格を指定します。 この値は品目テーブルから自動的に取得されますが、変更できます。 |
| 仕入諸掛 | 購買価格の固定請求。 この請求はは数量に関係しません。 |
| 割引率 | 割引率 (%)。 |
| 割引金額 | 販売単位ごとに金額で表した割引。 |
| 総額 | 割引が適用されない場合の金額。 |
| 件数 | 品目の在庫単位で表したトランザクション数量。 |
| 下位部品表 | 特定の下位 BOM の部品表 (BOM) 番号。 |
| サブ経路 | 特定の下位工程の工順番号。 |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>[供給予測] ページの [財務分析コード] タブ

**財務分析コード** タブには、**概要** タブで現在選択されている行のすべての財務分析コード 値が表示されます。

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>[供給予測] ページの [在庫分析コード] タブ

**在庫分析コード** タブには、**概要** タブで現在選択されている行のすべての在庫分析コード 値が表示されます。

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>[供給予測] ページの [配賦] グリッド

品目配賦キーを使用している場合、または1つ以上の将来の期間の品目予測を入力した場合は、**概要** タブのツール バーで **予測の配賦** を選択することで、予測を配賦できます。その後、**配賦** グリッドの明細行によって示される方法で数量が配分されます。

## <a name="demand-forecast-lines"></a>需要予測の明細行

需要予測を使用すると、顧客に対する需要を入力または生成できます。 これは、販売およびマーケティングの担当者が、将来の予測期間の予想される需要についてマスター プランの担当者に通知するのに役立ちます。

需要予測は、品目、品目グループ、品目配賦キー、顧客、および顧客グループ別に入力できます。 さまざまなエンティティやレコードの **需要予測** ページを開く方法の詳細については、このトピックの [予測行の表示と手動入力](#manual-entry) を参照してください。

**需要予測** ページの上部には、需要予測明細行のグリッドと一連のタブが表示され、選択した予測明細行に関する詳細を表示および 設定できます。 ページの下部には配賦グリッド **配賦** が表示されます。

次のサブセクションでは、各タブで使用できるすべてのフィールドと、ページのアクション ペインと **概要** タブのツール バーで使用できるすべてのコマンドについて 説明 します。

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>アクション ペインの [需要予測] ページ上のコマンド

次の表で、アクション ペインの **需要予測** ページで使用可能なコマンドについて示します。

| コマンド | 説明 |
|---|---|
| 保存 | 現在の設定を保存します。 |
| 編集 | ページの設定を編集する場合に有効にします。 |
| 新規 | 予測明細行を上のグリッドに追加します。 |
| 消去 | 選択した予測行を上部グリッドから削除します。 |
| 予測残高 | 現在の会計年度に対して選択した行のモデル ID に対して計算された予測残高を表示します。 残高は期間 (月) 別に分割されます。 |
| キャッシュ フロー予測 | 一般会計に割り当てられなければならない予測トランザクションを表示します。 詳細については、「[キャッシュ フロー予測](../../finance/cash-bank-management/cash-flow-forecasting.md)」を参照してください。 |
| 分析コードの表示 | **概要** タブのグリッドに表示する製品、保存スペース、トラッキング分析コードを選択します。 |
| 一般会計プレビュー | 選択したトランザクションの総勘定元帳エントリを表示します。 |
| 見積明細行の転送 | 選択したプロジェクトに見積明細行を転送します。 |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>[需要予測] ページの [概要] タブのツール バー コマンド

次の表は、**需要予測** ページの **概要** タブ上のツールバーで使用可能なコマンドについて示します。

| コマンド | 説明 |
|---|---|
| 予測の配賦 | 配賦方法を使用する場合は、予測トランザクションの個々のスケジュール行を生成します。 行の数量は、選択した時間間隔、数量、および期間全体の金額に従って、日付別に分配されます。 |
| 一括更新 | **予測トランザクションの編集** ページを開きます。 (このトピックの後の [予測トランザクションの一括更新](#bulk-update) セクションをご覧ください。) |
| 在庫予測 | 選択した品目/モデルの組み合わせに対してフィルター処理される **在庫予測** ページのビューを開きます。 (このトピックの後の [在庫予測](#inventory-forecast) セクションをご覧ください。) |
| 在庫品目要求の作成 | プロジェクト関連の予測トランザクションの品目要求、および販売注文または品目仕訳帳明細行を作成するダイアログ ボックスを開きます。 |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [概要] タブ

次の表は、**需要予測** ページの **概要** タブにあるフィールドを示します。

| フィールド | 説明 |
|---|---|
| **タスク名** | 予測明細行の作成に使用されたバッチ タスクの名前。 |
| **モデル** | トランザクションが関連付けられている予測モデル。 |
| **日** | トランザクションの開始日。 |
| **顧客 ID** | トランザクションに関連付けられている顧客アカウント。 |
| **顧客グループ** | トランザクションに関連付けられている顧客グループ。 |
| **品目番号** | 品目の識別子。 |
| **製品名** | 品目の説明。 |
| **品目配賦キー** | 在庫予測配賦中に使用される品目配賦キー。 |
| **販売数量** | 指定された販売単位でのトランザクション数量。 |
| **単位** | 品目が販売される単位。 |
| **金額** | 予測トランザクションが予測に占める総額 (総額から割引を差し引いた額)。 |
| **販売価格** | **価格単位** フィールドで指定された単位数に対する販売価格。 この値は品目から自動的に設定されますが、変更することができます。 |
| **販売通貨** | 予測トランザクションに使用される通貨。 既定の通貨は自動的に入力されますが、別のテンプレートを選択できます。 |
| **CW 数量** | 特定の Catch Weight 単位の予測数量。 |
| **CW 単位** | 販売される品目の Catch Weight 単位。 この値は、品目設定から自動的に取得されます。 |
| (他の分析コード) | 追加の製品分析コード、保管分析コード、および追跡分析コードをグリッドの列として表示できます。 表示されたその他の分析を選択するには、アクション ペインで **分析コードの表示** を選択します。 |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [概要] タブ

**一般** タブには、**概要** タブで現在選択されている明細行に関する詳細な情報が表示されます。この情報の一部は、**概要** タブから繰り返されます。次の表では、**一般** タブに固有のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| 需要予測の順序番号 | 需要予測明細行の固有番号。 この番号は、**マスター プラン パラメータ** ページで需要予測で選択された番号順序を使用して生成されます。 |
| 品目グループ | トランザクションが関連付けられている品目グループ。 |
| レポート  | このオプションを *はい* に設定して、トランザクションをレポートに含めます。 |
| 備考 | 予測トランザクションに関するコメントを入力します。 |
| 有効 | このチェック ボックスをオンにすると、トランザクションが予算レポートに含まれます。 このチェック ボックスの設定は、トランザクション報告時に変更できません。 |
| キャッシュ フロー予測に含める | 予測トランザクションを一般会計に割り当てるには、このチェックボックスを選択します。 このチェック ボックスの設定は、トランザクション報告時に変更できません。 詳細については、「[キャッシュ フロー予測](../../finance/cash-bank-management/cash-flow-forecasting.md)」を参照してください。 |
| 売上税グループ | 予測トランザクションの税を指定する場合に使用される税グループ。 |
| 品目消費税グループ | 予測トランザクションの税を指定する場合に使用される品目税グループ。 |
| メソッド | <p>予測トランザクションの割り当て方法を選択します。</p><ul><li>**なし** - 配賦は行われません。</li><li>**期間** - 各期間で同じ数量を予測します。 この値を選択した場合は、**単位あたり** フィールドに数量を指定し、**単位** フィールドに時間の単位を指定します。</li><li>**キー** - 予測数量は、**期間キー** フィールドで指定した期間割り当てキーに基づいて割り当てられます。 この方法は、季節変動を考慮する場合に使用できます。</li><ul>|
| 間隔 | <p>予測の対象となる期間を示す時間間隔の数値を入力します。 このフィールドは、**メソッド** フィールドで、*期間* を選択した場合にのみ使用できます。</p><p>たとえば、**メソッド** フィールドで *期間* を選択し、**単位あたり** フィールドに *1* を入力し、**単位** フィールドで *月* を選択します。 **終了** フィールドで、1 年先となる終了日を指定します。 この場合、ヘッダー行で指定された品目および数量に基づき、翌年の各月に対する予測明細行を 1 行ずつ作成します。 |
| 単位 | 時間間隔の単位を *日*、*月* または *年* から選択します。 その後割り当ては、**単位あたり** フィールドで指定した日数、月数、または年数に対応します。|
| 期間キー | 予測の配賦に使用する期間割り当てキーを指定します。 詳細については、[予算計画データ配賦](../../finance/budgeting/budget-planning-data-allocation.md) を参照してください。 |
| 終了 | **単位あたり** フィールドと **単位** フィールドを使用する場合の終了日を指定します。 |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [品目] タブ

**品目** タブには、**概要** タブで現在選択されている明細行に関する詳細な品目情報が表示されます。この情報の一部は、**概要** タブから繰り返されます。次の表では、**品目** タブに固有のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| 価格単位 | 販売価格が適用される販売単位数。 この値は品目テーブルから自動的に取得されますが、変更できます。 |
| 販売諸費用 | 販売価格の固定請求。 この請求はは数量に関係しません。 |
| 原価価格 | 在庫単位ごとの現在の予測トランザクションの原価。 この値は品目テーブルから取得されますが、変更できます。 |
| 割引率 | 割引率 (%)。 |
| 割引金額 | 販売単位ごとに金額で表した割引。 |
| 総額 | 割引が適用されない場合の金額。 |
| 在庫数量 | 品目の在庫単位で表したトランザクション数量。 |
| 特定の BOM を使用 | 特定の下位 BOM の BOM 番号。 |
| 特定の工程を使用 | 特定の下位工程の工順番号。 |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [プロジェクト] タブ

**プロジェクト** タブには、**概要** タブで現在選択されている明細行に関する詳細な品目情報が表示されます。この情報の一部は、**概要**、**一般** または **品目** タブから繰り返されます。次のテーブルでは、**プロジェクト** タブに固有のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| プロジェクト日付 | 需要予測トランザクションの日付。 |
| プロジェクト ID | 現在のトランザクションによって参照されるプロジェクトの識別子。 |
| 資金調達元 | 需要予測が関連付けられている資金調達ソース。 |
| 活動番号 | 需要予測トランザクションが関連付けられている活動。 |
| カテゴリ | 現在のトランザクションのコスト カテゴリ。 |
| 明細行プロパティ | トランザクションが関連付けられているステータス。 |
| 取引 ID | 需要予測トランザクションのシステム識別子。 |
| コスト金額 | 需要予測トランザクションの量。 |
| 単価 | 出荷単位ごとの価格。 |
| 変更者 | 選択したトランザクションを最後に変更した作業者の識別子。 |
| 請求書の日付 | 支払予定日を入力します。 |
| 消去日 | 削除日を表示または変更します。 予測が作成されると、プロジェクトの終了日が削除日として設定されます。 プロジェクトに終了日がない場合、プロジェクト日付が適用されます。 このフィールドは、固定価格プロジェクトや投資プロジェクトに対してのみ適用されます。 |
| 原価支払日 | 購買支払の予定日を入力します。 |
| 販売支払日 | 販売支払の予定日を入力します。 |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [財務分析コード] タブ

**財務分析コード** タブには、**概要** タブで現在選択されている行のすべての財務分析コード 値が表示されます。

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>[需要予測] ページの [在庫分析コード] タブ

**在庫分析コード** タブには、**概要** タブで現在選択されている行のすべての在庫分析コード 値が表示されます。

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>[需要予測] ページの [配賦] グリッド

品目配賦キーを使用している場合、または1つ以上の将来の期間の品目予測を入力した場合は、**概要** タブのツール バーで **予測の配賦** を選択することで、予測を配賦できます。その後、**配賦** グリッドの明細行によって示される方法で数量が配分されます。

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>在庫予測

供給予測明細行と需要予測明細行ページには、**在庫予測** ボタンが表示され、同じ品目/モデルの組み合わせでフィルター処理される **在庫予測** ページが表示されます。 この在庫予測は、同じ品目に対して入力された供給と需要の残高を表します。 この値は編集できません。 在庫予測を使用すると、在庫管理チームは、予測される次の期間に品目の在庫に対して予想される変更を確認するのに役立ちます。

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>[需要予測] ページ上のアクション ペイン

次の表で、アクション ペインの **需要予測** ページで使用可能なコマンドについて示します。

| 操作 | 説明 |
|---|---|
| 供給予測 | 選択した品目/モデルの組み合わせに対してフィルター処理される **供給予測** ページのビューを開きます。 |
| 需要予測 | 選択した品目/モデルの組み合わせに対してフィルター処理される **需要予測** ページのビューを開きます。 |
| 在庫 \> 分析コードの表示 | **概要** グリッドのグリッドに表示する製品、保存スペース、トラッキング分析コードを選択します。 |

### <a name="the-grid-on-the-inventory-forecast-page"></a>[在庫予測] ページ上のグリッド

次の表では、**品目予測** ページのグリッド内のフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| **モデル** | トランザクションが関連付けられている予測モデル。 |
| **品目番号** | 品目の識別子。 |
| **予算日付** | 予測トランザクションの日付。 |
| **予測の種類** | トランザクションのソース (*需要予測* または *供給予測*)。 |
| **CW 数量** | 特定の Catch Weight 単位の予測数量。 |
| **件数** | 在庫単位の予測数量。 |
| **CW 累計** | 同じ品目に対して複数の予測明細行が累計された場合の、Catch Weight 単位の累計予測数量。 |
| **下位部品表** | 特定の下位 BOM の BOM 番号。 |
| **サブ経路** | 特定の下位工程の工順番号。 |
| (他の分析コード) | 追加の分析コードをグリッド内で列として表示できます。 表示されたその他の分析コードを選択するには、アクション ペインで **在庫 \> 分析コードの表示** 分析の表示 を選択します。 |

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>予測トランザクションの一括更新

既存の予測トランザクション明細行を処理するには、この手順を使用します。 予測トランザクション明細行をコピー、編集、および削除できます。

1. 供給予測明細行または需要予測明細行ページで、**一括更新** を選択します。
1. ダイアログ ボックスで、**フィルター** を選択します。
1. **範囲** タブで、コピー、編集、または削除するソース予測データを特定する基準を選択します。 このデータには、予測モデル、品目番号、および顧客アカウントが含まれます。
1. **OK** を選択して、選択を確定します。

    データを選択した後、**予測トランザクションの編集** ダイアログ ボックスを使用して、データをどのようにコピー、編集、または削除するのかを定義できます。

    > [!NOTE]
    > フィルター処理の手順は、**一括編集** 機能が前提条件となります。 このオプションをスキップすると、**すべての** 予測明細行が選択および更新されます。 このため、トランザクションが意図せずに重複または削除を引き起こす可能性があります。

1. **管理** セクションで、選択した予測トランザクションをコピー、更新、または削除するかどうかを選択します。
1. 予測のパラメータを変更するには、**フィールドの修正** セクションを使用します。 パラメータのチェック ボックスを選択し、使用可能なオプションから選択します。 たとえば、**モデル** チェック ボックス をオンにし、予測モデル番号を選択します。 既存の予測明細行が選択した予測モデルにコピーされます。
1. **期間の変更** セクションを使用して、予測の開始日と終了日を予測の前後に移動します。 チェック ボックスを選択し、数量および期間のフィールドを使用して、予測日を動かす必要がある期間を定義します。 負の数量を入力すると、開始日を前に動かします (前に動かします)。

    たとえば、予測トランザクションの開始日を6か月遅らせる場合は、このチェック ボックスをオンにし、数量として *6* を入力し、期間として *月* を選択します。

1. 実際の予測データを更新するには、**フィールドを訂正** セクションを使用します。 **フィールド** で、変更する基準を選択します。 **係数** フィールドで、選択した基準に適用する増倍係数を入力するか、加算または減算の定数を入力します。 たとえば、基準として *数量* を選択し、係数 *1.5* を入力すると、品目数量に 1.5 掛になります。 または、品目数量を 25 単位減らすには、定数として *-25* と入力します。
1. **財務分析コード** セクションを使用して、予測明細行の財務分析コードを更新します。 変更する財務分析コードを選択し、選択した分析コードに適用する値を入力します。
1. **OK** を選択して変更を適用します。

## <a name="run-forecast-planning"></a>予測計画の実行

需要予測や供給予測を入力した後、予測計画を実行して材料および能力の総必要量を計算し、計画オーダーを生成することができます。

1. **マスター プラン \> 予測 \> 予測計画** の順に移動します。
1. **予測計画** フィールドで、予測計画を選択します。
1. 各計画タスクの処理時間を記録するには、**処理時間を追跡** を有効化します。
1. **スレッド数** フィールドに値を入力します。 (詳細については、[マスター プランのパフォーマンスを向上させる](master-planning-performance.md) を参照します。)
1. **コメント** フィールドに、テキストを入力して必要な追加情報を取得します。
1. **含めるレコード** クイックタブで、**フィルター** を選択して品目の選択を制限します。
1. **バックグラウンドで実行** クイック タブで、バッチのパラメータを指定します。
1. **OK** を選択します。

計算される要求を表示するには、**総必要量** ページを開きます。 たとえば、**リリースされた製品** ページの **計画** タブの **要求** セクションで、**総必要条件** を選択します。

生成された計画オーダーを表示するには、**マスター プラン \> 共通 \> 計画されたオーダー** に移動し、予測計画を選択します。

## <a name="additional-resources"></a>追加リソース

- [需要予測の概要](introduction-demand-forecasting.md)
- [需要予測の設定](demand-forecasting-setup.md)
- [統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)
- [ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]