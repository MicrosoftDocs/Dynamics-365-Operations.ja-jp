---
title: 手動で選択したファイルからバッチ モードでデータをインポートする
description: このトピックでは、バッチ モードで手動で選択したファイルからデータをインポートする方法について説明します。
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075624"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>手動で選択したファイルからバッチ モードでデータをインポートする

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) フレームワークを使用して、手動で選択した受信ファイルからバッチ モードでデータをインポートするには、インポートをサポートする ER [形式](er-overview-components.md#format-component) を構成します。 その後、その形式をデータ ソースとして使用する **宛先** タイプの [モデル マッピング](er-overview-components.md#model-mapping-component) を実行します。 データをインポートするには、インポートするファイルを参照し、手動で選択します。 

バッチ モードでのデータ インポートをサポートする新しい ER 機能により、このプロセスを無人プロセスとして構成できます。 ER 構成を使用して、ER ユーザー インターフェイス (UI) から新しいバッチ ジョブをスケジュールすることで、データ インポートを実行できます。

このトピックでは、バッチ モードで手動で選択したファイルからデータのインポートを完了する方法について説明します。 例では、業務データとして仕入先トランザクションを使用します。 これらの例のステップは、**USMF** 社で完了することができます。 コーディングは必要ありません。

## <a name="prerequisites"></a>必要条件

このトピックの例を完了するには、次のアクセスが必要です:

- 次のいずれかのロール:

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

- 1099 payments の ER 形式およびモデル コンフィギュレーション

### <a name="create-the-required-er-configurations"></a>必要な ER 構成の作成

必要な ER 構成を作成し、その他の前提条件を取得するには、次のいずれかの手順に従います:

- **7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677)** 業務プロセスの一部である **Microsoft Excel ファイルからの ER インポート データ** タスク ガイドを再生します。 これらのタスク ガイドでは、Microsoft Excel ファイルから仕入先トランザクションを対話型でインポートする ER 構成を設計および使用するプロセスについて説明します。 詳細については、[Excel 形式で受信ドキュメントを解析する](parse-incoming-documents-excel.md) を参照してください。
- [SharePoint からのデータ インポートを構成する](er-configure-data-import-sharepoint.md) にある例を完了します。 これらの例では、SharePoint フォルダーに保存されている Excel ファイルから仕入先トランザクションを対話型でインポートする ER 構成を設計および使用するプロセスについて説明します。

### <a name="download-the-required-er-configurations"></a>必要な ER 構成のダウンロード

