---
title: フォリオの管理
description: この記事では、フォリオの使用方法について説明します。 通常、フォリオは、出荷ごとの 1 つのエンティティまたは会社に対する 1 つの仕入先の商品で構成されます。 1 つのフォリオにある商品は、1 つのコンテナに入るか、または複数のコンテナに分散されることがあります。
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ab5729cd441246a6c04ac060d5a69f949bfe47c5
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725497"
---
# <a name="manage-folios"></a>フォリオの管理

[!include [banner](../../includes/banner.md)]

多くの場合、フォリオは税関の法規によって決定されます。 出荷ごとの 1 つのエンティティまたは会社に対する 1 つの仕入先の商品により構成されます。 1 つのフォリオにある商品は、1 つのコンテナーで管理されます。

**すべてのフォリオ** ページを開くには、**荷揚原価 \> フォリオ \> すべてのフォリオ** に移動します。 このページには、現在のすべてのフォリオの一覧が表示されます。 アクション ウィンドウのボタンを使用して、フォリオの作成、削除、および操作を行うことができます。 一覧でフォリオを選択すると、**フォリオ** ページにその詳細が表示されます。

## <a name="action-pane"></a>アクション ウィンドウ

**すべてのフォリオ** と **フォリオ** ページのアクション ウィンドウには、選択したフォリオを操作するボタンが表示されます。 各ボタンは 1 つのアクションを実行します。 アクション ウィンドウにはタブも含まれており、各タブで一連の関連するボタンが提供されます。 記載されている場合以外は、次のサブセクションで説明されているすべてのボタンとタブは、リスト ビュー (**すべてのフォリオ** ページ) と詳細ビュー (**フォリオ** ページ) の両方で使用可能です。

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>アクション ウィンドウに直接表示されるボタン

次の表で、アクション ウィンドウで直接使用可能なボタンについて示します。

| ボタン | 説明 |
|---|---|
| 新規 | フォリオを作成します。 |
| 消去 | 開いているまたは選択したフォリオを削除します。 |
| 航海原価 | **航海原価** ページを開くと、航海中のすべての商品についてフォリオ レベルの原価を表示または追加することができます。 フォリオ原価を手動で航海に追加したとき、原価照会ページに自動的に追加され、**航海原価** ページで指定された方法にしたがってすべての商品に割り当てられます。 |

### <a name="buttons-on-the-manage-tab"></a>管理タブのボタン

次の表で、アクション ウィンドウの **管理** タブで使用可能なボタンについて示します。

| ボタン | 説明 |
|---|---|
| 入庫リストの転記 | フォリオのすべての発注書明細行の入庫リストを転記します。  |
| 製品受領書の転記 | フォリオのすべての発注書明細行の製品受領書を転記します。 |
| 請求書の転記 | フォリオのすべての発注書明細行の請求書を転記します。  |
| 移動オーダーの出荷 | 関連する出荷の現在のフォリオに関連付けられている移動オーダー明細行の移動オーダーを転記します。 |
| 移動オーダーの入庫 | 関連する出荷の現在のフォリオに関連付けられている移動オーダー明細行の移動オーダー入荷を転記します。 |
| 輸送中の商品の受領 | フォリオで輸送中のすべてのオーダー明細行を受信します。 |
| ドキュメント受領 | **ドキュメント受領済** オプションの設定を *はい* に更新します。 このボタンを使用すると、品目や購買注文明細行がロックされ、さらに更新されることはありません。 |
| 自動原価の検索 | 関連する航海原価を検索します。 これらの原価が既に検索または更新されている場合、次のメッセージを受信します。「未請求の原価明細行が存在します。 上書きしますか?」 フォリオに添付され、請求済の航海原価は上書きされないことに注意してください。 |
| 着荷仕訳帳の作成 | 高度な倉庫機能を使用して、組織の着荷仕訳帳を生成します。 **数量の初期化** (推奨)、**輸送中の商品から作成** や **発注書から作成** を選択することができます。 最後のオプションは、輸送中の商品処理が使用されているかどうかにより異なります。 |
| 見越計上原価 | 原価タイプが借方に指定された勘定科目を持つ原価が発生します。 通常、このボタンは在庫が移動中か、商品が受領されて請求された場合に使用されます。 |

