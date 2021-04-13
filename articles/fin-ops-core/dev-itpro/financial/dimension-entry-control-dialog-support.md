---
title: ダイアログ上の分析コード エントリ コントロールをサポート
description: 分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。
author: robinarh
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26321
ms.assetid: ec5f2f8c-eb9b-4fbe-a388-be145b2bf98b
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c313493d560b7a8bc0840dcf1b350c54a8d943b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753916"
---
# <a name="support-for-dimension-entry-controls-on-dialogs"></a><span data-ttu-id="cd02b-103">ダイアログ上の分析コード エントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="cd02b-103">Support for Dimension Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd02b-104">分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cd02b-104">Describes the code pattern for putting a Dimension Entry control on a dialog.</span></span>

<span data-ttu-id="cd02b-105">分析コード エントリ コントロールをダイアログに追加するためのコード パターンが Dynamics AX 2012 から変更されました。</span><span class="sxs-lookup"><span data-stu-id="cd02b-105">The code pattern to add Dimension Entry controls to dialogs has changed from Dynamics AX 2012.</span></span> <span data-ttu-id="cd02b-106">これは、古いモデルの例です。</span><span class="sxs-lookup"><span data-stu-id="cd02b-106">This is an example of the old model:</span></span>

```xpp
DimensionDefaultingControllerNoDS dimDefaultingController;
dimDefaultingController = DimensionDefaultingControllerNoDS::constructInGroupWithValues(true, true, true, 0, _formRun, financialDimensionGroup, "@SYS123456");
dimDefaultingController.setNonActiveValueTolerance(ErrorTolerance::Error);
dimDefaultingController.pageActivated();
dimDefaultingController.loadValues(dimensionAttributeValueSetId);
```

<span data-ttu-id="cd02b-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="cd02b-107">In the current release, this code would be converted to:</span></span>
    
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

<span data-ttu-id="cd02b-108">`addToDialog` の 2 番目のパラメーターでは、ダイアログの要件を満たすコントローラー クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd02b-108">For the second parameter on `addToDialog`, choose the controller class that satisfies the requirements for your dialog.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd02b-109">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cd02b-109">Additional resources</span></span>

[<span data-ttu-id="cd02b-110">既定の分析コード コントロールの分析コード エントリ コントロールへの移行</span><span class="sxs-lookup"><span data-stu-id="cd02b-110">Migrate default dimensions controls to Dimension Entry controls</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="cd02b-111">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="cd02b-111">Uptake of Dimension Entry controls</span></span>](dimension-entry-control-uptake.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]