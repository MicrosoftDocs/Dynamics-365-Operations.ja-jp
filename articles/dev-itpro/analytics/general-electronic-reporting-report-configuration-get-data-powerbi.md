---
title: "Power BI にデータをプルする電子申告 (ER) のコンフィギュレーション"
description: "このトピックでは、電子申告 (ER) コンフィギュレーションを使用して Finance and Operations のインスタンスから Power BI サービスへのデータ転送を調整する方法について説明します。"
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: e2d3c03a75fd03dfd3a96a181eff20f934546ec4
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Power BI にデータをプルする電子申告 (ER) のコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、電子申告 (ER) コンフィギュレーションを使用して Finance and Operations のインスタンスから Power BI サービスへのデータ転送を調整する方法について説明します。 たとえば、このトピックでは、転送する必要があるビジネス データとしてのイントラスタット トランザクションを使用します。 Power BI マップの視覚化は、このイントラスタット トランザクション データを使用して Power BI レポートで会社のインポート/エクスポート活動の分析のためのビューを表示します。

## <a name="overview"></a>概要

Microsoft Power BI は、外部のデータ ソースを一貫性、視覚的な没入型、および対話型の洞察に変換するソフトウェア サービス、アプリ、コネクタの集合です。 電子申告 (ER) は、Microsoft Dynamics 365 for Finance and Operations のユーザーが容易にデータ ソースをコンフィギュレーションし、Finance and Operations から Power BI へデータの転送を手配します。 データは、OpenXML ワークシート (Microsoft Excel ワークブックのファイル) 形式のファイルとして転送されます。 転送されたファイルは、その目的にコンフィギュレーションされた Microsoft SharePoint Server に保存されます。 保存されたファイルは、視覚化 (テーブル、グラフ、マップなど) を含むレポートを作成し、Power BI で使用されます。 Power BI レポートは、Power BI ユーザーで共有され、Power BI ダッシュボード、および Finance and Operations のページでアクセスされます。 ここでは、次のタスクについて説明します:

- Finance and Operations を構成します。
- Finance and Operations からデータを取得するために、ER形式のコンフィギュレーションを準備します。
- Power BI にデータを転送するために ER 環境のコンフィギュレーション。
- Power BI レポートを作成するために転送されたデータの使用。
- Power BI レポートが Finance and Operations にアクセスできるようにします。

## <a name="prerequisites"></a>前提条件
このトピックの例を完了するには、次のアクセスが必要です:

- 次のロールのいずれか 1 つのために Finance and Operations にアクセスします:

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

- Finance and Operations で使用するようにコンフィギュレーションされた SharePoint Server へのアクセス
- Power BI フレームワークへのアクセス

