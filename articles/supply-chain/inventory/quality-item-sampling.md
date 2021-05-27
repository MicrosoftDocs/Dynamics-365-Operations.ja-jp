---
title: 品質管理品目サンプリング
description: このトピックでは、品目サンプリングの設定方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022231"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="2ede9-103">品質管理品目サンプリング</span><span class="sxs-lookup"><span data-stu-id="2ede9-103">Quality management item sampling</span></span>

<span data-ttu-id="2ede9-104">品目サンプリングは、品質関連の一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="2ede9-105">検査する必要がある現在の現物在庫の量を定義します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="2ede9-106">サンプリングは、固定数量、割合、または完全なライセンス プレートに基づいて行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="2ede9-107">品目サンプリングの設定</span><span class="sxs-lookup"><span data-stu-id="2ede9-107">Set up item sampling</span></span>

<span data-ttu-id="2ede9-108">品目サンプリングを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="2ede9-109">**在庫管理 \> 設定 \> 品質管理 \> 品目サンプリング** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="2ede9-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-110">Select **New**.</span></span>
1. <span data-ttu-id="2ede9-111">**品目サンプリング** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="2ede9-112">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="2ede9-113">**値** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="2ede9-114">この値は、隣のフィールドで選択された数量の仕様に関連します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="2ede9-115">テストが失敗した場合にロット全体または注文明細行の数量をブロックする必要がある場合は、**プロセス** セクションで、**完全ブロック** ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2ede9-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="2ede9-116">このチェック ボックスをオフにすると、テストに失敗した場合でも品質指示内の品目のみがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="2ede9-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2ede9-117">Select **Save**.</span></span>
1. <span data-ttu-id="2ede9-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="2ede9-119">*倉庫プロセスの品質管理* 機能により、その他の品目のサンプリング機能が追加されます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="2ede9-120">これにより、*品目サンプリング スコープ* の概念が追加され、完全なライセンス プレートを数量指定として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2ede9-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="2ede9-121">この機能をオンにする場合は、[倉庫プロセスの品質管理](quality-management-for-warehouses-processes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ede9-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
