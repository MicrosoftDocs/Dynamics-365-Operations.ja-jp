---
title: ウェーブ ラベル印刷
description: この記事では、ウェーブ ラベル印刷についての説明と、設定方法について解説します。
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 18620602c5f3cf6a69a36ef7248f35e5509337b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901824"
---
# <a name="wave-label-printing"></a>サイクル ラベル印刷

[!include [banner](../includes/banner.md)]

ウェーブ ラベル印刷では、ウェーブの実行中にウェーブのテンプレートから直接ラベルを作成して印刷できる新しいウェーブ ステップ メソッドが導入され、ラベル印刷に代わるアプローチを提供します。 そのため、作業者がモバイル デバイス上で作業指示を実行する前に、ラベルは既に利用可能となっています。 作業者は、ピッキング後ではなく、ピッキング中に必要なラベルを貼ることができます。

ウェーブ ラベル印刷では、Zebra プログラム言語 (ZPL) を使用してラベル レイアウトが作成されます。 ラベルのレイアウトは、ヘッダー、本文、フッターの3つのセクションに分かれており、重複した構造を持つラベルを使用することができます。 ウェーブ ラベルのテンプレートは、システムに使用するラベルのレイアウトの指示を出します。 使用するプリンターはユーザーが指定できます。 また、必要に応じて、複数のプリンターで同時にラベルを印刷することもできます。 **ウェーブ ラベルの履歴** ページには、この設定を使用して作成されたすべてのラベルのレコードが表示されます。

作業ヘッダーに基づいたラベルの印刷と照合、作業ヘッダーごとの区切りラベルの印刷、コンテナー内容のラベル、ケースのラベル、その他のラベルを印刷することができます。

> [!NOTE]
> この機能は、ドキュメント ルーティングに基づく既存のラベル印刷機能を置き換えるものではありません。

ウェーブ ラベル印刷では、次の機能拡張が提供されます。

- コンテナ化を使用せずに、単一の作業ラインにカートン数に応じたラベルを印刷します。 ("カートン" とは、出荷単位の順序グループライン上で指定された出荷単位を意味します。)
- 複数の異なるラベル シーケンスを印刷します (たとえば、カートンとパレット ラベル)。
- ラベル リストを含有し (たとえば、1/124、2/124、...124/124) 、リストの範囲を定義します (たとえば、作業ライン、積荷ライン、出荷)。
- 船荷証券を生成する前に、ラベルに船荷証券 ID を作成して印刷します。
- それぞれのカートンに対して固有のシリアル出荷コンテナー コード (SSCC) を作成し、各ラベルに含めます。
- 船荷証券 ID と SSCC で使用する、GS1 に準拠したシーケンス番号を作成します。
- モバイル デバイスとリッチ クライアントの両方からラベルを再印刷します。
- ラベルを無効化し (例 : 小口ピックのシナリオなど)、再印刷を行います。
- ウェーブ ラベル履歴をクリーンアップします。
- ドキュメント ルーティング レイアウトに対して行われた改善は、ドキュメント ルーティング レイアウトとウェーブ ラベル レイアウト間で共有されます。 (詳細については、 [ライセンス プレート向けドキュメント ルーティング レイアウト ](../warehousing/document-routing-layout-for-license-plates.md)を参照してください。)

これらの機能強化により、パレット積みのカートンへのラベル付けがより効率的になります。 カートンを個別にスキャンすることで自動的に受注確認を行う大手の小売店に出荷している企業には、特に有用となります。

> [!NOTE]
> この記事で説明する構成シナリオは、業務上の要件に応じて個別に、または組み合わせて実装することができます。 連続して動作する複数のウェーブ ラベルのテンプレートを設計することができます (シナリオ3を参照のこと)。 たとえば、シナリオ１でカートン ラベルを印刷し、シナリオ２でパレット ラベルを印刷することができます (在庫のパレットのサイズや構成が異なる場合)。

## <a name="turn-on-the-wave-label-printing-feature"></a>ウェーブ ラベルの印刷機能をオンにする

Supply Chain Management のバージョン 10.0.21 の時点では、この機能は必須です。この機能は既定で有効になっていて、再度オフにできない状態です。 ただし、この機能は引き続き次のように[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)にリストされています。

- **モジュール:** *倉庫管理*
- **機能名 :** *ウェーブ ラベルの印刷*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>シナリオ1 : 1つのウェーブ ラベルを生成するウェーブ ラベルの印刷

