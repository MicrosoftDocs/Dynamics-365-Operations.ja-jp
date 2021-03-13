---
title: トラブルシューティングの分析レポート
description: この記事では、顧客のデータの変更が、顧客のワークスペースに表示されない場合の対処方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113264"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="1639d-103">トラブルシューティングの分析レポート</span><span class="sxs-lookup"><span data-stu-id="1639d-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="1639d-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="1639d-104">**Issue**</span></span>

<span data-ttu-id="1639d-105">顧客のデータの変更がいずれかの顧客のワークスペースの **分析** タブに表示されません。</span><span class="sxs-lookup"><span data-stu-id="1639d-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="1639d-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="1639d-106">**Cause**</span></span>

<span data-ttu-id="1639d-107">既定では、Microsoft Power BI レポートは、測定の配置バッチ ジョブのスケジュールに基づいて 4 時間ごとに更新されます。</span><span class="sxs-lookup"><span data-stu-id="1639d-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="1639d-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="1639d-108">**Resolution**</span></span>

<span data-ttu-id="1639d-109">この問題は、単なるタイミングの問題である場合があります。</span><span class="sxs-lookup"><span data-stu-id="1639d-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="1639d-110">この手順に従ってバッチ ジョブを開始し、分析ワークスペースを更新します。</span><span class="sxs-lookup"><span data-stu-id="1639d-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="1639d-111">**システム管理\>リンク\>バッチ ジョブ\>バッチ ジョブ** で、**バッチ ジョブ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="1639d-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="1639d-112">または、検索を使用して、**バッチ ジョブ** と入力します。</span><span class="sxs-lookup"><span data-stu-id="1639d-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="1639d-113">一覧で **測定の配置** ジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="1639d-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="1639d-114">ページの上部で **編集** を選択して、開始予定日/時刻を現在の時刻に近い分析を更新する値に設定します。</span><span class="sxs-lookup"><span data-stu-id="1639d-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![バッチ ジョブ](media/batch-jobs.png)
