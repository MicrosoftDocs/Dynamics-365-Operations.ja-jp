---
title: 倉庫の補充のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫補充の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828085"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="7b3a2-103">倉庫の補充のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7b3a2-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b3a2-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫補充の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="7b3a2-105">エラー メッセージ "完了していない補充作業があるために作業 %1 をブロック解除できません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7b3a2-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="7b3a2-106">Issue description</span></span>

<span data-ttu-id="7b3a2-107">ピッキング作業は、依存する補充作業のためブロックされます。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7b3a2-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="7b3a2-108">Issue resolution</span></span>

<span data-ttu-id="7b3a2-109">ウェーブ需要補充を使用するとき、ソース注文需要を満たすためにピッキング場所を補充する必要がある場合、補充作業とピッキング作業の両方がシステムによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="7b3a2-110">ただし、補充作業が完了するまで、ピッキング作業はブロックされます。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="7b3a2-111">補充作業が完了していない場合は、ピッキング場所に十分な在庫がないので、この動作は意図的です。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="7b3a2-112">補充作業を完了し、ピッキング作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="7b3a2-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]