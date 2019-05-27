---
title: 最初から用意されているレポートを生成および実行
description: このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550073"
---
# <a name="generate-and-run-out-of-box-reports"></a>最初から用意されているレポートを生成および実行

[!include[task guide banner](../includes/task-guide-banner.md)]

このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。



この記録の作成に使用するデモ データの会社は USRT です。 この記録は、システム管理者ロールを対象としています。


## <a name="launch-reports-from-workspaces"></a>ワークスペースからレポートの起動
1. [小売りとコマース] > [製品とカテゴリ] > [カテゴリと製品の管理] に移動します。
2. レポート セクションを展開または折りたたむには、矢印をクリックします。
3. 上位製品レポートをクリックします。
4. [開始日] フィールドに日付を入力します。
5. [終了日] フィールドで、日付を入力します。
6. [チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. ツリーで、「Contoso Retail\Contoso Retail USA\Central\Houston」を選択します。
    * これは、[小売レポート用] の既定の小売組織階層を示します。   [組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。      デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。     
8. [OK] をクリックします。
9. [ビュー] フィールドで、オプションを選択します。
10. [By] フィールドで、オプションを選択します。
11. [OK] をクリックします。

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a>[小売 & コマース] アプリ リンクの下にある照会と販売レポートからレポートを起動します。
1. [小売とコマース] > [照会およびレポート] > [販売レポート] > [カテゴリ売上レポート] に移動します。
2. [開始日] フィールドに日付を入力します。
3. [終了日] フィールドで、日付を入力します。
4. [チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. ツリーで、「Contoso Retail\Contoso Retail USA\West\Seattle」を選択します。
    * これは、[小売レポート用] の既定の小売組織階層を示します。   [組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。      デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。     
6. [OK] をクリックします。
7. [OK] をクリックします。

## <a name="export-an-hq-reports"></a>[HQ レポート] をエクスポート
1. [小売とコマース] > [照会およびレポート] > [販売レポート] > [組織売上レポート] に移動します。
2. [開始日] フィールドに日付を入力します。
3. [終了日] フィールドで、日付を入力します。
4. [OK] をクリックします。
5. [エクスポート] をクリックします。
6. PDF をクリックします。

