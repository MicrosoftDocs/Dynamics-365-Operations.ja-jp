---
title: ピッキング行のグループ化
description: この記事には、ピッキング行のグループ化の概要が含まれます。
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 00a4e07ac38a83cd4569006f3b6e2bdd59ed1a42
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334538"
---
# <a name="pick-line-grouping"></a>ピッキング行のグループ化

[!include [banner](../includes/banner.md)]

ピッキング行のグループでは、品目と場所が同じ複数の作業明細行を結合して、モバイル デバイスでユーザーに提示される 1 つのピッキングを作成できます。 したがって、倉庫の作業者は、可能な限り効率的な指示を受け取ることができますが、システムに必要な作業明細行の分割 (たとえば、異なるコンテナや注文など) も維持されます。

## <a name="turn-on-the-pick-line-grouping-feature"></a>ピッキング行のグループ機能をオンにする

この機能は使用する前にシステムでオンにする必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、この機能の状態を確認し、必要に応じて有効にすることができます。 この機能は、次のようにして表示されます。

- **モジュール:** *倉庫管理*
- **機能名:** *ピッキング行のグループ*

## <a name="set-up-pick-line-grouping"></a>ピッキング行のグループ化の設定

### <a name="create-a-mobile-device-menu-item"></a>品目のモバイル デバイス メニューの作成

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **メニュー項目名** フィールドに、*販売グループ行のピッキング* と入力します。
1. **タイトル** フィールドに、*販売グループ行ピッキング* と入力します。 このタイトルはモバイル デバイス メニューに表示されます。
1. **モード** フィールドで、*作業* を選択します。
1. **既存の作業を使用** オプションを *はい* に設定します。
1. **一般** クイック タブで、次の値を設定します。

    - **指示者** フィールドで、*ユーザー主導* を選択します。
    - **ライセンス プレートの生成** オプションを *はい* に設定します。
    - **グループ ピック** オプションを *はい* に設定します。
    - 残りのオプションに対しては規定値を受け入れます。

1. 次の手順に従って、モバイル デバイスのメニュー項目に対して有効な作業クラスを構成します。

    1. **作業クラス** クイック タブで、**新規** を選択します。
    2. **作業クラス ID** フィールドで、使用する倉庫に応じて *販売* または *SO ピッキング* のいずれかを選択できます。 このシナリオでは *SO ピッキング* を選択します。

        **作業指示書のタイプ** フィールドは自動的に *発注書* に設定されます。

### <a name="set-up-a-mobile-device-menu"></a>モバイル デバイス メニューを設定する

次の手順に従って、作成したメニュー項目を **出荷** メニューに追加します。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュー** の順に移動します。
1. アクション ウィンドウで、**編集** を選択します。
1. リスト ペインには、既存のすべてのモバイル デバイス メニューが表示されます。 リストで、*出荷* を選択します。
1. **使用可能なメニューとメニュー項目** のリストで、作成した *販売グループ列のピッキング* メニュー項目を検索して選択します。
1. 右矢印ボタンを選択して、*販売グループ列のピッキング* メニュー項目を **メニュー構造** の一覧に移動します。
1. 上向き矢印ボタンと下向き矢印ボタンを使用して、メニュー構造をメニューの目的の位置に移動します。
1. アクション ウィンドウで、**保存** を選択します。

### <a name="set-up-a-work-template"></a>作業テンプレートを設定する

1. **倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。
1. **ワーク オーダー タイプ** フィールドで、*販売注文* を選択します。
1. **概要** グリッドで、この機能で使用する作業テンプレートを検索および選択します。 このシナリオについては *51 ピッキングからステージ* を選択します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. このクエリの編集ダイアログ ボックスの、**ソーティング** タブで、**追加** を選択して、新しい行を追加し、次の値を設定します。

    - **テーブル** 列で、*一時的な作業トランザクション* を選択します。
    - **派生テーブル** 列で、*一時的な作業トランザクション* を選択します。
    - **フィールド** 列で、*品目番号* を選択します。
    - **検索の方向** 列で、*昇順* を選択します。

1. **OK** を選択してダイアログ ボックスを閉じて、選択項目を保存します。
1. 次のメッセージが表示されます: "グループはリセットされますが、続行しますか?" **はい** を選択して続行します。

> [!IMPORTANT]
> ピッキング行のグループ化機能を機能させるには、作業明細行を品目 ID で並べ替える必要があります。 同じ品目を含む行が順序付けされない場合は、グループ化されません。

## <a name="example"></a>例

### <a name="create-picking-work"></a>ピッキング作業の作成

