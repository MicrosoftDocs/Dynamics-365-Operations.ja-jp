---
title: 陸揚原価パラメーターの設定
description: この記事では、転記、状態の更新、番号順序、および動作用に陸揚原価モジュール全体で使用される一般情報および構成設定の設定方法について説明します。
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 609403b251338b7e792f3ab624fb37a1833c919b
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725524"
---
# <a name="landed-cost-parameters-setup"></a>陸揚原価パラメーターの設定

[!include [banner](../../includes/banner.md)]

**陸揚原価パラメーター** ページを使用して、転記、状態の更新、番号順序、および動作用に **陸揚原価** モジュール全体で使用される一般情報および構成設定を設定します。 パラメーターの設定は法人間で共有され、管理者によって変更できます。

## <a name="open-the-landed-cost-parameters-page"></a>陸揚原価パラメーター ページを開く

パラメーターを使用するには、**陸揚原価 \> 設定 \> 陸揚原価パラメーター** の順に移動してから、次のセクションの説明に従ってフィールドを設定します。

![陸揚原価パラメーター ページ。](media/landed-cost-parameters.png "陸揚原価パラメーター ページ")

## <a name="general-tab"></a>[全般] タブ

### <a name="general-fasttab"></a>全般クイック タブ

次の表では、**陸揚原価パラメーター** ページの **全般** タブの **全般** クイック タブで使用できるフィールドについて説明します。

| 設定 | 説明 |
|---|---|
| 輸送量を使用 | 輸送量は定義された期間に設定され、複数通貨を使用する商品の見積原価に使用されます。 輸送量を使用するには、このオプションを *はい* に設定します。 |
| 為替レート タイプ | 航海および航海コストに対して複数の通貨計算に使用する為替レートの既定のコレクション。 |
| 発注書の数量の更新 | ユーザーが発注書明細行の数量を変更した場合の処理を選択します。<ul><li>**承認** – 航海の数量は自動的に調整されます。</li><li>**警告** – 明細行が航海に関連付けられた場合、警告が表示されますが、航海の数量は更新されます。</li><li>**エラー** – 明細行が航海に関連付けられた場合、エラー メッセージが表示され、発注書を更新できません。 したがって、最初に注文明細行を航海から削除する必要があります。</li></ul> |
| カートンの数を自動的に更新 | このオプションを *はい* に設定すると、すべてのカートンがまとめて追加され、航海とコンテナー レベルで表示されます。 *いいえ* に設定すると、カートンの数は最初は 0 (ゼロ) に設定され、必要に応じて手動で編集できます。 |

### <a name="costing-fasttab"></a>原価計算クイック タブ

次の表では、**陸揚原価パラメーター** ページの **全般** タブの **原価計算** クイック タブで使用できるフィールドについて説明します。

