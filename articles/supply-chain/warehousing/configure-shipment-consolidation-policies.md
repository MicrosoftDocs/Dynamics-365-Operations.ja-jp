---
title: 出荷連結ポリシーを構成する
description: このトピックでは、既定およびユーザー定義の出荷連結ポリシーの設定方法について説明します。
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 03150ccdaeaf48754f04a4329cb1bc14ea2b6895
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840416"
---
# <a name="configure-shipment-consolidation-policies"></a>出荷連結ポリシーを構成する

[!include [banner](../includes/banner.md)]

出荷連結ポリシーを使用した出荷連結のプロセスを使用することで、倉庫への自動リリースと手動リリースの処理にて自動出荷連結が可能となります。 この機能を有効にした後は、初期ポリシーを構成する必要があります。 ポリシーが構成されていない場合は、販売明細行ごとに1つの積荷明細行を持つ個別の出荷が生成されます。

このトピックで説明するシナリオでは、既定およびユーザー定義の出荷連結ポリシーを設定する方法を示します。

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>出荷連結ポリシーの機能を有効化する

> [!IMPORTANT]
> このトピックで説明する[最初のシナリオ](#scenario-1)では、まず以前の出荷連結機能を使用するよう、倉庫の設定をします。 続いて、出荷統合ポリシーを使用できるようにします。 このようにして、アップグレード シナリオの機能を体験できます。 デモ データ環境を使用して最初のシナリオを実行する場合は、この機能を有効にしてからシナリオを開始する必要があります。

*出荷連結ポリシー* 機能を使用する前に 、システムでこの機能を有効にしておく必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *倉庫管理*
- **機能名:** *出荷連結*

## <a name="make-demo-data-available"></a>デモ データを有効化する

それぞれのトピックのシナリオでは、Microsoft Dynamics 365 Supply Chain Management で利用可能な標準的なデモデータに含まれる値とレコードを参照し ます。 ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>シナリオ1:既定の出荷連結ポリシーを構成する

*出荷連結ポリシー* 機能を有効にした後に、最低限の既定のポリシーを構成する必要がある場合には、次の2つの状況が想定されます。

- 既にデータが格納されている環境をアップグレードしている。
- 全く新しい環境を設定している。

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>クロス オーダー連結用に構成されている倉庫の環境をアップグレードする

この手順を開始する、基本的なクロスオーダー連結の機能が既に使用されている環境をシミュレートするには、*出荷連結ポリシー* 機能を無効にする必要があります。 続いて、機能管理を使用してこの機能を有効化することで、アップグレード後に出荷連結ポリシーを設定する方法を身につけることができます。

クロスオーダー連結の使用が既に構成されている倉庫環境で、既定の出荷連結ポリシーを設定するには、次の手順に従います。

1. **倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。
1. 一覧から、目的の倉庫レコードを検索して開きます (例:**USMF** デモデータ内倉庫 *24*)。
1. アクション ウィンドウで、**編集** を選択します。
1. **倉庫** のクイックタブで、 **倉庫にリリースする出荷を連結する** オプションを *はい* に設定し ます。
1. 連結が必要となるその他すべての倉庫に対して、手順 2 から 手順 4 を繰り返します。
1. ページを閉じます。
1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*出荷連結ポリシー* 機能を有効化します。 **機能管理** ワークスペースでは、この機能は *出荷連結* と呼ばれ ます。
1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。 機能の有効化後は、新しい **出荷連結ポリシー** メニュー項目を表示するには、ブラウザーの更新が必要となる場合があります。
1. アクション ウィンドウで、**既定の設定の作成** を選択して次のポリシーを作成します:

    - ポリシータイプ *販売注文* で使用する **クロスオーダー** のポリシー (以前の連結機能を使用するように設定している倉庫が少なくとも1つ存在する場合)
    - ポリシータイプ *販売注文* で使用する **既定** のポリシー
    - ポリシータイプ *移管の問題* で使用する **既定** のポリシー
    - ポリシータイプ *移管の問題* で使用する **クロスオーダー** のポリシー (以前の連結機能を使用するように設定している倉庫が少なくとも1つ存在する場合)

    > [!NOTE]
    > - いずれの **クロスオーダー ポリシー** も、注文番号のフィールドを除いて、以前のロジックと同じフィールドのセットを考慮します。 (このフィールドは、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)
    > - いずれの **既定** のポリシーも、注文番号のフィールドを含め、以前のロジックと同じフィールドのセットを考慮します。 (このフィールドは、注文番号、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)

1. ポリシータイプ *販売注文* が使用する **クロスオーダー** ポリシーを選択し、続いてアクション ウィンドウで **クエリの編集** を選択します。
1. [クエリの編集] ダイアログボックスで、**倉庫にリリースする出荷を連結する** オプションが *はい* に設定されている倉庫が一覧表示されます。 そのため、これらはクエリに含まれます。

### <a name="create-default-policies-for-a-new-environment"></a>新規環境で使用する既定のポリシーの作成

次の手順に従って、新規環境における既定の出荷連結ポリシーを設定します。

1. [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して、*出荷連結ポリシー* 機能を有効化します (まだ有効化していない場合)。 **機能管理** ワークスペースでは、この機能は *出荷連結* と呼ばれ ます。
1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. アクション ウィンドウで、**既定の設定の作成** を選択して次のポリシーを作成します:

    - ポリシータイプ *販売注文* で使用する **既定** のポリシー
    - ポリシータイプ *移管の問題* で使用する **既定** のポリシー

    > [!NOTE]
    > いずれの **既定** のポリシーも、注文番号のフィールドを含め、以前のロジックと同じフィールドのセットを考慮します。 (このフィールドは、注文番号、倉庫、輸送モード、住所などの要因に基づいて明細行を出荷に統合する目的で使用されます。)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>シナリオ 2: ユーザー定義の出荷連結ポリシーを構成する

このシナリオでは、ユーザー定義の出荷連結ポリシーを設定する方法を示します。 ユーザー定義のポリシーでは、出荷連結が複数の条件に基づいている場合であっても、複雑な業務要件に対応できます。 このシナリオ後半であつかう各ポリシーの例には、ビジネス ケースの簡単な説明が含まれています。 これらのサンプル ポリシーは、ピラミッド型のクエリの評価を確実に実行するような順序で設定する必要があります。 (つまり、最も条件が揃っている政策を優先的に評価する必要があります。)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>機能を有効化して、このシナリオで使用するマスター データを準備する

このシナリオの演習を行う前に、次のサブセクションで説明するとおり、機能を有効にして、フィルタ処理を行うために必要となるマスターデータを準備する必要があります。 (これら前提条件は、[出荷連結ポリシーの使用方法のシナリオ例](#example-scenarios)に記載されているシナリオにも適用されます。)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>機能を有効にして既定のポリシーを作成する

機能管理を使用してこの機能を有効化し (まだ有効化していない場合)、[シナリオ 1](#scenario-1)に記載されている既定の連結ポリシーを作成します。

#### <a name="create-two-new-product-filter-codes"></a>2 つの新しい製品フィルター コードを作成する

1. **倉庫管理 \> 設定 \> 製品フィルター \>  製品フィルター** に移動し、2つの製品フィルターを追加します:

    - 製品フィルター 1:

        - **フィルターコード :** *可燃性*
        - **フィルタータイトル :** *コード 4*

    - 製品フィルター 2:

        - **フィルターコード :** *爆発性*
        - **フィルタータイトル :** *コード 4*

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 品目番号 *M9200* の製品を開きます。 (選択する製品は、高度な \[WMS\] 処理が有効化されている必要があり、この製品は **USMF** のデモ データのWMSに対応しています。)
1. **倉庫** のクイックタブで、**コード 4** フィールドを *可燃性* に設定 します。
1. ページを閉じます。
1. 品目番号 *M9201* の製品を開きます。 (この製品は、**USMF** デモデータ内の WMS のプロセスにも対応しています。)
1. **倉庫** のクイックタブで、**コード 4** フィールドを *爆発性* に設定 します。
1. ページを閉じます。

#### <a name="create-a-new-transportation-mode-of-delivery"></a>新規配送モードを作成する

1. **輸送管理 \> 設定 \> 配送業者 \> 方式** に移動します。
1. 連結クエリでで使用する輸送モードを作成し、*航空路* と名付けます。
1. **輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。
1. 配送業者を作成し、以下の設定を行います:

    - **配送業者 :** *航空路*
    - **名前 :** *航空路*
    - **モード :** *航空路*

1. 新たな配送業者の **サービス** クイックタブで、次の設定を含む行を追加します:

    - **配送サービス :** *Air*
    - **輸送方法 :** *Air*

1. アクション ウィンドウで、**保存** を選択します。

    > [!NOTE]
    > 新たな配送業者を保存すると、新たな行の **サービス** グリッドの **荷渡方法** フィールドが自動的に *Airwa-Air* に設定されます。 *Airwa-Air* モードで販売注文を使用する場合は 、関連する出荷に対しては輸送モード *航空路* が使用されます。

#### <a name="create-an-order-pool"></a>オーダー プールの作成

1. **販売とマーケティング \> 設定\> 販売注文 \>オ ーダープール** に移動します。
1. 連結クエリで使用する注文管理グループを作成します。 このオーダー プールには、次の設定が必要となります :

    - **プール :** 他のプールで使用されていない整数を入力します。
    - **名前 :** *ShipCons*

1. **販売とマーケティング \> 顧客 \> すべての顧客** に移動します。
1. 顧客番号 *US-003* の顧客を開きます。
1. **販売注文の既定の設定** クイックタブで、**販売注文のオーダープール** フィールドを、作成した注文管理グループに設定します。
1. ページを閉じ、顧客番号 *US-004* の顧客に対して、手順 4 と 手順 5 を繰り返します。

### <a name="create-example-policy-1"></a>ポリシー例 1 を作成する

この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客 + モード* を作成します :

- このポリシーでは、顧客アカウント (*US-001*) と荷渡方法 (*Airwa-Air*) を照会します。
- 未出荷に対する連結をオフにします。
- 連結は注文 ID ごとに行われます。 (つまり、注文や倉庫などにおける出荷ごとに別の出荷が存在することになります。)

このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:

    - **ポリシー名 :** *CustomerMode*
    - **ポリシーの説明 :** *顧客アカウントと荷渡方法*

1. **未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。
1. アクション ウィンドウで、**保存** を選択します。
1. **連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. [クエリの編集] ダイアログ ボックスのグリッド内の **範囲** タブで、**フィールド** のフィールドが、*顧客アカウント* に設定されている行を探し、その行の **基準** フィールドを *US-001* に設定し ます。
1. **追加** を選択して、グリッドに以下の設定を持つ行を追加します:

    - **テーブル :** *注文明細行*
    - **派生テーブル :** *注文明細行*
    - **フィールド :** *荷渡方法*
    - **基準 :** *Airwa-Air*

1. **OK** を選択してダイアログ ボックスを閉じます。

> [!NOTE]
> このビジネス ケースでは、荷渡方法に *Airwa-Air* を利用している顧客 *US-001* の注文ラインが、注文をまたいで連結されることはありません。 このポリシーは、この顧客に対して他のすべての荷渡方法の出荷が連結されている場合に、順序どおりに使用されることを意図しています。

### <a name="create-example-policy-2"></a>ポリシー例 2 を作成する

この例では、以下のビジネス ケースにて使用可能なポリシー、*危険物* を作成します :

- このポリシーでは、フィルターコード (*危険物*) と荷渡方法 (*Airwa-Air*) を照会します。
- 未出荷に対する連結をオンにします。
- 連結は複数の注文を横断して行われます。 (アカウント、倉庫などには別々の出荷がありますが、クエリで指定された品目グループ内でのみ出荷されます。)

このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:

    - **ポリシー名 :** *品目のタイプ*
    - **ポリシーの説明 :** *複数の注文間で同じタイプの品目を統合します*

1. **未処理の出荷を含む連結** オプションは、 *はい* に設定します。
1. アクション ウィンドウで、**保存** を選択します。
1. **連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. [クエリの編集] ダイアログボックスの **結合** タブで、ツリー **テーブル \> 積荷の詳細** を展開して選択します。
1. **結合するテーブルの追加** を選択します。
1. 表示されたリレーション グリッドで、**関係性** フィールドが *倉庫品目番号 (品目番号)* に設定されている行を探して選択し、**選択** を選択します。 
1. **範囲** タブで、 **追加** を選択して、グリッドに以下の設定を持つ行を追加します:

    - **テーブル :** *倉庫の品目番号*
    - **派生テーブル :** *倉庫の品目番号*
    - **フィールド :** *コード4*
    - **基準 :** *可燃性*

1. **OK** を選択してダイアログ ボックスを閉じます。

> [!NOTE]
> このビジネス ケースでは、品目に特定のフィルターコードを含むすべての注文明細行 (つまり、**code 4** フィールドが *可燃性* に設定されているフィルターコード ) は、複数の注文間で同じタイプの他の品目と統合されます。 同じアカウント、倉庫、品目グループが未出荷である場合は、新たな明細行が関連付けられます。

### <a name="create-example-policy-3"></a>ポリシー例 3 を作成する

この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客要求* を作成します :

- このポリシーでは、特定の顧客アカウントを照会します。
- 未出荷に対する連結をオンにします。
- 連結は複数の注文間で行われますが、これは顧客の要求に基づいて行われます。 (複数の注文が、同じ顧客要求番号と倉庫に基づいて出荷にグループ化されます。)

このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:

    - **ポリシー名 :** *CustomerOrderNo*
    - **ポリシーの説明 :** *顧客の PO に基づいて明細行を連結する*

1. **未処理の出荷を含む連結** オプションは、 *はい* に設定します。
1. アクション ウィンドウで、**保存** を選択します。
1. **連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *顧客の要求* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. **残りのフィールド** の一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. [クエリの編集] ダイアログ ボックスの **範囲** タブで、**フィールド** のフィールドが、*顧客アカウント* に設定されている行を探し、その行の **基準** フィールドを *US-001* に設定し ます。
1. **OK** を選択してダイアログ ボックスを閉じます。

> [!NOTE]
> このビジネス ケースでは、販売注文にて同じ顧客要求番号を持つすべての注文明細行が、販売注文番号に関係なく、1つの出荷に連結されます。 (顧客要求番号は顧客の発注書の \[PO\]番号として使用されます。) 同一のアカウント、倉庫、顧客要求で未処理の出荷がある場合は、新たな明細行が関連付けられます。 このポリシーは、顧客が1日の内に同一の PO 番号を含む追加の注文明細行を複数回送信し、すべての明細行を 1 つの出荷にグループ化する場合に使用できます。 (例としては、単一の船荷証券と単一の梱包明細がある場合が考えられます。)

### <a name="create-example-policy-4"></a>ポリシー例 4 を作成する

この例では、以下のビジネス ケースにて使用可能なポリシー、*顧客が許可する連結* を作成します :

- このポリシーでは、特定のオーダープールにクエリを実行して、連結出荷を承認する顧客を識別します。
- 未出荷に対する連結をオフにします。
- 連結は、既定の連結注文ポリシーで選択されたフィールドを使用して、 (**倉庫へのリリースで出荷を連結する** チェック ボックスを複製する目的で) 複数の注文間で行われます。

- 別のオーダー プールを選択することで、販売注文のルールを上書きできます。

このビジネス ケースに対して、出荷連結ポリシーを作成するには、次の手順に従います。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:

    - **ポリシー名 :** *オーダー プール*
    - **ポリシーの説明 :** *オーダー プールに基づいて複数の注文を連結します*

1. **未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。
1. アクション ウィンドウで、**保存** を選択します。
1. **連結フィールド** クイックタブの **残りのフィールド** ボックスの一覧で、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. [クエリの編集] ダイアログ ボックスの **範囲** タブで、**追加** を選択して、グリッドに次の設定を持つ行を追加します:

    - **テーブル:** *販売注文*
    - **派生テーブル:** *販売注文*
    - **フィールド :** *プール*
    - **基準 :** *ShipCons*

1. **OK** を選択してダイアログ ボックスを閉じます。

> [!NOTE]
> このビジネス ケースでは、販売注文が同じオーダー プールに属するすべての注文明細行が、同一のアカウント、倉庫、荷渡方法が使用する販売注文を通じて 1 つの出荷に連結されます。 オーダー プールの代わりに、その他の任意のフィールドを使用して顧客のグループを識別し、既定の販売注文ヘッダーを使用することができます。 これは、倉庫ではなく顧客が連結の必要性を推進している場合に使用できます。 (これまでの連結ロジックでは、倉庫が連結の必要性を推進していました。)

### <a name="create-example-policy-5"></a>ポリシー例 5 を作成する

この例では、以下のビジネス ケースにて使用可能なポリシー、*倉庫が許可する連結* を作成します :

- このポリシーでは、特定のオーダープールにクエリを実行して、連結出荷が可能な倉庫を識別します。
- 未出荷に対する連結をオフにします。
- 連結は、既定の連結注文ポリシーで選択されたフィールドを使用して、 (**倉庫へのリリースで出荷を連結する** チェック ボックスを複製する目的で) 複数の注文間で行われます。

通常、このビジネスケースでは、 [シナリオ 1](#scenario-1)で作成した既定のポリシーを使用して対処することができます。 ただし、以下の手順で同様のポリシーを手動で作成することも可能です。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. アクション ウィンドウで、**新規** を選択し、次の設定を持つポリシーを作成します:

    - **ポリシー名 :** *クロス オーダー*
    - **ポリシーの説明 :** *特定の倉庫のクロス オーダー連結*

1. **未処理の出荷を含む連結** オプションは、 *いいえ* のままにします。
1. アクション ウィンドウで、**保存** を選択します。
1. **連結フィールド** クイックタブの **残りのフィールド** フィールドで、 **フィールド名** フィールドが *荷渡方法* に設定されている行を選択します。
1. **追加** ボタンの![右矢印](media/forward-button.png)を選択して、フィールドを **選択したフィールド** 一覧に移動します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. [クエリの編集] ダイアログ ボックスの **範囲** タブで、**フィールド** のフィールドが、*倉庫* に設定されている行を探し、その行の **基準** フィールドを *61, 63* に設定し ます。
1. **OK** を選択してダイアログ ボックスを閉じます。

### <a name="set-the-order"></a>順序を設定する

以上ですべてのポリシーの作成が完了しました。続いて、ポリシーが適用される順序を決定する必要があります。 以下の手順では、条件数が最も多いポリシーの優先度を高く評価する、ピラミッド型方式の設定例を示しています。

1. **倉庫管理  \> 設定 \> 倉庫へのリリース \> 出荷統合ポリシー** に移動します。
1. **ポリシー タイプ** フィールドを *販売注文* に設定します。
1. 左の列に表示されているポリシーをそれぞれ選択し、続いてアクション ウィンドウの **上へ移動** または **下へ移動** ボタンを使用して、ポリシーを次の順序で配置します :

    1. CustomerMode
    1. 品目タイプ
    1. CustomerOrderNo
    1. 注文管理グループ
    1. クロス オーダー
    1. 既定

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a>出荷連結ポリシーの使用方法を示すシナリオ例

次のシナリオでは、このトピックで作成した出荷連結ポリシーの使用例を説明しています。 各シナリオでは、倉庫への自動リリースや手動リリース処理を行う過程で、出荷連結ポリシーを使用した出荷連結処理を行う方法を説明しています。

- シナリオ 1: [販売注文の自動リリースを使用して、出荷が倉庫にリリースされた場合に出荷を連結する](../warehousing/consolidate-shipments-automatic.md)
- シナリオ 2: [出荷連結ポリシーが、[倉庫へのリリース] ページで上書きされている場合に出荷を連結する](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- シナリオ 3 - [積荷計画ワークベンチから倉庫へのリリース機能を使用して出荷を連結する](../warehousing/consolidate-shipments-load-planning-workbench.md)
- シナリオ 4: [出荷連結ワークベンチを使用して出荷を連結する](../warehousing/consolidate-shipments-manual-workbench.md)
- シナリオ 5: [出荷連結ページを使用して出荷を手動で連結する](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>追加リソース

- [出荷連結ポリシー](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]