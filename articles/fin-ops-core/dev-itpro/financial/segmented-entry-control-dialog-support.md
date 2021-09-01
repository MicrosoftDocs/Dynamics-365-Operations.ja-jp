---
title: ダイアログ上のセグメント化されたエントリ コントロールをサポート
description: セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25571
ms.assetid: cd09af5e-2e6e-41fd-8e74-6612afb016f5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e7e73f8de3af956accc867a1b4ca56396bd644c3af117d7cd6cc5a2ff329978
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759213"
---
# <a name="support-for-segmented-entry-controls-on-dialogs"></a>ダイアログ上のセグメント化されたエントリ コントロールをサポート

[!include [banner](../includes/banner.md)]

セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。

セグメント化されたエントリ コントロールをダイアログに追加するプロセスが変更されました。 このコードは、Dynamics AX 2012 の例です。

```xpp
DialogField dialogFeeLedgerDimension;
LedgerDimensionAccountController ledgerDimensionAccountController;
dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703");
ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);
```

現在のリリースでは、このコードは次のように変換されます。

```xpp
DialogField dialogFeeLedgerDimension;
dialogFeeLedgerDimension = SegmentedEntryControlBuild::addToDialog(
    dialog, 
    classstr(LedgerDimensionAccountController), 
    extendedTypeStr(LedgerDimensionAccount), 
    "@SYS119703", 
    feeLedgerDimension);
```

2 番目のパラメーターでは、ダイアログの要件を満たすクラスを選択します。  オプションは次のとおりです。

-   LedgerDimensionAccountController
-   LedgerDimensionDefaultAccountController
-   DimensionDynamicAccountController
-   BudgetLedgerDimensionController
-   BudgetPlanningLedgerDimensionController

このシナリオは、セグメント化されたエントリについての簡単なダイアログ シナリオです。 さらに高度なシナリオは次のとおりです。

-   動的アカウントをバインドしています。
-   会社の選択をサポートしています。
-   勘定構造選択のサポート。


## <a name="additional-resources"></a>追加リソース

[セグメント化されたエントリ コントロールのデザイン時メタデータ](segmented-entry-control-metadata-specification.md)

[セグメント化されたエントリ コントロールの `Parm` メソッド](segmented-entry-control-parm-method-specification.md)

[セグメント化されたエントリ コントロールの移行](segmented-entry-control-conversion.md)

[セグメント化されたエントリ コントロールに関する移行ガイダンス](segmented-entry-control-migration-guidance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]