このシナリオでは、各カートンを個別にスキャンすることで、受注を自動的に確認する大手の小売業者向けの出荷ラベルの印刷方法を解説しています。

このシナリオでは、エンドツーエンドのフローを説明します。

### <a name="make-demo-data-available"></a>デモ データを有効化する

このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。

### <a name="make-sure-that-the-wave-label-method-is-available"></a>ウェーブ ラベルのメソッドが使用可能であることを確認します

場合によっては、ウェーブ ラベルの印刷メソッドを利用するには、ウェーブ プロセスのメソッドを再生成する必要があります。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。
1. **WaveLabelPrinting** がリストに含まれていることを確認します。 表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。

### <a name="configure-a-wave-template"></a>ウェーブのテンプレートを構成する

ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。
1. **62 出荷の既定** などのテンプレートを選択します。
1. **メソッド** クイックタブで、**ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。
1. **選択したメソッド** 列で、**ウェーブ ラベルの印刷** メソッドを選択し、**ウェーブ ステップ コード** フィールドを *PrintLabel* に設定します。 ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。

### <a name="create-a-wave-label-layout"></a>ウェーブ ラベルのレイアウトを作成する

ラベル レイアウトでは、ラベルに印刷される情報と、ラベルのレイアウトを制御します。ここでは、プリンターに送信される ZPL コードを入力します。

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。
1. 以下の設定をしたレコードを作成します:

    - **ラベルのレイアウト ID :** *カートン*
    - **説明 :** *カートン (SSCC)*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**ウェーブ ラベル行の設定** を選択します。

    **ウェーブ ラベル行の設定** ページが表示されます。 ここでは、ラベルの動的な部分を構成できます。

1. 以下の設定を持つ行を追加します :

    - **行 Id:** *WaveLabel*
    - **行テーブル名 :** *WHSWaveLabel*
    - **行の開始位置 :** *0*

        このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。

    - **行の高さ :** *0*

        このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。 行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。 この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。

    - **ページごとの行数 :** *1*

        このフィールドでは、各ラベルに印刷できる行の数を定義します。

        > [!NOTE]
        > この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。

1. ページを閉じます。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *作業タイプ*
    - **基準:** *ピッキング*

    このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。

1. 船荷証券 ID を印刷できるようにするには、**結合** タブで **作業ライン** テーブルを選択し、**出荷** テーブルを結合します。
1. クエリ エディター ダイアログボックスを閉じます。
1. **印刷テキストレイアウト** クイック タブには、**ヘッダー セクション**、**ボディ セクション**、**フッター セクション** の3つのセクションがあります。 **ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。 たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > この設定では、ラベルを1部ずつ印刷します。 さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。 たとえば、各ラベルを4部印刷するには、**\^PQ4** を指定します。

以上でラベルを使用する準備が整いました。

### <a name="create-a-wave-label-type"></a>ウェーブ ラベルのタイプを作成する

ウェーブ ラベルのタイプは、ウェーブ ラベル テンプレートを出荷単位の順序グループ ライン上の出荷単位にリンクするために使用されます。

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル タイプ** に移動します。
1. 以下の設定のあるウェーブ ラベル タイプを追加します :

    - **ラベル タイプ :** *カートン*
    - **説明 :** *カートン*

### <a name="set-up-unit-sequence-groups"></a>単位順序グループを設定します

次に、ウェーブ ラベル タイプの出荷単位順序グループを設定します。

1. **倉庫管理 \> 設定 \> 倉庫 \> 出荷単位の順序グループ** に移動します。
1. **Ea Box PL** グループを選択します。
1. **ボックス** 明細行では 、**ウェーブ レベル タイプ** フィールドに *カートン* を設定します。

### <a name="create-a-wave-label-template"></a>ウェーブ ラベルのテンプレートを作成する

次は、ウェーブ ラベルタイプのウェーブ ラベル テンプレートを作成します。

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。
1. ウェーブ レベル テンプレートを追加し、ヘッダーに以下の値を設定します :

    - **ラベル テンプレート名 :** *カートン ラベル*
    - **説明 :** *カートン ラベル*
    - **ウェーブ ステップ コード :** *PrintLabel*
    - **倉庫:** *62*

