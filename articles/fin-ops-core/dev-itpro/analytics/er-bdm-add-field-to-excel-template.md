---
title: Microsoft Excel のビジネス ドキュメント テンプレートへの新しいフィールドの追加
description: このトピックでは、ビジネス ドキュメント管理機能を使用して、Microsoft Excel でビジネス ドキュメント テンプレートに新しいフィールドを追加する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d6e0f2c914b8d348ef6eac42557fb46c53df04a9
ms.sourcegitcommit: d16d370dab734e09312cb06711beca9cca52d4c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809523"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Microsoft Excel のビジネス ドキュメント テンプレートへの新しいフィールドの追加

[!include[banner](../includes/banner.md)]

ビジネス ドキュメントを Microsoft Excel 形式で生成するために使用されるテンプレートに新しいフィールドを追加できます。 これらのフィールドを、生成されたドキュメントにアプリケーションの必要な情報を入力するために使用されるプレースホルダーとして追加できます。 追加するすべてのフィールドに、データソースへのバインドを指定し、テンプレートを使用してビジネス ドキュメントを生成するときにフィールドに入力するアプリケーション データを指定することもできます。

この機能の詳細を知るには、このトピックの例を実行します。 この例では、テンプレートを更新して、生成された自由書式の請求書のフォームのフィールドに入力する方法を示します。

## <a name="configure-business-document-management-to-edit-templates"></a>テンプレートを編集するための、ビジネス ドキュメント管理のコンフィギュレーション

ビジネス ドキュメント管理 (BDM) は、[電子報告 (ER) の概要](general-electronic-reporting.md) フレームワークを基に構築されているため、BDM を使用して作業を開始できるようにするには、必要な ER パラメーターと BDM パラメーターをコンフィギュレーションする必要があります。

1.  Microsoft Dynamics 365 Financeのインスタンスにシステム管理者としてサインインします。
2.  [ビジネス ドキュメント管理の概要](er-business-document-management.md) トピックの例の、次の手順を実行します。

    1.  ER パラメーターのコンフィギュレーション。
    2.  BDM 有効にします。

これで、BDM を使用して、ビジネス ドキュメント テンプレートを編集することができます。

## <a name="import-er-solutions-that-contain-a-template"></a>テンプレートを含む ER ソリューションのインポート

この手順の例では、正式に公開された ER ソリューションを使用しています。 このソリューションの ER コンフィギュレーションを Finance の現在のインスタンスにインポートする必要があります。

このソリューションの**自由書式の請求書 (Excel)** ER 形式コンフィギュレーションには、BDM を使用して編集できる Excel 形式のビジネス ドキュメント テンプレートが含まれています。 この ER 形式コンフィギュレーションの最新バージョンを Microsoft Dynamics Lifecycle サービス (LCS) からインポートします。 対応する ER データ モデルと ER モデル マッピングのコンフィギュレーションが自動的にインポートされます。

ER コンフィギュレーションをインポートする方法の詳細については、[ER コンフィギュレーション ライフサイクルの管理](general-electronic-reporting-manage-configuration-lifecycle.md) を参照してください。

![LCS 共有アセット ライブラリ ページ](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>ER ソリューションテンプレートの編集

1.  **ビジネス ドキュメント管理**のワークスペースへのアクセス権を持つユーザーとして、ログインします。
2.  **ビジネス ドキュメント管理**のワークスペースを開きます。

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM-AddFldExcel-Workspace.png)

3.  グリッドで、**自由書式の請求書 (Excel)** テンプレートを選択します。
4.  右ウィンドウで、**新しいテンプレート**を選択すると、選択したテンプレートに基づく新しいテンプレートが作成されます。
5.  **タイトル**フィールドに、新しいテンプレートのタイトルとして**自由書式の請求書 (Excel) Contoso** を入力します。
6.  **OK** を選択して、編集プロセスの開始を確認します。

BDM テンプレートのエディターページが表示されます。 Microsoft Office 365 を使用して、選択したテンプレートを埋め込みコントロールでオンラインで編集できます。

