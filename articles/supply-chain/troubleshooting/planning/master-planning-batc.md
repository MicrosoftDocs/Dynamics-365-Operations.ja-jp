---
title: マスター プランの品目を関連する補充グループ値でフィルター処理できません
description: マスター プランの品目を関連する補充グループ値でフィルター処理できません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049477"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="001b5-103">マスター プランの品目を関連する補充グループ値でフィルター処理できません</span><span class="sxs-lookup"><span data-stu-id="001b5-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="001b5-104">KB 番号: 4612572</span><span class="sxs-lookup"><span data-stu-id="001b5-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="001b5-105">現象</span><span class="sxs-lookup"><span data-stu-id="001b5-105">Symptoms</span></span>

<span data-ttu-id="001b5-106">品目補充テーブルの関連レコードの値に基づいて、マスター プラン バッチ ジョブに含まれる品目をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="001b5-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="001b5-107">(たとえば、**仕入先** や **補充グループ** の 値で品目をフィルター処理する場合など)。</span><span class="sxs-lookup"><span data-stu-id="001b5-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="001b5-108">バッチ ジョブのフィルター設定を使用すると、**品目** テーブルから **品目補充** テーブルへの結合を作成し、クエリで品目補充テーブルからフィールド値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="001b5-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="001b5-109">ただし、この設定を完了した後も、システムは品目補充テーブルから指定されたフィールド値に一致する品目に対してだけでなく、品目補充全体に対して計画オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="001b5-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="001b5-110">解決策</span><span class="sxs-lookup"><span data-stu-id="001b5-110">Resolution</span></span>

<span data-ttu-id="001b5-111">バッチ ジョブ フィルターでは、品目についてのみフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="001b5-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="001b5-112">**品目補充** テーブルに結合を追加できますが、そのテーブルに対して行うフィルター設定はクエリの出力に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="001b5-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="001b5-113">実行時にシステムは、すべての補充グループと、フィルター処理された品目に含まれるすべてのバリエーションに対する計画を実行します。</span><span class="sxs-lookup"><span data-stu-id="001b5-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="001b5-114">実行に品目が既に含まれていれば、品目フィルターに含まれる補充グループは計画出力に影響しません。</span><span class="sxs-lookup"><span data-stu-id="001b5-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