| 設定 | 説明 |
|---|---|
| 転記明細 | 元帳の値調整を選択します。<ul><li>**合計** – 合計値が元帳に転記されます。</li><li>**品目グループ** – 調整は、品目グループごとに指定されます。</li><li>**品目番号** – 調整は、品目ごとに指定されます。 この値は最も詳細です。</li></ul> |
| ゼロ原価を許可 | このオプションを *いいえ* に設定すると、 ユーザーが見積航海コストの値を含まない航海請求書または発注書に対する原価見積を転記しようとする場合、エラーが表示されます。 エラー メッセージに、原価 0 (ゼロ) を割り当てできないというメッセージが表示され、請求書の転記が失敗します。 この場合、ユーザーは見積を手動で更新 (または自動原価の再構成) してから、更新された値を取り込むか、適用されない場合は原価を削除できます。<p>このオプションを *はい* に設定すると、その航海コストは空白になります。 この場合、原価領域に応じて 0 (ゼロ) の価格が割り当てされます。 その後、航海が入庫したときに、仕入先の原価請求書をゼロ価格の原価に対して処理できます。</p><p>自動原価レコードで見積を構成して、ゼロ価格の原価が表示されないようにすることをお勧めします。 この見積は完全に正確ではありませんが、想定されるゼロ原価よりも正確である必要があります。</p> |
| 調整転記日付 | 買掛金勘定の航海コスト請求を転記すると、決済テーブル (在庫調整) も更新されます。 請求仕訳帳を表示している間に、**航海コストの選択** ページで、既定で設定される日付を選択します。<ul><li>**トランザクションの日付** – 仕訳帳の日付 (転記日付) を使用します。</li><li>**発注書請求日** – 在庫 (発注書) 請求書の財務転記日付を使用します。</li><li>**選択した日付** – ユーザーは転記日付を指定できます。 この日付は空白のままにできますが、原価請求の転記時にまだ空白の場合は、エラーが表示されます。</li></ul> |
| 仕入請求書伝票の使用 | このオプションが *はい* に設定されている場合、原価計上トランザクションでは仕入請求書に使用されるのと同じ伝票番号を使用します。 *いいえ* に設定されている場合、システムは **陸揚原価パラメーター** ページの **番号順序** タブで設定された **原価の見越計上伝票** の番号順序に対して、次に使用可能な番号を使用します。<p>このオプションは、**買掛金勘定パラメーター** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションが *はい* に設定される場合にのみ影響を与えます。</p> |
| 清算勘定への手動転記のブロック | このオプションを *はい* に設定して、仕入先請求仕訳帳のアクション ウィンドウで **機能 \> 航海コストの選択** を選択することにより、トランザクションが航海にリンクされてない場合に精算勘定に転記されないようにします。 このオプションを *はい* に設定して、航海および清算勘定が正しく決済されるようにすることをお勧めします。 |
| 原価タイプの掛売見越勘定を使用 | このオプションが *はい* に設定されている場合、**原価タイプ コード** ページの関連する原価タイプ コードに対して構成される掛売見越勘定が、経費として原価を計上するために使用されます。<p>このオプションは、**買掛金勘定パラメーター** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションが *はい* に設定される場合にのみ影響を与えます。 |
| 差異として調整を転記 | このオプションを *はい* に設定すると、標準機能が上書きされ、見積原価と実際原価間の差異に関連する在庫調整トランザクションが強制的に差異勘定に転記されます。<p>このオプションを *いいえ* に設定すると、差異に関連する在庫調整トランザクションが、原価計算方法および原価タイプ コードの構成に基づいて処理されます。 標準原価の場合でも、差異は差異勘定に転記されます。 移動加重平均 (WMA) の場合、差異は差異勘定または在庫に転記されます。</p><p>このオプションは、**買掛金勘定パラメーター** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションが *はい* に設定される場合にのみ影響を与えます。</p> |

### <a name="validation-fasttab"></a>検証クイック タブ

次の表では、**陸揚原価パラメーター** ページの **全般** タブの **検証** クイック タブで使用できるフィールドについて説明します。

| 設定 | 説明 |
|---|---|
| 複数原価請求書 | 同じ雑費の航海、フォリオ、またはコンテナ―に対して複数の請求書を処理する場合の処理を選択します。<ul><li>**承認** – 複数の原価請求を許可する必要があります。</li><li>**警告** – 警告が表示されます。</li><li>**エラー** – エラー メッセージが表示されます。</li></ul> |
| フォリオごとに複数の仕入先 | 1 つのフォリオに複数の仕入先の発注書を追加した場合の処理を選択します。<ul><li>**承認** – アクションを許可する必要があります。</li><li>**警告** – 警告が表示されますが、アクションを実行できます。</li><li>**エラー** – エラー メッセージが表示され、アクションは実行されません。</li></ul><p>関税ブローカーまたは現地の法律により、このフィールドに対する特定の値が義務付けられている場合があります。</p> |
| 複数の荷渡方法の許容範囲 | 航海とは異なる配送モードを使用する発注書の商品がその航海に追加された場合の処理を選択します。<ul><li>**承認** – アクションを許可する必要があります。</li><li>**警告** – 警告が表示されますが、アクションを実行できます。</li><li>**エラー** – エラー メッセージが表示され、アクションは実行されません。</li></ul> |
| 複数の倉庫許容範囲 | 異なる倉庫に配送する必要がある複数の注文明細行が含まれる場合の処理を選択します。 これらの注文明細行は、複数の発注書に分割される場合があります。<ul><li>**承認** – アクションを許可する必要があります。</li><li>**警告** – 警告が表示されます。</li><li>**エラー** – エラー メッセージが表示されます。</li></ul> |
| 容積がありません | ユーザーが容積のない品目を航海に追加した場合の処理を選択します。<ul><li>**承認** – 品目を許可する必要があります。</li><li>**警告** – 警告が表示されます。</li><li>**エラー** – エラー メッセージが表示されます。</li></ul><p>容積を使用して費用を計算および分割する場合は、*警告* または *エラー* のいずれかを選択することをお勧めします。</p> |
| 航海原価のないサービス プロバイダー | ユーザーが、航海にリンクされていないサービス プロバイダーに対して請求書を処理しようとする場合の処理を選択します。 <ul><li>**承認** – アクションを許可する必要があります。</li><li>**警告** – 警告が表示されます。</li><li>**エラー** – エラー メッセージが表示されます。</li></ul><p>*警告* を選択することをお勧めします。</p> |