![BDM テンプレートのエディター ページ](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>テンプレートに新しいフィールドのラベルを追加する

1.  BDM テンプレート エディター ページの Excel リボンの**表示**タブで、編集可能な Excel テンプレートの**ヘッダーとグリッド線**チェック ボックスをオンにします。

    ![ヘッダーとグリッド線チェック ボックスをオンにする](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  セル **E8: F8** を選択します。
3.  Excel リボンの**ホーム**タブで、**結合して中央揃え**を選択して、選択したセルを新しい結合されたセル **E8: F8** に結合します。
4.  結合されたセル **E8: F8** に、**URL** を入力します。
5.  結合されたセル **E7:F7** を選択し、**書式のコピー/貼り付け**を選択して、結合されたセル **E8: F8** を選択して結合されたセル **E7:F7** と同じように書式設定します。

    ![テンプレートに追加する新しいフィールド ラベル](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>新しいフィールドのスペースを確保するテンプレートの書式設定

1.  BDM テンプレート エディター ページで、結合されたセル **G8 H8** を選択します。
2.  Excel リボンの**ホーム**タブで、**結合して中央揃え**を選択して、選択したセルを新しい結合されたセル **G8: H8** に結合します。
3.  結合されたセル **G7:H7** を選択し、**書式のコピー/貼り付け**を選択して、結合されたセル **G8:H8** を選択して結合されたセル **G7:H7** と同じように書式設定します。

    ![新しいフィールド用に確保されたスペース](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  **名前**ボックス フィールドで **CompanyInfo** を選択します。

    現在の Excel テンプレートの **CompanyInfo** の範囲には、生成されたレポートのヘッダーに、販売者として現在の会社の詳細を記入するために使用するすべてのフィールドが含まれています。

    ![選択された CompanyInfo の範囲](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>テンプレートに新しいフィールドを追加する

1.  **BDM テンプレート エディター** ページのアクション ウィンドウで、**形式の表示**を選択します。
2.  **テンプレート構造**ウィンドウで、**追加**を選択します。

    > [!NOTE]
    > 新しいフィールドとして使用するテンプレートのセクションを調整する必要があります。 この調整は、結合されたセル **G8: H8** をフォーマットすることによって既に行われています。

    ![テンプレートに新しいフィールドを追加する](./media/BDM-AddFldExcel-AddCell.png)

3.  テンプレートにセルとして新しいフィールドを追加するには、**Excel\Cell** を選択します。

    テンプレートに新しい範囲を追加する場合は、**Excel\Range** を選択できます。 入力される範囲には、複数のセルを含めることができます。 これらのセルは、後で追加できます。
    
    追加するフィールドの現在のテンプレート構造に最も適した親コンポーネントであるため、**CompanyInfo** テンプレート コンポーネントが、**テンプレート構造**ウィンドウで自動的に選択されます。
    
4.  **Excel の範囲** フィールドに、**CompanyURL_Value** を入力します。
5.  **OK** を選択します。

    ![テンプレート構造に追加された CompanyURL_Value フィールド](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  **テンプレート構造**ウィンドウで、省略符号ボタン (...) を選択し、**バインディングの表示**を選択します。

    ![選択されたバインディングの表示](./media/BDM-AddFldExcel-ShowBindings.png)

    **テンプレート構造**ウィンドウに、基になる ER 形式で使用できるデータ ソースが表示されます。

7.  基になる ER 形式のデータ ソースに連結する予定のフィールドとして **CompanyInfo_Value** を選択します。
8.  **テンプレート構造**ウィンドウの**データ ソース** セクションで、**モデル \> InvoiceBase \> CompanyInfo** を展開します。
9.  **CompanyInfo** で、**WebsiteURI** 項目を選択します。

    ![選択された WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. **バインド**を選択します。
11. **テンプレート構造**ウィンドウで、**保存**をクリックし、BDM テンプレート エディター ページを閉じます。

**ビジネス ドキュメント管理**ワークスペースでは、更新されたテンプレートが右ウィンドウの**テンプレート** タブに表示されます。 グリッドで、編集したテンプレートの**ステータス** フィールドが**下書き**に変更され、**リビジョン** フィールドが空白でなくなっていることを確認します。 これらの変更は、このテンプレートの編集のプロセスが開始されたことを示します。

![ビジネス ドキュメント管理ワークスペースで編集されたテンプレート](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>会社設定の確認

1.  **組織管理 \> 組織 \> 法人**の順に移動します。
2.  **連絡先情報**クイック タブに、会社 URL が入力されていることを確認します。

![法人ページに入力された会社 URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>更新されたテンプレートをテストするためのビジネス ドキュメントの生成

1.  アプリケーションで、会社を **USMF** に変更し、**売掛金勘定 \> 請求書 \> すべての自由書式の請求書**に移動します。
2.  請求書 **FTI-00000002** を選択し、**印刷管理**を選択します。
3.  左ウィンドウで、**モジュール - 売掛金勘定 \> ドキュメント \> 自由書式の請求書**を展開します。
4.  **自由書式の請求書**で、**元のドキュメント** レベルを選択して、処理する請求書の範囲を指定します。
5.  右ウィンドウの、**レポート形式**フィールドで、指定されたドキュメント レベルの**自由書式の請求書 (Excel) Contoso** テンプレートを選択します。

    ![選択した自由書式の請求書 (Excel) Contoso テンプレート](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  **Esc** を押して、現在のページを閉じます。
7.  **印刷 \> 選択済**を選択します。
8.  生成されたドキュメントをダウンロードして、Excel で開きます。

    ![Excel の自由書式の請求書](./media/BDM-AddFldExcel-PreviewReport.png)

変更したテンプレートは、選択した品目に対して自由書式の請求書レポートを生成するために使用されます。 テンプレートに加えた変更によってこのレポートがどのように影響を受けるかを分析するには、別のアプリケーション セッションでテンプレートを変更した直後に、1 つのアプリケーション セッションでこのレポートを実行します。

## <a name="related-links"></a>関連リンク

[電子申告 (ER) の概要](general-electronic-reporting.md)

[ビジネス ドキュメント管理の概要](er-business-document-management.md)

[OPENXML 形式のレポートを生成するコンフィギュレーションを設計する](tasks/er-design-reports-openxml-2016-11.md)
