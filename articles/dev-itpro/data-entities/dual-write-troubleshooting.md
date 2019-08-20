---
title: データ統合のトラブルシューティング ガイド
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations と Common Data Service 間のデータ統合に関するトラブルシューティングの情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797278"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="2cfc6-103">データ統合のトラブルシューティング ガイド</span><span class="sxs-lookup"><span data-stu-id="2cfc6-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="2cfc6-104">Common Data Service のプラグイン トレースを有効にし、デュアル書き込みプラグイン エラーの詳細を確認</span><span class="sxs-lookup"><span data-stu-id="2cfc6-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="2cfc6-105">デュアル書き込み同期で問題またはエラーが発生した場合は、トレース ログでエラーを検査できます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="2cfc6-106">エラーを検査する前に、[プラグインと登録](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) の指示に従い、プラグイン トレースを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="2cfc6-107">これで、エラーを検査できます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="2cfc6-108">Dynamics 365 for Sales にログインします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="2cfc6-109">設定アイコン (ギア) をクリックし、**詳細設定**を選びます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="2cfc6-110">**設定**メニューで、**カスタマイズ > プラグイン トレース ログ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="2cfc6-111">タイプ名 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** をクリックして、エラー詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="2cfc6-112">Finance and Operations のデュアル書き込み同期エラーを確認</span><span class="sxs-lookup"><span data-stu-id="2cfc6-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="2cfc6-113">テスト中にエラーを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="2cfc6-114">LifeCycle Services (LCS) にログインします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="2cfc6-115">デュアル書き込みテストを実行するために、選択した LCS プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="2cfc6-116">クラウド ホスト環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="2cfc6-117">LCS に表示されるローカル アカウントを使用して、Finance and Operations VM にデスクトップをリモートします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="2cfc6-118">イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="2cfc6-119">**アプリケーションとサービス ログ > Microsoft > Dynamics > AX-DualWriteSync > オペレーション**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="2cfc6-120">エラーと詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="2cfc6-121">Finance and Operations から、別の Common Data Service 環境をリンクおよび解除の方法</span><span class="sxs-lookup"><span data-stu-id="2cfc6-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="2cfc6-122">リンクを更新する場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="2cfc6-123">Finance and Operations 環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="2cfc6-124">データ管理を開きます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-124">Open Data Management.</span></span>
+ <span data-ttu-id="2cfc6-125">**アプリの CDS にリンク**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="2cfc6-126">実行中のすべてのマッピングを選択し、**停止**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="2cfc6-127">実行中のすべてのマッピングを選択し、**削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2cfc6-128">**CustomerV3-Account** テンプレートが選択されている場合、**削除**オプションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="2cfc6-129">必要に応じて、選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-129">Unselect it if needed.</span></span> <span data-ttu-id="2cfc6-130">**CustomerV3-Account** は古いプロビジョニングされたテンプレートであり、見込み客から現金化ソリューションで動作します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="2cfc6-131">グローバルにリリースされているため、すべてのテンプレートの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="2cfc6-132">**リンク解除の環境**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="2cfc6-133">**はい**をクリックし、確認します。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="2cfc6-134">新しい環境をリンクするには、[インストール ガイド](https://aka.ms/dualwrite-docs) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2cfc6-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