## <a name="configure-document-management-parameters"></a>ドキュメント管理パラメーターのコンフィギュレーション
1. **ドキュメント管理パラメーター** ページで、サイン インしている会社 (この例では DEMF 会社) が使用する SharePoint Serverへのアクセスをコンフィギュレーションします。
2. アクセス権があることを確認するために、SharePoint Server への接続をテストします。

    [![ドキュメント管理パラメーター ページ](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. コンフィギュレーションされた SharePoint サイトを開きます。 Power BI データセットのソースとして Power BI レポートに必要なビジネス データがある Excel ファイルを ER が格納する新しいフォルダーを作成します。
4. Finance and Operations では、**ドキュメント タイプ** ページで、作成した SharePoint フォルダーにアクセスするために使用される新しいドキュメント タイプを作成します。 **グループ** フィールドに **ファイル** を入力し、**場所** フィールドに **SharePoint** を入力し、SharePoint フォルダーのアドレスを入力します。

    [![ドキュメント タイプ ページ](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER パラメーターのコンフィギュレーション
1. **電子申告** のワークスペースで、**電子申告パラメーター** のリンクをクリックします。
2. **添付ファイル** タブで、すべてのフィールドの **ファイル** ドキュメント タイプを選択します。
3. **電子申告** のワークスペースで、**有効日に設定** をクリックして必要なプロバイダーを有効にします。 詳細については、**ER サービス プロバイダーの選択**のタスク ガイド を再生してください。

## <a name="use-an-er-data-model-as-the-source-of-data"></a>データのソースとして ER データ モデルを使用
Power BI レポートで使用されるビジネス データのソースとして、ER データ モデルが必要です。 このデータ モデルは、ER コンフィギュレーション リポジトリからアップロードされます。 詳細については、「[Lifecycle Services の電子申告コンフィギュレーションのダウンロード](download-electronic-reporting-configuration-lcs.md)」、または**Lifecycle Services からのコンフィギュレーションの ER インポート**を参照してください。 選択した ER コンフィギュレーション リポジトリからアップロードされるデータ モデルとして、**イントラスタット** を選択します。 (この例では、モデルのバージョン 1 が使用されています)。**コンフィギュレーション** のページで、**イントラスタット** ER モデル コンフィギュレーションにアクセスできます。

[![構成ページ](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER 形式のコンフィギュレーションをデザイン
ビジネス データのソースとして**イントラスタット** データ モデルを使用する新しい ER 形式のコンフィギュレーションを作成する必要があります。 この形式のコンフィギュレーションは、OpenXML (Excel ファイル) 形式の電子ドキュメントとして出力結果を生成する必要があります。 詳細については、**OPENXML 形式でレポートのコンフィギュレーションを ER 作成する**のタスク ガイドを再生してください。 次の図に示すように、新しいコンフィギュレーションに**インポート/エクスポート活動**の名前を付けます。 ER 形式をデザインするときにテンプレートとして、「[ER データのインポートとエクスポートの詳細](https://go.microsoft.com/fwlink/?linkid=845208)」 Excel ファイルを使用します。 (形式のテンプレートをインポートする方法について、タスク ガイドを再生してください。)

[![インポート/エクスポート活動のコンフィギュレーション](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

**インポート/エクスポート活動**形式のコンフィギュレーションを変更するには、次の手順に従います。

1. **デザイナー** をクリックします。
2. **形式** タブで、この形式の **Excel 出力ファイル**のファイル要素に名前を付けます。

    [![Excel 出力ファイル要素](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. **マッピング** タブで、この形式で実行されるたびに生成される Excel ファイルの名前を指定します。 値の**インポートとエクスポートの詳細**を返して関連する式をコンフィギュレーションします (.xlsx ファイル名拡張子は自動的に追加されます)。

    [![形式デザイナー](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. この形式の新しいデータ ソースの品目を追加します。 (この列挙は、さらにデータ バインディングのために必要です。)

    1. データ ソース **direction\_enum** に名前を付けます。
    2. データ ソース タイプとして、**データ モデルの列挙** を選択します。
    3. **方向**データ モデルの列挙を参照してください。

    [![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. 次の図に示すように、**イントラスタット**データ モデルの要素と設計された形式の要素のバインディングを完了します。

    [![バインディングの完了](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

実行後、ER 形式は Excel 形式で出力の結果を生成します。 出力結果にイントラスタット トランザクションの詳細を送信し、インポート活動またはエクスポート活動のいずれかを記述するトランザクションとして分離します。 **イントラスタット** ページ (**税** &gt; **申告** &gt; **対外貿易** &gt; **イントラスタット**) のイントラスタット トランザクションのリストのための新しい ER フォーマットをテストするには、**実行** をクリックします。

[![イントラスタット ページ](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

次の出力の結果が生成されます。 書式設定で指定したとおり、ファイルは**Import and export details.xlsx**と名前が付けられます。

[![Import and export details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER 送信先のコンフィギュレーション
特別な方法で新しい ER 形式のコンフィギュレーションの出力結果を送信するために ER フレームワークをコンフィギュレーションする必要があります。

- 出力結果は、選択した SharePoint Server のフォルダに送信する必要があります。
- 形式のコンフィギュレーションを実行するたびに、同じ Excel ファイルの新しいバージョンを作成する必要があります。

**電子申告** のページ (**組織管理** &gt; **電子申告**) で、**電子申告の送信先** の項目をクリックして、新しい送信先を追加します。 **参照**フィールドで、以前に作成した**エクスポート/インポート活動**の形式のコンフィギュレーションを選択します。 参照用の新しいファイル送信先レコードを追加するには、次の手順に従います。

1. **名前**フィールドに、ファイルの送信先のタイトルを入力します。
2. **ファイル名**で、Excel ファイル形式のコンポーネントの名前 **Excel 出力ファイル** を選択します。

新しい送信先レコードの **設定** ボタンをクリックします。 次に、**送信先の設定** のダイアログ ボックスで、次の手順に従います。

1. **Power BI** タブで、**有効** オプションを **はい** に設定します。
2. **SharePoint** フィールドで、以前に作成した **共有** ドキュメント タイプを選択します。

## <a name="schedule-execution-of-the-configured-er-format"></a>コンフィギュレーションされた ER 形式の実行をスケジュールする
1. **コンフィギュレーション** ページ (**組織管理** &gt; **電子申告** &gt; **コンフィギュレーション**) のコンフィギュレーション ツリーで、以前に作成した **インポート/エクスポート活動** のコンフィギュレーションを選択します。
2. この形式を使用できるように、バージョン 1.1 の状態を **ドラフト** から **完了** に変更します。

    [![構成ページ](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. **インポート/エクスポート活動** コンフィギュレーションの完了したバージョンを選択し、**実行** をクリックします。 コンフィギュレーションした送信先は、Excel 形式で生成される出力結果に適用されることに注意してください。
4. 無人モードでこのレポートを実行するには、**バッチ処理** オプションを **はい** に設定します。
5. このバッチ実行の必要な再実行をスケジュールするために **再実行** をクリックします。 再実行は、更新されたデータが Finance and Operations から Power BI に転送される頻度を定義します。

    [![電子申告パラメーター ダイアログ ボックス](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. これをコンフィギュレーションした後、**バッチ ジョブ** のページ (**システム管理 &gt; 照会 &gt; バッチ ジョブ**) に ER レポートの実行ジョブを見つけることができます。

    [![バッチ ジョブのページ](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. このジョブを初めて実行すると、送信先は、選択した SharePoint のフォルダにコンフィギュレーションされた名前を持つ新しい Excel ファイルを作成します。 その後ジョブが実行されるたびに、送信先は新しいバージョンの Excel ファイルを作成します。

    [![Excel ファイルの新しいバージョン](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>ER 形式の出力結果を使用して Power BI データセットを作成
1. Power BI にサイン インして、既存の Power BI グループ (ワークスペース) を開くか、新しいグループを作成します。 **データにインポートまたは接続** セクションの **ファイル** の下の **追加** をクリックするか、左ウィンドウの **データセット** の横にあるプラス記号 (**+**) をクリックします。

    [![データセットの作成](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. **SharePoint – チーム サイト** オプションを選択してから、使用している SharePoint Server のパス (上記の例では、`https://ax7partner.litware.com`) を入力します。
3. **/共有ドキュメント/GER データ/PowerBI** フォルダを参照し、新しい Power BI データセットのためのデータのソースとして作成した Excel ファイルを選択します。

    [![Excel ファイルの選択](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. **接続** をクリックし、**インポート** をクリックします。 新しいデータセットは、選択された Excel ファイルに基づいて作成されます。 データセットは、新しく作成されたダッシュボードに自動的に追加できます。

    [![ダッシュボードのデータセット](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. このデータセットの更新スケジュールをコンフィギュレーションして、定期更新を強制します。 定期更新により、SharePoint Server 上に作成された Excel ファイル の新しいバージョンを使用して ER レポートの定期実行による Finance and Operations からの新しいビジネス データの消費が可能になります。

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>新しいデータセットを使用して Power BI レポートを作成
1. 作成した **インポートとエクスポートの詳細** Power BI データセットをクリックします。
2. 視覚化をコンフィギュレーションします。 たとえば **入力済マップ** の視覚化を選択して、次のようにコンフィギュレーションします:

    - **CountryOrigin** データセット フィールドをマップ視覚化の **場所** フィールドに割り当てます。
    - **金額** データセット フィールドをマップ視覚化の **彩度** フィールドに割り当てます。
    - **活動** と **年** のデータセット フィールドに、マップ視覚化の **フィルター** フィールド コレクション を追加します。

3. **インポートとエクスポートの詳細レポート**として Power BI レポートを保存します。

    [![インポートとエクスポートの詳細レポート](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    地図には、Excel ファイルに示されている国/地域 (この例ではオーストリアとスイス) が表示されていることに注意してください。 これらの国/地域は、それぞれの請求額の割合の色分けが表示されます。

4. イントラスタット トランザクションのリストを更新します。 イタリアからの輸出トランザクションが追加されます。

    [![イントラスタット トランザクションのリスト](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. ER レポートの次のスケジュールされた実行と Power BI データセットの次のスケジュールされた更新を待ちます。 次に、Power BI レポート (インポート トランザクションのみを表示するように選択) を確認します。 更新されたマップにイタリアが表示されます。

    [![更新されたマップ](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance-and-operations"></a>Finance and Operations で Power BI レポートにアクセスします。
Finance and Operations と Power BI の統合を設定します。 詳細については、「[ワークスペースの Power BI 統合のコンフィギュレーション](configure-power-bi-integration.md)」を参照してください。

1. Power BI 統合 (**組織管理** &gt; **ワークスペース** &gt; **電子申告ワークスペース**) をサポートする **電子申告** ワークスペース ページで、**オプション** &gt; **レポート カタログを開く** をクリックします。
2. 作成した **インポートとエクスポートの詳細** Power BI レポートを選択して、選択されたページでアクション項目としてレポートを表示します。
3. アクション項目をクリックして、Power BI でデザインされたレポートを表示する Finance and Operations のページを開きます。

    [![インポートとエクスポートの詳細レポート](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>その他のリソース

[電子申告の送信先](electronic-reporting-destinations.md)

[電子申告の概要](general-electronic-reporting.md)

