---
title: 二重書き込みウィザードを使用して環境をリンクする
description: このトピックでは、二重書き込みウィザードを使用して、Finance and Operations アプリ環境を Common Data Service 環境にリンクする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96d1564c5a16602b4895985e76e91c40eb09222f
ms.sourcegitcommit: 8a4e2adb999112e1b6576bcb3e93e29834ba36aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2020
ms.locfileid: "3376038"
---
# <a name="use-the-dual-write-wizard-to-link-your-environments"></a><span data-ttu-id="99202-103">二重書き込みウィザードを使用して環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="99202-103">Use the dual-write wizard to link your environments</span></span>

[!include [banner](../../includes/banner.md)]



1. <span data-ttu-id="99202-104">Common Data Service 環境にリンクする Finance and Operations アプリ環境にサインインします。</span><span class="sxs-lookup"><span data-stu-id="99202-104">Sign in to the Finance and Operations app environment that you want to link to your Common Data Service environment.</span></span>
2. <span data-ttu-id="99202-105">**ワークスペース \> データ管理**に移動して、**デュアル書き込み**のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="99202-105">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>

    ![二重書き込みタイル](media/navigate-to-data-management.png)

3. <span data-ttu-id="99202-107">**環境への新しいリンク** を選択して、**Common Data Service へのリンク設定** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="99202-107">Select **New link to environment** to open the **Setup link to Common Data Service** wizard.</span></span>
4. <span data-ttu-id="99202-108">**環境の選択** ページには、サインインしたユーザーが環境管理者であるすべての Common Data Service 環境が一覧表示されます。リンク先の Common Data Service 環境を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="99202-108">The **Choose environment** page lists all the Common Data Service environments where the signed-in user is an environment admin. Select the Common Data Service environment to link to, and then select **Next**.</span></span>

    ![環境ページを選択する](media/data-service-environment.png)

5. <span data-ttu-id="99202-110">法人を選択して、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="99202-110">Select your legal entities, and then select **Next**.</span></span>

    ![法人の選択手順](media/select-legal-entities.png)

    <span data-ttu-id="99202-112">正常性チェックを実行し、システムが二重書き込みを有効にするための要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="99202-112">A health check is run to verify that your system meets the requirements for enabling dual-write.</span></span> <span data-ttu-id="99202-113">正常性チェックでは、すべての前提条件が完了していることも確認します。</span><span class="sxs-lookup"><span data-stu-id="99202-113">The health check also verifies that all the prerequisites have been completed.</span></span> <span data-ttu-id="99202-114">いずれかの正常性チェックが失敗した場合は、次の手順に進む前に、すべての前提条件を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="99202-114">If any health check test fails, make that you've completed all the prerequisites before you move on to the next step.</span></span>

    <span data-ttu-id="99202-115">次の例では、アプリを接続するためのアクセスが許可されているかどうかのテストが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="99202-115">In the following example, the test about whether access was granted to connect the apps failed.</span></span> <span data-ttu-id="99202-116">この場合、最初に適切なアプリケーション ID を作成して、アプリを接続するためのアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99202-116">In this case, you must first grant access to connect the apps by the creating the appropriate application IDs.</span></span> <span data-ttu-id="99202-117">その後、ウィザードを再実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99202-117">You must then rerun the wizard.</span></span>

    ![正常性チェック ページ](media/health-check.png)

6. <span data-ttu-id="99202-119">概要、プライバシー通知、同意を確認し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="99202-119">Review the summary, privacy notice, and consent, and then select **Create**.</span></span>

<span data-ttu-id="99202-120">Finance and Operations アプリを Common Data Service 環境にリンクしました。</span><span class="sxs-lookup"><span data-stu-id="99202-120">You've now linked your Finance and Operations app to the Common Data Service environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="99202-121">エンティティ マップが表示されない場合、または空白のページが表示される場合は、システム要件と前提条件の一部としてインストールした二重書き込みアプリケーション オーケストレーション ソリューションを **適用** してください。</span><span class="sxs-lookup"><span data-stu-id="99202-121">If you don't see your entity maps, or if you see a blank page, be sure to **Apply** the Dual-write application orchestration solution that you installed as part of the system requirements and prerequisities.</span></span>

7. <span data-ttu-id="99202-122">二重書き込みアプリケーション オーケストレーション ソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="99202-122">Apply the dual-write application orchestration solution.</span></span>

    <span data-ttu-id="99202-123">Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたばかりのエンティティ マップを適用します。</span><span class="sxs-lookup"><span data-stu-id="99202-123">In the Finance and Operations app, on the **Dual-write** page, select **Apply Solution** to apply the entity maps that you just downloaded and installed.</span></span> <span data-ttu-id="99202-124">ソリューションを適用すると、既定のエンティティ マップが公開されていることが確認できます。</span><span class="sxs-lookup"><span data-stu-id="99202-124">After you apply the solution, you should see that the default entity maps are published.</span></span>

     ![エンティティ マップの適用](media/apply-entity-maps.png)

<span data-ttu-id="99202-126">Microsoft が発行した二重書き込みエンティティ マップ ソリューションを環境に正常にインポートして適用しました。</span><span class="sxs-lookup"><span data-stu-id="99202-126">You've now successfully imported and applied a Microsoft-published dual-write entity map solution to your environment.</span></span>

![エンティティ マップは正常にリンクされました](media/entity-maps-linked.png)


## <a name="next-steps"></a><span data-ttu-id="99202-128">次のステップ</span><span class="sxs-lookup"><span data-stu-id="99202-128">Next steps</span></span>

[<span data-ttu-id="99202-129">エンティティ マップの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="99202-129">Enable entity maps for dual-write</span></span>](enable-entity-map.md)
