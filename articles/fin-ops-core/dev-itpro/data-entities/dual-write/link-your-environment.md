---
title: 二重書き込みウィザードを使用して環境をリンクする
description: このトピックでは、二重書き込みウィザードを使用して、Finance and Operations アプリ環境を Common Data Service 環境にリンクする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
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
ms.openlocfilehash: 05ccc8458881e47e42ae29d941b25cf5afe04504
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279124"
---
# <a name="use-the-dual-write-wizard-to-link-your-environments"></a><span data-ttu-id="f3413-103">二重書き込みウィザードを使用して環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="f3413-103">Use the dual-write wizard to link your environments</span></span>

[!include [banner](../../includes/banner.md)]



1. <span data-ttu-id="f3413-104">Common Data Service 環境にリンクする Finance and Operations アプリ環境にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f3413-104">Sign in to the Finance and Operations app environment that you want to link to your Common Data Service environment.</span></span>
2. <span data-ttu-id="f3413-105">**ワークスペース \> データ管理**に移動して、**デュアル書き込み**のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3413-105">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>

    ![二重書き込みタイル](media/navigate-to-data-management.png)

3. <span data-ttu-id="f3413-107">**環境への新しいリンク** を選択して、**Common Data Service へのリンク設定** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3413-107">Select **New link to environment** to open the **Setup link to Common Data Service** wizard.</span></span>
4. <span data-ttu-id="f3413-108">**環境の選択** ページには、サインインしたユーザーが環境管理者であるすべての Common Data Service 環境が一覧表示されます。リンク先の Common Data Service 環境を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3413-108">The **Choose environment** page lists all the Common Data Service environments where the signed-in user is an environment admin. Select the Common Data Service environment to link to, and then select **Next**.</span></span>

    ![環境ページを選択する](media/data-service-environment.png)

5. <span data-ttu-id="f3413-110">法人を選択して、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3413-110">Select your legal entities, and then select **Next**.</span></span>

    ![法人の選択手順](media/select-legal-entities.png)

    <span data-ttu-id="f3413-112">正常性チェックを実行し、システムが二重書き込みを有効にするための要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3413-112">A health check is run to verify that your system meets the requirements for enabling dual-write.</span></span> <span data-ttu-id="f3413-113">正常性チェックでは、すべての前提条件が完了していることも確認します。</span><span class="sxs-lookup"><span data-stu-id="f3413-113">The health check also verifies that all the prerequisites have been completed.</span></span> <span data-ttu-id="f3413-114">いずれかの正常性チェックが失敗した場合は、次の手順に進む前に、すべての前提条件を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f3413-114">If any health check test fails, make that you've completed all the prerequisites before you move on to the next step.</span></span>

    <span data-ttu-id="f3413-115">次の例では、アプリを接続するためのアクセスが許可されているかどうかのテストが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="f3413-115">In the following example, the test about whether access was granted to connect the apps failed.</span></span> <span data-ttu-id="f3413-116">この場合、最初に適切なアプリケーション ID を作成して、アプリを接続するためのアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3413-116">In this case, you must first grant access to connect the apps by the creating the appropriate application IDs.</span></span> <span data-ttu-id="f3413-117">その後、ウィザードを再実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3413-117">You must then rerun the wizard.</span></span>

    ![正常性チェック ページ](media/health-check.png)

6. <span data-ttu-id="f3413-119">概要、プライバシー通知、同意を確認し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3413-119">Review the summary, privacy notice, and consent, and then select **Create**.</span></span>

<span data-ttu-id="f3413-120">Finance and Operations アプリを Common Data Service 環境にリンクしました。</span><span class="sxs-lookup"><span data-stu-id="f3413-120">You've now linked your Finance and Operations app to the Common Data Service environment.</span></span> <span data-ttu-id="f3413-121">次の手順では、エンティティ マップの二重書き込みを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3413-121">The next step is to enable entity maps for dual-write.</span></span>

![エンティティ マップは正常にリンクされました](media/entity-maps-linked.png)

> [!NOTE]
> <span data-ttu-id="f3413-123">エンティティ マップが表示されない場合、または空白のページが表示される場合は、Finance and Operations アプリのエンティティ マップ ソリューションをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="f3413-123">If you don't see your entity maps, or if you see a blank page, be sure to install the entity map solution for the Finance and Operations app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f3413-124">次のステップ</span><span class="sxs-lookup"><span data-stu-id="f3413-124">Next steps</span></span>

[<span data-ttu-id="f3413-125">エンティティ マップの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="f3413-125">Enable entity maps for dual-write</span></span>](enable-entity-map.md)
