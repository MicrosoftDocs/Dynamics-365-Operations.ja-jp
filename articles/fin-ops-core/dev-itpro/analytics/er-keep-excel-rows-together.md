---
title: 同じ Excel ページに行をまとめる ER 形式を設計する
description: このトピックでは、同じ Microsoft Excel ページで一緒に行を維持する電子レポート (ER) 形式を設計する方法について説明します。
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 06782a4933fb5c3e86ad436b853f207fd3d5cddb
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612373"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>同じ Excel ページに行をまとめる ER 形式を設計する

[!include [banner](../includes/banner.md)]


このトピックでは、システム管理者または電子報告書業務コンサルタントの役割を持つユーザーが、[電子レポート (ER)](general-electronic-reporting.md)[形式](er-overview-components.md#format-component) を構成して、Microsoft Excel で送信文書を生成し、文書のページ設定を管理する方法について説明します。

この例では、Excel で自由書式の請求書を印刷するために使用される Microsoft 提供の ER 形式を変更します。 変更を行った場合、生成された自由形式請求書レポートの改ページ位置の自動修正を管理して、可能であれば単一の請求明細のすべての行が同じページに保持されます。

このトピックの手順は、**USMF** 会社で完了することができます。 コーディングは必要ありません。

この例では、サンプル会社 **Litware, Inc.** に必要な ER [構成](general-electronic-reporting.md#Configuration) を作成します。 **Litware, Inc.** (`http://www.litware.com`) サンプル会社の構成プロバイダーが ER フレームワークにリストされており、**有効** アクティブとマークされていることを確認します。 この構成プロバイダーがリストに表示されない場合、または **有効** としてマークされていない場合、[構成プロバイダーの作成および有効としてマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) の手順に従ってください。

## <a name="enter-a-new-free-text-invoice"></a>新しい自由書式の請求書の入力

1. [自由形式の請求書の作成](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) の手順に従って自由形式の請求書を追加します。

    1. 単一明細行を請求に追加します。
    2. 請求明細に 5 つのメモを追加します。

    ![添付ファイル ページで請求明細メモをレビューする。](./media/er-keep-excel-rows-together-notes.png)

2. [明細行のコピー](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) の手順に従って、前の手順で追加した請求明細行をコピーする 5 つの追加の請求明細行を作成します。

    ![自由形式の請求書ページで自由形式の請求明細行をレビューします。](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a> ER フレームワークを構成する

[ER フレームワークの構成](er-quick-start2-customize-report.md#ConfigureFramework)に記載の手順に従って、 ER パラメーターの最小限のセットを構成します。 ER フレームワークを使って、標準的な ER フォーマットのカスタム バージョンを設計する前に、この設定を完了しておく必要があります。

## <a name="import-the-standard-er-format-configuration"></a>標準 ER フォーマットの構成をインポートする

[標準的な ER フォーマットの構成をインポートする](er-quick-start2-customize-report.md#ImportERSolution1) に記載の手順に従って、標準的な ER の構成を現在の Dynamics 365 Finance のインスタンスに追加します。 例えば、**自由書式の請求書 (Excel)** 形式構成のバージョン **252.116** をインポートします。 基本の **請求書モデル** 構成のの基本バージョン **252** が、必要な **請求書モデル マッピング** 構成と共に、リポジトリから自動的にインポートされます。

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>標準 ER 形式を使用するための印刷管理の設定

標準 ER 形式を使用して自由書式の請求書を印刷するために **売掛金勘定** モジュールの印刷管理を構成するには、[印刷管理を設定する](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) 手順に従います。

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>標準 ER 形式の形式の出力先を構成する

[スクリーンのプレビューの形式の出力先を構成する](er-quick-start1-new-solution.md#ConfigureDestination) の手順に従って、標準 ER 形式の [スクリーン](er-destination-type-screen.md)  ER 出力先を構成して、生成されたレポートを PDF 形式に変換し、新しいブラウザのタブでプレビュー表示します。

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>標準 ER 形式を使用した自由書式の請求書を印刷する

1. [自由書式の請求書を印刷](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) の手順に従って、標準 ER 形式を使用して、追加された請求書の自由書式の請求書レポートを Excel 形式で生成します。
2. 生成した Excel ブックをダウンロードし、Excel デスクトップ アプリケーションで確認します。

    請求書の 6 行目がレポートの最初のページで開始し、2 ページ目に続く点に注意してください。 2 ページ目に最後の注記が表示され、それが 6 番目の請求書の行に属しているということは明らかではありません。 したがって、請求行のコンテンツの中央の改ページにより、このドキュメントがより読みにくくなります。

    ![Excel デスクトップ アプリケーションで生成された自由形式請求書の改ページ位置の自動修正を確認する。](./media/er-keep-excel-rows-together-invoice1.gif)

このトピックの残りの手順では、標準 ER 形式を調整して、同じページの単一請求明細行のすべてのコンテンツを維持することで、請求書レポートの外観と読み取りを向上させる方法を示します。

## <a name="create-a-custom-format"></a> カスタム形式の作成

[カスタム形式の作成](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) の手順に従って、インポートされたER 形式からひとつの形式を派生させ、編集および変更用に使用できる **自由書式請求書 (Excel) カスタム** ER 構成を作成します。

## <a name="edit-the-custom-format"></a>カスタム形式を編集する

1. [カスタム形式の作成](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) の手順に従って、ER 形式デザイナーを編集するために派生した ER 形式を開きます。
2. **形式フォーマット** ページで、左ペインのフォーマット コンポーネント ツリーで、**自由形式テキスト請求書\>シート\>InvoiceLines** を展開し、**InvoiceLines_Values** コンポーネントを選択します。
3. **フォーマット** タブで、**行をまとめて保持** オプションを　**はい** に設定します。

    ![形式デザイナー ページで、編集可能なER形式の [行をまとめて保存] オプションを設定します。](./media/er-keep-excel-rows-together-format.png)

4. **保存** を選択して、ページを閉じます。

## <a name="mark-the-custom-format-as-runnable"></a>カスタム形式を実行可能としてマークする

[カスタム形式を実行可能としてマークする](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) の手順に従って、カスタム ER 形式の変更されたバージョンを実行可能にします。

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>カスタム ER 形式を使用するための印刷管理の設定

カスタム ER 形式を使用して自由書式の請求書を印刷するために **売掛金勘定** モジュールの印刷管理を構成するには、[印刷管理を設定する](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) 手順に従います。

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>カスタム ER 形式の形式の出力先を構成する

[スクリーンのプレビューの形式の出力先を構成する](er-quick-start1-new-solution.md#ConfigureDestination) の手順に従って、カスタム ER 形式の **スクリーン** ER 出力先を構成して、生成されたレポートを PDF 形式に変換し、新しいブラウザのタブでプレビュー表示します。

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>カスタム ER 形式を使用した自由書式の請求書を印刷する

1. [自由書式の請求書を印刷](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) の手順に従って、カスタム ER 形式を使用して、追加された請求書の自由書式の請求書レポートを Excel 形式で生成します。
2. 生成した Excel ブックをダウンロードし、Excel デスクトップ アプリケーションで確認します。

    6 行目の請求書が 2 ページ目に開始し、この請求明細を表す Excel 行すべてがそのページにまとめて表示されます。

    ![Excel デスクトップ アプリケーションで生成された自由形式請求書の更新された改ページ位置の自動修正をレビューします。](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>追加リソース

[ドキュメントを Excel 形式で生成するためのコンフィギュレーションを設計する](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
