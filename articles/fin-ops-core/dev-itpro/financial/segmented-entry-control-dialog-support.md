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
ms.openlocfilehash: b89858f978f2e21d26b97ec3382d96944ae404d5
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111582"
---
# <a name="support-for-segmented-entry-controls-on-dialogs"></a><span data-ttu-id="2ccad-103">ダイアログ上のセグメント化されたエントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="2ccad-103">Support for Segmented Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ccad-104">セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2ccad-104">Describes the code pattern to add Segmented Entry controls to dialogs.</span></span>

<span data-ttu-id="2ccad-105">セグメント化されたエントリ コントロールをダイアログに追加するプロセスが変更されました。</span><span class="sxs-lookup"><span data-stu-id="2ccad-105">The process to add Segmented Entry controls to dialogs has changed.</span></span> <span data-ttu-id="2ccad-106">このコードは、Dynamics AX 2012 の例です。</span><span class="sxs-lookup"><span data-stu-id="2ccad-106">This code is an example from Dynamics AX 2012:</span></span>

```xpp
DialogField dialogFeeLedgerDimension;
LedgerDimensionAccountController ledgerDimensionAccountController;
dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703");
ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);
```

<span data-ttu-id="2ccad-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="2ccad-107">In the current release, this code would be converted to:</span></span>

```xpp
DialogField dialogFeeLedgerDimension;
dialogFeeLedgerDimension = SegmentedEntryControlBuild::addToDialog(
    dialog, 
    classstr(LedgerDimensionAccountController), 
    extendedTypeStr(LedgerDimensionAccount), 
    "@SYS119703", 
    feeLedgerDimension);
```

<span data-ttu-id="2ccad-108">2 番目のパラメーターでは、ダイアログの要件を満たすクラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="2ccad-108">For the second parameter, choose the class that satisfies the requirements for your dialog.</span></span>  <span data-ttu-id="2ccad-109">オプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2ccad-109">The options are:</span></span>

-   <span data-ttu-id="2ccad-110">LedgerDimensionAccountController</span><span class="sxs-lookup"><span data-stu-id="2ccad-110">LedgerDimensionAccountController</span></span>
-   <span data-ttu-id="2ccad-111">LedgerDimensionDefaultAccountController</span><span class="sxs-lookup"><span data-stu-id="2ccad-111">LedgerDimensionDefaultAccountController</span></span>
-   <span data-ttu-id="2ccad-112">DimensionDynamicAccountController</span><span class="sxs-lookup"><span data-stu-id="2ccad-112">DimensionDynamicAccountController</span></span>
-   <span data-ttu-id="2ccad-113">BudgetLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="2ccad-113">BudgetLedgerDimensionController</span></span>
-   <span data-ttu-id="2ccad-114">BudgetPlanningLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="2ccad-114">BudgetPlanningLedgerDimensionController</span></span>

<span data-ttu-id="2ccad-115">このシナリオは、セグメント化されたエントリについての簡単なダイアログ シナリオです。</span><span class="sxs-lookup"><span data-stu-id="2ccad-115">This scenario is a simple dialog scenario around Segmented Entry.</span></span> <span data-ttu-id="2ccad-116">さらに高度なシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2ccad-116">More advanced scenarios include:</span></span>

-   <span data-ttu-id="2ccad-117">動的アカウントをバインドしています。</span><span class="sxs-lookup"><span data-stu-id="2ccad-117">Binding the dynamic account type.</span></span>
-   <span data-ttu-id="2ccad-118">会社の選択をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2ccad-118">Company selection support.</span></span>
-   <span data-ttu-id="2ccad-119">勘定構造選択のサポート。</span><span class="sxs-lookup"><span data-stu-id="2ccad-119">Account structure selection support.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2ccad-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2ccad-120">Additional resources</span></span>

[<span data-ttu-id="2ccad-121">セグメント化されたエントリ コントロールのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="2ccad-121">Design-time metadata for Segmented Entry controls</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="2ccad-122">セグメント化されたエントリ コントロールの `Parm` メソッド</span><span class="sxs-lookup"><span data-stu-id="2ccad-122">`Parm` methods for Segmented Entry controls</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="2ccad-123">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="2ccad-123">Migrate Segmented Entry controls</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="2ccad-124">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="2ccad-124">Migration guidance for Segmented Entry controls</span></span>](segmented-entry-control-migration-guidance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]