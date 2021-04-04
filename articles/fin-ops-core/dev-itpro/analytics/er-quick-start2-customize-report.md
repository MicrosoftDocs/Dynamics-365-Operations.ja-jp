---
title: ER 形式を調整してカスタム電子ドキュメントを生成
description: このトピックでは、Microsoft が提供する電子レポート (ER) 形式を調整して、カスタム電子ドキュメントを生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c643c913d9bc9233c891709593dff995284e2e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569000"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>ER 形式を調整してカスタム電子ドキュメントを生成

[!include[banner](../includes/banner.md)]

このトピックの手順では、システム管理者または電子レポート機能コンサルタントのロールのユーザーが次のタスクを実行する方法について説明します:

- [電子申告 (ER) フレームワーク](general-electronic-reporting.md) のパラメーターを構成します。
- Microsoft が提供し、[仕入先支払](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) の処理中に、支払いファイルを生成するために使用する ER コンフィギュレーションをインポートします。
- Microsoft が提供する標準 ER 形式コンフィギュレーションのカスタム バージョンを作成します。
- カスタム ER 形式コンフィギュレーションを変更して、特定銀行の要求を満たす支払いファイルを生成します。
- カスタム ER 形式コンフィギュレーションで、標準 ER 形式コンフィギュレーションに対して行われた変更を採用します。

次の手順はすべて **GBSI** 社で行うことができます。 コーディングは必要ありません。

