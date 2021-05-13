---
title: ユーザーに割り当てられた作業がキャンセルできない
description: ユーザーに割り当てられた作業がキャンセルできない
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924404"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="647b3-103">ユーザーに割り当てられた作業がキャンセルできない</span><span class="sxs-lookup"><span data-stu-id="647b3-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="647b3-104">エラーコード: WAX708</span><span class="sxs-lookup"><span data-stu-id="647b3-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="647b3-105">現象</span><span class="sxs-lookup"><span data-stu-id="647b3-105">Symptoms</span></span>

<span data-ttu-id="647b3-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="647b3-106">The system shows the following error message:</span></span>

> <span data-ttu-id="647b3-107">ユーザーに割り当てられた作業はキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="647b3-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="647b3-108">原因</span><span class="sxs-lookup"><span data-stu-id="647b3-108">Cause</span></span>

<span data-ttu-id="647b3-109">作業はユーザーによってロックされており、キャンセルすることができません。</span><span class="sxs-lookup"><span data-stu-id="647b3-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="647b3-110">これを確認するには、作業 ID を開き、**一般** タブを開きます。作業がロックされている場合は、**作業ステータス** フィールドが *進行中* に設定され、**ロック元** フィールドはユーザー ID に設定されます。</span><span class="sxs-lookup"><span data-stu-id="647b3-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="647b3-111">解像度</span><span class="sxs-lookup"><span data-stu-id="647b3-111">Resolution</span></span>

<span data-ttu-id="647b3-112">作業をキャンセルするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="647b3-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="647b3-113">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="647b3-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="647b3-114">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="647b3-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="647b3-115">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="647b3-115">Select **OK**.</span></span>
1. <span data-ttu-id="647b3-116">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="647b3-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="647b3-117">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="647b3-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
