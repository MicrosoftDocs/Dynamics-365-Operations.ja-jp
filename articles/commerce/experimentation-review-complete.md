---
title: バリエーションのレベルを上げて実験を完了する
description: このトピックでは、Dynamics 365 Commerce のバリエーションのレベルを正常に上げて、実験を完了する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930232"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="1fbbb-103">バリエーションのレベルを上げて実験を完了する</span><span class="sxs-lookup"><span data-stu-id="1fbbb-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="1fbbb-104">このトピックでは、実験で最良の結果が得られたバリエーションのレベルを上げる方法と実験を完了する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="1fbbb-105">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1fbbb-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="1fbbb-107">[![実験ユーザー体験 - 確認と完了](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1fbbb-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="1fbbb-108">[実験を実行](experimentation-run-monitor.md) して、実際のサイトで使用するバリエーションを決定するのに十分なデータを収集したら、バリエーションのレベルを上げて実験を終了します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="1fbbb-109">バリエーションのレベルを上げる</span><span class="sxs-lookup"><span data-stu-id="1fbbb-109">Promote a variation</span></span>
<span data-ttu-id="1fbbb-110">サードパーティ サービスの実験に関連するデータと分析を使用して、どのバリエーションが最適な結果を得たかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="1fbbb-111">実際のサイトの現在のコンテンツを、成功するバリエーションに置き換えて、Web サイトのすべてのユーザーが使用できるようにするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="1fbbb-112">サイト ビルダーの**実験**タブに移動して、実験を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="1fbbb-113">上部バーで**実験の完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="1fbbb-114">**実験の完了**ダイアログ メニューで、**実験データの確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="1fbbb-115">サードパーティ サービスが開き、メトリックスを検証して、どのバリエーションが最も効果的かを判断します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="1fbbb-116">サイト ビルダーの**実験の完了**ダイアログ メニューで、成功するバリエーションを選択して、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="1fbbb-117">サードパーティ サービスを開いて、実験を停止します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="1fbbb-118">サイト ビルダーで、**完了**を選択して、元の実際のページを上書きし、成功するバリエーションを公開して、Web サイトのすべてのユーザーが使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="1fbbb-119">現在の実際のページを保持し、バリエーションを公開しないことを選択した場合は、**元のページの再公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="1fbbb-120">実験の削除</span><span class="sxs-lookup"><span data-stu-id="1fbbb-120">Delete your experiment</span></span>
<span data-ttu-id="1fbbb-121">Commerce で完了した実験を削除する必要はありませんが、容量を節約したり、ワークスペースをクリーンアップするために、実験を削除することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="1fbbb-122">実験を削除するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="1fbbb-123">サイト ビルダーの**実験**タブに移動して、実験を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="1fbbb-124">実験がまだ有効な場合は、続行する前にサードパーティサービスの実験を停止してください。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="1fbbb-125">コマンド バーの**発行取り消し**を選択して、実際のサイトからバリエーションのコンテンツを削除します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="1fbbb-126">コマンド バーで**削除**を選択し、実験を削除します。</span><span class="sxs-lookup"><span data-stu-id="1fbbb-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="1fbbb-127">前のステップ</span><span class="sxs-lookup"><span data-stu-id="1fbbb-127">Previous step</span></span>
[<span data-ttu-id="1fbbb-128">実験の実行と監視</span><span class="sxs-lookup"><span data-stu-id="1fbbb-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
