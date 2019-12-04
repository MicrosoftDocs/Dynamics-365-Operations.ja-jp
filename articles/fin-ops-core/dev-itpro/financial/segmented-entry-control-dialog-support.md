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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25571
ms.assetid: cd09af5e-2e6e-41fd-8e74-6612afb016f5
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03cba235e34fa2e241d878e90763519ac84c9d29
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812105"
---
# <a name="support-for-segmented-entry-controls-on-dialogs"></a><span data-ttu-id="6706c-103">ダイアログ上のセグメント化されたエントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="6706c-103">Support for Segmented Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6706c-104">セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6706c-104">Describes the code pattern to add Segmented Entry controls to dialogs.</span></span>

<span data-ttu-id="6706c-105">セグメント化されたエントリ コントロールをダイアログに追加するプロセスが変更されました。</span><span class="sxs-lookup"><span data-stu-id="6706c-105">The process to add Segmented Entry controls to dialogs has changed.</span></span> <span data-ttu-id="6706c-106">これは、Dynamics AX 2012 の例です。</span><span class="sxs-lookup"><span data-stu-id="6706c-106">This is an example from Dynamics AX 2012:</span></span>

    DialogField dialogFeeLedgerDimension;
    LedgerDimensionAccountController ledgerDimensionAccountController;
    dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703");
    ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);

<span data-ttu-id="6706c-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="6706c-107">In the current release, this code would be converted to:</span></span>

    DialogField dialogFeeLedgerDimension;
    dialogFeeLedgerDimension = SegmentedEntryControlBuild::addToDialog(
        dialog, 
        classstr(LedgerDimensionAccountController), 
        extendedTypeStr(LedgerDimensionAccount), 
        "@SYS119703", 
        feeLedgerDimension);

<span data-ttu-id="6706c-108">2 番目のパラメーターでは、ダイアログの要件を満たすクラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6706c-108">For the second parameter, choose the class that satisfies the requirements for your dialog.</span></span>  <span data-ttu-id="6706c-109">オプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6706c-109">The options are:</span></span>

-   <span data-ttu-id="6706c-110">LedgerDimensionAccountController</span><span class="sxs-lookup"><span data-stu-id="6706c-110">LedgerDimensionAccountController</span></span>
-   <span data-ttu-id="6706c-111">LedgerDimensionDefaultAccountController</span><span class="sxs-lookup"><span data-stu-id="6706c-111">LedgerDimensionDefaultAccountController</span></span>
-   <span data-ttu-id="6706c-112">DimensionDynamicAccountController</span><span class="sxs-lookup"><span data-stu-id="6706c-112">DimensionDynamicAccountController</span></span>
-   <span data-ttu-id="6706c-113">BudgetLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="6706c-113">BudgetLedgerDimensionController</span></span>
-   <span data-ttu-id="6706c-114">BudgetPlanningLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="6706c-114">BudgetPlanningLedgerDimensionController</span></span>

<span data-ttu-id="6706c-115">これは、セグメント化されたエントリについての簡単なダイアログ シナリオです。</span><span class="sxs-lookup"><span data-stu-id="6706c-115">This is a simple dialog scenario around Segmented Entry.</span></span> <span data-ttu-id="6706c-116">さらに高度なシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6706c-116">More advanced scenarios include:</span></span>

-   <span data-ttu-id="6706c-117">動的アカウントをバインドしています。</span><span class="sxs-lookup"><span data-stu-id="6706c-117">Binding the dynamic account type.</span></span>
-   <span data-ttu-id="6706c-118">会社の選択をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6706c-118">Company selection support.</span></span>
-   <span data-ttu-id="6706c-119">勘定構造選択のサポート。</span><span class="sxs-lookup"><span data-stu-id="6706c-119">Account structure selection support.</span></span>


<a name="additional-resources"></a><span data-ttu-id="6706c-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6706c-120">Additional resources</span></span>
--------

[<span data-ttu-id="6706c-121">セグメント化されたエントリ コントロールのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="6706c-121">Design-time metadata for Segmented Entry controls</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="6706c-122">セグメント化されたエントリ コントロールの Parm メソッド</span><span class="sxs-lookup"><span data-stu-id="6706c-122">Parm methods for Segmented Entry controls</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="6706c-123">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="6706c-123">Migrate Segmented Entry controls</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="6706c-124">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="6706c-124">Migration guidance for Segmented Entry controls</span></span>](segmented-entry-control-migration-guidance.md)



