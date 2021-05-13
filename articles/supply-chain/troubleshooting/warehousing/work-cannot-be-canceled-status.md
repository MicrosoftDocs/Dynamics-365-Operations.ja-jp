---
title: 作業の状態が原因で作業をキャンセルできない
description: 作業の状態が原因で作業をキャンセルできない
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924258"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="a03df-103">作業の状態が原因で作業をキャンセルできない</span><span class="sxs-lookup"><span data-stu-id="a03df-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="a03df-104">エラーコード: WAX2190</span><span class="sxs-lookup"><span data-stu-id="a03df-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="a03df-105">現象</span><span class="sxs-lookup"><span data-stu-id="a03df-105">Symptoms</span></span>

<span data-ttu-id="a03df-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="a03df-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a03df-107">作業 %1 は、状態が %2 であるためキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="a03df-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="a03df-108">原因</span><span class="sxs-lookup"><span data-stu-id="a03df-108">Cause</span></span>

<span data-ttu-id="a03df-109">現在の状態では、作業をキャンセルできません。</span><span class="sxs-lookup"><span data-stu-id="a03df-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="a03df-110">作業ヘッダーまたは作業明細行に予定された **作業状態** 値がありません。</span><span class="sxs-lookup"><span data-stu-id="a03df-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="a03df-111">作業ヘッダーの **作業状態** フィールドは *未終了* または *処理中* に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="a03df-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="a03df-112">解像度</span><span class="sxs-lookup"><span data-stu-id="a03df-112">Resolution</span></span>

<span data-ttu-id="a03df-113">作業をキャンセルするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a03df-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="a03df-114">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a03df-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a03df-115">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="a03df-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="a03df-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a03df-116">Select **OK**.</span></span>
1. <span data-ttu-id="a03df-117">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a03df-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="a03df-118">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a03df-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
