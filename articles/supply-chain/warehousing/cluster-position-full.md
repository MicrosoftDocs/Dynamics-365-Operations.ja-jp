---
title: クラスター位置フル
description: この記事では、クラスター位置フル機能について説明します。 この機能により、クラスター ピッキングが使用されているときに、コンテナやトートの容量制限においてより大きな誤差を許容できるため、作業の中断に関するルールをより厳格に適用することができます。
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9361448ba7993ba7cc126d6dd60a45fe497b2e84
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218775"
---
# <a name="cluster-position-full"></a>クラスター位置フル

[!include [banner](../includes/banner.md)]

*クラスター位置フル* 機能を使用することで、クラスター ピッキングが使用されているときに、コンテナやトートの容量制限において、より大きな誤差を許容できるため、作業の中断に関するルールをより厳格に適用することができます。 一般的なシナリオでは、選択されたコンテナーには作業指示書のすべての品目が適合するわけではありません。 クラスター ピッキングの対象となる倉庫の作業者は、このシナリオに対するオプションがほとんどないため、より大きなコンテナサイズに変更するか、上司と協力して別の解決策を考えなければなりません。

この機能により、クラスター内の作業単位のいずれかで **フル** ボタンを実行する機能が導入されます。 以前のバージョンでは、このオプションは、通常の注文のピッキングに対してのみ使用でき、クラスター ピッキングには使用できませんでした。 ただし、この機能は、残りの作業をキャンセルするという点で、標準の **フル** ボタンとは異なります。 ユーザーが同じクラスタに別の在庫置場を追加することを推奨するものでも、自動的に新しい作業を作成するものでもありません。

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>クラスター ポジション フル機能のオン/オフ

この記事で説明する機能を使用するには、ご利用システムで *クラスター ポジション フル* 機能がオンになっている必要があります。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *クラスター ポジション フル* 機能を検索して、この機能のオン/オフを切り替えることができます。

## <a name="setup"></a>設定

このセクションでは、*クラスター位置フル* の機能を設定および使用する際のガイドラインと例を示します。

### <a name="make-sample-data-available"></a>サンプル データを有効化する

