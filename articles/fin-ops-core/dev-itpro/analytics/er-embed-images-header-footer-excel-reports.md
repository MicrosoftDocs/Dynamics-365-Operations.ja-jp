---
title: ER 形式をデザインして、ページのヘッダーまたはフッターに画像が埋め込まれた Excel 形式でレポートを生成する
description: この記事では、電子申告 (ER) を使用して、ページのヘッダーまたはフッターに画像や図形が埋め込まれたビジネス ドキュメントを生成する方法について説明します。
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 5b46d92094bb3f2dab67a5cb2f0e1a34b05d52f0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281815"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>ER 形式をデザインして、ページのヘッダーまたはフッターに画像が埋め込まれた Excel 形式でレポートを生成する

[!include[banner](../includes/banner.md)]

この記事では、システム管理者または電子レポート機能コンサルタントのロールのユーザーが次のタスクを実行する方法について説明します。

- [電子申告 (ER)](general-electronic-reporting.md) フレームワークのパラメーターを構成します。
- Microsoft が[提供](general-electronic-reporting.md#Provider)し、[自由書式の請求書](../../../finance/accounts-receivable/create-free-text-invoice-new.md)を生成するために使用される、Microsoft Excel 形式の[テンプレート](er-fillable-excel.md#excel-file-component)に基づいた ER [コンフィギュレーション](general-electronic-reporting.md#Configuration)をインポートします。
- Microsoft が提供する標準 ER 形式コンフィギュレーションの[カスタム (派生)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) バージョンを作成します。
- フッターに会社のロゴ画像が含まれる自由書式の請求書レポートを生成するカスタム ER 形式のコンフィギュレーションを変更します。

この記事の手順は、**USMF** 会社で完了することができます。 コーディングは必要ありません。 開始する前に、次のファイルをダウンロードして保存する必要があります。

| 説明        | ファイル名 |
|--------------------|-----------|
| 会社のロゴ画像 | [会社の logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>コンテンツ

- [法人を構成する](#ConfigureLegalEntity)
- [ER フレームワークの構成](#ConfigureFramework)

    - [ER パラメーターの構成](#ConfigureParameters)
    - [ER 構成 プロバイダーをアクティブにする](#ActivateProvider)

        - [ER 構成 プロバイダーの一覧を確認](#ReviewProvidersList)
        - [新しい ER 構成 プロバイダーを追加](#AddProvider)
        - [新しい ER 構成プロバイダーの有効化](#ActivateAddedProvider)

- [標準 ER 形式 コンフィギュレーションをインポート](#ImportERSolution1)

    - [標準 ER コンフィギュレーションをインポート](#ImportERFormat)
    - [インポートされた ER コンフィギュレーションのレビュー](#ReviewImportedERSolution)

- [標準 ER 形式を使用した自由書式の請求書を印刷する](#PrintInvoice1)

    - [印刷管理を設定する](#ConfigurePrintManagement1)
    - [自由書式の請求書を印刷する](#ProcessInvoice1)

- [標準 ER 形式のカスタマイズ](#CustomizeProvidedFormat)

    - [カスタム形式の作成](#DeriveProvidedFormat)
    - [カスタム形式を編集する](#ConfigureDerivedFormat)
    - [カスタム形式を実行可能としてマークする](#MarkFormatRunnable)

- [カスタム ER 形式を使用した自由書式の請求書を印刷する](#PrintInvoice2)

    - [印刷管理を設定する](#ConfigurePrintManagement2)
    - [自由書式の請求書を印刷する](#ProcessInvoice2)

- [追加リソース](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>法人を構成する

1. **組織管理** \> **組織** \> **法人** の順に移動します。
2. **法人** ページの **会社のロゴ画像のレポート** クイック タブで、**変更** を選択します。
3. **アップロードする画像ファイルの選択** ダイアログ ボックスで、**参照** を選択して、以前にダウンロードした **Company logo.png** ファイルを選択します。
4. **保存** を選択し、**法人** ページを閉じます。

![法人ページで選択された会社のロゴ画像。](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a> ER フレームワークをコンフィギュレーション

電子申告の機能コンサルタント ロールのユーザーは、ER フレームワークを使用して標準 ER 形式のカスタム バージョンをデザインする前に、最低限の ER パラメータのセットをコンフィギュレーションする必要があります。

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER パラメーターのコンフィギュレーション

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**関連リンク** セクションで、**電子申告パラメーター** を選択します。
3. **電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。
4. **添付** タブで、次のパラメーターを設定します:

    - **コンフィギュレーション** フィールドで、**USMF** 社の **ファイル** タイプを選択します。
    - **ジョブ アーカイブ**、**一時的**、**ベースライン**、および **その他** フィールドで、**ファイル** タイプを選択します。

ER パラメーターについては、[ER フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md) を参照してください。

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a> ER コンフィギュレーション プロバイダーをアクティブにする

追加されたすべての ER 構成は、ER 構成プロバイダーによって所有されているものとしてマークされます。 **電子申告** ワークスペースで有効化された ER 構成プロバイダーは、この目的に使用されます。 したがって、ER 構成に追加または編集する前に、**電子申告** ワークスペースの ER 構成プロバイダーを有効化する必要があります。

> [!NOTE]
> コンフィギュレーションの所有者のみが ER コンフィギュレーションを編集できます。 ER コンフィギュレーションを編集する前に、適切な ER 構成プロバイダーを **電子申告** ワークスペースで有効化する必要があります。

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a> ER コンフィギュレーション プロバイダーの一覧をレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。
3. **構成プロバイダー テーブル** ページでは、各プロバイダー レコードの名前と URL が一意になります。 このページの内容をレビューします。 **Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER 構成プロバイダーを追加](#AddProvider) します。

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a> 新しい ER 構成プロバイダーを追加

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。
3. **構成プロバイダー** ページで、**新規** を選択します。
4. **名前** フィールドに、**Litware, Inc.** と入力
5. **インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。
6. **保存** を選択します。

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>新しい ER 構成プロバイダーの有効化

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの **構成プロバイダー** セクションで、**Litware, Inc.** を選び、**有効に設定** を選択します。

ER コンフィギュレーション プロバイダーについては、[コンフィギュレーション プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a> 標準 ER 形式コンフィギュレーションをインポート

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a> 標準 ER コンフィギュレーションをインポート

Dynamics 365 Finance の現在のインスタンスに標準的な ER 構成を追加するには、そのインスタンスに構成された ER [リポジトリ](general-electronic-reporting.md#Repository) からインポートする必要があります。

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して **Microsoft** プロバイダーのリポジトリの一覧を表示します。
3. **コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。 [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md) に接続するための承認を求めるメッセージが表示されたら、その承認の指示に従います。
4. **構成リポジトリ** ページの、左ウィンドウの構成ツリーで、**自由書式の請求書 (Excel)** 形式の構成を選択します。
5. **バージョン** クイック タブで、選択した ER 形式コンフィギュレーションの最新バージョン (**240.112** など) を選択します。
6. **インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。

![構成リポジトリ ページに 標準 ER コンフィギュレーションをインポートします。](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> [グローバル リポジトリ](er-download-configurations-global-repo.md) へのアクセスに問題がある場合は、Microsoft Dynamics Lifecycle Services (LCS) から[構成をダウンロード](download-electronic-reporting-configuration-lcs.md) ができます。

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a> インポートされた ER コンフィギュレーションのレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。
3. **構成** ページにある左ペインの構成ツリーで、**請求書モデル** を展開します。
4. 選択した **自由書式の請求書 (Excel)** ER 形式に加えて、その他の必要な ER コンフィギュレーションがインポートされます。 コンフィギュレーションツリーで、次の ER コンフィギュレーションが使用可能であることを確認してください。

    - **請求書モデル** – このコンフィギュレーションには、請求書発行ビジネス ドメインのデータ構造を表すデータ モデル ER コンポーネントが含まれています。
    - **請求書モデル マッピング** – この構成には、実行時にデータ モデルがアプリケーション データが格納される方法を記述するモデル マッピング ER コンポーネントが含まれています。
    - **自由書式の請求書 (Excel)** – この構成には、形式と形式マッピング ER コンポーネントが含まれています。 形式コンポーネントは、Excel 形式のテンプレートに基づいてレポートのレイアウトを指定します。 形式マッピング コンポーネントは、モデル データ ソースが含まれており、このデータ ソースが実行時にレポート レイアウトを埋めるためにどのように使用されるかを指定します。

![コンフィギュレーション ページのインポートされた ER コンフィギュレーション。](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>標準 ER 形式を使用した自由書式の請求書を印刷する

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>印刷管理を設定します

1. **売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。
2. **自由形式の請求書** ページで、**FTI-00000002** 請求書を選択し、アクション ウィンドウの **請求書** タブの **印刷管理** グループで、**印刷管理** を選択します。
3. **印刷管理設定** ページの左側のツリーで、**モジュール - 売掛金勘定 \> ドキュメント \> 自由書式の請求書** を展開し、**元の \<Default\>** 品目を選択します。
4. **レポート形式** フィールドで、**自由書式の請求書 (Excel)** を選択します。
5. **Esc** キーを選択して、**印刷管理設定** ページを終了し、**自由書式の請求書** ページに戻ります。

![印刷管理の設定ページにおける標準 ER 形式による自由書式の請求書の印刷管理設定。](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>自由書式の請求書を印刷する

1. **自由形式の請求書** ページで、**FTI-00000002** 請求書が選択されていることを確認して、アクション ウィンドウの **請求書** タブの **ドキュメント** グループで、**印刷** \> **選択済** を選択します。
2. 生成された請求書を Excel 形式でダウンロードし、プレビュー用に開きます。
3. 指定された ER 形式の Excel テンプレートの構造に従って、生成された請求書のページ フッターには、現在のページ番号とレポートのページ合計数に関する情報が含まれます。

![生成された自由書式の請求書。](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a> 標準 ER 形式のカスタマイズ

このセクションの例では、Microsoft が提供する ER コンフィギュレーションを使用して、Excel 形式の自由書式の請求書を生成できます。 ただし、生成される請求書のページ フッターに会社のロゴ画像配置のカスタマイズを追加する必要があります。

この場合、Litware, Inc. の担当者として、Microsoft から提供されている **自由書式の請求書 (Excel)** コンフィギュレーションに基づく新しい ER 形式のコンフィギュレーションを作成 (派生) する必要があります。

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a> カスタム形式の作成

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの左ウィンドウの構成ツリーで、**請求書モデル** を展開し、**自由書式の請求書 (Excel)** を選択します。 Litware, Inc. は、この ER 形式コンフィギュレーションのインポートされたバージョン (**240.112** など) をカスタム バージョンのベースとして使用します。
3. **コンフィギュレーションの作成** を選択して、ドロップ ダウンのダイアログ ボックスを開きます。 このダイアログ ボックスを使用して、カスタムの支払形式の新しいコンフィギュレーションを作成します。
4. **新規** フィールド グループで、**派生元の名前: 自由書式の請求書 (Excel)、Microsoft** オプションを選択します。
5. **名前** フィールドに、**自由書式の請求書 (Excel) カスタム** を入力します。
6. **構成の作成** を選択します。

![コンフィギュレーションの作成ドロップダウン ダイアログ ボックスでの、カスタムの支払形式用コンフィギュレーションの作成。](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

**自由書式の請求書 (Excel) カスタム** ER 形式のコンフィギュレーションのバージョン 240.112.1 が作成されます。 このバージョンは **ドラフト** の状態で、編集することができます。 カスタム ER 形式の現在の内容は、Microsoft が提供する形式の内容と一致しています。

![構成ページで作成された ER 形式コンフィギュレーションの新しいバージョン。](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>カスタム形式を編集する

会社のロゴ画像がレポートの各ページのフッターに配置されるカスタム形式を構成します。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの左ウィンドウの構成ツリーで、**支払モデル** を展開し、**自由書式の請求書 (Excel) カスタム** を選択します。
3. **バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **240.112.1** を選択します。
4. **デザイナー** をクリックします。
5. **形式デザイナー** ページで、**詳細表示** を選択して形式要素の詳細情報が表示されます。
6. 次の要素を展開し、確認します:

    - **Excel** タイプの **自由書式の請求書** 要素。 この要素は、Excel ブック形式で請求書を生成するために使用されます。
    - **シート** タイプの **自由書式の請求書 \\ 請求書** 要素。 この要素は、生成された Excel ブックのワークシートを生成するために使用されます。
    - **フッター** タイプの **自由書式の請求書 \\ 請求書 \\ フッター** 要素。 この要素は、請求書のフッターの入力に使用されます。

7. **自由書式の請求書 \\ 請求書 \\ フッター** 要素を選択します。

    ![ER 操作デザイナーのフッター要素。](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > 生成された請求書のすべてのページ フッターには、現在のページ番号とレポートのページの合計数に関する情報が含まれます。 ご覧のように、**自由書式の請求書 \\ 請求書 \\フッター** 要素には子要素は含まれません。 したがって、使用されている Excel テンプレートは、すべてのレポートのフッターの中央にページングの詳細を表示するように構成されます。

8. **追加** をクリックし、追加する形式要素の **Excel \\ 画像** を選択します。

    1. **配置** フィールドで、**右** を選択します。
    2. **高さをスケール** フィールドで、**相対** を選択します。
    3. **割合でスケール** フィールドに **70** と入力します。
    4. **OK** を選択します。

        > [!NOTE]
        > **Excel \\ 画像** 要素は、会社のロゴ画像を追加し、ページ フッターの右側に配置するために使用されます。

    ![コンポーネントのプロパティ ダイアログ ボックスでの画像要素のプロパティ。](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. 左側の形式構造ツリーで、追加した **画像** 要素を選択し、**マッピング** タブで **モデル** データ ソースを展開します。
10. **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** を展開して、**model.InvoiceBase.CompanyInfo.Logo** データ ソース フィールドを選択します。 [コンテナー](er-formula-supported-data-types-composite.md#container) タイプのデータ ソース フィールドでは、会社のロゴ画像がメディア コンテンツとして公開されます。
11. **バインド** を選択します。 **画像** 形式要素は、**model.InvoiceBase.CompanyInfo.Logo** データ ソース フィールドにバインドされるようになります。 このため、実行時に、会社のロゴ画像は生成される請求書のフッターに配置されます。

    ![画像形式要素は、ER 操作デザイナーの model.InvoiceBase.CompanyInfo.Logo データ ソース フィールドにバインドされます。](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. **保存** を選択し、**デザイナー** ページを閉じます。

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>カスタム形式を実行可能としてマークする

カスタム書式の最初のバージョンが作成されたため、ステータスが **ドラフト** になり、テストを目的として形式を実行できます。 レポートを実行するには、カスタム ER 形式を参照する支払方法を使用して、仕入先支払を処理します。 既定では、申請から ER 形式を呼び出すと、**完了済** または **共有** のステータスを持つバージョンのみが考慮されます。 この動作により、未完成の設計を持つ ER 形式が使用されるのを防ぐことができます。 ただし、テストの実行には、**ドラフト** のステータスを持つ ER 形式のバージョンをアプリケーションに強制的に使用させることができます。 これにより、変更が必要な場合は、現在の形式バージョンを調整できます。 詳細については、[適合性](electronic-reporting-destinations.md#applicability) を参照してください。

ER 形式のドラフト バージョンを使用するには、ER 形式を明示的にマークする必要があります。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3. **ユーザー パラメーター** ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。
4. **編集** を選択して現在のページを編集可能にして、**自由書式の請求書 (Excel) カスタム** を選択します。
5. **ドラフトの実行** オプションを **はい** に設定します。

![構成ページでカスタム形式を実行可能とマークします。](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>カスタム ER 形式を使用した自由書式の請求書を印刷する

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>印刷管理を設定します

1. **売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。
2. **自由形式の請求書** ページで、**FTI-00000002** 請求書を選択し、アクション ウィンドウの **請求書** タブの **印刷管理** グループで、**印刷管理** を選択します。
3. **印刷管理設定** ページの左側のツリーで、**モジュール - 売掛金勘定** \> **ドキュメント** \> **自由書式の請求書** を展開し、**元の** **\<Default\>** 品目を選択します。
4. **レポート形式** フィールドで、**自由書式の請求書 (Excel) カスタム** を選択します。
5. **Esc** を選択して、**印刷管理設定** ページを終了し、**自由書式の請求書** ページに戻ります。

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>自由書式の請求書を印刷する

1. **自由形式の請求書** ページで、**FTI-00000002** 請求書が選択されていることを確認して、アクション ウィンドウの **請求書** タブの **ドキュメント** グループで、**印刷** \> **選択済** を選択します。
2. 生成された請求書を Excel 形式でダウンロードし、プレビュー用に開きます。
3. カスタム ER 形式の構造に従って、生成される請求書のページ フッターには、レポートのページングに関する情報に加えて、会社のロゴ画像が含まれることに注意してください。

![生成された自由書式の請求書は、ページ フッターに会社のロゴ画像が含まれています。](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>追加リソース

- [ドキュメントを Excel 形式で生成するためのコンフィギュレーションを設計する](er-fillable-excel.md)
- [ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md)