1. **一般** クイックタブで、**ウェーブ ラベル タイプ** フィールドを *カートン* に設定し ます。
1. **ウェーブ ラベル テンプレートの詳細** クイック タブで、次の設定を含む新たな行を追加します。

    - **ラベルのレイアウト ID :** *カートン*
    - **プリンター名** 適切な ZPL プリンターを選択します。
    - **クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。

1. アクション ウィンドウで、**保存** を選択します。
1. オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。 **ウェーブ ラベル テンプレートの詳細** クイックタブで、**クエリの編集** を選択します。 続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **テーブル:** *出荷*
    - **派生テーブル:** *出荷*
    - **フィールド :** *アカウント番号*
    - **条件 :** 関連する顧客アカウント番号を入力します。

    完了後は、**OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。

1. アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。
1. クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド :** *参照読み込み行の Id (レコード ID)*
    - **検索の方法:** *昇順*

1. **OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。
1. グループのリセット操作の確認を促すメッセージ ボックスが表示されます。 **はい** を選択して続行します。
1. アクション ウィンドウで、**ウェーブ ラベル テンプレート グループ** を選択します。
1. **ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、**参照フィールド名** フィールドが *参照積荷行 ID* に設定されている行を選択し、この行の **ラベルのビルド ID** チェックボックスを選択します。

    > [!NOTE]
    > この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。 このラベル番号は、ラベルのレイアウトに印刷できます。

### <a name="configure-number-sequence-extensions"></a>シーケンス番号の拡張機能を構成する

シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。 この構成は、こののシナリオでは任意となります。 詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>販売注文を作成して倉庫にリリースする

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。
1. 以下の設定で販売注文を作成します:

    - **顧客アカウント:** *US-001*
    - **倉庫:** *62*

1. 次の設定を持つ 2 つの販売明細行を追加します :

    - 販売注文明細行 1:

        - **品目番号:** *A0001*
        - **数量:** *9024*
        - **出荷単位 :** *ea* (9024 ea = 376 Box = 47 PL)

    - 販売注文明細行 2:

        - **品目番号:** *A0002*
        - **数量:** *9016*
        - **出荷単位 :** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > ここで扱っている項目や数量はあくまでも一例です。 前述の手順で定義した出荷単位のシーケンス グループを使用し、*ea* から *Box* および *PL* への適切な単位変換を定義し、倉庫 *62* に在庫がある必要があります。 詳細については、[測定単位と在庫のポリシー](unit-measure-stocking-policies.md)を参照してください。

1. 販売注文明細行 1 を選択します。 続いて、**在庫** メニューの **販売注文明細行** セクションで、**引当** を選択します。
1. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。
1. 販売注文明細行 2 については、手順 4 と 5 を繰り返します。
1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    以下のイベントが発生します :

    - システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。 ラベルのレイアウトはラベル フォーマットの定義に使用され、ラベル テンプレートで選択されたプリンタで印刷されるラベルとなります。
    - ウェーブ ラベルが生成され、印刷されます。 ラベルの数は、カートンの数と等しくなります (この例では、1 行目の 376 ボックスラベルと 2 行目の 322 ボックスラベル)。
    - 出荷に対して新たな船荷証券 ID が生成されます。 シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。 

次のページから、ウェーブ ラベルを表示および再印刷できます。 各ページのアクション ペインにある **出荷** タブの **関連情報** グループで、**ウェーブ ラベル** を選択します。

- すべての出荷 \> 出荷詳細
- すべての貨物 \> 貨物の詳細
- すべてのウェーブ
- ウェーブ ラベル
- ウェーブ ラベル履歴

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>シナリオ 2 : コンテナ化に使用するウェーブ ラベル印刷 (ウェーブ ラベル レコードなし)

このシナリオでは、コンテナ化を利用して品目を自動的にカートンに分割し、ウェーブ ラベルのレコードが必要とされない場合に、ウェーブ ラベルを印刷することができます。 この場合、コンテナー IDは、SSCC のプレースホルダーとして機能します。

このシナリオとシナリオ 1 の主な相違点は次のとおりです :

