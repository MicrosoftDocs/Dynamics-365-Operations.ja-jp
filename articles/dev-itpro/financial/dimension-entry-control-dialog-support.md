---
title: "ダイアログ上の分析コード エントリ コントロールをサポート"
description: "分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26321
ms.assetid: ec5f2f8c-eb9b-4fbe-a388-be145b2bf98b
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f5eb1b69e85a7d8677638f5b1faf28950b0626b7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="support-for-dimension-entry-controls-on-dialogs"></a><span data-ttu-id="d1860-103">ダイアログ上の分析コード エントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="d1860-103">Support for Dimension Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1860-104">分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d1860-104">Describes the code pattern for putting a Dimension Entry control on a dialog.</span></span>

<span data-ttu-id="d1860-105">分析コード エントリ コントロールをダイアログに追加するためのコード パターンが Dynamics AX 2012 から変更されました。</span><span class="sxs-lookup"><span data-stu-id="d1860-105">The code pattern to add Dimension Entry controls to dialogs has changed from Dynamics AX 2012.</span></span> <span data-ttu-id="d1860-106">これは、古いモデルの例です。</span><span class="sxs-lookup"><span data-stu-id="d1860-106">This is an example of the old model:</span></span>

    DimensionDefaultingControllerNoDS dimDefaultingController;
    dimDefaultingController = DimensionDefaultingControllerNoDS::constructInGroupWithValues(true, true, true, 0, _formRun, financialDimensionGroup, "@SYS123456");
    dimDefaultingController.setNonActiveValueTolerance(ErrorTolerance::Error);
    dimDefaultingController.pageActivated();
    dimDefaultingController.loadValues(dimensionAttributeValueSetId);

<span data-ttu-id="d1860-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="d1860-107">In the current release, this code would be converted to:</span></span>

    DialogField dimensionEntryField;
    DimensionEntryControl dimensionEntryValues;
    dimensionEntryField = DimensionEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionEntryController));
    dimensionEntryValues = dimensionEntryField.control();
    dimensionEntryValues.parmNonActiveValueErrorTolerance(ErrorTolerance::Error);
    dimensionEntryValues.parmDisplayValues(true);
    dimensionEntryValues.reactivate();
    dimensionEntryValues.loadAttributeValueSet(dimensionAttributeValueSetId);

<span data-ttu-id="d1860-108">`addToDialog` の 2 番目のパラメーターでは、ダイアログの要件を満たすコントローラー クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1860-108">For the second parameter on `addToDialog`, choose the controller class that satisfies the requirements for your dialog.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1860-109">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d1860-109">Additional resources</span></span>

[<span data-ttu-id="d1860-110">分析コード エントリ コントロールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="d1860-110">Dimension Entry control migration walkthrough</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="d1860-111">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="d1860-111">Dimension Entry control uptake</span></span>](dimension-entry-control-uptake.md)




