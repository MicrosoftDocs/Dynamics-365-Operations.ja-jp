---
title: 新しい環境の配置
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して新しい環境を配置する方法について説明します。
author: manado
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 3fa8d7151cc65a55593851ae36551b1a541b0fa3
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537092"
---
# <a name="deploy-a-new-environment"></a><span data-ttu-id="e8ed0-103">新しい環境の配置</span><span class="sxs-lookup"><span data-stu-id="e8ed0-103">Deploy a new environment</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="e8ed0-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用してサンドボックス (レベル 2 以上) および運用環境のプロセスの手順を詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-104">This topic walks through the process of deploying sandbox (Tier 2 and above) and production environments with the [self-service deployment](infrastructure-stack.md) experience.</span></span> <span data-ttu-id="e8ed0-105">このような環境を配置する次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-105">Refer to the following procedure to deploy these environments.</span></span>

1. <span data-ttu-id="e8ed0-106">プロジェクト ダッシュボード ページで **構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-106">Select **Configure** on the project dashboard page.</span></span>
2. <span data-ttu-id="e8ed0-107">配置する環境の **アプリケーション** および **プラットフォーム** バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-107">Select the **Application** and **Platform** version for the environment that you want to deploy.</span></span> 
3. <span data-ttu-id="e8ed0-108">環境の**一意の名前**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-108">Provide a **unique name** for the environment.</span></span>
4. <span data-ttu-id="e8ed0-109">この環境を配置する**地域**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-109">Select the **region** where you want this environment to be deployed.</span></span> 
5. <span data-ttu-id="e8ed0-110">環境で**デモ データ**を読み込むかどうかや、**空のデータベース**が必要かどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-110">Choose whether you want to load **demo data** in your environment or if you want an **empty database**.</span></span>
6. <span data-ttu-id="e8ed0-111">製品で「はじめに」ライブラリとして設定される **BPM ライブラリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-111">Select the **BPM library** that will be set as the Getting started library in the product.</span></span>
7. <span data-ttu-id="e8ed0-112">カスタマイズを適用する場合は、アセット ライブラリでソフトウェア配置可能タブで、使用可能な **AOT パッケージ** (カスタマイズ パッケージ) のリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-112">Select from a list of available **AOT packages** (customization packages) on the Software Deployable tabs in the Asset Library if you want to apply customizations.</span></span> <span data-ttu-id="e8ed0-113">バージョン 8.1 以上のビルド環境から生成されたパッケージのみ選択してください。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-113">Only packages generated from a build environment on version 8.1 and above should be selected.</span></span> <span data-ttu-id="e8ed0-114">互換性のないバージョンからパッケージを適用すると、環境に悪影響を与えるがあります。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-114">Applying a package from an incompatible version will have an adverse effect on the environment.</span></span>
8. <span data-ttu-id="e8ed0-115">この環境に関連する**通知**を受け取る **2 つのユーザー電子メール アドレス**を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-115">Specify **two user email addresses** that will receive **notifications** related to this environment.</span></span> <span data-ttu-id="e8ed0-116">これらのユーザーは、既にプロジェクト チームに所属しているユーザー (ISV またはパートナーなど) に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-116">These users are in addition to the users who are already on the project team (such as an ISV or a partner).</span></span>
9. <span data-ttu-id="e8ed0-117">Finance and Operations 製品で**システム管理者**として設定され**るユーザー**の**電子メール アドレス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-117">Select the **email address** of the **user** that will be set as the **system administrator** in the Finance and Operations product.</span></span>
10. <span data-ttu-id="e8ed0-118">構成を検証した後、**送信** をクリックして配置をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-118">After you validate the configurations, click **Submit** to trigger the deployment.</span></span>

<span data-ttu-id="e8ed0-119">環境配置はすぐに開始され、完了までに **1 ～ 2 時間**かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-119">The environment deployment starts immediately and could take anywhere between **1-2 hours** to complete.</span></span> 

<span data-ttu-id="e8ed0-120">配置の進行状況を常時監視するには、**環境の詳細**ページを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-120">To closely monitor the deployment progress, you can view the **Environment details** page.</span></span> <span data-ttu-id="e8ed0-121">環境の状態は、**配置中**または**配置済み/失敗**のいずれかに変更されます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-121">The environment state should change to either **Deploying** or **Deployed/Failed**.</span></span>

<span data-ttu-id="e8ed0-122">配置が**成功した**場合、環境の状態は**配置済み**になり、環境の管理者として設定されたユーザーは環境にログインできるようになります。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-122">If the deployment **succeeds**, the environment state will be **Deployed**, and the user set as the environment administrator will be able to sign in to the environment.</span></span>

<span data-ttu-id="e8ed0-123">配置が**失敗した**場合、Microsoft [サポート チケット](../lifecycle-services/lcs-support.md)を作成し、サポート チケットで**最後のアクティビティ ID** (**環境詳細** ページの **環境の管理** で確認できます) を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-123">If the deployment **fails**, then create a Microsoft [support ticket](../lifecycle-services/lcs-support.md) and provide the **Last Activity ID** (available under **Manage environment** on the **Environment details** page) in the support ticket.</span></span>

## <a name="delete-an-environment"></a><span data-ttu-id="e8ed0-124">環境の削除</span><span class="sxs-lookup"><span data-stu-id="e8ed0-124">Delete an environment</span></span>

<span data-ttu-id="e8ed0-125">環境の詳細ページを使用して配置された状態にある環境を直接削除することができます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-125">You can delete an environment that is in the deployed state directly through the environment details page.</span></span> <span data-ttu-id="e8ed0-126">環境を削除するには、環境の詳細ページに移動し、アクション バーで **削除** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-126">To delete an environment, go to the environment details page and click the  **Delete** button on the action bar.</span></span> <span data-ttu-id="e8ed0-127">削除する環境の名前を入力するように要求する確認ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-127">A confirmation dialog box will display asking you to enter the name of the environment that you want to delete.</span></span> <span data-ttu-id="e8ed0-128">環境の名前を入力し、**はい** を選択すると、削除操作が開始されます。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-128">After you enter the environment name and select **Yes**, the deletion operation will start.</span></span> <span data-ttu-id="e8ed0-129">削除処理が完了すると、環境を再配置する場合は、この環境の **構成** ボタンがプロジェクト ダッシュボードで有効になります。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-129">When the deletion operation is complete, the **Configure** button for this environment will be enabled on the project dashboard if you want to redeploy the environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="e8ed0-130">環境を再配置するには、環境を削除し、上記の手順を使用してもう一度を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8ed0-130">To redeploy an environment, you will need to delete the environment and then deploy it again using the steps listed above.</span></span> 
