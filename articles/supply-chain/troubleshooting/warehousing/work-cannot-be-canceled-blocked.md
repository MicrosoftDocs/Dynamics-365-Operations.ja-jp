---
title: ブロックされているため作業をキャンセルできない
description: ブロックされているため作業をキャンセルできない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924282"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="a0ea6-103">ブロックされているため作業をキャンセルできない</span><span class="sxs-lookup"><span data-stu-id="a0ea6-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="a0ea6-104">エラー コード: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="a0ea6-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="a0ea6-105">現象</span><span class="sxs-lookup"><span data-stu-id="a0ea6-105">Symptoms</span></span>

<span data-ttu-id="a0ea6-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a0ea6-107">作業 %1 は、理由タイプ %2 によってブロックされているためキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="a0ea6-108">キャンセルされる前に、作業のブロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="a0ea6-109">原因</span><span class="sxs-lookup"><span data-stu-id="a0ea6-109">Cause</span></span>

<span data-ttu-id="a0ea6-110">作業はブロックされており、キャンセルすることができません。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="a0ea6-111">**作業** ページの **一般** タブで、**ブロック** オプションが *はい* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="a0ea6-112">この設定は、作業がブロックされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="a0ea6-113">**ブロックの理由** タブには、作業がブロックされた理由が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="a0ea6-114">解像度</span><span class="sxs-lookup"><span data-stu-id="a0ea6-114">Resolution</span></span>

<span data-ttu-id="a0ea6-115">作業のブロックを解除するには、**ブロックの理由** タブを選択し、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="a0ea6-116">**作業ブロック理由** フィールドが *未定義の理由* に設定されている場合: アクション ウィンドウの **作業** タブにある **作業** グループで、**作業のブロック解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="a0ea6-117">**作業ブロック理由** フィールドが *処理中のウェーブ* に設定されている場合: アクション ウィンドウで **関連情報** タブにある **関連情報** グループで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="a0ea6-118">**ウェーブ** ページのアクション ウィンドウで、**ウェーブ** タブにある **ウェーブ** グループで、**ウェーブ データのクリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="a0ea6-119">回避策</span><span class="sxs-lookup"><span data-stu-id="a0ea6-119">Workaround</span></span>

<span data-ttu-id="a0ea6-120">前の手順で問題が解決しなかった場合は、次の手順に従って作業をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="a0ea6-121">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a0ea6-122">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。現在、**作業状態** の値は、*未処理*、*進行中*、*キャンセル済*、*結合済*、または *終了済* です。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="a0ea6-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-123">Select **OK**.</span></span>
1. <span data-ttu-id="a0ea6-124">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="a0ea6-125">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0ea6-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