1. 次の ER 構成をダウンロードし、ローカルに保存します。

    | コンテンツの説明 | ファイル |
    |---------------------|------|
    | **1099 支払モデル** ER データ モデル構成 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **仕入先のトランザクションのインポート用 (Excel)** ER 形式の構成 | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. [XML ファイルから読み込む](er-defer-sequence-element.md#import-the-sample-er-configurations) ER オプションを使用して、ダウンロードした ER 構成を次の順序で Dynamics 365 Finance のインスタンスにインポートします。

    1. ER データ モデル構成
    2. ER フォーマット構成

### <a name="download-the-required-excel-files"></a>必要な Excel ファイルのダウンロード

- 次のサンプル データ セットをダウンロードし、ローカルに保存します。

    | コンテンツの説明 | ファイル |
    |---------------------|------|
    | インポート用のサンプル データを含む **1099import-data.xlsx** の受信ファイル | [1099import data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>前提条件の確認

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページで、バッチ モードでのデータ インポート用に準備された ER ソリューションを確認します。
3. **仕入先のトランザクションのインポート用 (Excel)** 形式の構成を確認します。

    - この構成の形式コンポーネントは、受信 Excel ファイルを解析するように設計されています。
    - この構成のモデル マッピング コンポーネントは、解析された Excel ファイルのデータを使用して基本データ モデルを入力するために使用されます。

    ![ER UI からバッチ モードでデータをインポートするための ER 形式の構成。](./media/er-configure-data-import-batch-configurations-1.png)

4. **1099 支払モデル** データ モデル構成を確認します。

    - この構成のモデル コンポーネントは、実行中の ER コンポーネント間でデータを渡すために使用されるデータ モデルの構造を表します。
    - この構成のモデル マッピング コンポーネントを使用して、実行された形式コンポーネントからデータをプルし、アプリケーション テーブルを更新します。

    ![ER UI からバッチ モードでデータをインポートするためのデータ モデルの構成。](./media/er-configure-data-import-batch-configurations-2.png)

5. Excel で **1099import-data.xlsx** ファイルを開きます。

    ![バッチ モードでインポートするデータを含むサンプル Excel ファイル。](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>UI からの ER のバッチ データ インポートの有効化

1. **システム管理** \> **ワークスペース** \> **機能管理** の順に移動します。
2. **機能管理** ワークスペースで、**手動でアップロードしたドキュメントの ER インポートを一括で実行する** 機能を選択し、**今すぐ有効化** を選択します。

## <a name="import-data-from-manually-selected-excel-files"></a>手動で選択した Excel ファイルからのデータのインポート

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページで、**1099 支払モデル** データ モデル構成を選択します。
3. **コンポーネントの構成** FastTab で、**For 1099 manual transactions import** リンクを選択します。
4. **モデルからデータ ソースへのマッピング** ページには、**For 1099 manual transactions import** モデル マッピングが事前に選択されています。 **実行** を選択します。
5. **パラメーター** タブで、**参照** を選択します。 **1099import-data.xlsx** ファイルを検索して選択し、**OK** を選択します。
6. **伝票 ID の入力** フィールドで、**V-00001** と入力します。
7. **バックグラウンドで実行** タブで、**バッチ処理** オプションを **はい** に設定します。

    **タスクの説明** フィールドが **モデル マッピングの実行 'For 1099 manual transactions import'、構成 '1099 支払モデル'** に設定されていることに注意してください。 この値は、選択したモデル マッピングの実行が新しいバッチ ジョブとしてスケジュールされることを示します。

    ![電子申告パラメーター ダイアログ ボックスで、バッチ モードでのデータ インポートの詳細を指定します。](./media/er-configure-data-import-batch-execution-parameters.png)

8.  **OK** を選択します。 新しいバッチ ジョブがスケジュールされたことを通知するメッセージが表示されます。

    ![モデルからデータ ソース へのマッピング ページの新しいスケジュールされたバッチ ジョブに関するメッセージ。](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>バッチ ジョブ ページでデータのインポート結果を確認

1. **共通** \> **照会** \> **バッチ ジョブ** \> **私のバッチ ジョブ** の順に移動します。
2. **バッチ ジョブ** ページ で、バッチ ジョブの一覧をフィルター処理してスケジュール済のバッチを見つけて選択します。
3. **ジョブ ID** リンクを選択して、ジョブの詳細を確認します。
4. **バッチ タスク** FastTab で **ログ** を選択します。

    ![バッチ ジョブ ページの ログ ボタン。](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. 実行の詳細を確認します。

    ![バッチ ジョブ ページでスケジュールされているバッチ ジョブの実行ログ。](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>データ インポート パラメーターの変更

バッチがスケジュールされ、まだ実行されていない間は、スケジュールされたデータ インポートのパラメーターを変更できます。

1. **共通** \> **照会** \> **バッチ ジョブ** \> **私のバッチ ジョブ** の順に移動します。
2. **バッチ ジョブ** ページ で、バッチ ジョブの一覧をフィルター処理してスケジュール済のバッチを見つけて選択します。
3. **ステータスの変更** を選択します。
4. **新しい状態の選択** ダイアログ ボックスで **保留** を選択し、**OK** を選択します。
5. **ジョブ ID** リンクを選択して、ジョブの詳細にアクセスします。
6. **バッチ タスク** FastTab で **パラメーター** を選択します。
7. **電子申告パラメーター** ダイアログ ボックスで、以下の手順を実行します:

    1. **参照** を選択して、データ インポートの代替ファイルを選択します。
    2. 仕入先トランザクションをインポートする伝票番号を変更するには、**伝票 ID の入力** を選択します。

        ![電子申告パラメーター ダイアログ ボックスで、スケジュールされているバッチ ジョブのデータ インポートのパラメーターを変更します。](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3.  **OK** を選択します。

8. バッチが選択状態であることを確認し、再度 **状態の変更** を選択します。
9. **新しい状態の選択** ダイアログ ボックスで **待機中** を選択し、**OK** を選択します。

## <a name="review-the-data-import-results-on-the-er-source-page"></a>ER ソース ページでデータのインポート結果を確認

1. **組織管理** \> **電子申告** \> **電子申告ソース** に移動します。
2. データのインポート時に自動的に作成された **仕入先のトランザクションのインポート用 (Excel)** レコードを選択します。

    ![電子申告ソース ページの仕入先のトランザクションのインポート用 (Excel) 構成のレコード。](./media/er-configure-data-import-batch-files-source-1.png)

3. **ソースのファイルの状態** を選択します。
4. **ファイル** と **インポート形式のソース ログ** FastTabs で、インポートの詳細を確認します。
5. **ファイル** FastTab で、レコードを選択します。 インポートしたファイルがこのレコードに関連付けられていることに注意してください。

    ![インポートしたファイルは、ソースのファイルの状態ページでレコードに関連付けられます。](./media/er-configure-data-import-batch-files-source-2.png)

6. **添付** を選択して、インポートしたファイルを確認します。

    ![ドキュメント ビュー ページにインポートされたファイル。](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > これらの添付ファイルを維持するために、ER フレームワークでは、ER パラメーターの **その他** フィールドで現在の会社に [設定](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されているドキュメント タイプを使用します。

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>1099 の仕入先決済ページでのデータのインポート結果の確認

1. **買掛金勘定** \> **定期処理タスク** \> **税金 1099** \> **1099 の仕入先決済** の順に移動します。
2. **開始日** フィールドに **12/31/2017** (2017 年 12 月 31 日) を入力します。
3. **手動 1099 トランザクション** を選択します。

    ![1099 税トランザクション ページでインポートされた仕入先トランザクション。](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
