---
title: 新しい環境の配置
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して新しい環境を配置する方法について説明します。
author: rashmansur
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 1d2fe3602369a198529fc7be4401012d6343caca
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744823"
---
# <a name="deploy-a-new-environment"></a><span data-ttu-id="34e90-103">新しい環境の配置</span><span class="sxs-lookup"><span data-stu-id="34e90-103">Deploy a new environment</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="34e90-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用してサンドボックス (レベル 2 以上) および運用環境のプロセスの手順を詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="34e90-104">This topic walks through the process of deploying sandbox (Tier 2 and above) and production environments with the [self-service deployment](infrastructure-stack.md) experience.</span></span> <span data-ttu-id="34e90-105">このような環境を配置する次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="34e90-105">Refer to the following procedure to deploy these environments.</span></span>

1. <span data-ttu-id="34e90-106">プロジェクト ダッシュボード ページで **構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-106">Select **Configure** on the project dashboard page.</span></span>
2. <span data-ttu-id="34e90-107">配置する環境の **アプリケーション** および **プラットフォーム** バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-107">Select the **Application** and **Platform** version for the environment that you want to deploy.</span></span> 
3. <span data-ttu-id="34e90-108">環境の **一意の名前** を指定してください。</span><span class="sxs-lookup"><span data-stu-id="34e90-108">Provide a **unique name** for the environment.</span></span>
4. <span data-ttu-id="34e90-109">この環境を配置する **地域** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-109">Select the **region** where you want this environment to be deployed.</span></span> 
5. <span data-ttu-id="34e90-110">環境で **デモ データ** を読み込むかどうかや、**空のデータベース** が必要かどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-110">Choose whether you want to load **demo data** in your environment or if you want an **empty database**.</span></span>
6. <span data-ttu-id="34e90-111">製品で「はじめに」ライブラリとして設定される **BPM ライブラリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-111">Select the **BPM library** that will be set as the Getting started library in the product.</span></span>
7. <span data-ttu-id="34e90-112">カスタマイズを適用する場合は、アセット ライブラリでソフトウェア配置可能タブで、使用可能な **AOT パッケージ** (カスタマイズ パッケージ) のリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-112">Select from a list of available **AOT packages** (customization packages) on the Software Deployable tabs in the Asset Library if you want to apply customizations.</span></span> <span data-ttu-id="34e90-113">バージョン 8.1 以上のビルド環境から生成されたパッケージのみ選択してください。</span><span class="sxs-lookup"><span data-stu-id="34e90-113">Only packages generated from a build environment on version 8.1 and above should be selected.</span></span> <span data-ttu-id="34e90-114">互換性のないバージョンからパッケージを適用すると、環境に悪影響を与えるがあります。</span><span class="sxs-lookup"><span data-stu-id="34e90-114">Applying a package from an incompatible version will have an adverse effect on the environment.</span></span>
8. <span data-ttu-id="34e90-115">この環境に関連する **通知** を受け取る **2 つのユーザー電子メール アドレス** を指定します。</span><span class="sxs-lookup"><span data-stu-id="34e90-115">Specify **two user email addresses** that will receive **notifications** related to this environment.</span></span> <span data-ttu-id="34e90-116">これらのユーザーは、既にプロジェクト チームに所属しているユーザー (ISV またはパートナーなど) に追加されます。</span><span class="sxs-lookup"><span data-stu-id="34e90-116">These users are in addition to the users who are already on the project team (such as an ISV or a partner).</span></span>
9. <span data-ttu-id="34e90-117">製品で **システム管理者** として設定される **ユーザー** の **電子メール アドレス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34e90-117">Select the **email address** of the **user** that will be set as the **system administrator** in the product.</span></span>
10. <span data-ttu-id="34e90-118">構成を検証した後、**送信** をクリックして配置をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="34e90-118">After you validate the configurations, click **Submit** to trigger the deployment.</span></span>
11. <span data-ttu-id="34e90-119">チャネルの使用を計画する場合は、[Retail Cloud Scale Unit の初期化](initialize-retail-channels.md) も必要です。</span><span class="sxs-lookup"><span data-stu-id="34e90-119">If you plan to use channels, you must also [Initialize Retail Cloud Scale Unit](initialize-retail-channels.md).</span></span>

