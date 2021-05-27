---
title: リリース済製品 V2 エンティティを使用して品目をインポートできない
description: リリース済製品 V2 エンティティを使用して品目をインポートできません。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026669"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="0a4b6-103">リリース済製品 V2 エンティティを使用して品目をインポートできない</span><span class="sxs-lookup"><span data-stu-id="0a4b6-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="0a4b6-104">KB 番号: 4611825</span><span class="sxs-lookup"><span data-stu-id="0a4b6-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="0a4b6-105">現象</span><span class="sxs-lookup"><span data-stu-id="0a4b6-105">Symptoms</span></span>

<span data-ttu-id="0a4b6-106">*リリース済製品V2* エンティティを使用して品目をインポートしようとする場合は、次のような エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a4b6-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="0a4b6-107">品目にレコードを作成することはできません - 分析コード グループを追跡する (ResResGroupingDimensionGroupItem)。</span><span class="sxs-lookup"><span data-stu-id="0a4b6-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="0a4b6-108">品目番号: 2040663、バッチ。</span><span class="sxs-lookup"><span data-stu-id="0a4b6-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="0a4b6-109">レコードが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="0a4b6-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="0a4b6-110">解像度</span><span class="sxs-lookup"><span data-stu-id="0a4b6-110">Resolution</span></span>

<span data-ttu-id="0a4b6-111">新しいリリース済製品をインポートするには、*リリースされた製品 V2* エンティティの代わりに、*リリースされた製品作成 V2* エンティティを使用する必要 があります。</span><span class="sxs-lookup"><span data-stu-id="0a4b6-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
