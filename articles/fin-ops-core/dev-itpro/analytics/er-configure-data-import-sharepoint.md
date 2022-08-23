---
title: SharePoint からのデータ インポートをコンフィギュレーションする
description: この誇示では、Microsoft SharePoint からデータをインポートする方法について説明します。
author: kfend
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 11208267de0cc35db55c64ccf2de224df854404d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277789"
---
# <a name="configure-data-import-from-sharepoint"></a>SharePoint からのデータ インポートをコンフィギュレーションする

[!include[banner](../includes/banner.md)]

電子申告 (ER) フレームワークを使用して受信ファイルからデータをインポートするには、インポート処理をサポートする ER 形式をコンフィギュレーションし、データ ソースとしてその形式を使用する **宛先** タイプのモデル マッピングを実行する必要があります。 データをインポートするには、インポートするファイルに移動する必要があります。 受信ファイルは、ユーザーにより手動で選択できます。 Microsoft SharePoint からのデータのインポートをサポートするための新しい ER 機能を使用すると、このプロセスを無人プロセスとしてコンフィギュレーションできます。 ER コンフィギュレーションを使用して、Microsoft SharePoint フォルダーに格納されているファイルからデータのインポートを実行できます。 この記事では、SharePoint からインポートを完了する方法について説明します。 例では、業務データとして仕入先トランザクションを使用します。

## <a name="prerequisites"></a>必要条件
この記事に記載の例を完了するには、次のアクセスが必要です:

- 次のロールのいずれかにアクセスします。

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

- アプリケーションで使用するようにコンフィギュレーションされた、Microsoft SharePoint Server のインスタンスへアクセスします。
- 1099 支払の ER 形式およびモデル コンフィギュレーション。

### <a name="create-required-er-configurations"></a>必須な ER コンフィギュレーションの作成
**7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677)** 業務プロセスの一部である **Microsoft Excel ファイルからの ER インポート データ** タスク ガイドを再生します。 これらのタスク ガイドでは、デザインのプロセスおよび Microsoft Excel ファイルから仕入先トランザクションを対話型でインポートする ER コンフィギュレーションの使用について説明します。 詳細については、[Excel 形式で受信ドキュメントを解析する](parse-incoming-documents-excel.md) を参照してください。 タスク ガイドが完了すると、次の設定になります。

#### <a name="er-configurations"></a>ER コンフィギュレーション

- ER モデル構成、**1099 支払モデル**
- ER 形式コンフィギュレーション、**Excel から仕入先のトランザクションをインポートするための形式**

