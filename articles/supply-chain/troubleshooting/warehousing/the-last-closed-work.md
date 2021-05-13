---
title: 最後の終了した作業明細行をプットにする必要がある
description: 最後の終了した作業明細行をプットにする必要がある
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924378"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="8d63a-103">最後の終了した作業明細行をプットにする必要がある</span><span class="sxs-lookup"><span data-stu-id="8d63a-103">The last closed work line must be a put</span></span>

<span data-ttu-id="8d63a-104">エラーコード: WAX1285</span><span class="sxs-lookup"><span data-stu-id="8d63a-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="8d63a-105">現象</span><span class="sxs-lookup"><span data-stu-id="8d63a-105">Symptoms</span></span>

<span data-ttu-id="8d63a-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="8d63a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="8d63a-107">最後の終了した作業明細行はプットにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d63a-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="8d63a-108">原因</span><span class="sxs-lookup"><span data-stu-id="8d63a-108">Cause</span></span>

<span data-ttu-id="8d63a-109">現在の状態では、作業をキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="8d63a-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="8d63a-110">最後の作業明細行では、**作業状態** フィールドは *クローズ済* に設定されていますが、**作業タイプ** フィールドは *プット* に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="8d63a-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="8d63a-111">解像度</span><span class="sxs-lookup"><span data-stu-id="8d63a-111">Resolution</span></span>

<span data-ttu-id="8d63a-112">作業をキャンセルするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8d63a-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="8d63a-113">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8d63a-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="8d63a-114">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d63a-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="8d63a-115">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d63a-115">Select **OK**.</span></span>
1. <span data-ttu-id="8d63a-116">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d63a-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="8d63a-117">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d63a-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
