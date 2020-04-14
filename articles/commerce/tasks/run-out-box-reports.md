---
title: 最初から用意されているレポートを生成および実行
description: このタスク ガイドを使用して、異なるワークスペースからバックオフィスの最初から用意されているレポート、およびコマースの照会 & 販売レポートを実行します。
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
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140764"
---
# <a name="generate-and-run-out-of-box-reports"></a>最初から用意されているレポートを生成および実行

[!include [banner](../includes/banner.md)]

このタスク ガイドを使用して、異なるワークスペースからバックオフィスの最初から用意されているレポート、およびコマースの照会 & 販売レポートを実行します。

この記録の作成に使用するデモ データの会社は USRT です。 この記録は、システム管理者ロールを対象としています。

## <a name="launch-reports-from-workspaces"></a>ワークスペースからレポートの起動
1. Retail とコマース > 製品とカテゴリ > カテゴリと製品の管理に移動します。
2. レポート セクションを展開または折りたたむには、矢印をクリックします。
3. 上位製品レポートをクリックします。
4. [開始日] フィールドに日付を入力します。
5. [終了日] フィールドで、日付を入力します。
6. [チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. ツリーで、「Contoso Retail\Contoso Retail USA\Central\Houston」を選択します。
    * これは、コマース レポート用の既定の組織階層を示します。   組織管理 > 組織 > 組織階層の目的に移動し、コマース レポートを選択し、割り当て済の階層で既定の列が選択されている階層名を確認します。 デモ データの一部として (このタスクの記録に使用)、地域ごとの店舗がレポート用の既定の組織階層となっています。     
8. [OK] をクリックします。
9. [ビュー] フィールドで、オプションを選択します。
10. [By] フィールドで、オプションを選択します。
11. [OK] をクリックします。

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>照会および販売レポートからのレポートを開始します
1. Retail とコマース > 照会およびレポート > 販売レポート > カテゴリ売上レポートに移動します。
2. [開始日] フィールドに日付を入力します。
3. [終了日] フィールドで、日付を入力します。
4. [チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. ツリーで、「Contoso Retail\Contoso Retail USA\West\Seattle」を選択します。
    * これは、コマース レポート用の既定の組織階層を示します。 組織管理 > 組織 > 組織階層の目的に移動し、コマース レポートを選択し、割り当て済の階層で既定の列が選択されている階層名を確認します。 デモ データの一部として (このタスクの記録に使用)、地域ごとの店舗がレポート用の既定の組織階層となっています。     
6. [OK] をクリックします。
7. [OK] をクリックします。

## <a name="export-an-hq-reports"></a>[HQ レポート] をエクスポート
1. Retail とコマース > 照会およびレポート > 販売レポート > 組織売上レポートに移動します。
2. [開始日] フィールドに日付を入力します。
3. [終了日] フィールドで、日付を入力します。
4. [OK] をクリックします。
5. [エクスポート] をクリックします。
6. PDF をクリックします。

