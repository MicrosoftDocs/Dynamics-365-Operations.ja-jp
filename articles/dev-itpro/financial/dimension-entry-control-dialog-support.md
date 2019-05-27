---
title: ダイアログ上の分析コード エントリ コントロールをサポート
description: 分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26321
ms.assetid: ec5f2f8c-eb9b-4fbe-a388-be145b2bf98b
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cce80252b59700be52f458ac8bc9cec279b2154
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537387"
---
# <a name="support-for-dimension-entry-controls-on-dialogs"></a><span data-ttu-id="c7b96-103">ダイアログ上の分析コード エントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="c7b96-103">Support for Dimension Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7b96-104">分析コード エントリ コントロールをダイアログに配置するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c7b96-104">Describes the code pattern for putting a Dimension Entry control on a dialog.</span></span>

<span data-ttu-id="c7b96-105">分析コード エントリ コントロールをダイアログに追加するためのコード パターンが Dynamics AX 2012 から変更されました。</span><span class="sxs-lookup"><span data-stu-id="c7b96-105">The code pattern to add Dimension Entry controls to dialogs has changed from Dynamics AX 2012.</span></span> <span data-ttu-id="c7b96-106">これは、古いモデルの例です。</span><span class="sxs-lookup"><span data-stu-id="c7b96-106">This is an example of the old model:</span></span>

    DimensionDefaultingControllerNoDS dimDefaultingController;
    dimDefaultingController = DimensionDefaultingControllerNoDS::constructInGroupWithValues(true, true, true, 0, _formRun, financialDimensionGroup, "@SYS123456");
    dimDefaultingController.setNonActiveValueTolerance(ErrorTolerance::Error);
    dimDefaultingController.pageActivated();
    dimDefaultingController.loadValues(dimensionAttributeValueSetId);

<span data-ttu-id="c7b96-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="c7b96-107">In the current release, this code would be converted to:</span></span>
    
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

<span data-ttu-id="c7b96-108">`addToDialog` の 2 番目のパラメーターでは、ダイアログの要件を満たすコントローラー クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="c7b96-108">For the second parameter on `addToDialog`, choose the controller class that satisfies the requirements for your dialog.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7b96-109">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c7b96-109">Additional resources</span></span>

[<span data-ttu-id="c7b96-110">分析コード エントリ コントロールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="c7b96-110">Dimension Entry control migration walkthrough</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="c7b96-111">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="c7b96-111">Dimension Entry control uptake</span></span>](dimension-entry-control-uptake.md)



