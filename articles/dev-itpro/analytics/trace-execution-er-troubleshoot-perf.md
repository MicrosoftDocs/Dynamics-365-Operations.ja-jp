---
title: パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行
description: このトピックでは、パフォーマンス上の問題をトラブルシューティングするために電子申告 (ER) のパフォーマンス追跡機能を使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576549"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>パフォーマンス上の問題をトラブルシューティングするため ER 形式の実行を追跡します

[!include[banner](../includes/banner.md)]

電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインするプロセスの一部として、Microsoft Dynamics 365 for Finance and Operations からデータを取得し、生成される出力に入力したりするのに使用される方法を定義します。 ER パフォーマンス追跡機能を使用すると、ER 形式の実行に関する詳細の収集や、それらを使用してパフォーマンスの問題をトラブルシューティングするのにかかる時間と費用を大幅に削減できます。 このチュートリアルでは、Finance and Operations で実行される ER 形式のパフォーマン追跡を実行する方法、およびこれらの追跡情報を使用してパフォーマンスを向上する方法についてのガイドラインを示します。

## <a name="prerequisites"></a>必要条件

このチュートリアルの例を完了するには、次のアクセスが必要です:

- 次のロールのいずれか 1 つのために Finance and Operations にアクセスします:

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

- 次のいずれかの役割で、Finance and Operations と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) のインスタンスにアクセスします。

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

次のファイルをローカルにダウンロードして保存する必要もあります。

