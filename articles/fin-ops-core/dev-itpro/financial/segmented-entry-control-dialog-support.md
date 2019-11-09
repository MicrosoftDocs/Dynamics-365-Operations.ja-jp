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
ms.openlocfilehash: 717ec352997df3c87bbdc3dc836ec8da0bade13a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183302"
---
# <a name="support-for-segmented-entry-controls-on-dialogs"></a><span data-ttu-id="f472d-103">ダイアログ上のセグメント化されたエントリ コントロールをサポート</span><span class="sxs-lookup"><span data-stu-id="f472d-103">Support for Segmented Entry controls on dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f472d-104">セグメント化されたエントリ コントロールをダイアログに追加するためのコード パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f472d-104">Describes the code pattern to add Segmented Entry controls to dialogs.</span></span>

<span data-ttu-id="f472d-105">セグメント化されたエントリ コントロールをダイアログに追加するプロセスが変更されました。</span><span class="sxs-lookup"><span data-stu-id="f472d-105">The process to add Segmented Entry controls to dialogs has changed.</span></span> <span data-ttu-id="f472d-106">これは、Dynamics AX 2012 の例です。</span><span class="sxs-lookup"><span data-stu-id="f472d-106">This is an example from Dynamics AX 2012:</span></span>

    DialogField dialogFeeLedgerDimension;
    LedgerDimensionAccountController ledgerDimensionAccountController;
    dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703");
    ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);

<span data-ttu-id="f472d-107">現在のリリースでは、このコードは次のように変換されます。</span><span class="sxs-lookup"><span data-stu-id="f472d-107">In the current release, this code would be converted to:</span></span>

    DialogField dialogFeeLedgerDimension;
    dialogFeeLedgerDimension = SegmentedEntryControlBuild::addToDialog(
        dialog, 
        classstr(LedgerDimensionAccountController), 
        extendedTypeStr(LedgerDimensionAccount), 
        "@SYS119703", 
        feeLedgerDimension);

<span data-ttu-id="f472d-108">2 番目のパラメーターでは、ダイアログの要件を満たすクラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f472d-108">For the second parameter, choose the class that satisfies the requirements for your dialog.</span></span>  <span data-ttu-id="f472d-109">オプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f472d-109">The options are:</span></span>

-   <span data-ttu-id="f472d-110">LedgerDimensionAccountController</span><span class="sxs-lookup"><span data-stu-id="f472d-110">LedgerDimensionAccountController</span></span>
-   <span data-ttu-id="f472d-111">LedgerDimensionDefaultAccountController</span><span class="sxs-lookup"><span data-stu-id="f472d-111">LedgerDimensionDefaultAccountController</span></span>
-   <span data-ttu-id="f472d-112">DimensionDynamicAccountController</span><span class="sxs-lookup"><span data-stu-id="f472d-112">DimensionDynamicAccountController</span></span>
-   <span data-ttu-id="f472d-113">BudgetLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="f472d-113">BudgetLedgerDimensionController</span></span>
-   <span data-ttu-id="f472d-114">BudgetPlanningLedgerDimensionController</span><span class="sxs-lookup"><span data-stu-id="f472d-114">BudgetPlanningLedgerDimensionController</span></span>

<span data-ttu-id="f472d-115">これは、セグメント化されたエントリについての簡単なダイアログ シナリオです。</span><span class="sxs-lookup"><span data-stu-id="f472d-115">This is a simple dialog scenario around Segmented Entry.</span></span> <span data-ttu-id="f472d-116">さらに高度なシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f472d-116">More advanced scenarios include:</span></span>

-   <span data-ttu-id="f472d-117">動的アカウントをバインドしています。</span><span class="sxs-lookup"><span data-stu-id="f472d-117">Binding the dynamic account type.</span></span>
-   <span data-ttu-id="f472d-118">会社の選択をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f472d-118">Company selection support.</span></span>
-   <span data-ttu-id="f472d-119">勘定構造選択のサポート。</span><span class="sxs-lookup"><span data-stu-id="f472d-119">Account structure selection support.</span></span>


<a name="additional-resources"></a><span data-ttu-id="f472d-120">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f472d-120">Additional resources</span></span>
--------

[<span data-ttu-id="f472d-121">セグメント化されたエントリ コントロールのメタデータ詳細</span><span class="sxs-lookup"><span data-stu-id="f472d-121">Segmented Entry control Metadata Specification</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="f472d-122">セグメント化されたエントリ コントロールの Parm メソッド詳細</span><span class="sxs-lookup"><span data-stu-id="f472d-122">Segmented Entry control Parm method Specification</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="f472d-123">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="f472d-123">Segmented Entry control migration</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="f472d-124">セグメント化されたエントリ コントロール - 移行のガイダンス</span><span class="sxs-lookup"><span data-stu-id="f472d-124">Segmented Entry control - Migration guidance</span></span>](segmented-entry-control-migration-guidance.md)