### <a name="defaults-fasttab"></a>既定値クイック タブ

次の表では、**陸揚原価パラメーター** ページの **全般** タブの **既定値** クイック タブで使用できるフィールドについて説明します。

| 設定 | 説明 |
|---|---|
| 仕訳帳名 | *着荷仕訳帳の作成* 機能が使用する、既定の仕訳帳を選択します。 |
| 航海状態 | ユーザーがシステムで航海用のレンタル出荷コンテナーを設定する前に、その航海に必要な状態を選択します。 通常、このアクションは商品が輸送中またはドックにあるときに発生します。 |
| 輸送テンプレート | 新しいレンタル出荷コンテナーに使用する既定の輸送テンプレートを選択します。 通常は、レンタル費用を含む輸送テンプレートを選択します。 |
| 振替 | 配送の過剰/過少数量が定義された許容範囲内である場合は、移動仕訳帳が自動的に処理されます。 使用する既定の移動仕訳帳を選択します。 選択した移動仕訳帳名の **相手勘定** フィールドには値が必要です。 |
| 譲渡 | 過少配送が処理される場合、短期入庫数量は過少配送倉庫に転送されます。 使用する既定の譲渡仕訳帳を選択します。 |
| 非航海発注書を無効化 | 航海に関連付けられていない発注書に対する、陸揚原価の過剰/過少配送機能をオフにします。 |
| 輸送中の商品以外の発注書を無効化 | 輸送中の商品機能を使用しない発注書に対する、陸揚原価の過剰/過少配送機能をオフにします。 |
| 入庫支払猶予期間中の輸送中の商品 | 出荷コンテナーの最初の入庫後、その出荷コンテナー番号に対して追加の過剰入庫を完了できる日数を指定します。 |

## <a name="status-updates-tab"></a>状態の更新タブ

システムでは、状態の値を使用して各航海の状態を示します。 航海状態の値は、航海の追跡または定期処理バッチ ジョブによって自動的に適用されます。 または、航海を開いて、アクション ウィンドウの **管理** タブの **航海の更新** グループで状態を選択することにより、手動で適用することもできます。 

必要な数の航海状態の値を作成することができます。 ただし、そのうち 4 つは **陸揚原価パラメーター** ページの **状態の更新** タブの特別な目的で使用するよう定義される必要があります。 次の表に、ここで使用できるフィールドを示します。

| 設定 | 説明 |
|---|---|
| 原価計算済み | 航海が確定済みであることを示す航海状態を選択します。 |
| 輸送中 | 航海が輸送中であることを示す航海状態を選択します。 |
| 原価計算の準備 | 航海が原価計算の準備ができていることを示す航海の状態を選択します。 この状態は、**航海コストのクレジット** フィールドが *仕入先* に設定されているすべての在庫仕入請求書および航海コスト請求書がその航海に対して処理された場合に使用されます。 原価計算するプロセスに失敗した航海の状態は、*原価計算の準備* の状態となります。|
| 事前原価計算 | 航海が事前原価計算であることを示す航海状態を選択します。 この状態は、既に原価計算された後に、新しい原価トランザクションが航海に追加される場合に使用されます。 2 回目の運賃請求または予期しない滞船料を受け取った場合、以前に原価計算された航海に新しい原価トランザクションが追加される場合があります。 この状態は、原価計算された航海に新しい航海コストが追加される場合に自動的に適用されます。 |