- **ウェーブ ラベル テンプレート :** ウェーブ ラベル テンプレートでウェーブ ラベルのタイプを選択する必要はなく、ラベル ビルドのグループ化も必要ありません。 それ以外の場合は、シナリオ1での解説と同じ方法で、ウェーブ ラベル テンプレートを構成し、ウェーブ テンプレートにリンクします。 ウェーブ ラベルが生成されないようにするには、ウェーブ ラベル タイプを空白のままにしておく必要があります。
- **ウェーブ ラベル レイアウト :** ウェーブ ラベル レコードではなく、作業明細行のウェーブ ラベル レイアウト行を構成します。 ラベル レイアウトの行設定は、**WHSWorkLine** テーブルではなく、**WHSWaveLabel** テーブルを使用して設定する必要があります。 **ページあたりの行数** 設定は、ボディ セクションに含まれる行数を制御します。 

この構成は、複数の異なるアイテムを1つのラベル付きボックスやパレットに梱包する業務シナリオにも適しており、この梱包プロセスは作業を作成することで定義できます (例 : 出荷ごとにグループ化された作業など)。

このシナリオでは、エンドツーエンドのフローを説明します。

### <a name="make-demo-data-available"></a>デモ データを有効化する

このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。

### <a name="make-sure-that-the-wave-label-method-is-available"></a>ウェーブ ラベルのメソッドが使用可能であることを確認します

場合によっては、ウェーブ ラベルの印刷メソッドを利用するには、ウェーブ プロセスのメソッドを再生成する必要があります。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。
1. **WaveLabelPrinting** がリストに含まれていることを確認します。 表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。

### <a name="set-up-a-wave-template"></a>ウェーブ テンプレートの設定

ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。
1. **63 コンテナ化** などのテンプレートを選択します。
1. **メソッド** クイックタブで、**ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。
1. **選択したメソッド** 列で、**ウェーブ ラベルの印刷** メソッドを選択し、**ウェーブ ステップ コード** フィールドを *PrintLabel* に設定します。 ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。

### <a name="create-a-wave-label-layout"></a>ウェーブ ラベルのレイアウトを作成する

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。
1. 以下の設定をしたレコードを作成します:

    - **ラベルのレイアウト ID :** *カートン*
    - **説明 :** *カートン (SSCC)*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**ウェーブ ラベル行の設定** を選択します。

    **ウェーブ ラベル行の設定** ページが表示されます。 ここでは、ラベルの動的な部分を構成できます。

1. 以下の設定を持つ行を追加します :

    - **行 Id:** *WorkLine*
    - **行テーブル名 :** *WHSWorkLine*
    - **行の開始位置 :** *500*

        このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。

    - **行の高さ :** *-50*

        このフィールドは、各行の高さを定義します。 行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。

    - **ページごとの行数 :** *5*

        このフィールドでは、各ラベルに印刷できる行の数を定義します。

        > [!NOTE]
        > この設定により、作業ごとに複数の ZPL ラベルが印刷され、各ページには最大5行までの作業明細行を保存できます。 たとえば、12行のコンテナーに対してラベルを印刷すると、3部のラベルが印刷されます。 ピッキング ラインごとに個別のラベルを印刷する場合は、この値を *1* に設定してください。

1. ページを閉じます。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *作業タイプ*
    - **基準:** *ピッキング*

1. 船荷証券 ID を印刷できるようにするには、**結合** タブで **作業ライン** テーブルを選択し、**出荷** テーブルを結合します。
1. クエリ エディター ダイアログボックスを閉じます。
1. **印刷テキストレイアウト** クイック タブには、**ヘッダー セクション**、**ボディ セクション**、**フッター セクション** の3つのセクションがあります。 **ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。 たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. **ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > この設定では、ラベルを1部ずつ印刷します。 さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。 たとえば、各ラベルを4部印刷するには、**\^PQ4** を指定します。

以上でラベルを使用する準備が整いました。

### <a name="create-a-wave-label-template"></a>ウェーブ ラベルのテンプレートを作成する

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。
1. ウェーブ レベル テンプレートを追加し、ヘッダーに以下の値を設定します :

    - **ラベル テンプレート名 :** *コンテナー ラベル*
    - **説明 :** *コンテナー ラベル*
    - **ウェーブ ステップ コード :** *PrintLabel*
    - **倉庫:** *63*

1. **ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :

    - **ラベルのレイアウト ID :** *コンテナー*
    - **プリンター名** 適切な ZPL プリンターを選択します。
    - **クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。