- [ER フレームワークのコンフィギュレーション](#ConfigureFramework)

    - [ER パラメーターのコンフィギュレーション](#ConfigureParameters)
    - [ER コンフィギュレーション プロバイダーをアクティブにする](#ActivateProvider)

        - [ER 構成 プロバイダーの一覧を確認](#ReviewProvidersList)
        - [新しい ER コンフィギュレーション プロバイダーを追加](#ActivateProvider)
        - [ER コンフィギュレーション プロバイダーをアクティブにする](#ActivateAddedProvider)

- [標準 ER 形式 コンフィギュレーションをインポート](#ImportERSolution1)

    - [標準 ER コンフィギュレーションをインポート](#ImportERFormat1)
    - [インポートされた ER コンフィギュレーションのレビュー](#ReviewImportedERSolution)

- [処理用仕入先支払の準備](#PrepareVendorPayment)

    - [仕入先アカウントの銀行情報の追加](#AddBankAccount)
    - [仕入先支払の入力](#EnterVendorPayment)

- [標準 ER 形式を使用した仕入先支払の処理](#ProcessVendorPayment1)

    - [電子支払方法の設定](#ConfigureMethodOfPayment1)
    - [仕入先支払のプロセス](#ProcessPayment1)

- [標準 ER 形式のカスタマイズ](#CustomizeProvidedFormat)

    - [カスタム形式の作成](#DeriveProvidedFormat)
    - [カスタム形式の編集](#ConfigureDerivedFormat)
    - [カスタム形式を実行可能としてマーク](#MarkFormatRunnable)

- [カスタム ER 形式を使用した仕入先支払の処理](#ProcessVendorPayment2)

    - [電子支払方法の設定](#ConfigureMethodOfPayment2)
    - [仕入先支払のプロセス](#ProcessPayment2)

- [標準 ER 形式コンフィギュレーションの新バージョンをインポート](#ImportERSolution2)

    - [標準 ER コンフィギュレーションの新バージョンをインポート](#ImportERFormat2)
    - [インポートされた ER 形式コンフィギュレーションのレビュー](#ReviewImportedERFormat)

- [インポートされた形式の新バージョンの変更をカスタム形式で採用](#AdoptNewBaseVersion)

    - [カスタム形式の現在のドラフト バージョンを完了](#CompleteDerivedFormat)
    - [カスタム形式を新しい基準バージョンにリベース](#RebaseDerivedFormat)
    - [リベースされた ER 形式を使用して仕入先支払の処理](#ProcessPayment3)

- [追加リソース](#References)

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
> ER 構成の所有者のみが編集できます。 したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a> ER コンフィギュレーション プロバイダーの一覧をレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。
3. **構成プロバイダー テーブル** ページでは、各プロバイダー レコードの名前と URL が一意になります。 このページの内容をレビューします。 **Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER コンフィギュレーション プロバイダーを追加](#ActivateProvider) します。

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a> 新しい ER コンフィギュレーション プロバイダーを追加

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**関連リンク** セクションで、**構成プロバイダー** を選択します。
3. **構成プロバイダー** ページで、**新規** を選択します。
4. **名前** フィールドに、**Litware, Inc.** と入力
5. **インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。
6. **保存** を選択します。

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a> ER コンフィギュレーション プロバイダーをアクティブにする

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの **構成プロバイダー** セクションで、**Litware, Inc.** を選び、**有効に設定** を選択します。

ER コンフィギュレーション プロバイダーについては、[コンフィギュレーション プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a> 標準 ER 形式コンフィギュレーションをインポート

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a> 標準 ER コンフィギュレーションをインポート

標準 ER コンフィギュレーションを現在の Microsoft Dynamics 365 Finance のインスタンスに追加するには、インスタンスにコンフィギュレーションされた ER [リポジトリ](general-electronic-reporting.md#Repository) からインポートする必要があります。

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。
3. **コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。 Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。
4. **コンフィギュレーション リポジトリ** ページにて、ウィンドウの左側のコンフィギュレーション ツリーで、**BACS (英国)** 形式コンフィギュレーションを選択します。
5. **バージョン** クイック タブで、選択した ER 形式コンフィギュレーションのバージョン **1.1** を選択します。
6. **インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。

![レポジトリ ページのコンフィギュレーション](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> [グローバル リポジトリ](er-download-configurations-global-repo.md) へのアクセスに問題がある場合は、Microsoft Dynamics Lifecycle Services (LCS) から[コンフィギュレーションをダウンロード](download-electronic-reporting-configuration-lcs.md) ができます。

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a> インポートされた ER コンフィギュレーションのレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。
3. **コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開します。
4. 選択した **BACS (英国)** ER 形式に加えて、その他の必要な ER コンフィギュレーションがインポートされたことに注意してください。 コンフィギュレーションツリーで、次の ER コンフィギュレーションが使用可能であることを確認してください。

    - **支払モデル** – このコンフィギュレーションには、支払業務ドメインのデータ構造を表す[データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components) ER コンポーネントが含まれています。
    - **支払モデルのマッピング 1611** – このコンフィギュレーションには、実行時にデータ モデルがアプリケーション データが格納される方法を記述する[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components) ER コンポーネントが含まれています。
    - **BACS (英国)** – このコンフィギュレーションには、[形式](general-electronic-reporting.md#FormatComponentOutbound) と形式マッピング ER コンポーネントが含まれています。 形式コンポーネントは、レポートのレイアウトを指定します。 形式マッピング コンポーネントには、モデル データソースが含まれており、実行時にこのデータソースを使用することによってレポートのレイアウトがどのように入力されるかを指定します。

![構成ページ](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a> 処理用仕入先支払の準備

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a> 仕入先アカウントの銀行情報の追加

後に参照される仕入先アカウントの銀行情報を、登録済の支払に追加する必要があります。

1. **買掛金勘定** \> **仕入先** \> **すべての仕入先** に移動します。
2. **すべての仕入先** ページで、**GB_SI_000001** 仕入先アカウントを選択し、アクション ウィンドウの **仕入先** タブの **設定** グループで、**銀行アカウント** を選択します。
3. **仕入先の銀行アカウント** ページで、**新規** を選択して、次の情報を入力します:

    1. **銀行アカウント** フィールドで、 **GBP OPER** を入力します。
    2. **銀行グループ** フィールドで、**BankGBP** を選択します。
    3. **銀行アカウント番号** フィールドで、**202015** を入力します。
    4. **SWIFT コード** フィールドで、<a id="DefineSWIFTCode"></a>**CHASDEFXXXX** を入力します。
    5. **IBAN** フィールドで、**GB33BUKB20201555555555** を入力します。
    6. **支店コード** フィールドで、既定値 <a id="DefineRoutingNumber"></a>**123456** をそのまま使用します。

    ![仕入先の銀行アカウント ページ](./media/er-quick-start2-bank-account.png)

4. **保存** を選択します。
5. ページを閉じます。
6. **すべての仕入先** ページで、**GB_SI_000001** 仕入先アカウントを開きます。
7. 必要に応じて、仕入先の詳細ページで、**編集** を選びページの編集が可能です。
8. **支払い** クイックタブの **銀行アカウント** フィールドで、**GBP OPER** を選択します。

    ![仕入先の詳細ページ](./media/er-quick-start2-bank-account-reference.png)

9. **保存** を選択します。
10. ページを閉じます。

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a> 仕入先支払の入力

[支払提案](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) を使用して、新しい仕入先の支払いを入力する必要があります。

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. **仕入先支払仕訳帳** ページで、**新規** を選択します。
3. **名前** フィールドで、**VendPay** を選択します。
4. **明細行** を選択します。
5. **支払提案** \> **支払提案の作成** の順にクリックします。
6. **仕入先支払提案** ダイアログボックスで、**GB_SI_000001** 仕入先アカウントのみのレコードをフィルター処理するための条件をコンフィギュレーションし、**OK** を選択します。
7. **00000007_Inv** 請求書の明細行を選び、**支払作成** を選択します。

    ![仕入先支払提案のダイアログ ボックス](./media/er-quick-start2-payment-proposal.png)

8. 入力された支払いが、**電子** 支払方法を使用するようにコンフィギュレーションされていることを確認します。

    ![仕入先支払のページ](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a> 標準 ER 形式を使用した仕入先支払の処理

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a> 電子支払方法の設定

インポートされた ER 形式のコンフィギュレーションを使用するには、電子支払方法をコンフィギュレーションする必要があります。

1. **買掛金勘定** \> **支払設定** \> **支払方法** に移動します。
2. **支払方法 - 仕入先** ページで、ウィンドウの左側の **電子** 支払方法を選択します。
3. **編集** を選択します。
4. **ファイル形式** のクイックタブで、**一般的なエクスポート形式** のオプションを **はい** に設定します。
5. **形式の構成のエクスポート** フィールドで、**BACS (英国)** 形式コンフィグレーションを選択します。

    ![支払方法 - 仕入先ページ](./media/er-quick-start2-method-of-payment1.png)

6. **保存** を選択します。

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a> 仕入先支払のプロセス

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. **仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択し、**明細行** を選択します。
3. **仕入先支払** ページで、**支払生成** を選択します。
4. **支払生成** ダイアログ ボックスで、次の情報を入力してください:

    - **支払方法** フィールドで、**電子** を選択します。
    - **銀行口座** フィールドで、 **GBSI OPER** を選択します。

5. **OK** を選択します。
6. **電子申告パラメータ** ダイアログ ボックスで、**印刷の管理レポート** オプションを **はい** に選定して、**OK** を選択します。

    ![電子申告パラメーター ダイアログ ボックスのページ](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > 支払ファイルに加えて、管理レポートを生成できるようになります。

7. Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:

    - Excel 形式の管理レポート
    - TXT 形式の支払ファイル

        提供された ER 形式の[構造](#PositionRoutingNumber) に従って、生成されたファイルの支払明細行は、コンフィギュレーションされた銀行アカウントの[定義済み](#DefineRoutingNumber) 支店コードで開始してください。

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a> 標準 ER 形式のカスタマイズ

このセクションに表示されている例では、Microsoft が提供する ER コンフィギュレーションを使用して仕入先支払ファイルを BACS 形式で生成しますが、特定の銀行の要求をサポートするには、カスタマイズを追加する必要があります。 また、ER コンフィギュレーションの新しいバージョンが使用可能になったときにカスタム形式をアップグレードすることもできます。 ただし、最小限のコストでアップグレードを実行できるようにする必要があります。

この場合、Litware, Inc. の担当者として、**BACS (英国)** Microsoft から提供されているコンフィギュレーションを基準として使用して、新しい ER 形式のコンフィギュレーションを作成 (派生) する必要があります。

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a> カスタム形式の作成

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国)** を選択します。 Litware, Inc. は、この ER 形式コンフィギュレーションのバージョン 1.1 をカスタム バージョンのベースとして使用します。
3. **コンフィギュレーションの作成** を選択して、ドロップ ダウンのダイアログ ボックスを開きます。 このダイアログ ボックスを使用して、カスタムの支払形式の新しいコンフィギュレーションを作成することができます。
4. **新しい** フィールド グループで、**派生元の名前: BACS (英国)、Microsoft** オプションを選択します。
5. **名前** フィールドに、**BACS (英国カスタム)** と入力します。

    ![構成の作成ドロップダウン ダイアログボックス](./media/er-quick-start2-add-derived-format.png)

6. **コンフィギュレーションの作成** を選択します。

**BACS (英国カスタム)** ER 形式コンフィギュレーションのバージョン 1.1.1 が作成されます。 このバージョンは **ドラフト** の[状態](general-electronic-reporting.md#component-versioning) で、編集することができます。 カスタム ER 形式の現在の内容は、Microsoft が提供する形式の内容と一致しています。

![構成ページ](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a> カスタム形式の編集

銀行固有の要件を満たすには、カスタム形式をコンフィギュレーションする必要があります。 たとえば、銀行は生成される支払ファイルに、処理済の仕入先支払にてエージェント ロールが割り当てられている銀行のワールドワイド インターバンク ファイナンシャル テレコミュニケーション (SWIFT) コードを含めることを要求する場合があります。 SWIFT コードは、世界中の特定の銀行を識別する国際銀行コードです。 銀行識別子コード (BICs) とも呼ばれます。 SWIFT コードは半角 11 文字で入力する必要があり、生成された支払ファイルの各支払明細行の先頭に入力する必要があります。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国カスタム)** を選択します。
3. **バージョン** クイック タブで、選択したコンフィギュレーションのバージョン **1.1.1** を選択します。
4. **デザイナー** をクリックします。
5. **形式デザイナー** ページで、**詳細表示** を選択して形式要素の詳細情報が表示されます。
6. 次の要素を展開し、確認します:

    - **フォルダー** タイプの **BACSReportsFolder** 要素。 この要素は、ZIP 形式で出力を生成するために使用されます。
    - **ファイル** タイプの **ファイル** 要素。 この要素は、TXT 形式で支払ファイルを生成するために使用されます。
    - **シーケンス** タイプの **取引** 要素。 この要素は、支払ファイルで単一の支払明細行を生成するために使用されます。
    - **シーケンス** タイプの **取引** 要素。 この要素は、単一支払明細行の個々のフィールドを生成するために使用されます。

7. **トランザクション** 要素を選択します。

    ![ER 操作デザイナーのトランザクション要素](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <a id="PositionRoutingNumber"></a> すべての支払明細行が銀行支店コードで開始するには、指定されたレポートはコンフィギュレーションされます。 **VendBankRouteNum** 形式の要素は、この目的に使用されます。 

8. **追加** をクリックし、追加する形式要素の **テキスト\\文字列** を選択します:

    1. **名前** フィールドに、**vendBankSWIFT** と入力します。
    2. **最小の長さ** フィールドに **11** を入力します。
    3. **最大の長さ** フィールドに **11** を入力します。
    4. **OK** を選択します。

    > [!NOTE]
    > **VendBankSWIFT** 要素は、生成されたファイルに仕入先銀行の SWIFT コードを入力するために使用されます。

9. 形式構造ツリーで、**vendBankSWIFT** を選択します。
10. **上へ移動** を選択して、選択した形式要素がレベル 1 上に移動します。 **vendBankSWIFT** 要素が、親 **取引** 要素下の <a id="PositionSWIFTCode"></a> 最初の要素になるまで、この手順を繰り返します。

    ![ER 操作デザイナーのトランザクション下の最初の要素なる VendBankSWIFT](./media/er-quick-start2-derived-format1.png)

11. **vendBankSWIFT** がまだ形式構造ツリーで選択されている状態で、**マッピング** タブを選択し、**モデル** データ ソースを展開します。
12. **model.Payment** \> **model.Payment.CreditorAgent** を展開し、**model.Payment.CreditorAgent.BICFI** データ ソース フィールドを選択します。 このデータ ソースのフィールドでは、処理済の仕入先支払で、エージェント ロールが割り当てられている仕入先銀行の SWIFT コードが公開されます。
13. **バインド** を選択します。 **vendBankSWIFT** 形式要素は、SWIFT コードが生成された支払いファイルに入力されるように、**model.Payment.CreditorAgent BICFI** データ ソース フィールドにバインドされるようになります。

    ![ER 操作デザイナーで model.Payment.CreditorAgent.BICFI データ ソース フィールドにバインドされた vendBankSWIFT 形式要素](./media/er-quick-start2-derived-format2.png)

14. **保存** を選択します。
15. デザイナー ページを閉じます。

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a> カスタム形式を実行可能としてマーク

これで、カスタム書式の最初のバージョンが作成され、ステータスが **ドラフト** になり、テストを目的として実行できます。 レポートを実行するには、カスタム ER 形式を参照する支払方法を使用して、仕入先支払を処理する必要があります。 既定では、申請から ER 形式を呼び出すとき、**完了済** または **共有** のステータスを持つバージョンのみが[考慮](general-electronic-reporting.md#component-versioning) されます。 この動作により、未完成の設計を持つ ER 形式が使用されるのを防ぐことができます。 ただし、テストの実行には、**ドラフト** のステータスを持つ ER 形式のバージョンをアプリケーションに強制的に使用させることができます。 これにより、変更が必要な場合は、現在の形式バージョンを調整できます。 詳細については、[適合性](electronic-reporting-destinations.md#applicability) を参照してください。

ER 形式のドラフト バージョンを使用するには、ER 形式を明示的にマークする必要があります。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3. **ユーザー パラメーター** ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。
4. **編集** を選択し、必要に応じて現在のページを編集可能にします。
5. ウィンドウの左側にあるコンフィグレーション ツリーで、**BACS (英国カスタム)** を選択します。
6. **ドラフトの実行** オプションを **はい** に設定します。

    ![コンフィギュレーション ページのドラフト実行オプション](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a> カスタム ER 形式を使用した仕入先支払の処理

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a> 電子支払方法の設定

カスタム ER 形式を使用して仕入先支払を処理するには、電子支払方法をコンフィギュレーションする必要があります。

1. **買掛金勘定** \> **支払設定** \> **支払方法** に移動します。
2. **支払方法 - 仕入先** ページで、ウィンドウの左側の **電子** 支払方法を選択します。
3. **編集** を選択します。
4. **ファイル形式** クイック タブで、**一般的な電子エクスポート形式** オプションを **はい** に設定します。
5. **形式の構成のエクスポート** フィールドで、**BACS (英国カスタム)** 形式コンフィグレーションを選択します。

    ![支払方法 - 仕入先ページ](./media/er-quick-start2-method-of-payment2.png)

6. **保存** を選択します。

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a> 仕入先支払のプロセス

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. **仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択します。
3. **明細行** を選択します。
4. **仕入先支払** ページのグリッドの上で、**支払ステータス** \> **なし** を選択します。
5. **支払の生成** を選択します。
6. **支払生成** ダイアログ ボックスで、次の情報を入力してください:

    - **支払方法** フィールドで、**電子** を選択します。
    - **銀行口座** フィールドで、 **GBSI OPER** を選択します。

7. **OK** を選択します。
8. **電子申告パラメータ** ダイアログ ボックスで、**印刷の管理レポート** オプションを **はい** に選定して、**OK** を選択します。

    > [!NOTE]
    > 支払ファイルに加えて、管理レポートのみ生成できるようになります。

9. Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:

    - Excel 形式の管理レポート
    - TXT 形式の支払ファイル

        カスタム ER 形式の構造に従って、生成されたファイルの支払明細行は、支払が処理された仕入先の銀行アカウントに対して[入力](#DefineSWIFTCode) された SWIFT コードで[開始](#PositionSWIFTCode) されることに注意してください。

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a> 標準 ER 形式コンフィギュレーションの新バージョンをインポート

このセクションに表示されている例では、サポート技術情報の記事 [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) に関する通知が表示されます。 Microsoft が発行した **BACS (英国)** ER 形式の新バージョンについて通知されます。 この新バージョンでは、管理レポートに加えて、仕入先支払の処理中にユーザーが支払通知レポートと出席メモ レポートを生成できます。 この機能の使用を開始する必要があります。

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a> 標準 ER コンフィギュレーションの新バージョンをインポート

ER コンフィギュレーションの新バージョンを現在の Finance インスタンスに追加するには、コンフィギュレーションした ER [リポジトリ](general-electronic-reporting.md#Repository) からインポートする必要があります。

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ コンフィグレーション** ページの **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択し、**リポジトリ** を選択して Microsoft プロバイダーのリポジトリの一覧を表示します。
3. **コンフィギュレーション リポジトリ** ページで、**グローバル** タイプのリポジトリを選択し、**開く** を選択します。 Regulatory Configuration Service に接続するために承認を求める場合は、その承認の指示に従います。
4. **コンフィギュレーション リポジトリ** ページにて、ウィンドウの左側のコンフィギュレーション ツリーで、**BACS (英国)** 形式コンフィギュレーションを選択します。
5. **バージョン** クイック タブで、選択した ER 形式コンフィギュレーションのバージョン **3.3** を選択します。
6. **インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。

![レポジトリ ページのコンフィギュレーション](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> [グローバル化 リポジトリ](er-download-configurations-global-repo.md) のアクセスに問題がある場合は、代わりに LCS から[コンフィグレーションをダウンロード](download-electronic-reporting-configuration-lcs.md) できます。

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a> インポートされた ER 形式コンフィギュレーションのレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。
3. **コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国)** を選択します。
4. **バージョン** FastTab で、バージョン **3.3** を選択します。
5. **デザイナー** をクリックします。
6. **形式デザイナー** ページで、**BACSReportsFolder** 形式要素を展開できます。
7.  バージョン 3.3 には、仕入先支払の処理時に、支払通知レポートを生成するために使用される **PaymentAdviceReport** 形式要素が含まれていることに注意してください。

    ![ER 操作デザイナーの PaymentAdviceReport 形式要素](./media/er-quick-start2-imported-solution2.png)

8. デザイナー ページを閉じます。

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a> インポートされた形式の新バージョンの変更をカスタム形式で採用

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a> カスタム形式の現在のドラフト バージョンを完了

カスタム形式の現在のステータスを保持する場合は、そのステータスを **ドラフト** から **完了済** に変更して、ドラフト バージョン 1.1.1 を完了します。

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。
3. **コンフィギュレーション** ページのウィンドウ左側のコンフィギュレーション ツリーで、**支払モデル** から **BACS (英国)** を展開して、**BACS (英国カスタム)** を選択します。
4. **バージョン** クイックタブで、**ステータスの変更** \> **完了済**、そして **OK** を選択します。

バージョン 1.1.1 のステータスは、**ドラフト** から **完了済** に変更され、バージョンは読み取り専用になります。 新しい編集可能バージョンの 1.1.2 が追加され、ステータスが **ドラフト** になりました。 このバージョンを使用すると、カスタム ER 形式でさらに変更を加えることができます。

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a> カスタム形式を新しい基本バージョンにリベース

カスタマイズの **BACS (英国)** 形式によるバージョン 3.3 の新機能を使用するには、カスタム コンフィギュレーション **BACS (英国カスタム)** の基本コンフィギュレーション バージョンを変更する必要があります。 このプロセスは、[再ベース中](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)と呼ばれています。 **BACS (英国)** のバージョン 1.1 の代わりに、バージョン 3.3 を使用します。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **コンフィギュレーション** ページでウィンドウの左側のコンフィギュレーション ツリーで、**支払モデル** を展開、**BACS (英国カスタム)** を選択します。
3. **バージョン** クイックタブで、バージョン **1.1.2** を選び、**リベース** を選択します。
4. **リベース** ダイアログ ボックスの **ターゲット バージョン** フィールドで、基準コンフィグレーションのバージョン **3.3** を選択し、新しい基準として適用およびコンフィグレーションを更新するために使用します。

    ![ダイアログ ボックスのリベース](./media/er-quick-start2-rebase1.png)

5. **OK** を選択します。
6. ドラフト バージョンの番号は **1.1.2** から **3.3.2** に変更され、その変更は基本バージョンに反映されます。

    カスタム バージョンと基本バージョンがマージされると、自動的にマージされない形式変更のため、いくつかの矛盾が発見される可能性があります。

    ![コンフィグレーション ページで競合のあるリベース コンフィギュレーション](./media/er-quick-start2-rebase2.png)

    競合が検出された場合は、形式デザイナーで手動で解決する必要があります。

7. **バージョン** FastTab で、バージョン **3.3.2** を選択します。
8. **デザイナー** をクリックします。
9. **形式デザイナー** ページの **詳細** クイックタブで、リベースの競合レコードを選び、**基準値の適用** を選択します。

    ![ER 操作デザイナーのリベース競合レコード](./media/er-quick-start2-rebase3.png)

10. **保存** を選択します。

    リベースの競合レコードは、**詳細** クイックタブに表示されなくなります。

    ![ER 操作デザイナーで解決される競合](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > 基準モデルのバージョン 3 を、この ER 形式で使用する必要があることを確認して、競合を解決しました。

11. **BACSReportsFolder** \> **ファイル** \> **トランザクション** \> **トランザクション** を展開します。
12. **マッピング** タブで、カスタム ER 形式のバージョン 3.3.2 は、使用しているカスタマイズ (**vendBankSWIFT** 形式要素とそのバインド) と Microsoft が提供する基準 ER 形式のバージョン 3.3 の新しい機能の両方 (入れ子になった要素とコンフィグレーションされたバインド と共にある **PaymentAdviceReport**) を含みます。 新しい基準バージョンをカスタマイズして適用した場合は、マウスを数回クリックするだけで変更を適用することができます。

    ![ER 操作デザイナーでの結合形式](./media/er-quick-start2-rebase5.png)

13. デザイナー ページを閉じます。

> [!NOTE]
> リベース アクションを元に戻すことができます。 このリベースをキャンセルするには、**バージョン** クイックタブで **BACS (英国カスタム)** 形式のバージョン **1.1.1** を選び、**このバージョンを取得** を選択します。 バージョン 3.3.2 は、1.1.2 の番号が振り直され、ドラフト バージョン 1.1.2 の内容とバージョン 1.1.1 のコンテンツが一致するようになります。

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a> リベース ER 形式を使用した仕入先支払の処理

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. **仕入先支払仕訳帳** ページで、以前作成した支払仕訳帳を選択します。
3. **明細行** を選択します。
4. **仕入先支払** ページのグリッドの上で、**支払ステータス** \> **なし** を選択します。
5. **支払の生成** を選択します。
6. **支払生成** ダイアログ ボックスで、次の情報を入力してください:

    - **支払方法** フィールドで、**電子** を選択します。
    - **銀行口座** フィールドで、 **GBSI OPER** を選択します。

7. **OK** を選択します。
8. **電子申告パラメータ** ダイアログ ボックスで、次の情報を入力してください:

    - **管理レポートの印刷** オプションを **はい** に設定します。
    - **支払通知の印刷** オプションを **はい** に設定します。

    ![電子申告パラメーター ダイアログ ボックス](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > 支払ファイルに加えて、制御レポートと支払通知レポートの両方を生成できるようになりました。

9. **OK** を選択します。
10. Zip ファイルをダウンロードしてから、次のファイルをそこから抽出します:

    - Excel 形式の管理レポート
    - Excel 形式の支払通知レポート

        ![Excel 形式の支払通知レポート](./media/er-quick-start2-payment-advice-report.png)

    - TXT 形式の支払ファイル

        生成されたファイルの支払明細行は、支払が処理された仕入先の銀行アカウントに対して入力 された SWIFT コードで開始 されることに注意してください。

        ![TXT 形式の支払ファイル](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [ER コンフィギュレーションを Lifecycle Services からダウンロードする](download-electronic-reporting-configuration-lcs.md)
- [ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]