---
title: "サブスクリプション見積もりツール"
description: "このトピックでは、Lifecycle Services (LCS) で利用可能なサブスクリプション試算ツールを Microsoft Dynamics 365 Finance and Operations で使用する方法について説明します。"
author: manalidongre
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b3a8d07586d6756bb7fc10f591dd58647c85e5b0
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="subscription-estimator"></a><span data-ttu-id="45ad4-103">サブスクリプション見積もりツール</span><span class="sxs-lookup"><span data-stu-id="45ad4-103">Subscription estimator</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45ad4-104">サブスクリプション見積もりツールは、Microsoft Dynamics Lifecycle Services (LCS) で使用できるツールです。</span><span class="sxs-lookup"><span data-stu-id="45ad4-104">Subscription estimator is a tool that is available in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="45ad4-105">Microsoft は、このツールを使用して、顧客に対して準備する必要がある実稼働環境の初期サイズを見積ります。</span><span class="sxs-lookup"><span data-stu-id="45ad4-105">Microsoft uses this tool to estimate the initial size of the production environment that must be provisioned for a customer.</span></span> <span data-ttu-id="45ad4-106">顧客が実稼働環境の配置を要求する前に、トランザクション カウントの観点からピーク作業負荷を見積もり、その情報を LCS にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad4-106">Before customers can request deployment of a production environment, they must estimate their peak workloads in terms of transaction counts and then upload that information to LCS.</span></span> <span data-ttu-id="45ad4-107">ユーザー ライセンスの詳細およびトランザクション カウントを使用してサブスクリプション要件を推測することにより、サブスクリプション見積もりツールは、プロビジョニングされた環境が顧客の業務要件を満たしていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-107">By using the details of user licenses and transaction counts to infer subscription requirements, the Subscription estimator tool helps ensure that the provisioned environment meets the customer's business requirements.</span></span>

<span data-ttu-id="45ad4-108">サブスクリプション試算ツールを使用するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="45ad4-108">Follow these steps to use the Subscription estimator tool.</span></span>

