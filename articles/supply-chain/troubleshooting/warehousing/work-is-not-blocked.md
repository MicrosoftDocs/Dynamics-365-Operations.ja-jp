---
title: 作業はブロックされていない
description: 作業はブロックされていない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924207"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="6aaa0-103">作業はブロックされていない</span><span class="sxs-lookup"><span data-stu-id="6aaa0-103">Work isn't blocked</span></span>

<span data-ttu-id="6aaa0-104">エラー コード: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="6aaa0-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="6aaa0-105">現象</span><span class="sxs-lookup"><span data-stu-id="6aaa0-105">Symptoms</span></span>

<span data-ttu-id="6aaa0-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="6aaa0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6aaa0-107">ID %1 の作業はブロックされていません。</span><span class="sxs-lookup"><span data-stu-id="6aaa0-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="6aaa0-108">原因</span><span class="sxs-lookup"><span data-stu-id="6aaa0-108">Cause</span></span>

<span data-ttu-id="6aaa0-109">ウェーブの **ブロックされたウェーブ** オプションは、*いいえ* に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6aaa0-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="6aaa0-110">現在ブロックされていないので、作業のブロックを解除できません。</span><span class="sxs-lookup"><span data-stu-id="6aaa0-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="6aaa0-111">解像度</span><span class="sxs-lookup"><span data-stu-id="6aaa0-111">Resolution</span></span>

 <span data-ttu-id="6aaa0-112">**ブロックされたウェーブ** オプションが *はい* に設定されている場合のみ、ブロックを解除できます。</span><span class="sxs-lookup"><span data-stu-id="6aaa0-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