| ファイル                                  | コンテンツ                               |
|---------------------------------------|---------------------------------------|
| model.version.1 のパフォーマンス追跡     | [ER データ モデル構成のサンプル](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| metadata.version.1 のパフォーマンス追跡  | [ER メタデータ構成のサンプル](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| mapping.version.1.1 のパフォーマンス追跡 | [ER モデル マッピング構成のサンプル](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| format.version.1.1 のパフォーマンス追跡  | [ER フォーマット構成のサンプル](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>ER パラメーターのコンフィギュレーション

Finance and Operations で生成された各 ER パフォーマンス追跡は、実行ログ レコードの添付ファイルとして保管されます。 Finance and Operations のドキュメント管理 (DM) フレームワークを使用してこれらの添付ファイルを管理します。 ER パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡を添付するのに使用する DM ドキュメント タイプを指定する必要があります。 Finance and Operation の、**電子申告**ワークスペースで、**電子申告パラメーター**を選択します。 次に、**電子申告パラメーター** ページの**添付ファイル** タブの**その他**フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。

![Finance and Operations の電子申告パラメーター ページ](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

**その他**ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを**ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。

- **クラス:** 添付ファイル
- **グループ:** ファイル

![Finance and Operations のドキュメント タイプ ページ](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> DM 添付ファイルは会社固有であるため、選択したドキュメント タイプは、現在の Finance and Operations インスタンスのすべての会社で使用可能である必要があります。

### <a name="configure-rcs-parameters"></a>RCS パラメーターのコンフィギュレーション

Finance and Operations で生成される ER パフォーマンス追跡は、ER 形式デザイナーと ER マッピング デザイナーを使用して、分析用に RCS にインポートされます。 ER パフォーマンス追跡は ER 形式に関連する実行ログ レコードの添付ファイルとして格納されるため、RCS パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡の添付に使用する DM ドキュメント タイプを指定する必要があります。 会社用にプロビジョニングされた RCS のインスタンスの、**電子申告**ワークスペースで、**電子申告パラメーター**を選択します。 次に、**電子申告パラメーター** ページの**添付ファイル** タブの**その他**フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。

![RCS の電子申告パラメーター ページ](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

**その他**ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを**ドキュメント タイプ** ページ (**組織管理 \> ドキュメント管理 \> ドキュメント タイプ**): で次のようにコンフィギュレーションする必要があります。

- **クラス:** 添付ファイル
- **グループ:** ファイル

## <a name="design-an-er-solution"></a>ER ソリューションのデザイン

仕入先トランザクションを表示する新しいレポートを生成するため、新しい ER ソリューションのデザインを開始したとします。 現時点では、選択した仕入先のトランザクションは**仕入先トランザクション** ページ (**買掛金勘定 \> 仕入先 \> すべての仕入先**に移動し、仕入先を選択してから、アクション ウィンドウの**仕入先**タブの**トランザクション** グループで、**トランザクション**を選択します) で検索できます。 ただし、XML 形式の 1 つの電子ドキュメントで、すべての仕入先トランザクションを同時に処理する必要があります。 このソリューションは、必要なデータ モデル、メタデータ、モデル マッピング、および形式コンポーネントを含むいくつかの ER コンフィギュレーションで構成されます。

1. 会社用にプロビジョニングされた RCS のインスタンスにサインインします。
2. このチュートリアルでは、サンプル会社 **Litware, Inc.** のコンフィギュレーションを作成または変更します。 そのため、このコンフィギュレーション プロバイダーが RCS に追加され、有効として選択されていることを確認してください。 手順については、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) を参照してください。
3. **電子レポート**ワークスペースで、**レポート コンフィギュレーション**タイルを選択します。
4. **構成**ページで、前提条件としてダウンロードした ER コンフィギュレーションを RCS に次の順序でインポートします: データ モデル、メタデータ、モデル マッピング、フォーマット。 各コンフィギュレーションについて、次の手順を実行します。

    1. アクション ウィンドウで、**交換 \> XML ファイルからロード**を選択します。
    2. **参照**を選択して、必要な ER コンフィギュレーションに適したファイルを XML 形式で選択します。
    3. **OK** を選択します。

    ![RCS の構成ページ](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>ER ソリューションを実行して追跡実行する

ER ソリューションの最初のバージョンのデザインが完了したとします。 これにより、Finance and Operations インスタンスでテストを行い、実行パフォーマンスを分析できます。

### <a id='import-configuration'></a>ER コンフィギュレーションを RCS から Finance and Operations にインポートする

1. Finance and Operations インスタンスへログインします。
2. このチュートリアルでは、RCS インスタンス (ER コンポーネントを設計する場所) から、Finance and Operations インスタンス (テストして最後に使用する場所) にコンフィギュレーションをインポートします。 したがって、必要なコンポーネントがすべて準備されたことを確認する必要があります。 手順については、[規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) を参照してください。
3. これらの手順に従って、コンフィギュレーションを RCS から Finance and Operations にインポートします。

    1. **電子申告**ワークスペースの、**Litware, inc.** コンフィギュレーション プロバイダーのタイルで、**リポジトリ**を選択します。
    2. **コンフィギュレーション リポジトリ** ページで、**RCS** タイプのリポジトリを選択し、**開く**を選択します。
    3. **コンフィギュレーション** クイック タブで、**パフォーマンス追跡形式**コンフィギュレーションを選択します。
    4. **バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **1.1** を選択し、**インポート**を選択します。

    ![Finance and Operations のコンフィギュレーション レポジトリ ページ](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

データ モデルとモデル マッピングコン フィギュレーションの対応するバージョンは、インポートされた ER 形式コンフィギュレーションの前提条件として自動的にインポートされます。

### <a name="turn-on-the-er-performance-trace"></a>ER パフォーマンス追跡を有効にする

1. Finance and Operations で、**組織管理 \> 電子申告 \> 構成**の順に移動します。
2. **構成**ページ、アクション ウィンドウ、**構成**タブ、**詳細設定**グループで、**ユーザー パラメーター**を選択します。
3. **ユーザー パラメーター** ダイアログ ボックスの**実行トレース** セクションで、次の手順を実行します。

    1. **実行トレース形式**フィールドで、**デバッグ トレース形式**を選択して、ER 形式実行の詳細の収集を開始します。 この値が選択されている場合、パフォーマンス追跡によって、次のアクションに費やされた時間に関する情報が収集されます。

        - データを取得するために呼び出されるモデル マッピングで各データ ソースを実行する
        - 生成される出力にデータを入力するため各項目の形式を処理する

        **実行トレース形式**フィールドを使用して、実行詳細が ER 形式およびマッピング要素で格納される生成済パフォーマンス追跡の形式を指定します。 **デバッグ トレース形式**を値として選択することにより、ER 操作デザイナーでトレースの内容を分析して、トレースに記載されている ER 形式またはマッピング要素を確認できます。

    2. 次のオプションを**はい**に設定して、ER モデル マッピングおよび ER フォーマット コンポーネントの実行に関する具体的な詳細を収集します。

        - **クエリ統計情報の収集** – このオプションが有効になっている場合、パフォーマンス追跡では次の情報が収集されます。

            - データ ソースによって作成されたデータベース呼び出し数
            - データベースに対する複製呼び出し数
            - データベース呼び出しを行うために使用された SQL ステートメントの詳細

        - **キャッシュのアクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では ER モデル マッピングのキャッシュ使用に関する情報が収集されます。
        - **データ アクセスの追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプの実行されたデータ ソースに対するデータベースへの呼び出し回数に関する情報が収集されます。
        - **リスト列挙の追跡** – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプのデータ ソースから要求されたレコード数に関する情報が収集されます。

    > [!NOTE]
    > **ユーザー パラメーター** ダイアログ ボックスのパラメーターは、ユーザーと現在の会社に固有です。

    ![Finance and Operations のユーザー パラメーター ダイアログ ボックス](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>ER 形式を実行する

1. Finance and Operations で、**DEMF** 会社を選択します。
2. **組織管理 \> 電子申告 \> コンフィギュレーション**の順に移動します。
3. **コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡形式**項目を選択します。
4. アクション ウィンドウで、**実行**を選択します。

生成されるファイルによって、6 つの仕入先の 265 トランザクションに関する情報が表示されることに注意してください。

## <a name="review-the-execution-trace"></a>実行追跡の確認

### <a id='export-trace'></a> 生成された追跡を Finance and Operations からエクスポートします。

パフォーマンス追跡は、ソースの ER 形式から切り離され、外部の zip ファイルにシリアル化されます。

1. Finance and Operations で、**組織管理 \> 電子申告 \> 構成デバッグ ログ**の順に移動します。
2. **電子申告実行ログ**ページ、左ウィンドウの、**コンフィギュレーション名**フィールドで、**パフォーマンス追跡形式**を選択し、**パフォーマンス追跡形式**コンフィギュレーションの実行によって生成されたログ レコードを検索します。
3. ページの右上隅にある**添付ファイル**ボタン (紙クリップ記号) を選択するか、**Ctrl + Shift + A** を押します。

    ![Finance and Operations の電子申告実行ログ ページの添付ファイル ボタン](./media/GER-PerfTrace-GER-DebugLog.png)

4. **電子申告実行ログの添付ファイル** ページの、アクション ウィンドウで、**開く**を選択してパフォーマンス追跡を zip ファイルとして取得し、ローカルに保管します。

    ![Finance and Operations の電子申告実行ログ ページの添付ファイル](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> 生成されるトレースは、**GUID** 形式のみの固有のレポート ID を通じて、ソース ER レポートを参照しています。 形式のバージョン番号付けは考慮されません。

実行される ER 形式と ER モデル マッピングに対して生成されたパフォーマンス追跡間の関連付けは、使用されたルート記述子と共通データ モデルに基づいていることに注意してください。 形式のバージョン番号付けおよびモデル マッピングは考慮されません。 モデル マッピングに対する**モデル マッピングの既定値**フラグの設定も考慮されません。

### <a id='import-trace'></a> 生成された追跡を RCS にインポートします

1. RCS の、**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。
2. **構成**ページのコンフィギュレーション ツリーで、**パフォーマンス追跡モデル**項目を展開し、**パフォーマンス追跡形式**項目を選択します。
3. アクション ウィンドウで、**デザイナー**を選択します。
4. **形式デザイナー**の、アクション ウィンドウで、**パフォーマンス追跡**を選択します。
5. **パフォーマンス追跡結果の設定**ダイアログ ボックスで、**パフォーマンス追跡のインポート**を選択します。
6. **参照**を選択して、事前に Finance and Operations からエクスポートした zip ファイルを選択します。
7. **OK** を選択します。

    ![RCS のパフォーマンス追跡結果の設定ダイアログ ボックス](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>RCS での分析に対するパフォーマンス追跡の使用 – 形式実行

1. RCS の、**形式デザイナー** ページで、**展開/折りたたみ**を選択してすべての形式項目の内容を展開します。

    現在の形式の一部の項目に関して、追加情報が表示されることに注意してください。

    - 形式項目を使用して生成された出力にデータを入力するのに費やした実際の時間
    - 出力全体の生成に費やされた合計時間の割合で表される同じ時間

    ![RCS の形式デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. **形式デザイナー** ページを閉じます。

### <a id='use-trace'></a>RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング

1. RCS、**コンフィギュレーション** ページのコンフィギュレーション ツリーで、**パフォーマンス追跡マッピング**項目を選択します。
2. アクション ウィンドウで、**デザイナー**を選択します。
3. **デザイナー** をクリックします。
4. **モデル マッピング デザイナー** ページの、アクション ウィンドウで、**パフォーマンス追跡**を選択します。
5. 事前にインポートした追跡を選択します。
6. **OK** を選択します。

現在のモデル マッピングの一部のデータ ソース項目に関する、新しい情報が利用可能になることに注意してください。

- データ ソースを使用してデータの取得に費やした実際の時間
- モデル マッピング全体の実行に費やされた合計時間の割合で表される同じ時間

VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースの実行中は、現在のモデル マッピングがデータベース要求を重複することを ER から通知されることに注意してください。 この重複が発生するのは、仕入先トランザクションの一覧が、反復する仕入先レコードごとに 2 回呼び出されるためです。

- 1 回の呼び出しでは、構成されたバインディングに基づいて、データ モデルの各トランザクションの詳細を入力します。
- もう 1 回の呼び出しで、データ モデルの仕入先ごとに計算されたトランザクション数を入力します。

![RCS のモデル マッピング デザイナー ページで重複したデータベース要求に関するメッセージ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

**\[Q:530\]** の値は、テーブルから VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースにレコードを返すため、VendTrans テーブルが 530 回呼び出されたことを示します。 **\[530\]** の値は、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースが、そのデータ ソースからレコードを返し、データ モデルで詳細を入力するために 530 回呼び出されたことを示します。

265 トランザクションの詳細を取得するための呼び出し数を減らし、モデルマッピングのパフォーマンスを向上させるため、VendTable/\<Relations/VendTrans.VendTable\_AccountNum データ ソースに対してキャッシュを使用することをお勧めします。

それは LedgerTransTypeList データ ソースに対して行われる呼び出し数を減らすのにも役立ちます。 このデータ ソースは、**LedgerTransType** 列挙の各値をラベルに関連付けるために使用されます。 このデータ ソースを使用すると、適切なラベルを検索して、各仕入先トランザクションのデータ モデルに入力できます。 このデータ ソースへの現在の呼び出し数 (9,027) は、265 トランザクションに対して非常に高くなっています。

![データ ソースへの 9,027 の呼び出しを示す、RCS のモデル マッピング デザイナー ページ](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>実行追跡からの情報に基づいてモデル マッピングを改善する

### <a name="modify-the-logic-of-the-model-mapping"></a>モデル マッピングのロジックを変更する

1. 次の手順に従ってキャッシュを使用すると、データベースへの重複呼び出しを防ぐことができます。

    1. RCS、**モデル マッピング デザイナー** ページの、**データ ソース** ウィンドウで、**VendTable** 項目を選択します。
    2. **キャッシュ**を選択します。
    3. **VendTable** 項目を展開し、VendTable データ ソース (**\<関係**項目) の一対多の関係の一覧を展開してから、**VendTrans.VendTable\_AccountNum** 項目を選択します。
    4. **キャッシュ**を選択します。

    ![重複呼び出しを防ぐためのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. LedgerTransTypeList データ ソースを VendTable データ ソースのスコープに移動するには、次の手順に従います。

    1. **データ ソース タイプ** ウィンドウで、**関数**項目を展開し、**計算済フィールド**項目を選択します。
    2. **データ ソース** ウィンドウで、**VendTable** 項目を選択します。
    3. **追加**を選択します。
    4. **名前**フィールドで、**\$TransType** を入力します。
    5. **式の編集**を選択します。
    6. **式**フィールドに、**LedgerTransTypeList** を入力します。
    7. **保存** を選択します。
    8. **式の編集**ページを閉じます。
    9. **OK**をクリックします。

3. 次の手順に従って、**\$TransType** フィールドをキャッシュします。

    1. **LedgerTransTypeList** 項目を選択します。
    2. **キャッシュ**を選択します。
    3. **VendTable.\$TransType** 項目を選択します。
    4. **キャッシュ**を選択します。

    ![$TransType フィールドのキャッシュ設定](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. 次の手順に従って **\$TransTypeRecord** フィールドを変更し、キャッシュされた **\$TransType** フィールドを使用開始できるようにします。

    1. **データ ソース** ウィンドウで、**VendTable** 項目を展開し、**\<関係**項目を展開し、**VendTrans.VendTable\_AccountNum** 項目を展開してから、**VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** 項目を選択します。
    2. **編集**を選択します。
    3. **式の編集**を選択します。
    4. **式**フィールドで、次の式を検索します。

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. **式**フィールドで、次の式を入力します。

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. **保存** を選択します。
    7. **式の編集**ページを閉じます。
    8. **OK** を選択します。

5. **保存** を選択します。
6. **モデル マッピング デザイナー** ページを閉じます。
7. **モデル マッピング** ページを閉じます。

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER モデル マッピングの変更されたバージョンを完了する

1. RCS、**コンフィギュレーション** ページの、**バージョン** クイック タブで、**パフォーマンス追跡マッピング** コンフィギュレーションのバージョン **1.2** を選択します。
2. **ステータスの変更**を選択します。
3. **完了**を選択します。

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a>変更された ER モデル マッピング コンフィギュレーションを RCS から Finance and Operations にインポートする

このトピックの先のセクション [ER コンフィギュレーションを RCS から Finance and Operations にインポートする](#import-configuration) の手順を繰り返して、**パフォーマンス追跡マッピング** コンフィギュレーションのバージョン 1.2 を Finance and Operations にインポートします。

## <a name="run-the-modified-er-solution-to-trace-execution"></a>変更された ER ソリューションを実行して追跡実行する

### <a name="run-the-er-format"></a>ER 形式を実行する

このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。

## <a name="review-the-execution-trace"></a>実行追跡の確認

### <a name="export-the-generated-trace-from-finance-and-operations"></a>生成された追跡を Finance and Operations からエクスポートする

このトピックの先のセクション [生成された追跡を Finance and Operations からエクスポートする](#export-trace) の手順を繰り返して、新しいパフォーマンス追跡をローカルに保存します。

### <a name="import-the-generated-trace-into-rcs"></a>生成された追跡を RCS にインポートする

このトピックの先のセクション [生成された追跡を RCS にインポートする](#import-trace) の手順を繰り返して、新しいパフォーマンス追跡を RCS にインポートします。

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング

このトピックの先のセクション [RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング](#use-trace) の手順を繰り返して、最新のパフォーマンス追跡を分析します。

モデル マッピングに対して行った調整によって、データベースへの重複するクエリが消去されたことに注意してください。 このモデル マッピングのデータベース テーブルおよびデータ ソースへの呼び出し数も減少しました。 したがって、ER ソリューション全体のパフォーマンスが向上しました。

![RCS の、モデル マッピング デザイナー ページで、VendTable データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

追跡情報で、VendTable データ ソースの **\[12\]** の値は、このデータソースが 12 回呼び出されたことを示します。 **\[Q:6\]** の値は、6 つの呼び出しが VendTable テーブルへのデータベース呼び出しに変換されたことを示します。 **\[C:6\]** の値は、データベースからフェッチされたレコードがキャッシュされ、その他の 6 つの呼び出しがキャッシュを使用して処理されたことを示します。

LedgerTransTypeList データソースへの呼び出し数が 9,027 から 240 に減少したことに注意してください。

![RCS の モデル マッピング デザイナー ページで、LedgerTransTypeList データ ソースに関する情報を追跡します。](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a>Finance and Operations での実行追跡の確認

RCS に加えて、Finance and Operations の一部のバージョンでは ER フレームワーク デザイナー経験に対する機能が提供される場合があります。 Finance and Operations のこれらのバージョンには**デザイン モードを有効にする**オプションがあり、有効にすることができます。 このオプションは**電子申告パラメーター**ページの**一般**タブで検索できます。このページは**電子申告**ワークスペースから開くことができます。

![Finance and Operations の電子申告パラメーター ページでデザイン モード オプションを有効にする](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Finance and Operations のいずれかのバージョンを使用する場合は、生成されたパフォーマンス追跡の詳細を Finance and Operations で直接分析できます。 Finance and Operations からエクスポートして RCS にインポートする必要はありません。

## <a name="review-the-execution-trace-by-using-external-tools"></a>外部ツールを使用した実行追跡の確認

### <a name="configure-user-parameters"></a>ユーザー パラメーターのコンフィギュレーション

1. Finance and Operations で、**組織管理 \> 電子申告 \> 構成**の順に移動します。
2. **構成**ページ、アクション ウィンドウ、**構成**タブ、**詳細設定**グループで、**ユーザー パラメーター**を選択します。
3. **ユーザー パラメーター** ダイアログ ボックス、**実行トレース** セクションの、**実行トレース形式**フィールドで、**PerfView XML** を選択します。

### <a name="run-the-er-format"></a>ER 形式を実行する

このトピックの先のセクション [ER 形式を実行する](#run-format) の手順を繰り返して、新しいパフォーマンス追跡を生成します。

Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。 このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。 次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。
