---
title: 分析レポートは更新されない
description: このトピックでは、顧客のデータの変更が、顧客のワークスペースに表示されない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898576"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="24291-103">分析レポートは更新されない</span><span class="sxs-lookup"><span data-stu-id="24291-103">Analytic reports are not updated</span></span>

<span data-ttu-id="24291-104">**払出**</span><span class="sxs-lookup"><span data-stu-id="24291-104">**Issue**</span></span>

<span data-ttu-id="24291-105">顧客のデータの変更がいずれかの顧客のワークスペースの**分析**タブに表示されません。</span><span class="sxs-lookup"><span data-stu-id="24291-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="24291-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="24291-106">**Cause**</span></span>

<span data-ttu-id="24291-107">既定では、Microsoft Power BI レポートは、測定の配置バッチ ジョブのスケジュールに基づいて 4 時間ごとに更新されます。</span><span class="sxs-lookup"><span data-stu-id="24291-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="24291-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="24291-108">**Resolution**</span></span>

<span data-ttu-id="24291-109">この問題は、単なるタイミングの問題である場合があります。</span><span class="sxs-lookup"><span data-stu-id="24291-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="24291-110">この手順に従ってバッチ ジョブを開始し、分析ワークスペースを更新します。</span><span class="sxs-lookup"><span data-stu-id="24291-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="24291-111">**システム管理\>リンク\>バッチ ジョブ\>バッチ ジョブ**で、**バッチ ジョブ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="24291-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="24291-112">または、検索を使用して、**バッチ ジョブ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="24291-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="24291-113">一覧で**測定の配置**ジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="24291-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="24291-114">ページの上部で**編集**を選択して、開始予定日/時刻を現在の時刻に近い分析を更新する値に設定します。</span><span class="sxs-lookup"><span data-stu-id="24291-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![バッチ ジョブ](media/batch-jobs.png)