1. アクション ウィンドウで、**保存** を選択します。
1. オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。 **ウェーブ ラベル テンプレートの詳細** クイックタブで、**クエリの編集** を選択します。 続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **テーブル:** *出荷*
    - **派生テーブル:** *出荷*
    - **フィールド :** *アカウント番号*
    - **条件 :** 関連する顧客アカウント番号を入力します。

    完了後は、**OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。

### <a name="configure-number-sequence-extensions"></a>シーケンス番号の拡張機能を構成する

シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。 この構成は、こののシナリオでは任意となります。 詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>販売注文を作成して倉庫にリリースする

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。
1. 以下の設定で販売注文を作成します:

    - **顧客アカウント:** *US-001*
    - **倉庫:** *63*

1. 販売注文明細行を5行追加します :

    - 販売注文明細行 1:

        - **品目番号:** *A0001*
        - **数量:** *10*

    - 販売注文明細行 2:

        - **品目番号:** *A0002*
        - **数量:** *20*

    - 販売注文明細行 3:

        - **品目番号:** *L0006*
        - **数量:** *20*

    - 販売注文明細行 4:

        - **品目番号:** *L0100*
        - **数量:** *40*

    - 販売注文明細行 5:

        - **品目番号:** *L0101*
        - **数量:** *50*

    > [!NOTE]
    > ここで扱っている項目や数量はあくまでも一例です。 これらには、指定された倉庫の在庫が含まれている必要があります。

1. 販売注文明細行 1 を選択します。 続いて、**在庫** メニューの **販売注文明細行** セクションで、**引当** を選択します。
1. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。
1. 追加の販売注文明細行については、手順 4 と 5 を繰り返します。
1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    以下のイベントが発生します :

    - システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。 ラベルのレイアウトは、ラベル フォーマットの定義に使用され、結果として 5つの行を含むのラベルとなり、ラベル テンプレートで選択したプリンタで印刷されます。
    - 出荷に対して新たな船荷証券 ID が生成されます。 シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。 

これらのウェーブ ラベルを再印刷するには、**倉庫管理 \> 照会とレポート \> ウェーブラベル履歴** に移動します。

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>シナリオ 3 : 複数層のラベルのウェーブ ラベル印刷

このシナリオでは、倉庫管理プロセスで複数の階層階層の出荷ラベルが必要な場合の、ウェーブ ラベル印刷機能の使用方法を解説します。 たとえば、カートンとパレットに対して別々のラベルの印刷を行い、改ラベルを出荷全体で印刷する必要がある場合があります。 改ラベルとは、出荷 ID のラベルやバーコードなどの、ロールとコンテナーの間の仕切りとして使用できるセパレート タイプのラベルを意味し、印刷後のラベルの仕分けが簡単になります。

このシナリオとシナリオ１における構成の主な相違点は、改ラベルが有効になっていることを除いて、複数のウェーブ ラベル タイプをウェーブ ラベル テンプレートと出荷単位シーケンス グループ ラインに関連付ける必要があるという点です。 この構成を実行するには、このシナリオで次の要素を設定します :

- **ウェーブの処理方法 :** ウェーブ ラベル メソッドを「繰り返し可能」に設定し、ウェーブのテンプレートに2回以上 (またはそれ以上) を追加し、異なるウェーブのステップ コードを設定します。
- **ウェーブ ラベル テンプレート :** ウェーブ ラベルのテンプレートを設定し、ウェーブ テンプレートとリンクさせます。 それぞれのウェーブ ラベル テンプレートには、独自のウェーブ ラベル タイプがあります。
- **ウェーブ ラベル レイアウト :** 複数のウェーブ ラベル レイアウトを作成します。 ラベルの「層」ごとに独立したラベル レイアウトがあり、ラベル破断のレイアウトも用意されています。

このシナリオでは、エンドツーエンドのフローを説明します。

### <a name="make-demo-data-available"></a>デモ データを有効化する

このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。

### <a name="set-up-a-wave-process-method"></a>ウェーブ プロセス メソッドの設定

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。
1. **WaveLabelPrinting** がリストに含まれていることを確認します。 表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。
1. **waveLabelPrinting** メソッドに、 **メソッドを繰り返し可能にする** チェックボックスを選択します。