1. <span data-ttu-id="45ad4-109">LCS で、Finance and Operations の実装プロジェクトに関連付けられているプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-109">In LCS, open the project that is associated with the implementation project for Finance and Operations.</span></span>
2. <span data-ttu-id="45ad4-110">ページの上部にあるハンバーガー アイコン選択し、**サブスクリプション見積もりツール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-110">At the top of the page, select the hamburger icon, and then select **Subscription estimator**.</span></span>
<span data-ttu-id="45ad4-111">[![サブスクリプション見積もりツール](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span><span class="sxs-lookup"><span data-stu-id="45ad4-111">[![subscription estimator](./media/subscription_estimator_01.png)](./media/subscription_estimator_01.png)</span></span>
3. <span data-ttu-id="45ad4-112">サンプルの使用状況プロファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="45ad4-112">Download the sample usage profile.</span></span>
4. <span data-ttu-id="45ad4-113">各タブで必要な質問に回答します。小売顧客の場合は、**Retail と Commerce** タブ上の質問に回答してください。</span><span class="sxs-lookup"><span data-stu-id="45ad4-113">Answer the required questions on each tab. If you're a Retail customer, be sure to answer the questions on the **Retail and Commerce** tab.</span></span>
5. <span data-ttu-id="45ad4-114">使用状況プロファイルをローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-114">Save the usage profile locally.</span></span>
6. <span data-ttu-id="45ad4-115">使用プロファイルをアップロードするには、**新しい見積もり** を選択し、見積もりに名前を付け、使用プロファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="45ad4-115">To upload the usage profile, select **New estimate**, name the estimate, and then upload the usage profile.</span></span>
7. <span data-ttu-id="45ad4-116">アップロードが完了した後、**アクティブとしてマークする**を選択し見積もりを有効にします。</span><span class="sxs-lookup"><span data-stu-id="45ad4-116">After the upload is completed, select **Mark as Active** to activate an estimate.</span></span> <span data-ttu-id="45ad4-117">生産の配置をコンフィギュレーションするために有効な見積が必要です。</span><span class="sxs-lookup"><span data-stu-id="45ad4-117">An active estimate is required in order to configure a production deployment.</span></span>

<span data-ttu-id="45ad4-118">有効でアクティブな見積があるときは、**構成** ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="45ad4-118">When there is a valid active estimate, the **Configure** button becomes available.</span></span> <span data-ttu-id="45ad4-119">このボタンを使用すると、製造環境の展開を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-119">You can use this button to request a production environment deployment.</span></span>

> [!NOTE]
> <span data-ttu-id="45ad4-120">複数の見積を使用できますが、1 つの見積に**アクティブ**とマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="45ad4-120">Although you can have multiple estimates, one estimate must be marked as **Active**.</span></span> <span data-ttu-id="45ad4-121">実稼動環境が配置された後、または環境の配置がサインオフされた後、アクティブな見積もりはロックされます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-121">After the production environment has been deployed, or deployment of the environment has received sign-off, the active estimate is locked.</span></span> <span data-ttu-id="45ad4-122">別の見積もりを有効見積もりとしてマークするには、LCS のサポート ポータルを使用してサポート要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-122">To mark a different estimate as the active estimate, create a support request by using the Support portal in LCS.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="45ad4-123">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="45ad4-123">Frequently asked questions</span></span>

<span data-ttu-id="45ad4-124">**質問:** アクティブな見積もりがあるにもかかわらず、実稼動環境の**コンフィギュレーション**ボタンが有効なのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="45ad4-124">**Question:** Why isn't the **Configure** button for deploying a production environment available, even though there is an active estimate?</span></span> <span data-ttu-id="45ad4-125">また、プロジェクト ダッシュ ボード上のアクション センターに警告メッセージが表示されるのはなぜでしょうか。</span><span class="sxs-lookup"><span data-stu-id="45ad4-125">And why does a warning message appear in the Action center on the project dashboard?</span></span>

<span data-ttu-id="45ad4-126">**回答:** 複数の実装プロジェクトがある場合、**コンフィギュレーション**ボタンを有効にされていない可能性があり、アクション センターに不足しているライセンス数に関する警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-126">**Answer:** If you have multiple implementation projects, the **Configure** button might not be enabled and a warning message will appear in the Action center regarding an insufficient number of licenses.</span></span> <span data-ttu-id="45ad4-127">サポート リクエストを記録すると、サポート チームがこの問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-127">Log a support request, and the support team can help resolve this issue.</span></span>

<span data-ttu-id="45ad4-128">**質問:** 見積もりに**有効**とマークするとエラーが発生するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="45ad4-128">**Question:** Why does an error occur when I mark an estimate as **Active**?</span></span>

<span data-ttu-id="45ad4-129">**回答:** 見積を**有効**とマークすると、次のエラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="45ad4-129">**Answer:** When you mark an estimate as **Active**, you might receive the following error message:</span></span>

- <span data-ttu-id="45ad4-130">**見積が作成されますが、要件を満たしていません** - このエラーは、入力されたトランザクション明細行がサブスクリプション見積もりツールの制限内にない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-130">**Estimate created but does not meet requirements** – This error occurs if transaction lines that are entered aren't within the limits of the Subscription estimation tool.</span></span> <span data-ttu-id="45ad4-131">このエラーを解決するには、サポート要求を作成し、使用プロファイルを添付します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-131">To resolve this error, create a support request, and attach the usage profile.</span></span> <span data-ttu-id="45ad4-132">次に、インスタンスのサイズを手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="45ad4-132">Your instance can then be manually sized.</span></span>

<span data-ttu-id="45ad4-133">その他のエラー メッセージが表示されたり、その他の問題が発生した場合は、サポート チームがその問題に対処できるようにサポート リクエストを作成し、アクティブな見積もりを添付します。</span><span class="sxs-lookup"><span data-stu-id="45ad4-133">If you receive any other error message or encounter any other issue, create a support request, and attach your active estimate so that the support team can address the issue.</span></span>