### <a name="buttons-on-the-general-tab"></a>一般タブのボタン

次の表で、アクション ウィンドウの **一般** タブで使用可能なボタンについて示します。

| ボタン | 説明 |
|---|---|
| 入庫リスト | フォリオのすべての発注書明細行の入庫リストを転記します。  |
| 製品受領書 | 使用されている場合、製品受領書のレコードを表示します。 |
| 品目到着 | 使用されている場合、品目着荷仕訳を表示します。 |
| 原価照会 | 原価照会ページを開いて、出荷コンテナー、フォリオ、および発注書など、航海の原価すべてを表示します。 表示アクションを使用して、ページの正確な表示を調整できます。 原価照会ページで、すべての領域、品目、および原価タイプ コードを表示できます。 これらの品目を削除することにより、原価をグループ化してページを調整することができます。 この機能は、サイズと色を使用している場合に役立ちます。 ページに表示される分析コードを変更できます。 **原価** ページには、**転記** タブの **借方** 入力が *品目* に設定されている原価タイプ コードのみが表示されます。 |

## <a name="header-view"></a>ヘッダーの表示

**ヘッダー** ビューを開くには、フォリオを開き、フォリオの見出しの右上にある **ヘッダー** タブを選択します。

### <a name="settings-on-the-general-fasttab"></a>全般クイック タブの設定

次の表で、フォリオの **ヘッダー** ビューの **一般** クイックタブで使用可能なフィールドについて説明します。