### <a name="set-up-a-wave-template"></a>ウェーブ テンプレートの設定

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。
2. **62 出荷の既定** などのテンプレートを選択します。
3. **メソッド** クイックタブで、**ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。
4. **選択した方法** 列で、*カートン* などの **ウェーブ ステップ コード** 値を **ウェーブ ラベルの印刷** メソッドに割り当てます。 ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。
5. **ウェーブ ラベルの印刷** メソッドを再度 **選択したメソッド** 列に移動します。
6. **選択されたメソッド** の列で、2 番目の **ウェーブ ラベルの印刷** メソッドに、*パレット* などの別の **ウェーブ ステップ コード** の値を割り当てます。 ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。

### <a name="create-three-wave-label-layouts"></a>3 つのウェーブ ラベルのレイアウトを作成する

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。
1. 以下の設定をしたレコードを作成します:

    - **ラベルのレイアウト ID :** *カートン*
    - **説明 :** *カートン (SSCC)*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**ウェーブ ラベル行の設定** を選択します。

    **ウェーブ ラベル行の設定** ページが表示されます。 ここでは、ラベルの動的な部分を構成できます。

1. 以下の設定を持つ行を追加します :

    - **行 Id:** *WaveLabel*
    - **行テーブル名 :** *WHSWaveLabel*
    - **行の開始位置 :** *0*

        このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。

    - **行の高さ :** *0*

        このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。 行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。 この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。

    - **ページごとの行数 :** *1*

        このフィールドでは、各ラベルに印刷できる行の数を定義します。

        > [!NOTE]
        > この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。

1. ページを閉じます。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *作業タイプ*
    - **基準:** *ピッキング*

    このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。

1. 船荷証券 ID を印刷できるようにするには、**結合** タブで **作業ライン** テーブルを選択し、**出荷** テーブルを結合します。 
1. クエリ エディター ダイアログボックスを閉じます。
1. **印刷テキストレイアウト** クイック タブには、**ヘッダー セクション**、**ボディ セクション**、**フッター セクション** の3つのセクションがあります。 **ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。 たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > この設定では、ラベルを1部ずつ印刷します。 さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。 たとえば、各ラベルを4部印刷するには、**\^PQ4** を指定します。

1. 1番目のラベルを使用する準備が整いました。
1. 以下の設定を持つ 2 番目のレイアウト レコードを作成します :

    - **ラベルのレイアウト ID :** *パレット*
    - **説明 :** *パレット*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**ウェーブ ラベル行の設定** を選択します。

    **ウェーブ ラベル行の設定** ページが表示されます。 ここでは、ラベルの動的な部分を構成できます。

1. 以下の設定を持つ行を追加します :

    - **行 Id:** *WaveLabel*
    - **行テーブル名 :** *WHSWaveLabel*
    - **行の開始位置 :** *0*

        このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。

    - **行の高さ :** *0*

        このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。 行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。 この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。

    - **ページごとの行数 :** *1*

        このフィールドでは、各ラベルに印刷できる行の数を定義します。

        > [!NOTE]
        > この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。

1. ページを閉じます。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *作業タイプ*
    - **基準:** *ピッキング*

    このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。

1. 船荷証券 ID を印刷できるようにするには、**結合** タブで **作業ライン** テーブルを選択し、**出荷** テーブルを結合します。
1. クエリ エディター ダイアログボックスを閉じます。
1. **印刷テキストレイアウト** クイック タブには、**ヘッダー セクション**、**ボディ セクション**、**フッター セクション** の3つのセクションがあります。 **ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。 たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. **ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > この設定では、ラベルを1部ずつ印刷します。 さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。 たとえば、各ラベルを4部印刷するには、**\^PQ4** を指定します。

1. 2番目のラベルを使用する準備が整いました。
1. 以下の設定を持つ 3 番目のレイアウト レコードを作成します :

    - **ラベルのレイアウト ID :** *ブレイク*
    - **説明 :** *改ラベル*

1. アクション ウィンドウで、**保存** を選択します。
1. **印刷テキストレイアウト** クイック タブには、**ヘッダー セクション**、**ボディ セクション**、**フッター セクション** の3つのセクションがあります。 **ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーの ZPL コードを入力します。 次に例を示します。

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. 今回は、ボディは必要ありません。 そのため、**フッター セクション** セクションに必要なテキストを入力するだけです。 次に例を示します。

    ```plaintext
    ^XZ
    ```

    3番目のラベルを使用する準備が整いました。

    > [!NOTE]
    > この 3 番目のラベルは、ラベル ロール間の区切り線として使用される改ラベルです。

