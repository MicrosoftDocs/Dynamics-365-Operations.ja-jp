---
title: ダイアログ上の分析コード エントリ コントロールをサポート
description: 分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。
author: robinarh
manager: AnnBe
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26321
ms.assetid: ec5f2f8c-eb9b-4fbe-a388-be145b2bf98b
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9408c6d834ac1c56eac5d5e073def6516263454
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680514"
---
# <a name="support-for-dimension-entry-controls-on-dialogs"></a>ダイアログ上の分析コード エントリ コントロールをサポート

[!include [banner](../includes/banner.md)]

分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。

分析コード エントリ コントロールをダイアログに追加するためのコード パターンが Dynamics AX 2012 から変更されました。 これは、古いモデルの例です。

```xpp
DimensionDefaultingControllerNoDS dimDefaultingController;
dimDefaultingController = DimensionDefaultingControllerNoDS::constructInGroupWithValues(true, true, true, 0, _formRun, financialDimensionGroup, "@SYS123456");
dimDefaultingController.setNonActiveValueTolerance(ErrorTolerance::Error);
dimDefaultingController.pageActivated();
dimDefaultingController.loadValues(dimensionAttributeValueSetId);
```

現在のリリースでは、このコードは次のように変換されます。
    
```xpp
//When you create a dialog
DialogField dimensionEntryField;
DimensionEntryControl dimensionEntryValues;
dimensionEntryField = DimensionEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionEntryController));

//These lines should be executed after the dialog form is created (for example on “dialogPostRun()” or “postRun()”)
dimensionEntryValues = dimensionEntryField.control();
dimensionEntryValues.parmNonActiveValueErrorTolerance(ErrorTolerance::Error);
dimensionEntryValues.parmDisplayValues(true);
dimensionEntryValues.reactivate();
dimensionEntryValues.loadAttributeValueSet(dimensionAttributeValueSetId);
```

`addToDialog` の 2 番目のパラメーターでは、ダイアログの要件を満たすコントローラー クラスを選択します。

## <a name="additional-resources"></a>追加リソース

[既定の分析コード コントロールの分析コード エントリ コントロールへの移行](dimension-entry-control-migration.md)

[分析コード エントリ コントロールの取得](dimension-entry-control-uptake.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]