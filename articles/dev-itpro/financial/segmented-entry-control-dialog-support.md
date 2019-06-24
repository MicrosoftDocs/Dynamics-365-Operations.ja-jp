---
title: ダイアログ上のセグメント化されたエントリ コントロールをサポート
description: セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25571
ms.assetid: cd09af5e-2e6e-41fd-8e74-6612afb016f5
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50223d98a89fefddf056bf63fb69330ee3079f9f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552512"
---
# <a name="support-for-segmented-entry-controls-on-dialogs"></a>ダイアログ上のセグメント化されたエントリ コントロールをサポート

[!include [banner](../includes/banner.md)]

セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。

セグメント化されたエントリ コントロールをダイアログに追加するプロセスが変更されました。 これは、Dynamics AX 2012 の例です。

    DialogField dialogFeeLedgerDimension;
    LedgerDimensionAccountController ledgerDimensionAccountController;
    dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703");
    ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);

現在のリリースでは、このコードは次のように変換されます。

    DialogField dialogFeeLedgerDimension;
    dialogFeeLedgerDimension = SegmentedEntryControlBuild::addToDialog(
        dialog, 
        classstr(LedgerDimensionAccountController), 
        extendedTypeStr(LedgerDimensionAccount), 
        "@SYS119703", 
        feeLedgerDimension);

2 番目のパラメーターでは、ダイアログの要件を満たすクラスを選択します。  オプションは次のとおりです。

-   LedgerDimensionAccountController
-   LedgerDimensionDefaultAccountController
-   DimensionDynamicAccountController
-   BudgetLedgerDimensionController
-   BudgetPlanningLedgerDimensionController

これは、セグメント化されたエントリについての簡単なダイアログ シナリオです。 さらに高度なシナリオは次のとおりです。

-   動的アカウントをバインドしています。
-   会社の選択をサポートしています。
-   勘定構造選択のサポート。


<a name="additional-resources"></a>その他のリソース
--------

[セグメント化されたエントリ コントロールのメタデータ詳細](segmented-entry-control-metadata-specification.md)

[セグメント化されたエントリ コントロールの Parm メソッド詳細](segmented-entry-control-parm-method-specification.md)

[セグメント化されたエントリ コントロールの移行](segmented-entry-control-conversion.md)

[セグメント化されたエントリ コントロール - 移行のガイダンス](segmented-entry-control-migration-guidance.md)