![SharePoint からデータをインポートするための ER コンフィギュレーション。](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>データのインポートに対する受信ファイルのサンプル

- Excel ファイル **1099import-data.xlsx** と、インポートする必要がある仕入先トランザクション。

![SharePoint からインポートするためのサンプル Excel ファイル。](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> 仕入先トランザクションをインポートするための形式が既定のモデル マッピングとして選択されます。 したがって、**1099 支払モデル** のモデル マッピングを実行し、そのモデル マッピングが **宛先** タイプの場合、モデル マッピングは外部ファイルからデータをインポートするこの形式を実行します。 続いてそのデータを使用して、アプリケーション テーブルを更新します。

## <a name="configure-access-to-sharepoint-for-file-storage"></a>ファイル ストレージの SharePoint へのアクセスをコンフィギュレーションする
電子レポート ファイルを SharePoint の場所に保管するには、現在の会社によって使用される SharePoint Server のインスタンスへのアクセスをコンフィギュレーションする必要があります。 この例では、会社は USMF です。 手順については、[SharePoint ストレージのコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage) を参照してください。

1. [SharePoint ストレージのコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage) で手順を完了します。
2. コンフィギュレーションされた SharePoint サイトを開きます。
3. 受信した電子申告ファイルを保存できる次のフォルダーを作成します。

     - ファイルのインポート ソース (メイン) (次のスクリーン ショットに示された例)
     - ファイルのインポート ソース (代替)

    ![ファイルのインポート ソース (メイン)。](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (オプション) インポート後にファイルを保存できる次のフォルダーを作成します。 

    - ファイル アーカイブ フォルダー - このフォルダーは正常にインポートしたファイル用です。
    - ファイル警告フォルダー - このフォルダーは警告付きでインポートしたファイル用です。
    - ファイル エラー フォルダー - このフォルダーはインポートに失敗したファイル用です。

4. **組織管理 > ドキュメント管理 > ドキュメント タイプ** へ移動します。
5. 作成した SharePoint フォルダーにアクセスするために使用される次のドキュメント タイプを作成します。 手順については、[ドキュメント タイプのコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) を参照してください。

|文書種類       | グループ化              | 保管場所      | SharePoint フォルダー      |
|--------------------|--------------------|---------------|------------------------|
|SP メイン             |ファイル                |SharePoint     |ファイルのインポート ソース (メイン)|
|SP 代替             |ファイル                |SharePoint     |ファイルのインポート ソース (代替)|
|SP アーカイブ             |ファイル                |SharePoint     |ファイル アーカイブ フォルダー|
|SP 警告             |ファイル                |SharePoint     |ファイル警告フォルダー|
|SP エラー             |ファイル                |SharePoint     |ファイル エラー フォルダー|

![SharePoint 設定 – 新しいドキュメント タイプ。](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER 形式の ER ソースをコンフィギュレーションします。
1. **組織管理** \> **電子申告** \> **電子申告ソース** の順にクリックします。
2. **電子申告ソース** ページで、コンフィギュレーション済の ER 形式を使用してデータ インポートのソース ファイルをコンフィギュレーションします。
3. .Xlsx 拡張子のファイルのみがインポートされるように、ファイル名マスクを定義します。 ファイル名マスクはオプションであり、定義された場合にのみ使用されます。 ER 形式ごとにマスクを 1 つだけ定義できます。
4. 複数のインポート用ファイルが存在し、インポート順序が重要ではない場合は、**ファイルをインポート前に並べ替える** を **並べ替えない** に変更します
5. 以前に作成したすべての SharePoint フォルダーを選択します。

    [![ER ファイル ソースの設定。](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - ER *ソース* は、アプリケーションの会社ごとに個別に定義されます。 対照的に、ER *コンフィギュレーション* は会社間で共有されます。
> - ER 形式の ER ソース設定を削除すると、接続されているすべてのファイルの状態 (以下を参照) も確認によって削除されます。

## <a name="review-the-files-states-for-the-er-format"></a>ER 形式のファイルの状態を確認します。
1. **電子申告ソース** ページで、**ソースのファイル状態** を選択して現在の ER 形式のコンフィギュレーション済ファイル ソースの内容を確認します。
2. **ファイル** セクションで、ファイルの一覧を確認します。 このリストは、次のものを表します。

    - 該当するソース ファイルは、ファイル名マスク (ファイル名マスクが定義されている場合) に基づいており 、データのインポートの準備が整っています。 これらのファイルについては、**インポート フォーマットのソース ログ** セクションは空白になります。
    - 以前にインポートされたファイル。 これらの各ファイルについては、**インポート フォーマットのソース ログ** セクションで、このファイルのインポートの履歴を確認できます。

**組織管理** \> **電子申告** \> **ソースのファイルの状態** の順に選択することにより、**ソースのファイルの状態** ページを開くこともできます。 この場合、ページではすべての ER 形式のファイル ソースに関する情報、つまりファイル ソースが現在サインインしている会社でコンフィギュレーションされたという情報が提供されます。

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>SharePoint フォルダーにある Excel ファイルからのデータをインポートする
1. SharePoint では、仕入先トランザクションを含む Microsoft Excel ファイル **1099import data.xlsx** を、以前に作成した **ファイルのインポート ソース (メイン)** SharePoint フォルダーにアップロードします。

    [![SharePoint コンテンツ – インポート用 Microsoft Excel ファイル。](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. **ソースのファイルの状態** ページで、**更新** を選択してページを更新します。 SharePoint にアップロードされた Excel ファイルは、このページに **準備完了** という状態で表示されました。 次のステータスは、現在サポートされています。

    - **準備完了** – SharePoint フォルダーで新しいファイルごとに自動的に割り当てられます。 このステータスは、ファイルがインポートの準備ができていることを意味します。
    - **インポート中** – 他のプロセス (それらの多くが同時に実行されている場合) による使用を防ぐためにインポート プロセスによってファイルがロックされるときに、ER レポートによって自動的に割り当てられます。
    - **インポート済** – ファイルのインポートが正常に完了するときに、ER レポートによって自動的に割り当てられます。 このステータスは、インポートされたファイルがコンフィギュレーション済ファイル ソース (SharePoint フォルダー) から削除されたことを意味します。
    - **失敗** – ファイルのインポートがエラーまたは例外で完了するときに、ER レポートによって自動的に割り当てられます。
    - **保留中** – このページ上のユーザーによって手動で割り当てられます。 このステータスは、ファイルが現在インポートされないことを意味します。 このステータスは、いくつかのファイルのインポートを延期するために使用されます。

    [![選択したソースの更新され ER ファイル状態のページ。](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>データを SharePoint ファイルからインポート
1. ER コンフィギュレーション ツリーを開き、**1099 支払モデル** を選択し、ER モデル コンポーネントの一覧を展開します。
2. 選択した ER モデル構成のモデルのマッピングの一覧を開くためのモデル マッピングの名前を選択します。

    [![構成ページ。](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. **実行** を選択し、選択したモデル マッピングを実行します。 ER 形式のファイル ソースをコンフィギュレーションしたため、必要に応じて **ファイル ソース** オプションの設定を変更できます。 このオプションの設定を維持すると、コンフィギュレーション済ソース (この例では SharePoint フォルダー) から .xslx ファイルがインポートされます。

    この例では、1 つだけファイルをインポートしています。 ただし、複数のファイルがある場合、SharePoint フォルダーに追加された順序でインポートするよう選択されます。 ER 形式の各実行で、単一の選択されたファイルをインポートします。

    [![SharePoint からのインポートと ER モデル マッピングの実行。](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. モデル マッピングはバッチ モードで [無人](#limitations) で実行できます。 この場合、バッチがこの ER 形式を実行するたびに、単一のファイルがコンフィギュレーションされたファイル ソースからインポートされます。

    ファイルが SharePoint フォルダーから正常にインポートされると、そのフォルダーから削除され、正常にインポートされたファイルのフォルダー、または警告付きでインポートされたファイルのフォルダーに移動されます。 それ以外の場合は、失敗したファイルのフォルダーに移動されるか、失敗したファイルのフォルダーが設定されていない場合にはこのフォルダー内に保持されます。 

5. **V-00001** などの伝票 ID を入力し、**OK** を選択します。

    [![ER モデル マッピングの実行。](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. **ソースのファイルの状態** ページで、**更新** を選択してページを更新します。

    [![ソースの ER ファイル状態ページ。](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. **ファイル** セクションで、ファイルの一覧を確認します。 **インポート フォーマットのソース ログ** セクションでは、Excel ファイルのインポートの履歴を提供します。 このファイルが正常にインポートされなかったため、SharePoint フォルダーで **削除** としてマークされます。
8. **ファイルのインポート ソース (メイン)** SharePoint フォルダーを確認します。 正常にインポートされた Excel ファイルは、このフォルダーから削除されました。
9. **買掛金勘定** \> **定期処理のタスク** \> **税金 1099** \> **1099s の仕入先決済** の順に選択します。
10. **開始日** および **終了日** フィールドに、適切な値を入力します。 **手動 1099 トランザクション** を選択します。

    伝票 **V-00001** として SharePoint 上の Excel ファイルからインポートされた仕入先トランザクションが、ページに表示されます。

    [![1099 仕入先トランザクション ページ。](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>インポート用 Excel ファイルの準備
1. 以前に使用した Excel ファイルを開きます。 行 3 列 1で、アプリケーションに存在しない仕入先コードを追加します。 行に追加の false 仕入先情報を追加します。

    [![SharePoint からインポートするためのサンプル Microsoft Excel ファイル。](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. 仕入先トランザクションを含む更新済 Excel ファイルを **ファイルのインポート ソース (メイン)** SharePoint フォルダーにアップロードします。
3. ER コンフィギュレーション ツリーを開き、**1099 支払モデル** を選択し、ER モデル コンポーネントの一覧を展開します。
4. データのインポート処理中に不適切な仕入先コードがエラーと見なされるよう、モデル マッピングを更新するモデル マッピングの名前を選択します。
5. **デザイナー** をクリックします。
6. **検証** タブで、アプリケーションでインポートされた仕入先勘定が存在するかどうかを評価するようコンフィギュレーションされた、検証ルールの検証後のアクションを変更する必要があります。 **後検証アクション** フィールドの値を **実行停止** に更新し、変更内容を保存し、ページを閉じます。

    [![ER モデル マッピング デザイナーのページ。](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. 変更内容を保存し、ER モデル マッピング デザイナーを閉じます。
8. **実行** を選択し、変更した ER モデル マッピングを実行します。
9. **V-00002** などの伝票 ID を入力し、**OK** を選択します。

    情報ログには、正しくない仕入先勘定が含まれたファイルが SharePoint フォルダーにあり、インポートできないという通知が含まれています。

    [![ER モデル マッピングの実行の完了。](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. **ソースのファイルの状態** ページで **更新** を選択し、次に **ファイル** セクションでファイルの一覧を確認します。

    [![選択したソースの ER ファイル状態のページ。](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   **インポート形式のソース ログ** セクションでは、インポート プロセスが失敗したこと、およびファイルがまだ SharePoint フォルダーの中にあることを示します (**削除済** チェック ボックスが選択されていません)。 適切な仕入先コードを追加して SharePoint 上でこのファイルを修正してから、ファイルのインポート ソース (メイン) の SharePoint フォルダーに移動すると、ファイルを再度インポートできます。

11. **買掛金勘定** \> **定期処理のタスク** \> **税金 1099** \> **1099 の仕入先決済** の順に選択し、**開始日** および **終了日** フィールドで適切な値を入力し、**手動 1099 トランザクション** を選択します。

    伝票 V-00001 のトランザクションのみが使用可能です。 Excel ファイルで最後にインポートされたトランザクションのエラーが見つかった場合でも、伝票 V-00002 のトランザクションは存在しません。

## <a name=""></a><a name="limitations">制限</a>

Dynamics 365 Finance のバージョン 10.0.25 より前のバージョンでは、ER フレームワークのユーザー インターフェイス (UI) に、データ インポート用に無人モードでモデル マッピングを実行する、新しいバッチ ジョブを開始する機能を用意していません。 代わりに、構成された ER モデル マッピングをアプリケーション UI から呼び出して、受信ファイルからデータをインポートできるように、新しいロジックを開発する必要があります。 このロジックを開発するには、多少の技術的な作業が必要です。 

関連する ER API の詳細については、[Application update 7.3 での ER フレームワーク API の変更](er-apis-app73.md) の [データ インポート用の形式マッピングを実行するためのコード](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) セクションを参照してください。 `Application Suite` モデルの `BankImport_RU` クラスでコードを確認して、カスタム ロジックを実装する方法を確認します。 `BankImport_RU` クラスは、`RunBaseBatch` クラスを拡張します。 特に、`ERIModelMappingDestinationRun` オブジェクトが ER モデル マッピングのランナーとして作成される `runER()` メソッドを確認します。

Finance バージョン 10.0.25 以降では、ER フレームワーク UI に、無人モードでデータ インポート用にモデル マッピングを実行する、新しいバッチ ジョブを開始する機能があります。 このプロセスの詳細については、[手動で選択したファイルからバッチ モードでデータをインポートする](er-configure-data-import-batch.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[Application update 7.3 での ER フレームワーク API の変更](er-apis-app73.md)

[Application update 10.0.23 での ER フレームワーク API の変更](er-apis-app10-0-23.md)

[Application update 10.0.25 での ER フレームワーク API の変更](er-apis-app10-0-25.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