<span data-ttu-id="34e90-120">環境配置はすぐに開始され、完了までに **1 ～ 2 時間** かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="34e90-120">The environment deployment starts immediately and could take anywhere between **1-2 hours** to complete.</span></span> 

<span data-ttu-id="34e90-121">配置の進行状況を常時監視するには、**環境の詳細** ページを表示できます。</span><span class="sxs-lookup"><span data-stu-id="34e90-121">To closely monitor the deployment progress, you can view the **Environment details** page.</span></span> <span data-ttu-id="34e90-122">環境の状態は、**配置中** または **配置済み/失敗** のいずれかに変更されます。</span><span class="sxs-lookup"><span data-stu-id="34e90-122">The environment state should change to either **Deploying** or **Deployed/Failed**.</span></span>

<span data-ttu-id="34e90-123">配置が **成功した** 場合、環境の状態は **配置済み** になり、環境の管理者として設定されたユーザーは環境にログインできるようになります。</span><span class="sxs-lookup"><span data-stu-id="34e90-123">If the deployment **succeeds**, the environment state will be **Deployed**, and the user set as the environment administrator will be able to sign in to the environment.</span></span>

<span data-ttu-id="34e90-124">配置が **失敗した** 場合、Microsoft [サポート チケット](../lifecycle-services/lcs-support.md)を作成し、サポート チケットで **最後のアクティビティ ID** (**環境詳細** ページの **環境の管理** で確認できます) を指定します。</span><span class="sxs-lookup"><span data-stu-id="34e90-124">If the deployment **fails**, then create a Microsoft [support ticket](../lifecycle-services/lcs-support.md) and provide the **Last Activity ID** (available under **Manage environment** on the **Environment details** page) in the support ticket.</span></span>

## <a name="delete-an-environment"></a><span data-ttu-id="34e90-125">環境の削除</span><span class="sxs-lookup"><span data-stu-id="34e90-125">Delete an environment</span></span>

<span data-ttu-id="34e90-126">環境の詳細ページを使用して配置された状態にある環境を直接削除することができます。</span><span class="sxs-lookup"><span data-stu-id="34e90-126">You can delete an environment that is in the deployed state directly through the environment details page.</span></span> <span data-ttu-id="34e90-127">環境を削除するには、環境の詳細ページに移動し、アクション バーで **削除** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e90-127">To delete an environment, go to the environment details page and click the  **Delete** button on the action bar.</span></span> <span data-ttu-id="34e90-128">削除する環境の名前を入力するように要求する確認ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="34e90-128">A confirmation dialog box will display asking you to enter the name of the environment that you want to delete.</span></span> <span data-ttu-id="34e90-129">環境の名前を入力し、**はい** を選択すると、削除操作が開始されます。</span><span class="sxs-lookup"><span data-stu-id="34e90-129">After you enter the environment name and select **Yes**, the deletion operation will start.</span></span> <span data-ttu-id="34e90-130">削除処理が完了すると、環境を再配置する場合は、この環境の **構成** ボタンがプロジェクト ダッシュボードで有効になります。</span><span class="sxs-lookup"><span data-stu-id="34e90-130">When the deletion operation is complete, the **Configure** button for this environment will be enabled on the project dashboard if you want to redeploy the environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="34e90-131">環境を再配置するには、環境を削除し、上記の手順を使用してもう一度を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34e90-131">To redeploy an environment, you will need to delete the environment and then deploy it again using the steps listed above.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="34e90-132">クラウドでチャネル機能を使用している既存の顧客の場合、業務の継続的かつ中断のないサポートを確保するには、2020 年 1 月 31 日までに [Retail Cloud Scale Unit の初期化](initialize-retail-channels.md) を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="34e90-132">For existing customers using channel functionality in the cloud, to ensure continued and uninterrupted support for your business, we require that you [Initialize Retail Cloud Scale Unit](initialize-retail-channels.md) no later than January 31, 2020.</span></span> <span data-ttu-id="34e90-133">Store Scale Unit を独占して使用している顧客に対しては、アクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="34e90-133">There is no action required for customers who exclusively use Store Scale Unit.</span></span> <span data-ttu-id="34e90-134">延長が必要な場合は、Microsoft FastTrack Solution Architect までご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="34e90-134">Contact your Microsoft FastTrack Solution Architect if you require an extension.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]