ここで指定されたサンプル レコードと値を使用して [シナリオ例](#example-scenario) を実行するには、標準の [デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md) がインストールされているシステムを使用する必要があります。 また、開始する前に **USMF** 法人を選択する必要があります。

このシナリオは、実稼働システムで作業する際の機能ガイダンスとして使用することもできます。 ただし、その場合はここで説明した設定を独自の値に置き換える必要があります。

### <a name="cluster-profiles"></a>クラスター プロファイル

クラスター ID を自動的に生成するかどうか、使用するポジション数、クラスターを分割する場合、ピッキング作業の順序付けと検証方法を指定する必要があります。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> クラスター プロファイル** の順に移動します。
1. リスト ペインで、クラスター **レコードの作成** を選択します。
1. **一般** クイック タブで、次の値を検証します :

    - **クラスターID の生成 :** *はい*
    - **位置をアクティブ化する :** *はい*
    - **位置の数 :** *2*
    - **位置の名前 :** *数値*
    - **クラスターの分割位置 :**  *プット*
    - **検証タイプのソート :** *位置スキャン*

1. **クラスターの並べ替え** クイックタブを選択します。 グリッドは空白にする必要があります (ここには行が含まれていない必要があります)。

### <a name="work-templates"></a>作業テンプレート

クラスター ピッキングに使用するピッキング作業がどのように作成されるかを定義する必要があります。

1. **倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。
1. ページ上部で、**作業指示書の種類** フィールドを *販売注文* に設定します。
1. デモデータの中で、以下の作業テンプレートがリストされていることを確認してください。 これらが使用できない場合は、このシナリオを完了できません。

    - 61 SO ステージ
    - 61 SO クラスター ピッキング

### <a name="location-directives"></a>場所のディレクティブ

品目をピッキングする場所とプットする場所を指定する必要があります。

1. **倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。
1. リスト ヘッダーでは、**作業指示書のタイプ** フィールドを *販売注文* に設定します。
1. デモ データの中で、以下の販売注文ディレクティブがリストされていることを確認してください。 これらが使用できない場合は、このシナリオを完了できません。

    - 61 クラスター ピッキング
    - 61 SO 注文のピッキング

### <a name="mobile-device-menu-items"></a>モバイル デバイスのメニュー品目

クラスター ピッキングで指示された既存の作業を利用するには、モバイルデバイスのメニュー項目を構成する必要があります。 クラスターピッキングのモバイル デバイス メニュー項目で、 **作業の分割を許可** のパラメータをオンにして、*SO ピッキング* の作業クラスを追加する必要があります。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目** の順に移動します。
1. リスト ペインで、**クラスター ピッキングの作成** レコードを選択します。
1. アクション ペインで、**編集** を選択します。
1. **一般** クイック タブで、次の値を設定します。

    - **作業指示 :** *クラスター ピッキング*
    - **ライセンスプレートの生成:** *はい*
    - **作業の分割を許可する :** *はい*
    - **クラスタープロファイル ID :** *クラスターの作成*

    他のすべてのフィールドの既定値を受け入れます。

1. **作業クラス** クイックタブで、必要に応じて次の2行を追加します :

    - 1行目 (通常はデモデータに含まれています) :

        - **作業クラス ID :** *営業* 
        - **作業指示のタイプ :** *販売注文*

    - 2行目 (通常はデモデータに含まれません) :

        - **作業クラス ID:** *SO ピック*
        - **作業指示のタイプ :** *販売注文*

1. アクション ペインの **作業確認の設定** の設定に移動します。
1. **編集** を選択します。
1. グリッド内の行に以下の値を入力します。
    - **作業タイプ** - *ピック*
    - **製品確認** - *チェックボックスを確認する*

1. アクション ペインで **保存** を選択し、ページを閉じます。

## <a name="create-picking-work"></a>ピッキング作業の作成

クラスター ピッキングを開始する前に、いくつかの出荷作業を作成する必要があります。 前に作成したクラスター プロファイルは、2 つのクラスターのポジションを指定します。 したがって、販売注文ピッキングは少なくとも 2 つの作業 ID を作成する必要があります。 このシナリオでは、トランザクションが倉庫 *61* で発生し、品目 *L0101* と *T0100* が使用されます。 デモデータには、これら品目の手持在庫が十分にある必要があります。 トランザクションを完了するために十分な在庫があることを確認してください。

### <a name="create-sales-order-1"></a>販売注文の作成 1

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. **新規** を選択して新たに販売注文 1 を作成します。
1. **販売注文の作成** ダイアログ ボックスでは、次の値を設定します。

    - **顧客アカウント:** *US-010*
    - **倉庫:** *61*

1. **OK** を選択します。
1. 新しい販売注文が開かれます。 **販売注文明細行** クイックタブで、次の設定で明細行を追加します :

    - **品目番号:** *T0100*
    - **数量:** *5*

1. **明細行の詳細** クイックタブの **配送** タブで、**出荷日の確認** フィールドが今日の日付に設定されます。
1. **販売注文明細行** クイックタブで、次の設定を持つ 2 つ目の明細行を追加します :

    - **品目番号:** *L0101*
    - **数量:** *20*

1. **明細行の詳細** クイックタブの **配送** タブで、**出荷日の確認** フィールドが今日の日付に設定されます。
1. 追加した各行に対して、次の手順に従って在庫を引当します :

    1. 引当する行を選択します。
    2. **販売注文行** クイック タブで、**在庫 \> 予約** を選択します。
    3. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、在庫を引当てします。
    4. **引当** ページを閉じます。

1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    リリースが完了すると、作成されたウェーブ ID と出荷 ID を示す情報メッセージが表示されます。

### <a name="create-sales-order-2"></a>販売注文の作成 2

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. **新規** を選択して新たに販売注文 2 を作成します。
1. **販売注文の作成** ダイアログ ボックスでは、次の値を設定します。

    - **顧客アカウント:** *US-011*
    - **倉庫:** *61*

1. **OK** を選択します。
1. 新しい販売注文が開かれます。 **販売注文明細行** クイックタブで、次の設定で明細行を追加します :

    - **品目番号:** *L0101*
    - **数量:** *20*

1. **明細行の詳細** クイックタブの **配送** タブで、**出荷日の確認** フィールドが今日の日付に設定されます。
1. **販売注文明細行** クイックタブで、次の設定を持つ 2 つ目の明細行を追加します :

    - **品目番号:** *T0100*
    - **数量:** *2*

1. **明細行の詳細** クイックタブの **配送** タブで、**出荷日の確認** フィールドが今日の日付に設定されます。
1. 追加した各行に対して、次の手順に従って在庫を引当します :

    1. 引当する行を選択します。
    2. **販売注文行** クイック タブで、**在庫 \> 予約** を選択します。
    3. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、在庫を引当てします。
    4. **引当** ページを閉じます。

1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    リリースが完了すると、作成されたウェーブ ID と出荷 ID を示す情報メッセージが表示されます。

### <a name="get-work-ids-and-license-plate-numbers"></a>作業 ID とライセンスプレート番号の取得

2つのピッキングラインを持つ2つの作業 ID が作成されている必要があります。 次の手順に従って、作業 ID とライセンス プレート の割り当てを検索します。

1. **倉庫管理 \> 作業 \> 作業の詳細** の順に移動します。
1. **概要** グリッドで、今作成した 2つの販売注文の **注文番号** 列を検索します。 各販売注文については、対応する作業 ID をメモしておいてください。
1. 販売注文ごとに行を選択して、**明細行** グリッドに関連情報を表示します。 各品目がピッキングされる場所をメモします。
1. **在庫管理 \> 照会およびレポート \> 手持在庫リスト** の順に移動します。
1. アクション ペインで **寸法** を選択して、**寸法の表示** ダイアログ ボックスを開きます。
1. **ライセンス プレート**、**倉庫**、**品目番号** の各チェックボックスがオンになっていることを確認し、 **OK** を選択します。
1. **フィルター** ペインで、次のフィルタを設定します :

    - **品目番号** – *L0101* と *T100* の **いずれか** である
    - **倉庫** – **61** – *で始まる*

1. 表示された **ライセンス プレート** の値をメモします。

## <a name="example-scenario"></a><a name="example-scenario"></a>シナリオ例

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>モバイル デバイスフローの実行 – 製品に使用する作業確認の設定

1. 倉庫 *61* のユーザーとして、Warehouse Management モバイル アプリにログインします。
1. **アウトバウンド \> クラスター ピッキングの作成** に移動します。

    **タスク : 作業をクラスターに割り当てる** ページが表示されます。

1. 販売注文 1 に作業 ID を入力し、クラスター位置 1 に割り当てます。
1. **OK** (チェックマーク記号) を選択します。
1. 販売注文 2 に作業 ID を入力し、クラスター位置 2 に割り当てます。
1. **OK** (チェックマーク記号) を選択します。

    **タスク : クラスター ピッキングの作成 : ピック** ページが表示され、*品目 L0101 2 PL* が表示されます。

クラスター プロファイルでは、[ポジションの数] が 2 に設定されているため、最初の [統合ピッキング] に自動的に次の指示が表示されます : 品目 *L0101* を含む 2 つのパレット

次のステップの過程においてはいつでも、**詳細** タブを選択して、ピッキング場所などのタスクに関する追加情報を表示することができます。

1. **品目** フィールドを *L0101* に設定します。 これにより、このメニュー項目に必要な品目番号が確認されます (このメニュー項目を作成した際に **モバイル デバイス メニュー品目**  ページの **作業確認の設定** を選択して設定したものです)。
1. ピッキングされる場所の品目に関連付けられているライセンス プレート番号を入力します。 2 つのパレットを選択します。
1. **LP** フィールドを *LP\_PICK\_01* に設定します。
1. **OK** (チェックマーク記号) を選択します。

    **タスク : 並べ替え : クラスター ピッキングの作成** ページが表示されます。 ここでは、2つのピッキング済パレットをピックのポジションに並べ替えます。 このポジションは、ピッキングされた在庫を販売注文と区別するトートやコンテナになる可能性があります。

1. ポシション 1 (販売注文 1 に使用する) の位置にソートされる品目 (*L0101*) と数量 (*20* ea) の詳細を表示します。
1. **POSITION NA** フィールドを *1* に設定します。
1. **OK** (チェックマーク記号) を選択します。
1. ポシション 2 (販売注文 2 に使用する) の位置にソートされる品目 (*L0101*) と数量 (*20* ea) の詳細を表示します。
1. **POSITION NA** フィールドを *2* に設定します。
1. **OK** (チェックマーク記号) を選択します。

    **タスク : クラスター ピッキングの作成 : ピック** ページが表示され、*品目 T0100 7 ea* が表示されます。

このシナリオでは、ポシション 1 は、販売注文 1 を処理するにあたってピッキングする必要がある品目の数量全体を受け入れることができません。 ポシションは、"満杯" とマークする必要があります。 このシナリオでは、2つ目の品目の部分的なピッキングを行います。 2つ目の品目はポシション 1 のために部分的にピッキングし、注文を処理するにあたって残数量をピッキングするために新規作業を作成します。

1. メニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれる場合もあります) を選択し、続いて **満杯のポジション** を選択します。
1. 満杯になっているポジションを特定し、*1* を選択します。
1. **OK** (チェックマーク記号) を選択します。
1. 1 のポジションにピック可能なピック量を入力します。 ピッキングされる品目番号は、システムによって決定可能です。
1. *2* と入力します。
1. **OK** (チェックマーク記号) を選択します。
1. 品目番号を確認して、残りの品目のピッキングを 2 のポジションに対して完了します。
1. **品目** フィールドを *T0100* に設定します。
1. **OK** (チェックマーク記号) を選択します。
1. **LP** フィールドを *LPREPL04* に設定して、品目がピッキングされるライセンス プレートを入力します。
1. **OK** (チェックマーク記号) を選択します。
1. ポシション 2 (販売注文 2 に使用する) の位置にソートされる品目 (*T0100*) と数量 (*2* ea) の詳細を表示します。
1. **POSITION NA** フィールドを *2* に設定します。
1. **OK** (チェックマーク記号) を選択します。
1. ポシション 1 (販売注文 1 に使用する) の位置にソートされる品目 (*T0100*) と数量 (*2* ea) の詳細を表示します。
1. **POSITION NA** フィールドを *1* に設定します。
1. **OK** (チェックマーク記号) を選択します。

    **タスク : クラスター ピッキングの作成 : プット** ページが表示されます。

このシナリオでは、クラスターピッキングが完了しており、ユーザーは、ポジション 1とポジション 2からステージング場所である *STAGE01* にピック済品目を入れるように指示されています。

1. ページの情報を確認します。 総数である *44* がステージング場所にプットされることを示しています。
1. **OK** (チェックマーク記号) を選択します。

    「クラスターが完了」しましたというメッセージが表示されます。

以上で、**売上のピッキング** メニューの品目を使用して残余数量を選択できるようになります。 その後、**売上の荷積** メニュー品目を使用して、ステージング場所から荷積ドックに品目を移動することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]