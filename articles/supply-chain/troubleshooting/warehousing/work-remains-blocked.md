---
title: 作業がブロックされたまま
description: 作業がブロックされたまま
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924133"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="ce598-103">作業がブロックされたまま</span><span class="sxs-lookup"><span data-stu-id="ce598-103">Work remains blocked</span></span>

<span data-ttu-id="ce598-104">エラーコード: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ce598-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ce598-105">現象</span><span class="sxs-lookup"><span data-stu-id="ce598-105">Symptoms</span></span>

<span data-ttu-id="ce598-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="ce598-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ce598-107">関連付けられたサイクル %2 に状態 %3 があるため、作業 %1 はブロックされたままです。</span><span class="sxs-lookup"><span data-stu-id="ce598-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="ce598-108">原因</span><span class="sxs-lookup"><span data-stu-id="ce598-108">Cause</span></span>

<span data-ttu-id="ce598-109">次のいずれかの条件で示されているように、作業は、現在ウェーブで処理されており、ブロックを解除できません。</span><span class="sxs-lookup"><span data-stu-id="ce598-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="ce598-110">**ブロックの理由** タブで、1 つ以上の明細行の **作業ブロック理由** フィールドが、*処理中のウェーブ* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ce598-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="ce598-111">アクション ウィンドウの **関連情報** タブにある **関連情報** グループで **ウェーブ** を選択すると、**ウェーブステータス** フィールドが *処理中* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ce598-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce598-112">解像度</span><span class="sxs-lookup"><span data-stu-id="ce598-112">Resolution</span></span>

<span data-ttu-id="ce598-113">アクション ウィンドウにある **関連情報** タブの **関連情報** グループで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce598-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="ce598-114">**ウェーブ** ページのアクション ウィンドウで、**ウェーブ** タブにある **ウェーブ** グループで、**ウェーブ データのクリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce598-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="ce598-115">回避策</span><span class="sxs-lookup"><span data-stu-id="ce598-115">Workaround</span></span>

<span data-ttu-id="ce598-116">前の手順で問題が解決しなかった場合は、次の手順に従って作業をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="ce598-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="ce598-117">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce598-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ce598-118">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。現在、**作業状態** の値は、*未処理*、*進行中*、*キャンセル済*、*結合済*、または *終了済* です。</span><span class="sxs-lookup"><span data-stu-id="ce598-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ce598-119">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce598-119">Select **OK**.</span></span>
1. <span data-ttu-id="ce598-120">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ce598-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ce598-121">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce598-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