ピッキング行のグループ化を設定する前に、適格な出荷作業をいくつか作成する必要があります。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. **新規** を選択して新しい販売注文を作成します。
1. **顧客口座** フィールドで、*US-004* を選択します。
1. **一般** クイック タブの **倉庫** フィールドで、 *51* を選択します。
1. **OK** を選択します。
1. **販売注文明細行** クイックタブで、次の 6 行を追加します。

    - **明細行 1:** **品目番号** フィールドで、*M9200* を選択します。 **数量** フィールドに *3* と入力します。
    - **明細行 2:** **品目番号** フィールドで、*M9201* を選択します。 **数量** フィールドに *3* と入力します。
    - **明細行 3:** **品目番号** フィールドで、*M9202* を選択します。 **数量** フィールドに *2* と入力します。
    - **明細行 4:** **品目番号** フィールドで、*M9200* を選択します。 **数量** フィールドに *1* と入力します。
    - **明細行 5:** **品目番号** フィールドで、*M9200* を選択します。 **数量** フィールドに *3* と入力します。
    - **明細行 6:** **品目番号** フィールドで、*M9202* を選択します。 **数量** フィールドに *7* と入力します。

    各品目の合計数量の概要を次に示します。

    - **品目 M9200:** 各 *7* 個
    - **品目 M9201:** 各 *3* 個
    - **品目 M9202:** 各 *9* 個

1. 注文を倉庫にリリースする前に、ピッキング場所にすべての注文のすべての品目に十分な在庫があることを確認する必要があります。 **場所のディレクティブ** の設定を確認して、販売注文のピッキングに使用されるピッキング場所を決定します。 倉庫 *51* に Contoso のデモ データ環境を使用している場合は、利用可能な在庫が必要です。

    行ごとに在庫の予約を行う必要があります。

1. **販売注文明細行** クイック タブで、予約する必要がある明細行を 1 つ選択します。
1. グリッドの上部にある **在庫** メニューで、**引当** を選択します。
1. **引当** ページの、アクション ペインで **ロットの引当** を選択して、予約を適用します。 その後、ページを閉じます。
1. 引当する必要がある残りの行に対して、手順 8 ~ 10 を繰り返します。

    倉庫にリリースした販売注文を選択します。

1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    出荷とジョブが作成されたというメッセージと、バッチで実行するためにそのシステムが送信されたというメッセージが表示されます。

    6 行の作業に対して作業 ID が作成され、そのジョブと一部のジョブが終了すると、その作業 ID が作成されます。 行は品目番号順に並べ替えられます。

1. **倉庫管理 \> 作業 \> すべての作業** の順に移動して、作成した作業を表示します。 次の手順で必要になるので、**作業 ID** の値をメモしておきます。

### <a name="initiate-picking-from-the-mobile-device"></a>モバイル デバイスからのピッキングの開始

1. 倉庫 *51* に設定されているユーザーとして、モバイル デバイスにサインインします。
1. モバイル デバイスで、モバイル デバイス メニュー品目を含むメニューを選択します。 このシナリオでは **出荷** を選択します。
1. **販売グループ行ピッキング** メニュー品目を選択して、ピッキングを開始します。
1. 前の手順でメモした **作業 ID** 値を入力します。

    品目 *M9200* のすべてのピック明細行がグループ化されるピック ステップが表示され、各品目 *M9200を* の *7* つをピックする指示が表示される必要があります。

    > [!IMPORTANT]
    > モバイル デバイスでは、3 つのピッキング作業明細行のピッキング作業が、ユーザーの 1 つのピッキング ステップに集計されています。

1. ピッキング ステップを確定します。
1. 作業 ID の作業頁に移動して、品目 *M9200* の 3 つのピッキング明細行がすべて同時に閉じられていることを確認します。
1. モバイル デバイスに戻り、ピックを続行します。 品目 *M9201* の作業行 4 が表示されます。 注文には作業行が 1 行しかないので、集計する必要は何もありません。
1. ピッキング ステップを確定します。
1. モバイル デバイスの最後のピッキング ステップでは、ワーク オーダーから最後の 2 つのピッキング明細行を集計します。
1. 品目 *M9202* の各 *9* 個のピッキング ステップを完了します。
1. 作業を完了するには、プット ステップと、追加のピック / プットのペアを確認します。

> [!IMPORTANT]
>
> - 作業明細行は、順序が正しい場合にのみグループ化できます。
> - 次の機能はサポートされていません。
>
>   - CW 品目
>
>    作業に CW 品目がある場合は、ピッキングを開始する前にエラー メッセージが表示されます。
>
>   - ピース ピッキング
>   - 未完了の補充作業がある作業明細行
>   - 超過ピッキング
>   - 品目再配賦の未処理ピッキング


[!INCLUDE[footer-include](../../includes/footer-banner.md)]