### <a name="create-two-wave-label-types"></a>2 つのウェーブ ラベル タイプを作成する

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル タイプ** に移動します。
1. 以下の設定をしたレコードを作成します:

    - **ラベル タイプ :** *カートン*
    - **説明 :** *カートン*

1. 以下の設定を持つ 2 番目のレコードを作成します :

    - **ラベルタイプ :** *パレット*
    - **説明 :** *パレット*

### <a name="set-up-unit-sequence-groups"></a>単位順序グループを設定します

1. **倉庫管理 \> 設定 \> 倉庫 \> 出荷単位の順序グループ** に移動します。
1. **Ea Box PL** グループを選択、または作成します。
1. **ボックス** 明細行では 、**ウェーブ レベル タイプ** フィールドに *カートン* を設定します。
1. **PL** 明細行では 、**ウェーブ レベル タイプ** フィールドに *パレット* を設定します。

### <a name="create-wave-label-templates"></a>ウェーブ ラベルのテンプレートを作成する

1. **倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。
1. 以下の設定を持つラベル テンプレートを作成します :

    - **ラベル テンプレート名 :** *カートン ラベル*
    - **説明 :** *カートン ラベル*
    - **ウェーブ ステップ コード :** *カートン*
    - **倉庫:** *62*

1. **一般** クイック タブの **ウェーブ ラベル タイプ** フィールドで、*カートン* などの値を選択します。
1. **ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :

    - **ラベルのレイアウト ID :** *カートン*
    - **プリンター名** 適切な ZPL プリンターを選択します。
    - **クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。

1. アクション ウィンドウで、**保存** を選択します。
1. オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。 **ウェーブ ラベル テンプレートの詳細** クイックタブで、**クエリの編集** を選択します。 続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **テーブル:** *出荷*
    - **派生テーブル:** *出荷*
    - **フィールド :** *アカウント番号*
    - **条件 :** 関連する顧客アカウント番号を入力します。

    完了後は、**OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。

1. アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。
1. クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド :** *参照読み込み行の Id (レコード ID)*
    - **検索の方法:** *昇順*

1. 以下の設定を持つ2つ目の行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *出荷 ID*
    - **検索の方法:** *昇順*

1. **OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。
1. グループのリセット操作の確認を促すメッセージ ボックスが表示されます。 **はい** を選択して続行します。
1. アクション ウィンドウで、**ウェーブ ラベル テンプレート グループ** を選択します。
1. **ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、**参照フィールド名** フィールドが *出荷 ID* に設定されている行では、以下の値を設定します :

    - **改ラベルの印刷 :** このチェックボックスをオンにします。
    - **ラベルのレイアウト ID :** 改ラベルを選択します。 (たとえば、このシナリオで既に作成した *改ラベル* のレイアウトを作成します。)
    - **プリンター名 :** 改ラベルで使用するプリンターを選択します。 (通常、ラベル ロールを分割する目的で、**ウェーブ ラベル テンプレートの詳細** クイックタブで選択されているものと同じプリンタを選択する必要があります。 しかし、他のシナリオにも適用可能です。)

1. **参照フィールド名** フィールドが、*参照積荷行 ID*  に設定されている行では、**ラベルビルド ID** チェックボックスを選択します。

    > [!NOTE]
    > この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。 このラベル シーケンスは、ラベル レイアウトに印刷することができます。 また、異なる出荷のラベルは、選択された改ラベルで区切られます。

1. **OK** を選択して、**ウェーブ ラベル テンプレート グループ** ダイアログ ボックスを閉じます。
1. 以下の設定を持つ 2 つ目のラベル テンプレートを作成します :

    - **ラベル テンプレート名 :** *パレット ラベル*
    - **説明 :** *パレット ラベル*
    - **ウェーブ ステップ コード :** *パレット*
    - **倉庫:** *62*

1. **一般** クイック タブの **ウェーブ ラベル タイプ** フィールドで、*パレット* などの値を選択します。
1. **ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :

    - **ラベルのレイアウト ID :** *パレット*
    - **プリンター名** 適切な ZPL プリンターを選択します。
    - **クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。

1. アクション ウィンドウで、**保存** を選択します。
1. オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。 **ウェーブ ラベル テンプレートの詳細** クイックタブで、**クエリの編集** を選択します。 続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :

    - **テーブル:** *出荷*
    - **派生テーブル:** *出荷*
    - **フィールド :** *アカウント番号*
    - **条件 :** 関連する顧客アカウント番号を入力します。

    完了後は、**OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。 

1. アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。
1. クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド :** *参照読み込み行の Id (レコード ID)*
    - **検索の方法:** *昇順*

1. 以下の設定を持つ2つ目の行を追加します :

    - **表:** *作業明細行*
    - **派生テーブル:** *作業明細行*
    - **フィールド:** *出荷 ID*
    - **検索の方法:** *昇順*

1. **OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。
1. グループのリセット操作の確認を促すメッセージ ボックスが表示されます。 **はい** を選択して続行します。
1. アクション ウィンドウで、**ウェーブ ラベル テンプレート グループ** を選択します。
1. **ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、**参照フィールド名** フィールドが *出荷 ID* に設定されている行では、以下の値を設定します :

    - **改ラベルの印刷 :** このチェックボックスをオンにします。
    - **ラベルのレイアウト ID :** 改ラベルを選択します。 (たとえば、このシナリオで既に作成した *改ラベル* のレイアウトを作成します。)
    - **プリンター名 :** 改ラベルで使用するプリンターを選択します。 (通常、ラベル ロールを分割する目的で、**ウェーブ ラベル テンプレートの詳細** クイックタブで選択されているものと同じプリンタを選択する必要があります。 しかし、他のシナリオにも適用可能です。)

1. **参照フィールド名** フィールドが、*参照積荷行 ID*  に設定されている行では、**ラベルビルド ID** チェックボックスを選択します。

    > [!NOTE]
    > この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。 このラベル シーケンスは、ラベル レイアウトに印刷することができます。 また、異なる出荷のラベルは、選択された改ラベルで区切られます。

### <a name="configure-number-sequence-extensions"></a>シーケンス番号の拡張機能を構成する

シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。 この構成は、こののシナリオでは任意となります。 詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>販売注文を作成して倉庫にリリースする

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。
1. 以下の設定で販売注文を作成します:

    - **顧客アカウント:** *US-001*
    - **倉庫:** *62*

1. 販売注文明細行を2行追加します :

    - 販売注文明細行 1:

        - **品目番号:** *A0001*
        - **数量:** *9024*
        - **出荷単位 :** *ea* (9024 ea = 376 Box = 47 PL)

    - 販売注文明細行 2:

        - **品目番号:** *A0002*
        - **数量:** *9016*
        - **出荷単位 :** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > ここで扱っている項目や数量はあくまでも一例です。 前述の手順で定義した出荷単位のシーケンス グループを使用し、*ea* から *Box* および *PL* への適切な単位変換を定義し、倉庫 *62* に在庫がある必要があります。 詳細については、[測定単位と在庫のポリシー](unit-measure-stocking-policies.md)を参照してください。

1. 販売注文明細行 1 を選択します。 続いて、**在庫** メニューの **販売注文明細行** セクションで、**引当** を選択します。
1. **引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。
1. 販売注文明細行 2 については、手順 4 と 5 を繰り返します。
1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

    以下のイベントが発生します : 

    - システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。 ラベルのレイアウトはラベル フォーマットの定義に使用され、ラベル テンプレートで選択されたプリンタで印刷されるラベルとなります。
    - ウェーブ ラベルが生成され、印刷されます。 ラベルの数は、カートンの数と等しくなります (例 : 1行目の 376 ボック スラベル、2行目の 322 ボックス ラベル、1行目の 47 PL ラベル、2行目の 47 PLラベル、出荷 ID を持つ2つの改ラベル) 。
    - 出荷に対して新たな船荷証券 ID が生成されます。 シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。 

以下のページでは、ウェーブ ラベルを表示、再印刷ができます :

- すべての出荷 \> 出荷詳細
- すべての貨物 \> 貨物の詳細
- すべてのウェーブ
- ウェーブ ラベル
- ウェーブ ラベル履歴

これらのほとんどのページでは、アクションウィンドウの **出荷** タブにある **関連情報** グループの **ウェーブラベル** を選択することにより、関連する機能を見つけることができます。

## <a name="additional-resources"></a>追加リソース

- [ウェーブ ラベルの再印刷と無効化](reprint-and-void-wave-labels.md)
- [サイクル中にサイクル ラベルの印刷をスケジュールする](configure-task-based-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