## <a name="voyage-creator-tab"></a>航海作成者タブ

次の表は、**陸揚原価パラメーター** ページの **航海作成者** タブのセクションについて説明します。

| 項 | 説明 |
|---|---|
| 許容範囲 | **容積許容範囲外** および **重量許容範囲外** フィールドでは、超過容積および超過重量と見なされる商品のしきい値を定義します。 ユーザーが **航海編集** ページで商品を追加するときに、 容積または重量がここで設定した値を超える場合、システムに警告が表示されます。 各フィールドの値は、関連する出荷コンテナー タイプに対して設定されている最大容積または最大重量の割合で表されます。 この値は、最大容積または最大重量の 5 ～ 10% にすることをお勧めします。 |
| フォリオ作成設定 | システムでは、航海作成の処理中に複数のフォリオを作成できます。 このセクションを使用して、新しいフォリオをいつ作成する必要があるのかについて定義します。 このセクションの各行については、指定したテーブルとフィールドがチェックされ、一意のフィールド値ごとにフォリオが作成されます。 |

## <a name="cost-estimates-tab"></a>原価見積タブ

**陸揚原価パラメーター** ページの **原価見積** タブでは、1 つのフィールド **既定の原価計算バージョン** のみが提供されます。 このフィールドは、原価計算方法が *標準原価計算* である場合にのみ適用されます 。 *品目原価価格の更新* の定期処理タスクに使用する既定の原価計算バージョンを選択します。 新しい会計年度が始まる時には、この設定を毎回変更する必要があります。

## <a name="inventory-dimensions-tab"></a>在庫分析コード タブ

**陸揚原価パラメーター** ページの **在庫分析コード** タブを使用して、分析コードが使用される各陸揚原価ページで既定により表示される利用可能な在庫分析コードを制御します。

分析コードを選択してから、その分析コードが既定で表示される各ページの **航海明細行**、**輸送中の商品**、または **原価見積** オプションを *はい* に設定します。 必要に応じて、他の分析コードに対してもこの手順を繰り返します。

このタブの設定により、法人全体で指定された各ページの既定の分析コードが確立されます。 ただし、指定したページのいずれかを操作しているユーザーは、アクション ウィンドウで **在庫 \> 分析コードの表示** を選択することにより、既定の分析コードを上書きできます。

## <a name="number-sequences-tab"></a>番号順序タブ

**陸揚原価パラメーター** ページの **番号順序** タブでは、陸揚原価で必要な参照番号順序の各タイプが一覧表示されますが、それは法人間では共有されません。 一覧の各参照については、番号順序コードを選択します。


## <a name="shared-number-sequences-tab"></a>共有番号順序タブ

**陸揚原価パラメーター** ページの **共有番号順序** タブでは、陸揚原価の法人間で共有される参照番号順序の各タイプが一覧表示されます。 現在、一覧にある番号順序は 1 つです。 この番号順序は、航海 ID に使用されます。


## <a name="feature-visibility-tab"></a>機能の可視性タブ

陸揚原価は、Microsoft Dynamics 365 Supply Chain Management で複数の頻繁に使用されるページに機能 (フィールドおよび機能) を追加します 。 これらのページには、仕入先マスター データ、リリース済製品、発注書、移動オーダー、および倉庫の設定に関連するページが含まれます。 陸揚原価を使用している場合、その機能を利用する前にどこにでも表示できるようにする必要があります。 陸揚原価を使用していない場合、機能を非表示にして操作を妨げないようにすることができます。

**陸揚原価パラメーター** ページの **機能の可視性** タブで、**有効化** オプションを *はい* に設定して、陸揚原価機能が利用可能な場所で表示されるようにします。 *いいえ* に設定すると、一般ページの機能が陸揚原価以外で非表示になります。 ただし、このオプションが *いいえ* に設定されている場合でも、**陸揚原価パラメーター** ページを含むモジュール自体は、アクセスする適切なアクセス許可を持つユーザーが引き続き使用できます。
