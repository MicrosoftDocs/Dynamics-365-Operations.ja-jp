---
title: 新しい ER ソリューションを設計してカスタム レポートを印刷する
description: このトピックでは、電子レポート (ER) を設計してカスタム レポートを印刷する方法について説明します。
author: NickSelin
ms.date: 08/10/2020
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
ms.openlocfilehash: 90e5381c2d30753e3ad82a38d7361b411f1d7a87
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304396"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>新しい ER ソリューションを設計してカスタム レポートを印刷する

[!include[banner](../includes/banner.md)]

以下の手順では、システム管理者、電子レポートの開発者、電子レポート機能のコンサルタントのロールが付与されているユーザーが、ER のフレーム ワークを構成し、求められる ER ソリューションを構成して、特定のビジネス ドメインのデータにアクセスし、 Microsoft Office 形式でカスタムレポートを生成する方法を説明します。 これらの設定を **USMF** 社を使用して説明します。

- [ER フレームワークの構成](#ConfigureFramework)

    - [ER パラメーターの構成](#ConfigureParameters)
    - [ER 構成 プロバイダーをアクティブにする](#ActivateProvider)

        - [ER 構成 プロバイダーの一覧を確認](#ReviewProvidersList)
        - [新しい ER 構成 プロバイダーを追加](#AddProvider)
        - [ER 構成 プロバイダーをアクティブにする](#ActivateAddedProvider)

- [ドメイン固有のデータ モデルを設計する](#DesignModel)

    - [新たなデータ モデルのインポート](#ImportDataModel)
    - [新しいデータ モデル 構成の作成](#DesignDataModel)

        - [データ モデルに名前をつける](#NameDataModel)
        - [データ モデル フィールドを追加する](#FieldsEntry)
        - [データ モデルの設計を完了する](#CompleteDataModel)

- [構成データ モデルで使用するデータ モデルを設計する](#DesignMapping)

    - [新しいモデル マッピングの構成をインポートする](#ImportModelMapping)
    - [新しいモデル マッピングの構成を作成する](#CreateModelMapping)

        - [新しいモデル マッピングのコンポーネントを設計する](#DesignMappingComponent)
        - [データ ソースを追加してアプリケーション テーブルにアクセスする](#AddMmDataSource1)
        - [データ ソースを追加してアプリケーション リストにアクセスする](#AddMmDataSource2)
        - [ER ラベルを追加して指定した言語でレポートを生成する](#AddMmLabels)
        - [データ ソースを追加して、比較した列挙値の結果をテキスト値に変換する](#AddMmDataSource3)
        - [データ ソースをデータ モデル フィールドにバインドする](#AddMmBindings1)
        - [データ モデルのマッピングを完了する](#CompleteModelMapping)

- [カスタム レポートで使用するテンプレートを設計する](#DesignReportTemplate)
- [形式のデザイン](#DesignFormat)

    - [設計済みフォーマットの構成をインポートする](#FormatImport)
    - [新しい構成の書式設定の作成](#FormatCreate)

        - [レポートのテンプレートをインポートする](#ImportReportTemplate)
        - [フォーマットを構成する](#ConfigureFormat)
        - [レポートのタイトルに使用するデータのバインドを定義する](#DefineFormatBindings)
        - [モデル データ ソースをレビューする](#ReviewModelDataSource)
        - [フォーマットの要素をデータ ソース フィールドにバインドする](#BindFormatElements)

    - [ER から設計済みのフォーマットを実行する](#RunFormatFromER)

- [設計済みのフォーマットを調整する](#TuneFormat)

    - [フォーマットを修正して生成されたドキュメントの名前を変更する](#ModifyToChangeName)
    - [フォーマットを修正して質問の表示順を変更する](#ModifyToOrder)
    - [ER から修正済みのフォーマットを実行する](#RunFormatFromER2)
    - [フォーマットの設計を完了する](#CompleteFormat)

- [アプリケーション アーティファクトを開発して、設計済みのレポートを呼び出す](#DevelopCustomCode)

    - [ソース コードの修正](#ModifySourceCode)

        - [データ コントラクトのクラスを追加する](#DataContractClass)
        - [UI Builder のクラスを追加する](#UIBuilderClass)
        - [データ プロバイダーのクラスを追加する](#DataProviderClass)
        - [ラベル ファイルを追加する](#LabelsFile)
        - [レポート サービス クラスを追加する](#ServiceClass)
        - [レポートのコントローラ クラスを追加する](#ControllerClass)
        - [メニュー項目を追加する](#MenuItem)
        - [メニュー項目をメニューに追加する](#Menu)
        - [Visual Studio プロジェクトをビルドする](#BuildVSProject)

    - [アプリケーションからフォーマットを実行する](#RunFormatFromApp)

- [設計済みの ER ソリューションを調整する](#TuneSolution)

    - [モデルのマッピングを修正する](#ModifyModelMapping)

        - [データ ソースを追加してデータ コントラクト オブジェクトにアクセスする](#AddDataSource1)
        - [データ ソースを追加して ER フォーマット マッピング レコードにアクセスする](#AddDataSource2)
        - [データ ソースを追加して実行中の ER フォーマットのフォーマット マッピング レコードにアクセスする](#AddDataSource3)
        - [データ モデル内の実行中の ER フォーマットの名前を入力する](#AddBinding)
        - [データ モデルのマッピングを完了する](#CompleteModelMapping2)

    - [フォーマットを変更する](#ModifyFormat)

        - [新たなフォーマット要素を追加する](#AddFormatElement)
        - [追加されたフォーマット要素をバインドする](#BindAddedFormatElement)
        - [フォーマットの設計を完了する](#CompleteFormat2)

    - [アプリケーションからフォーマットを実行する](#RunFormatFromApp2)
    - [ER からフォーマットを実行する](#RunFormatFromER3)
    - [オン スクリーン プレビューに使用するフォーマットの出力先を構成する](#ConfigureDestination)
    - [アプリケーションからフォーマットを実行して、PDF ドキュメントでプレビューする](#RunFormatFromApp3)

- [追加リソース](#References)

この例では、[アンケート](../../../human-resources/hr-learning-questionnaires.md)モジュールで使用する新しい ER ソリューションを作成します。 この新しい ER ソリューションを使用すると、Microsoft Excel ワークシートをテンプレートに使用してレポートを設計することができます。 **アンケート** レポートは、既存の SQL Server Reporting Services (SSRS) レポートに加えて、Excel 形式や PDF 形式で生成できます。 必要に応じて、この新規レポートを後で修正することも可能です。 コーディングは必要ありません。

1. 既存のレポートを実行するには、**アンケート** \> **設計** \> **アンケート レポート** に移動してください。

    ![アンケート モジュールでアンケート レポートのメニュー項目を選択し、既存の SSRS レポートを実行する](./media/er-quick-start1-application-menu-origin.png)

2. **アンケート レポート** のダイアログ ボックスで、選択基準を指定します。 フィルターを適用するとレポートに、アンケート **SBCCrsExam** のみを表示させることができます。

    ![アンケート レポートのダイアログ ボックスで、選択基準を指定する](./media/er-quick-start1-ssrs-report-dialog.png)

以下の図では、 アンケート **SBCCrsExam** で使用する SSRS レポートが生成されたバージョンを示しています。

![生成済みの SSRS レポート](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a> ER フレームワークを構成

電子レポートの開発者ロールが付与されたユーザーは、ER フレームワークを使用して 新たな ER ソリューションを設計する前に、最小限の ER パラメータを構成する必要があります。

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>ER パラメーターの構成

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **電子申告** ワークスペースで、**電子申告パラメーター** を選択します。
3. **電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。
4. **添付** タブで、次のパラメーターを設定します:

    - **USMF** 社で使用する **構成** フィールドを、**ファイル** に設定します。
    - **ジョブ アーカイブ**、**テンポラリー**、 **ベースライン**、**その他** の各フィールドを **ファイル** に設定します。

ER パラメーターについては、[ER フレームワークの構成](electronic-reporting-er-configure-parameters.md) を参照してください。

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a> ER 構成 プロバイダーをアクティブにする

各ER の構成は、構成プロバイダーに所有権があるものとして表示されます。 そのため、ER 構成を追加、または編集する前に、**電子レポート** ワークスペースで ER 構成プロバイダーを有効化する必要があります。

> [!NOTE]
> ER 構成の所有者のみが編集できます。 したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a> ER 構成 プロバイダーの一覧をレビュー

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **電子レポート** ワークスペースの、**関連するリンク** セクションで、**構成プロバイダー** を選択します。
3. **構成プロバイダー** ページで、各構成プロバイダー レコードは一意の名称と URL を持っています。 このページの内容をレビューします。 **Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER 構成 プロバイダーを追加](#ActivateProvider) します。

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a> 新しい ER 構成 プロバイダーを追加

1. **構成 プロバイダー** ページで、**新規** を選択します。
2. **名前** フィールドに、**Litware, Inc.** と入力
3. **インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。
4. **保存** を選択します。

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a> ER 構成 プロバイダーをアクティブにする

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **電子レポート** ワークスペースの、構成プロバイダーに **Litware, Inc.** を選択します。
3. **有効に設定** を選択します。

ER 構成 プロバイダーについては、[構成 プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>ドメイン固有のデータ モデルを設計する

**アンケート** ビジネス ドメインで使用する [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components) コンポーネントを含む、新たな ER 構成を作成する必要があります。 このデータ モデルは後で、ER フォーマットを設計して **アンケート** レポートを作成する際に、データ ソースとして使用されます。

[新しいデータ モデル構成をインポートする](#ImportDataModel) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なデータ モデルをインポートすることができます。 あるいは、[新しいデータ モデルの構成を作成する](#DesignDataModel) セクションに記載されている手順を完了すると、ゼロからこのデータ モデルを設計することができます。

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>新しいデータ モデルのインポート

1. [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. 操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。
5. **参照** を選択し、**Questionnaires model.version.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

続けるには、次の手順をスキップしてください : [新しいデータ モデルの構成を作成する](#DesignDataModel)。

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>新しいデータ モデル 構成の作成

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
3. **構成の作成** を選択します。
4. ドロップダウン ダイアログ ボックスの、**名前** フィールドで、**アンケート モデル** を入力してください。
5. **構成を作成する** を選択して、構成を作成します。

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>データ モデルに名前をつける

1. **構成** ページの、構成ツリーで、**アンケート モデル** を選択します。
2. **デザイナー** をクリックします。
3. **データ モデル デザイナー** ページの、**全般** クイックタブ内の、 **名前** フィールドに <a name="DataModeName"></a>**アンケート** と入力します。

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>新しいデータ モデル フィールドを追加する

1. **データ モデル デザイナー** ページで、**新規** を選択します。
2. データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. 新しいノードの種類に、**モデル ルート** を選択します。
    2. **名前** フィールドに、<a name="RootDefinitionName"></a>**ルート** と入力します。
    3. **追加** を選択して新しいノードを追加します。

    このルートの記述子は、**アンケート** レポートにデータを提供する目的で使用されます。 1つのデータモデルには複数の記述子を含めることができます。 それぞれの記述子は、1つの ER フォーマットに対して指定することができ、レポートの生成に必要なデータを識別することができます。

3. 再度 **新規** を選択し、データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、次の手順を実行します :

    1. 新規ノードのタイプに、**アクティブなノードの子ノード** を選択します。
    2. **名前** フィールドに、**CompanyName** と入力します。
    3. **品目タイプ** フィールドで、**文字列** を選択します。
    4. **追加** を選択して、新しいフィールドを追加します。

    このフィールドは、このデータ モデルをデータ ソースとして使用する ER レポートに現在の会社名を渡すために必要となります。

4. 再度 **新規** を選択し、データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、次の手順を実行します :

    1. 新規ノードのタイプに、**アクティブなノードの子ノード** を選択します。
    2. **名前** フィールドに、**アンケート** と入力します。
    3. **品目タイプ** フィールドで、**レコード リスト** を選択します。
    4. **追加** を選択して、新しいフィールドを追加します。

    このフィールドは、このデータ モデルをデータソースとして使用する ER レポートにアンケートのリストを渡すために使用されます。

5. **アンケート** ノードを選択します。
6. 以下のデータ モデル構造が完成するまで、編集可能なデータ モデルの必須フィールドを同じ方法で追加していきます。

    | フィールド パス                                                    | データ型   | フィールドの指定/戻り値 |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | ルート                                                          |             | アンケート データを依頼する際に基準となるポイントです。 |
    | Root\\CompanyName                                             | 文字列      | 現在の会社の名前です。 |
    | Root\\ExecutionContext                                        | レコード      | フォーマット実行の詳細です。 |
    | Root\\ExecutionContext\\FormatName                            | 文字列      | 実行中の ER フォーマットの名前です。 |
    | Root\\Questionnaire                                           | レコード リスト | アンケートの一覧です |
    | Root\\Questionnaire\\Active                                   | 文字列      | 現在のアンケートの状態です。 |
    | Root\\Questionnaire\\Code                                     | 文字列      | 現在のアンケートのコードです。 |
    | Root\\Questionnaire\\Description                              | 文字列      | 現在のアンケートの説明です。 |
    | Root\\Questionnaire\\QuestionnaireType                        | 文字列      | 現在のアンケートのタイプです。 |
    | Root\\Questionnaire\\QuestionOrder                            | 文字列      | 現在のアンケートの番号順です。 |
    | Root\\Questionnaire\\ResultsGroup                             | レコード      | 現在のアンケートの結果パラメーターです。 |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | 文字列      | 現在の結果グループの ID コードです。 |
    | Root\\Questionnaire\\ResultsGroup\\Description                | 文字列      | 現在の結果グループの説明です。 |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | 実績        | 獲得できる最大ポイント数です。 |
    | Root\\Questionnaire\\Question                                 | レコード リスト | 現在のアンケートの質問の一覧です。 |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | 整数     | 現在の応答コレクションのシーケンス番号です。 |
    | Root\\Questionnaire\\Question\\Id                             | 文字列      | 現在の質問の ID コードです。 |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | 文字列      | 現在の質問が必須であるかどうかを示すフラグです。 |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | 文字列      | 現在の質問が主要なものであるかどうかを示すフラグです。 |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | 整数     | 現在の質問のシーケンス番号です。 |
    | Root\\Questionnaire\\Question\\Text                           | 文字列      | 現在の質問のテキストです。 |
    | Root\\Questionnaire\\Question\\Answer                         | レコード リスト | 現在の質問の回答の一覧です。 |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | 文字列      | 現在の回答が正しいものであるかどうかを示すフラグです。 |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | 実績        | 現在の回答が選択されたときに確定するポイントです。 |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | 整数     | 現在の回答のシーケンス番号です。 |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | 文字列      | 現在の回答のテキストです。 |

    以下の図は、**データ モデル デザイナー** ページ上の完成した編集可能なデータ モデルを示して います。

    ![ER データ モデル デザイナーで構成されたデータ モデル](./media/er-quick-start1-model2.png)

7. 変更を保存します。
8. **データ モデル デザイナー** ページを閉じます。

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>データモデルのデザインを完成させる

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの、構成ツリーで、**アンケート モデル** を選択します。
3. **バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。
4. **ステータスの変更** \> **完了** を選択します。

この構成のバージョン 1 の状態 **下書き** から **完了** に変更されます。 バージョン 1 を変更することはできなくなります。 このバージョンには、構成済みのデータ モデルが含まれており、その他の ER の構成の基礎として使用できます。 この構成のバージョン2が作成され、状態が **下書き** になります。 このバージョンを編集して、**アンケート** データ モデルを調整することができます。

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-model-configuration.png)

ER の構成に関する詳細情報については、 [電子レポート (ER) の概要](general-electronic-reporting.md#component-versioning) を参照してください。

> [!NOTE]
> 設定されたデータモデルは、**アンケート** の業務ドメインの概要を表わすものであり、Microsoft Dynamics 365 Finance に固有のアーティファクトとの関係はありません。

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>構成済みのデータモデルで使用するモデル マッピングをデザインする

電子レポート開発者のロールを付与されたユーザーは、**アンケート** データ モデルの[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)コンポーネントを含む、新たな ER 構成を作成する必要があります。 このコンポーネントは、財務に特化して構成されたデータモデルを実装しています。 構成済みのデータモデルの実行時にアプリケーション データの入力に使用する必要があるアプリケーション オブジェクトを指定するには、モデルマッピング コンポーネントを構成する必要があります。 このタスクを完了するには、財務における **アンケート** 事業ドメインのデータ構造の実装についての詳細を把握しておく必要があります。

続いて[新しいモデル マッピング構成をインポートする](#ImportModelMapping) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なデータ モデルをインポートすることができます。 あるいは、[新しいモデル マッピング構成を作成する](#CreateModelMapping) セクションに記載されている手順を完了すると、ゼロからこのモデル マッピングを設計することができます。

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>新しいモデル マッピング構成をインポートする

1. [アンケート mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. 操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。
5. **参照** を選択し、**アンケート mapping.version.1.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

続けるには、次の手順をスキップしてください : [新しいモデル マッピング構成を作成する](#CreateModelMapping)。

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>新しいモデル マッピング構成を作成する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの、構成ツリーで、**アンケート モデル** を選択します。
3. **構成の作成** を選択します。
4. ドロップダウン ダイアログ ボックスで、次の手順に従います。

    1. **新規** フィールドで、**データ モデル アンケートに基づいたモデル マッピング** を選択します。
    2. **名前** フィールドに、**アンケート マッピング** と入力します。
    3. **データ モデル定義** フィールドで、**ルート** の定義を選択します。
    4. **構成を作成する** を選択して、構成を作成します。

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>新しいモデル マッピング コンポーネントを設計する

1. **構成** ページの、構成ツリーで、**アンケート マッピング** を選択します。
2. **デザイナー** を選択して、マッピングの一覧を開きます。
3. **ルート** 定義に対して自動的に追加された **アンケート マッピング** マッピングを選択します
4. **デザイナー** を選択して、選択したマッピングの構成を開始します。

**ルート定義** に新しいマッピングが自動的に追加されます。 このマッピングは、**モデル** の方向に対応しています。 そのため、このマッピングを使用してデータ モデルに必要なデータを入力することができます。

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>データ ソースを追加してアプリケーション テーブルにアクセスする

アンケートの詳細を含むアプリケーション テーブルにアクセスするには、データソースを構成する必要があります。

1. **モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。
2. KMCollection テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが単一のアンケートを表します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ダイアログ ボックスの **名前** フィールドに **アンケート** と入力します。
    3. **テーブル** フィールドに、**KMCollection** と入力します。
    4. **問い合わせをする** オプションを **はい** に設定します。 これにより、実行時に [システムクエリ] ダイアログボックスで、このテーブルに[フィルタ処理](../../fin-ops/get-started/advanced-filtering-query-options.md)オプションを指定できるようになります。
    5. **OK** を選択して新しいデータ ソースを追加します。

3. **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。
4. KMQuestion テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが単一の質問を表します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ダイアログ ボックスで、**名前** フィールドに **質問** と入力します。
    3. **テーブル** フィールドに、**KMQuestion** と入力します。
    4. **OK** を選択して新しいデータ ソースを追加します。

5. **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。
6. KMAnswer テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが回答の質問を表します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. **名前** フィールドに、**回答** と入力します。
    3. **テーブル** フィールドに、**KMAnswer** と入力します。
    4. **OK** を選択して新しいデータ ソースを追加します。

7. **データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。
8. 親となる KMCollection テーブルのすべてのレコードから KMQuestionResultGroup テーブルのレコードへのアクセスに使用する新しい計算フィールドを追加します。

    1. **データ ソース** ペインで、**アンケート** を選択します。
    2. **追加** を選択します。
    3. ダイアログ ボックスで、**名前** フィールドに **\$ResultGroup** と入力します。
    4. **式の編集** を選択します。
    5. [ER 式エディター](general-electronic-reporting-formula-designer.md)で、 **式** フィールドに **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**  と入力し、KMCollection テーブルと KMQuestionResultGroup テーブル間の一対多の関係の[パス](er-formula-language.md#Paths)を使用します。
    6. **保存** を選択し、式エディターを閉じます。
    7. **OK** を選択して新しい計算フィールドを追加します。

9. **データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。
10. 親となる KMCollectionQuestion テーブルのすべてのレコードから KMQuestion テーブルの質問レコードへのアクセスに使用する新しい計算フィールドを追加します。

    1. **データ ソース** ペインで、**アンケート** を選択します。
    2. KMCollection テーブルの1対多の関係を含む **\<関係性** ノードを展開します。
    3. 関連する **KMCollectionQuestion** テーブルを選択し、**追加** をクリックし ます。
    4. ダイアログ ボックスで、 **名前**  フィールドに **\$Question** と入力します。
    5. **式の編集** を選択します。
    6. 式エディターの **式** フィールドで、**FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** と入力し、KMQuestion テーブルから適切な質問レコードを返します。
    7. **保存** を選択し、式エディターを閉じます。
    8. **OK** を選択して新しい計算フィールドを追加します。

11. **データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。
12. 親となる KMQuestion テーブルのすべてのレコードから KMAnswer テーブルの回答レコードへのアクセスに使用する新しい計算フィールドを追加します。

    1. **データソース** ペインで、**Questionnaire.\<Relations.KMCollectionQuestion.\$Question** を選択し、続いて **追加** を選択します。
    2. ダイアログ ボックスで、**名前** フィールドに **\$Answer** と入力します。
    3. **式の編集** を選択します。
    4. 式エディターの **式** フィールドで、**FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** と入力し、KMAnswer テーブルから適切な回答レコードを返します。
    5. **保存** を選択し、式エディターを閉じます。
    6. **OK** を選択して新しい計算フィールドを追加します。

13. **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル** を選択します。
14. 会社情報テーブルのメソッドへのアクセスに使用する新しいデータ ソースを追加します。 このテーブルの **find()** メソッドは、このマッピングが呼び出された現在の財務インスタンスの会社を表すレコードを返すことに注意してください。

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ダイアログ ボックスの **名前** フィールドに **CompanyInfo** と入力します。
    3. **テーブル** フィールドに、**CompanyInfo** と入力します。
    4. **OK** を選択して新しいデータ ソースを追加します。

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>データ ソースを追加してアプリケーション リストにアクセスする

アプリケーション リストへのアクセスに使用するデータ ソースを構成し、その値をアプリケーション テーブルの **列挙** 型のフィールドの値と比較する必要があります。 データ モデルの適切なフィールドにデータを入力するには、比較の結果を使用する必要があります。

1. **モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\列挙型** を選択します。
2. **EnumAppNoYes** リストの値へのアクセスに使用する新しいデータ ソースを追加します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ダイアログ ボックスの **名前** フィールドに **EnumAppNoYes** と入力します。
    3. **リスト** フィールドに、**NoYes** と入力します。
    4. **OK** を選択して新しいデータ ソースを追加します。

3. **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\\列挙型** を選択します。
4. **KMCollectionQuestionMode** リストの値へのアクセスに使用する新しいデータ ソースを追加します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ドロップダウン ダイアログボックスの **名前** フィールドに **EnumAppQuestionOrder** と入力します。
    3. **リスト** フィールドに、**KMCollectionQuestionMode** と入力します。
    4. **OK** を選択して新しいデータ ソースを追加します。

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>ER ラベルを追加して指定した言語でレポートを生成する

ER ラベルを追加して、モデル マッピングを呼び出すコンテキストで定義された言語に依存する値を返すよう、データ ソースの一部を構成することができます。

1. **モデル マッピング デザイナー**  ページの、 **データ ソース** ペインで、**回答** を選択し、続いて **編集** を選択します。
2. **ラベル** フィールドをアクティブ化します。
3. **翻訳** を選択します。
4. **テキストの翻訳** ダイアログ ボックスで、次の手順に従ってください :

    1. **ラベル ID** フィールドで、**PositiveAnswer** と入力します。
    2. **既定の言語のテキスト** フィールドに **はい** と入力します。
    3. **翻訳** を選択します。
    4. **ラベル ID** フィールドで、**NegativeAnswer** と入力します。
    5. **既定の言語のテキスト** フィールドに **いいえ** と入力します。
    6. **翻訳** を選択します。

5. **テキストの翻訳** ダイアログ ボックスを閉じます。
6. **キャンセル** を選択します。

![編集可能なモデル マッピングへの ER ラベルの追加](./media/er-quick-start1-adding-labels.png)

既定の言語に対してのみ ER ラベルを入力しました。 ER ラベルを他の言語に翻訳する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>データ ソースを追加してリストの比較結果値をテキスト値に変換する

列挙値とテキスト値の比較結果は、差分ソースに対して何度か変換する必要があるため、このロジックを単一のデータソースとして構成することをお勧めします。 ただし、このデータソースを再利用できるようにするには、パラメーター化されたデータソースとして設定する必要があります。 詳細情報については、[計算フィールド タイプのER データ ソースのパラメーター化された呼び出しに対応する](er-calculated-field-type.md)を参照してください。

1. **モデル マッピング デザイナー**  ページの、**データ ソース タイプ**  ペインで、**全般\\空のコンテナー** を選択します。
2. 新しいコンテナー データ ソースを追加します :

    1. **データ ソース** ペインで、**ルートの追加** を選択します。
    2. ダイアログ ボックスで、**名前** フィールドに **ヘルパー** と入力します。
    3. **OK** を選択し、新しいコンテナー データ ソースを追加します。

3. **データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。
4. 新しいデータ ソースを追加します :

    1. **データ ソース** ペインで、**ヘルパー** を選択します。
    2. **追加** を選択します。
    3. ドロップダウン ダイアログボックスの **名前** フィールドに **NoYesEnumToString** と入力します。
    4. **式の編集** を選択します。
    5. 式エディターで、**パラメーター** を選択します。
    6. 次の手順に従い、構成された式のパラメータを指定します :

        1. **新規** を選択します。
        2. ダイアログ ボックスで、**名前** フィールドに **引数** と入力します。
        3. **タイプ** フィールドで、データー型に **ブール** を選択します。
        4. **OK** を選択します。

    7. **式** フィールドで、**IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** と入力し、適切な ER ラベルのテキストを返すよう設定します。ER ラベルは実行コンテキストの言語と指定されたパラメータの値によって異なります。
    8. **保存** を選択し、式エディターを閉じます。
    9. **OK** を選択して新しいデータ ソースを追加します。

![ER モデル マッピング デザイナーで構成されたモデル マッピング](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>データ ソースをデータ モデル フィールドにバインドする

構成されたデータ ソースをデータ モデルのフィールドにバインドして、実行時にアプリケーション データに対するデータ モデルの入力方法を指定する必要があります。

1. **モデル マッピング デザイナー** ページの、**データ モデル** ペインで、**CompanyName** を選択します。
2. **データ ソース** ペインで、**CompanyInfo** を展開し、続いて以下の手順を実行します :

    1. CompanyInfo テーブルの **find()** メソッドを表わす、**CompanyInfo.find()** ノードを展開します。
    2. **CompanyInfo.find().Name** を選択します。
    3. **バインド** を選択し、構成されたモデル マッピングが実行時のコンテキストで呼び出される会社名を入力します。

3. **データ モデル** ペインで、**アンケート** を選択します。
4. **データ ソース** ペインで、**Questionnaire** を選択し、続いて **Bind** を選択してアンケートのレコードを入力します。
5. **データ モデル** ペインで、**アンケート** を展開し、続いて以下の手順を実行します :

    1. **データ モデル** ペインで、**アクティブ** を選択します。
    2. **データ モデル** ペインで、**編集** を選択します。
    3. **式** フィールドに **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** と入力し、リストされた値間の比較を行ったテキスト依存、言語依存の結果を入力します。

6. 以下の結果が得られるまで、同じ方法でデータ ソースをデータ モデル フィールドにバインドしていきます。

    | フィールド パス                                              | データ型   | アクション | バインド式 |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | 文字列      | バインド   | CompanyInfo.'find()'.Name |
    | アンケート                                           | レコード リスト | バインド   | アンケート |
    | Questionnaire\\Active                                   | 文字列      | 編集   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | 文字列      | バインド   | \@.kmCollectionId |
    | Questionnaire\\Description                              | 文字列      | バインド   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | 文字列      | バインド   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | 文字列      | 編集   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",<br>EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | レコード      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | 文字列      | バインド   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | 文字列      | バインド   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | 実績        | バインド   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | レコード リスト | バインド   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | 整数     | バインド   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | 文字列      | バインド   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | 文字列      | 編集   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | 文字列      | バインド   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | 整数     | バインド   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | 文字列      | バインド   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | レコード リスト | バインド   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | 文字列      | 編集   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | 実績        | バインド   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | 整数     | バインド   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | 文字列      | バインド   | \@.text |

    以下の画面は、**モデル マッピング デザイナー** のページ上で構成されたモデル マッピングの最終的な状態を示して います。

    ![ER モデル マッピング デザイナーで構成が完了したモデル マッピング](./media/er-quick-start1-mapping2.png)

7. 変更を保存します。
8. **モデル マッピング デザイナー** ページを閉じます。

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>モデル マッピングを完了する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの、構成ツリーで、**アンケート マッピング** を選択します。
3. **バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。
4. **ステータスの変更** \> **完了** を選択します。

この構成のバージョン 1.1 の状態 **下書き** から **完了** に変更されます。 バージョン 1.1 を変更することはできなくなります。 このバージョンには、構成済みのモデル マッピングが含まれており、その他の ER の構成の基礎として使用できます。 この構成のバージョン 1.2 が作成され、状態が **下書き** になります。 このバージョンを編集して、**アンケート マッピング** の構成を調整することができます。

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> ご利用の財務に固有となる実装となり、**アンケート** 業務ドメインを表わす抽象データ モデルです。

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>カスタム レポートで使用するテンプレートを設計する

ER フレームワークは、定義済みのテンプレートを使用して、Microsoft Office 形式 (Excel ワークブック、または Word ドキュメント) でレポートを生成します。 必要なレポートが生成されている間、構成されたデータフローに従って、テンプレートに必要なデータが入力されます。 ます、まずカスタム レポートデ使用するテンプレートを設計する必要があります。 このテンプレートは、カスタム レポートのレイアウトを表す構造を持つ Excel ワークブック形式で設計されている必要があります。 必要なデータを入力するすべての Excel 項目には名前を付ける必要があります。

1. [Questionnaires report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. ファイルを Excel で開き、ブックの構造を確認します。

以下の図に示すように、ダウンロードしたテンプレートは、特定のアンケートの質問とその適切な回答を印刷する意図で設計されています。

![指定されたアンケートを印刷する Excel テンプレート](./media/er-quick-start1-template-layout.png)

このテンプレートに Excel 名が追加され、アンケートの詳細が入力されます。 名前マネージャを使用すると、Excel の名前を確認できます。

![名前マネージャを使用して入力だれた Excel テンプレートの名前を確認する](./media/er-quick-start1-template-names.png)

レポート ラベルは、英語では固定テキストとして追加されています。 構成されたモデル マッピングの言語依存の式を使用した場合と同様に、ER フォーマット[ラベル](#AddMmLabels)を使用して、ラベルに入力する新しい Excel 名をレポート ラベルに置き換えることができます。 この場合、ER ラベルを編集可能な形式で追加する必要があります。

以下の画像のように、カスタム レポートのヘッダーを指定して、Excel が呼び出しできるようになっています。

![Excel テンプレートのカスタム レポート ヘッダー](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>形式のデザイン

電子レポート機能コンサルタントのロールが付与されているユーザーは、[フォーマット](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む新しい ER 構成を作成する必要があります。 実行時にレポートのテンプレートに必要となるデータをどのように入力するかを指定するには、フォーマットのコンポーネントを構成する必要があります。

[設計されたフォーマットの構成をインポートする](#FormatImport) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なフォーマットをインポートすることができます。 あるいは、[新しいフォーマットの構成を作成する](#FormatCreate) セクションに記載されている手順を完了すると、ゼロからこのフォーマットを設計することができます。

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>設計済みフォーマットの構成をインポートする

1. [アンケート format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. アクション ペインで、**変換** \> **XML ファイルから読み込む** を選択します。
5. **参照** を選択し、**アンケート format.version.1.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

続けるには、次の手順をスキップしてください : [新しいフォーマットの構成を作成する](#FormatCreate)。

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>新しい構成の書式設定の作成
 
1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの、構成ツリーで、**アンケート モデル** を選択します。
3. **構成の作成** を選択します。
4. ドロップダウン ダイアログ ボックスで、次の手順に従います。

    1. **新規** フィールドで、**データ モデル アンケートに基づいたフォーマット** を選択します。
    2. **名前** フィールドに、**アンケート レポート** と入力します。
    3. **データ モデルのバージョン** フィールドで、**1** を選択します。

        > [!NOTE]
        > - 基本データモデルの特定のバージョンを選択すると、対応するバージョンのデータ モデルの構造が、作成されたフォーマットの **モデル** のデータ ソース構造として表示されます。
        > - このフィールドは必須ではありません。 この場合、**下書き** 版のデータ モデルの構造は、作成されたフォーマットの **モデル** のデータソースの構造として表示されます。 その後、モデルを調整を行って、フォーマットにおける調整結果をすぐに確認することができます。 この方法では、データモデル、モデルマッピング、フォーマットを同時に構成する場合に、ER ソリューション設計の効率を向上させることが期待できます。
        > - 基本データ モデルの特定のバージョンを選択した場合、フォーマットの編集を開始したときに、後で **下書き** 版を使用するように切り替えることができます。

    4. **データ モデル定義** フィールドで、**ルート** の定義を選択します。

5. **構成を作成する** を選択して、構成を作成します。

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>レポートのテンプレートをインポートする

1. **構成** ページの、構成ツリーで、**アンケート レポート** を選択します。
2. **デザイナー** を選択して、カスタム フォーマットの構成を始めます。
3. **フォーマット デザイナー** ページの、アクション ペインで、**インポート** \> **Excel からインポートする** を選択します。
4. ダイアログ ボックスで、次の手順に従ってください :

    1. **テンプレートの選択** を選択します。
    2. ローカルに保存した **アンケート レポート template.xslx** ファイルを検索して選択し、**開く** を選択します。
    3. テンプレートをインポートするには、**OK** を選択します。

    ![レポートのテンプレートをインポートする](./media/er-quick-start1-template-import.png)

**Excel \\ファイル** フォーマットの要素は、自動的にルート要素として編集可能なフォーマットに追加されます。 さらに、**Excel \\範囲** フォーマットの要素、または **Excel \\セル** フォーマット要素のいずれかが、インポートされたテンプレートの認識された Excel 名ごとに自動的に追加されます。 **Excel\\ヘッダー** フォーマットで、**文字列** 要素がネストされているものは、インポートしたテンプレートのヘッダーの設定を反映して自動的に追加されます。

![ER 工程デザイナーに自動追加された要素を含むフォーマットの構成](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>フォーマットを構成する

1. フォーマット ツリーの **フォーマット デザイナー** ページで、**Excel** のルート要素を選択します。
2. ページ右側の **フォーマット** タブの **名前** フィールドに、 <a name="AddFormatRootElement"></a>**レポート** と入力します。
3. **優先する言語** フィールドで、**ユーザー設定** を選択して、ユーザーの優先する言語でレポートを実行します。
4. **優先する文化** フィールドで、**ユーザー設定** を選択して、ユーザーの優先する文化でレポートを実行します。

    ER プロセスで使用する言語と文化のコンテキストを指定する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。

    ![ER 操作デザイナーで設計されたレポートの言語と文化の設定を構成する](./media/er-quick-start1-template-format-structure1.png)

5. フォーマット ツリーで、ルート ノードを展開し、続いて **ResultsGroup** を選択します。
6. **フォーマット** タブの **レプリケーションの方向** フィールドで、**レプリケーションなし** を選択してください。この場合は、1つのアンケートに複数の結果グループが存在することを想定していないためです。

    ![ER 操作デザイナーで範囲フォーマット要素のレプリケーション方向を定義する](./media/er-quick-start1-template-format-structure2.png)

7. **保存** を選択します。

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>レポートのタイトルに使用するデータのバインドを定義する

生成されたレポートのタイトルの入力に使用するフォーマット要素のデータ バインディングを指定する必要があります。

1. **フォーマット デザイナー** ページの、右側の **マッピング** タブ形式で、**レポート\\ReportTitle** 要素を選択します。
2. **式の編集** を選択します。
3. 式エディターで、**翻訳** を選択します。
4. **テキストの翻訳** ダイアログ ボックスで、次の手順に従ってください :

    1. **ラベル ID** フィールドで、**ReportTitle** と入力します。
    2. **既定の言語のテキスト** フィールドに **アンケート レポート** と入力します。
    3. **翻訳** を選択してから、**保存** を選択します。
    4. **翻訳** を選択して、**テキストの翻訳** ダイアログ ボックスを閉じます。

5. 式エディターを閉じます。

    ![バインドを構成して生成されたレポートのタイトルを入力する](./media/er-quick-start1-add-report-title-label.png)

この手法を使用して、現在のテンプレートの他のすべてのラベルを言語依存にすることができます。 1つの ER 構成の追加ラベルを対応しているすべての言語に翻訳する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>モデル データ ソースをレビューする

1. **フォーマット デザイナー** ページの **マッピング** タブで、<a name="ModelDSName"></a>この ER フォーマットの基本データ モデルを表す **モデル** データ ソースを選択します。
2. **編集** を選択します。
3. **データ ソース プロパティ** ダイアログ ボックスの情報をを確認します。 このデータソースは、**アンケート** モデルの ER 構成に存在する **アンケート** データ モデル コンポーネントのバージョン 1 を表しています。

![ER 操作デザイナー モデルデータ ソースのプロパティ](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>フォーマットの要素をデータ ソース フィールドにバインドする

実行時のテンプレートへの入力方法を指定するには、適切な Excel 名に関連付けられたすべてのフォーマット要素を、このフォーマットのデータソースの 1 つのフィールドにバインドする必要があります。

1. フォーマット ツリーの **フォーマット デザイナー**  ページで、**レポート\\CompanyName** フォーマット要素を選択します。
2. **マッピング** タブで、**文字列** 型のデータ ソース フィールド **model.CompanyName** を選択します。
3. **バインド** を選択して、テンプレートに会社名を入力します。
4. フォーマット ツリーで、**レポート\\アンケート** 要素を選択し ます。
5. **マッピング** タブで、**レコード リスト** 型のデータ ソース フィールド **model.Questionnaire** を選択します。
6. **バインド** を選択します。
7. **詳細の表示** を選択して、フォーマット要素の詳細を表示します。

    **アンケート** 範囲フォーマット要素は、垂直方向に複製されるように構成されています。 **レコード リスト** 型のデータソースにバインドすると、Excel テンプレートの適切な **アンケート** の範囲が、バインドされたデータソースのすべてのレコードに対して繰り返されます。
 
    ![ER 操作デザイナーの適切なレコード リストのデータ ソースにアンケート範囲のフォーマット要素をバインドする](./media/er-quick-start1-bindings1.png)

    Excel テンプレートの **アンケート** 範囲は 5 から 14 行目までの間の定義されているため、これらの行は提出されたアンケートごとに繰り返されます。

    ![レコード リストのデータ ソースの各レコードに対して、生成されたレポートで繰り返される Excel テンプレートの行](./media/er-quick-start1-template-questionnaire-range.png)

8. 以下の表に示すように、残りのフォーマット要素にも同様のバインディングを設定してください。

    > [!NOTE]
    > この表では、「データソースパス」欄の情報は、 ER 機能 [相対パス](relative-path-data-bindings-er-models-format.md)がオンになっていることを前提としています。

    | フォーマット要素のパス                                      | データ ソースのパス |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**、**\@** が **model.Questionnaire** の場合 |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**、 **\@** が **model.Questionnaire.Question** の場合 |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer** **\@** が **model.Questionnaire.Answer** の場合 |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. 完了したら、**保存** を選択します。

以下の画面は、**フォーマット デザイナー** ページ上で構成されたデータ バインディングの最終的な状態を示して います。

![ER 操作デザイナーで構成されたデータ バインディング](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> 指定されたデータソースとバインディングの全体のコレクションは、構成されたフォーマットのフォーマット マッピング コンポーネントを表します。 このフォーマット マッピングは、レポート生成に向けて構成されたフォーマットを実行する際に呼び出されます。

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>ER から設計済みのフォーマットを実行する

**構成** ページから、テスト用にデザインされた形式を実行できます。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。
3. **下書き** 状態のフォーマット バージョンの **デザイナー** を選択します。
4. **フォーマット デザイナー** ページで、**実行** を選択します。
5. **ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
6. **OK** を選択してオプションを確認します。
7. **OK** を選択してレポートを実行します。
8. 生成されたレポートを確認します。

[既定](electronic-reporting-destinations.md#default-behavior)では、生成されたレポートは、ダウンロード可能な Excel ファイル形式で配信されます。 次の図は、生成されたレポートの2つのページを Excel 形式で示しています。

![Excel フォーマットで生成されたレポートの例 (ページ1)](./media/er-quick-start1-report1a.png)

![Excel フォーマットで生成されたレポートの例 (ページ2)](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>設計済みのフォーマットを調整する

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>フォーマットを修正して生成されたドキュメントの名前を変更する

既定では、生成されたドキュメントには現在のユーザーのエイリアスを使用して名前が付けられます。 フォーマットを変更することで、この動作を変更して、生成されたドキュメントにカスタム ロジックに基づいて名前を付けることができます。 たとえば、生成されたドキュメントの名前は、現在のセッションの日時とレポートのタイトルに基づいて付けることができます。

1. **フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。
2. **マッピング** タブで、**ファイル名の編集** を選択します。
3. **式** フィールドに、**CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** と入力します。
4. **保存** を選択し、式エディターを閉じます。
5. **保存** を選択します。

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>フォーマットを修正して質問の表示順を変更する

生成されたレポートでは、質問は正しく順序付けられていません。 フォーマットを変更することで順番を変更することができます。

1. **フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。
2. **マッピング** タブのフォーマット ツリーで、**レポート\\アンケート\\質問** を展開します。

    ![ER 作業工程デザイナーにおける範囲タイプの質問フォーマット要素](./media/er-quick-start1-bindings3.png)

3. **マッピング** タブで、**model.Questionnaire** を選択します。
4. **追加**\>**関数\\計算フィールド** を選択し、**Name** フィールドに **OrderedQuestions** と入力します。
5. **式の編集** を選択します。
6. 式の編集エディターの **式** フィールドに **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** を入力し、現在のアンケートの質問のリストをシーケンス オーダー番号順に並び替えます。
7. **保存** を選択し、式エディターを閉じます。
8. **OK** をクリックして、新しい計算フィールドの入力を完了します。
9. **マッピング** タブで、**model.Questionnaire.OrderedQuestions** を選択します。
10. フォーマットのツリーで、**Excel\\アンケート\\質問** を選択します。
11. **Bind** を選択し、 入れ子になった要素のすべてのバインディングで、現在の **model.Questionnaire.Questions** パスが新しい **model.Questionnaire.OrderedQuestions** パスに置き換えられていることを確認します。
12. **保存** を選択します。

![ER 操作デザイナーで、構成された OrderedQuestions データソースに アンケート フォーマット要素をバインドする](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>ER から修正済みのフォーマットを実行する

ER フレームワークから、テスト用に変更されたフィーマットを実行できます。

1. **フォーマット デザイナー** ページで、**実行** を選択します。
2. **ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
3. **OK** を選択してオプションを確認します。
4. **OK** を選択してレポートを実行します。
5. 生成されたレポートを確認します。

次の図は、質問が正しい順番に並べられた Excel 形式の生成レポートを示しています。

![質問を正しく並べ替えた Excel 形式のレポートを生成する](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>フォーマットの設計を完了する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。
3. **バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。
4. **ステータスの変更** \> **完了** を選択します。

この構成のバージョン 1.1 の状態 **下書き** から **完了** に変更されます。 バージョン 1.1 を変更することはできなくなります。 このバージョンには、構成済のフォーマットが含まれており、カスタム レポートの印刷に使用できます。 この構成のバージョン 1.2 が作成され、状態が **下書き** になります。 このバージョンを編集して、**アンケート** レポートのフォーマットを調整することができます。

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> 構成されたフォーマットは、**アンケート** レポートのデザインであり、財務固有のアーティファクトとの関係はありません。

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>アプリケーション アーティファクトを開発して、設計済みのレポートを呼び出す

システム管理者ロールが付与されたユーザーは、設定された ER フォーマットをアプリケーション ユーザー インターフェース (UI) から呼び出してカスタム レポートを生成できるように、新しいロジックを開発する必要があります。 現在 ER には、この種のロジックを構成する機能はありません。 そのため、多少の技術的な作業が必要となります。 

新しいロジックを開発するには、継続的なビルドに対応したトポロジをデプロイする必要があります。 詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](../perf-test/continuous-build-test-automation.md)を参照してください。 また、このトポロジの開発環境にもアクセスできる必要があります。 利用可能な ER の API については、[ER フレームワークの API](er-apis-app73.md) を参照してください。

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>ソース コードの修正

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>データ コントラクトのクラスを追加する

新しい **QuestionnairesErReportContract** クラスを Visual Studio プロジェクトに追加し、構成された ER フォーマットの実行に使用するデータ コントラクトを指定するコードを記述します。

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>UI Builder のクラスを追加する

新しい **QuestionnairesErReportUIBuilder** クラスを Visual Studio プロジェクトに追加し、実行の必要がある ER フォーマットのフォーマット マッピング ID の検索に使用するランタイム ダイアログ ボックスを生成するコードを作成します。 入力されたコードは、**[ルート](#RootDefinitionName)** 定義を使用して、**[アンケート](#DataModeName)** データ モデルを参照する **データ モデル** タイプのデータ ソースを含む ER フォーマットのみを検索します。

> [!NOTE]
> また、ER 統合ポイントを使用して ER フォーマットをフィルター処理することもできます。 詳細については、[フォーマット マッピングの検索を表示する API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup)を参照してください 。

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>データ プロバイダーのクラスを追加する

新しい **QuestionnairesErReportDP** クラスを Visual Studio プロジェクトに追加し、構成された ER フォーマットの実行に使用するデータ プロバイダーを導入するコードを記述します。 作成されたコードには、このデータ プロバイダーのデータ コントラクトのみが含まれます。

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>ラベル ファイルを追加する

Visual Studio プロジェクトに新しい **QuestionnairesErReportLabels\_en-US** ラベルを追加し、新たな UI リソースで使用する次のラベルを指定します :

- **\@QuestionnairesReport** ラベル : 米国英語 (en-US) で記述された **アンケート レポート (ER で実行)** のテキストを含む、新たなメニュー項目に使用される
- **\@QuestionnairesReportBatchJobDescription** ラベル : 選択された ER フォーマットがバッチジョブを実行するようにスケジュールされている場合に、バッチ ジョブのタイトルに使用される

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>レポート サービス クラスを追加する

Visual Studio プロジェクトに新しい **QuestionnairesErReportService** クラスを追加します。続いて ER フォーマットを呼び出し、それをフォーマット マッピング IDで識別し、データ コントラクトをパラメーターとして提供するコードを記述します。

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

アプリケーションデータを実行する ER フォーマットを使用する必要がある場合は、フォーマット マッピングで **データ モデル** タイプのデータ ソースを構成する必要があります。 このデータソースは、単一のルート定義を使用して、指定されたデータ モデルの特定の部分を参照します。 ER フォーマットを実行するとと、このデータソースを呼び出して、指定されたモデルとルート定義に対して構成されている適切な ER モデル マッピングにアクセスします。

ソースコードで作成し、データ コントラクトの一部として保存されているすべての情報は、このタイプの ER モデル マッピングを使用して、実行中の ER フォーマットに渡すことができます。 ER モデル マッピングでは、**[QuestionnairesErReportContract](#DataContractClass)** クラスを参照する **オブジェクト** 型のデータ ソースを設定する必要があります。 モデル マッピングを識別するには、このモデル マッピングを呼び出すデータ ソースを指定する必要があります。 作成されたコードでは、**[モデル](#ModelDSName)** の値を持つ **ERModelDataSourceName** 定数で指定されたこのデータソースが指定されます。 モデル マッピングに対して、どのデータ ソースがデータ コントラクトの公開に使用されているかを特定するには、データ ソース名を指定する必要があります。 作成されたコードでは、この名前は <a name="DataContractDSName"></a>**RunTimeParameters** の値を持つ **ParametersDataSourceName** 定数で指定されます。

> [!NOTE]
> 新しい環境では、ER モデル マッピング デザイナーでこのタイプのクラスが利用できるよう、ER メタデータの更新が必要となる場合があります。 詳細については、[電子レポート (ER) フレームワークの構成](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) を参照してください。

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>レポートのコントローラ クラスを追加する

Visual Studio プロジェクトに、新しい **QuestionnairesErReportController** クラスを追加し、提供された **QuestionnairesErReportUIBuilder** クラスのロジックに基づいて構築されたダイアログ ボックスで、同期モードまたはバッチモードのいずれかでERフォーマットを実行するコードを記述します。

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>メニュー項目を追加する

Visual Studio プロジェクトに新しい **QuestionnairesErReport** メニュー項目を追加します。 **オブジェクト** プロパティでは、このメニュー項目は **QuestionnairesErReportController** クラスを参照し、ER フォーマットを選択して実行するユーザーアクセス許可を指定するために使用されます。 **ラベル** プロパティでは、このメニュー項目は前述の手順で作成した **\@QuestionnairesReport** ラベルを参照し、アプリケーションの UI に正しいテキストが表示されるようになります。

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>メニュー項目をメニューに追加する

既存の **KM** メニューを Visual Studio プロジェクトに追加します。 このメニューには、**出力** タイプに新しい **QuestionnairesErReport** 項目を追加する必要があります。 この項目は、前のセクションで説明したメニュー項目 **QuestionnairesErReport** を参照する必要があります。

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Visual Studio プロジェクトをビルドする

プロジェクトをビルドして、新しいメニュー項目をユーザーが使用できるようにします。

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>アプリケーションからフォーマットを実行する

1. **アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。

    ![アンケート モジュールのアンケート レポート (ER による実行) メニュー項目を選択して、構成された ER フォーマットが実行する](./media/er-quick-start1-application-menu-modified.png)

2. ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。
3. **OK** を選択します。
4. **電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
5. **OK** を選択してオプションを確認します。
6. **OK** を選択してレポートを実行します。

    ![電子レポートのダイアログ ボックスで、選択基準を指定する](./media/er-quick-start1-report-run-dialog-page.png)

7. 生成されたレポートを確認します。

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>設計済みの ER ソリューションを調整する

構成された ER ソリューションを変更して、実行中の ER フォーマットの詳細にアクセスするために開発したデータ プロバイダ クラスを使用し、生成されたレポートにこの ER フォーマットの名前を入力することができます。

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>モデルのマッピングを修正する

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>データ ソースを追加してデータ コントラクト オブジェクトにアクセスする

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート マッピング** を選択します。
3. **デザイナー** を選択すると、**データソース マッピングに使用するモデル** ページが開きます。
4. **デザーナー** を選択して、モデル マッピング デザイナーで選択したデザイナーを開きます。
5. **モデル マッピング デザイナー** ページの **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\オブジェクト** を選択します。
6. **データ ソース** ペインで、**ルートの追加** を選択します。
7. ダイアログ ボックスの **名前** フィールドに、**QuestionnairesErReportService** クラスのソースコードで定義されている **[RunTimeParameters](#DataContractDSName)** を入力します。
8. **クラス** フィールドで、前述の手順で記述した **[QuestionnairesErReportContract](#DataContractClass)** を入力します。
9. **OK** を選択します。
10. **RunTimeParameters** を展開します。

追加されたデータソースは、実行中の ER フォーマット マッピングのレコード ID に関する情報を提供します。

![ER モデル マッピング デザイナーにデータソースを追加する](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>データ ソースを追加して ER フォーマット マッピング レコードにアクセスする

ER フォーマットのマッピング レコードへのアクセスに使用するデータソースを追加して、選択したモデル マッピングの編集を続行します。

1. **モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。
2. **データ ソース** ペインで、**ルートの追加** を選択します。
3. ダイアログ ボックスで、**名前** フィールドに **ER1** と入力します。
4. **テーブル** フィールドに、**ERFormatMappingTable** と入力します。
5. **OK** を選択します。

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>データ ソースを追加して実行中の ER フォーマットのフォーマット マッピング レコードにアクセスする

実行中の ER フォーマットのフォーマット マッピング レコードへのアクセスに使用するデータソースを追加して、選択したモデルマッピングの編集を続行します。

1. **モデル マッピング デザイナー** ページの **データ ソース タイプ** ウィンドウで、**関数\\計算フィールド** を選択します。
2. **データ ソース** ペインで、**ルートの追加** を選択します。
3. ダイアログ ボックスで、**名前** フィールドに **ER2** と入力します。
4. **式の編集** を選択します。
5. 式エディターで、**式** フィールドに、**FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** と入力します。
6. **保存** を選択し、式エディターを閉じます。
7. **OK** を選択します。

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>データ モデル内で実行中の ER フォーマットの名前を入力する

選択したモデルマッピングの編集を続けて、実行中の ER フォーマットの名前がデータモデルに入力されるようにします。

1. **モデル マッピング デザイナー** ページの、 **データ モデル** ペインで、**ExecutionContext** を展開し、続いて **ExecutionContext\\FormatName** 編集を選択します。
2. **データモデル** ペインで、**編集** を選択してデータ モデル フィールドのデータ バインドを構成します。
3. 式エディターで、**式** フィールドに **FIRSTORNULL (ER2.'\>Relations'.Format).Name** と入力します。
4. **保存** を選択し、式エディターを閉じます。

**FormatName** フィールドを使用したため、構成されたモデル マッピングでは、実行中にこのモデル マッピングの呼び出しを行う ER フォーマットの名前を公開するようになります。

![ER モデル マッピング デザイナーで追加されたデータソースのメソッドにデータ モデル フィールドをバインドする](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>モデル マッピングを完了する

1. **データ モデル デザイナー** ページで、**保存** を選択します。
2. ページを閉じます。
3. モデル マッピング ページを閉じます。
4. **構成** ページの構成ツリーで、**アンケート マッピング** の構成が選択されていることを確認してください。 続いて、**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。
5. **ステータスの変更** \> **完了** を選択します。

この構成のバージョン 1.2 の状態 **下書き** から **完了** に変更されます。 バージョン 1.2 を変更することはできなくなります。 このバージョンには、構成済みのモデル マッピングが含まれており、その他の ER の構成の基礎として使用できます。 この構成のバージョン 1.3 が作成され、状態が **下書き** になります。 このバージョンを編集して、**アンケート** モデル マッピングを調整することができます。

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>フォーマットを変更する

構成された ER フォーマットを変更することがで、ER フォーマットの実行時に生成されるレポートのフッターに名前が表示させることができます。

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>新たなフォーマット要素を追加する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。
3. **デザイナー** をクリックします。
4. **フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。
5. **追加** を選択して、 選択されたルート項目の **レポート** に新しいネストされたフォーマット要素を追加します。
6. **Excel\\フッター** を選択します。
7. **名前** フィールドに、**フッター** と入力します。
8. **レポート\フッター** を選択し、続いて **追加** を選択します。
9. **テキスト\\文字列** を選択します。

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>追加されたフォーマット要素をバインドする

1. **フォーマット デザーナー** ページ上の **マッピング** タブでのフォーマット ツリーで、**フッター\\文字列** 要素に対して **式の編集** を選択します。
2. 式エディターの **式** フィールドで、**CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** と入力します。
3. **保存** を選択し、式エディターを閉じます。
4. **保存** を選択します。

構成されたフォーマットが、**フッター\\文字列** 要素を使用して、生成されたレポートのフッターにその名前を入力するよう変更されます。

![ER 操作デザイナーで設定したフォーマットにフッター フォーマットの要素を追加する](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>フォーマットの設計を完了する

1. **形式デザイナー** ページを閉じます。
2. **構成** ページの構成ツリーで、**アンケート レポート** の構成が選択されていることを確認してください。 続いて、**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。
3. **ステータスの変更** \> **完了** を選択します。

この構成のバージョン 1.2 の状態 **下書き** から **完了** に変更されます。 バージョン 1.2 を変更することはできなくなります。 このバージョンには、構成済みのフォーマットが含まれており、その他の ER の構成の基礎として使用することができます。 この構成のバージョン 1.3 が作成され、状態が **下書き** になります。 このバージョンを編集して、**アンケート** レポートを調整することができます。

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>アプリケーションからフォーマットを実行する

1. **アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。
2. ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。
3. **OK** を選択します。
4. **ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
5. **OK** を選択してオプションを確認します。
6. **OK** を選択してレポートを実行します。
7. Excel フォーマットで生成されたレポートを確認してください。

生成されたレポートのフッターには、生成に使用した ER フォーマットの名前が含まれることに注意してください。

![Excel フォーマットで生成されたレポート](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>ER からフォーマットを実行する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。
3. アクション ウィンドウで、**実行** を選択します。
4. **電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
5. **OK** を選択してオプションを確認します。
6. **OK** を選択してレポートを実行します。
7. Excel フォーマットで生成されたレポートを確認してください。

生成されるレポートのフッターには、生成時に使用された ER 形式の名前が含まれないことに注意してください。これは ER から実行されたER フォーマットが呼び出したデータ コントラクト オブジェクトが、実行中のモデル マッピングに渡されないためです。

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>オン スクリーン プレビューに使用するフォーマットの出力先を構成する

1. **組織管理** \> **電子レポート** \> **電子レポートの送信先** に移動します。
2. **電子レポートの送信先** ページで、構成済の ER フォーマット **アンケート レポート** の送信先レコードを追加します。
3. **ファイルの送信先** クイックタブで、構成済み ER フォーマット **アンケート レポート** のルート要素として [追加された](#AddFormatRootElement)**レポート** フォーマット コンポーネントの [送信先](er-destination-type-screen.md)**画面** を設定します。
4. **PDF 変換設定** ファストタブで、送信先の構成を行い、レポートの印刷の向きを **横方向** に設定した[PDF フォーマット](electronic-reporting-destinations.md#OutputConversionToPDF)へと変換します。

![電子レポートのカスタム画面送信先を設定して ER フォーマットの送信先を構成する](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>アプリケーションからフォーマットを実行して、PDF ドキュメントでプレビューする

1. **アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。
2. ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。
3. **OK** を選択します。
4. **電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。
5. **OK** を選択してオプションを確認します。

    **宛先** クイック タブで、**出力** フィールドが  **画面** に設定されていることを確認します。 構成済の送信先を変更する場合は、**変更** を選択し ます。

    ![ER レポートのランタイム ダイアログ ボックスで構成された送信先を変更する](./media/er-quick-start1-run-settings.png)

6. **OK** を選択してレポートを実行します。
7. PDF フォーマットで生成されたレポートを確認してください。

    ![PDF フォーマットで生成されたレポートの画面上でのレビュー](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [電子報告のフォーミュラ言語](er-formula-language.md)
- [多言語レポートのデザイン](er-design-multilingual-reports.md)
- [電子申告フレームワーク API](er-apis-app73.md)
- [CASE 関数](er-functions-logical-case.md)
- [CONCATENATE 関数](er-functions-text-concatenate.md)
- [DATETIMEFORMAT 関数](er-functions-datetime-datetimeformat.md)
- [FILTER 関数](er-functions-list-filter.md)
- [FIRSTORNULL 関数](er-functions-list-firstornull.md)
- [FORMAT 関数](er-functions-text-format.md)
- [IF 関数](er-functions-logical-if.md)
- [ORDERBY 関数](er-functions-list-orderby.md)
- [SESSIONNOW 関数](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