| フィールド | 説明 |
|---|---|
| フォリオ | フォリオの名前。 この名前は、フォリオが作成されるときに自動的に生成されます。|
| 航海 | フォリオに関連付けられている航海。 |
| 関税ブローカー | フォリオの関税ブローカーを選択します。 関税ブローカーは仕入先で定義します。 作成した原価の自動決定が有効になります。 |
| 航空貨物運送状/船荷証券の保管 | フォリオに適用する社内貨物運送状または船荷証券を指定します。 |
| 法人 | フォリオに関連付けられている法人 (会社)。 |
| 貨物制御番号 | このフィールドは、一部の国や地域の関税部門で使用されます。 |
| 測定 | このフィールドにより、**荷揚原価** モジュールで指定された測定を有効にすることができます。 多くの場合、測定は商品の個別の容積や重量は分からないが、金額や数量よりもさらに正確な配賦が必要な組織により使用されます。 配送業者は重量または容積測定で提供し、品目または発注書のいずれかのレベルで設定できます。 パラメーターが選択されているか、または手動で入力されている場合、自動的に更新されます。 |
| 測定単位 | 指定した測定に適用する単位。 |
| カートン数 | フォリオのカートンの数。 このフィールドは、パラメーターの選択に応じて自動的に更新されます。 |
| 仕入先 | フォリオに関連付けられている仕入先を選択します。 このフィールドは情報提供のみを目的としています。 どの機能にも影響しません。 |
| 氏名 | 選択している仕入先勘定の名前。 |
| 備考 | フォリオに関連する追加情報すべてを入力します。 |
| 商品の説明 | フォリオを識別するのに役立つ商品の説明を選択します。 詳細については、[商品の説明](shipping-information-setup.md#description-of-goods) を参照してください。 |
| 評価日 | このフィールドは税入力ページに関連付けられています。 **荷揚原価** モジュールは、ここで設定した日付の税関為替レートが使用されます。 既定値は、税入力ページの日付です。 |
| 関税 ID | 税関 ID を入力します。 国や地域の関税部門がこの ID を提供します。 |
| 税率コード | フォリオに関連付ける税率コードを入力します。 通常、このコードは出荷先の国や地域ごとに必要です (そして定義されます)。 |

### <a name="settings-on-the-delivery-fasttab"></a>配送クイックタブの設定

次の表で、フォリオの **ヘッダー** ビューの **配送** クイックタブで使用可能な設定について説明します。

| フィールド | 説明 |
|---|---|
| フォリオ日付 | フォリオに関連付ける日付を選択します。 既定値は、航海の作成日です。 |
| 出荷港での ETA | 目的地の港 (「出荷先」の港) への予定到着時刻 (ETA)。 |
| 推定出荷日 | 通常、商品が倉庫に到着する予定日です。 このフィールドは、配送予定日を計算するときには使用されません。 (代わりに、追跡コントロールの配送予定日が使用されます。) このフィールドを設定することにより、値が追跡コントロールの配送予定日と照合され、[追跡コントロール センター](delivery-information-setup.md#tracking-control-center) を使用します。 |
| 元のドキュメントを受領しました | 元のドキュメントを受領した日付。 |
| ブローカーのアドバイス | ブローカーが指示された日付。 |
| 元の船荷証券が送信されました | 元の船荷証券が送られた日付。 |
| リリースされた商品 | 商品がリリースされた日付。 |
| 顧客の予定 | 顧客の予定日。 |
| 倉庫で出荷 | 商品が倉庫に配送された日付。 |
| 確認日 | 検証日。 |
| 出荷指示 | 配送の指示を受領した日付。 |
| 出荷元港 | 航海が出発した港。 |
| 出荷先港 | 航海が到着した港。 複数の港で停泊する場合があるため、出荷コンテナーには別の港があることがあります。 |

### <a name="settings-on-the-export-fasttab"></a>エクスポート クイックタブの設定

次の表で、フォリオの **ヘッダー** ビューの **エクスポート** クイックタブで使用可能な設定について説明します。

| フィールド | 説明 |
|---|---|
| 輸出者 | 輸出者はフォリオに保存できます。 国際取引では、発注書を 1 つの会社に送り、別の会社から商品を受け取る場合があります。 追跡およびドキュメントは税関に必要です。 輸出者の名前と住所をここに保存できます。 |
| 氏名 | 選択した輸出者の名前。 |

## <a name="lines-view"></a>明細行の表示

**明細行** ビューを開くには、フォリオを開き、フォリオの見出しの右上にある **明細行** タブを選択します。

### <a name="information-on-the-folio-fasttab"></a>フォリオ クイックタブの情報

**明細行** ビューの **フォリオ** クイックタブには、フォリオに関する情報が表示されます。 この記事で前述されているように、この情報のほとんどは **ヘッダー** ビューにも表示されます。

### <a name="information-and-buttons-on-the-lines-fasttab"></a>明細行クイックタブの情報とボタン

**明細行** ビューの **明細行** クイックタブには、現在のフォリオに含まれている全体または一部の発注書明細行に関する詳細が表示されます。

次のテーブルは、**明細行** ビューの **明細行** クイックタブで使用できるボタンを示しています。

| ボタン | 説明 |
|---|---|
| 除去 | 航海から選択した発注書明細行を削除します。 |
| 在庫 \> トランザクション | 選択した発注書明細行の在庫トランザクションを表示します。 輸送中の商品を使用している場合、元の注文および輸送中の商品も表示されることに注意してください。 |
| 在庫 \> 分析コードの表示 | 表示するトランザクションに対して表示される在庫分析コードを選択できるダイアログ ボックスを開きます。 |
| 更新反映 | 選択した発注書明細行の明細金額、重量、または容積に関連する情報を更新します。 |

### <a name="information-on-the-lines-details-fasttab"></a>明細行の詳細クイックタブの情報

**明細行** ビューの **明細行の詳細** クイックタブには、**明細行** クイックタブで現在選択している発注書明細行に関する詳細が表示されます。
