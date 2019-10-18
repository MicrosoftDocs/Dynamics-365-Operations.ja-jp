---
title: データ統合のトラブルシューティング ガイド
description: このトピックでは、Finance and Operations と Common Data Service 間のデータ統合に関するトラブル シューティングの情報を提供します。
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
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249112"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="e154b-103">データ統合のトラブルシューティング ガイド</span><span class="sxs-lookup"><span data-stu-id="e154b-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="e154b-104">Common Data Service のプラグイン トレース ログを有効にし、デュアル書き込みプラグイン エラーの詳細を検査</span><span class="sxs-lookup"><span data-stu-id="e154b-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="e154b-105">デュアル書き込み同期中に問題またはエラーが発生した場合は、これらの手順に従って追跡ログのエラーを検査します。</span><span class="sxs-lookup"><span data-stu-id="e154b-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="e154b-106">エラーを検査する前に、プラグイン トレース ログを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e154b-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="e154b-107">手順については、[チュートリアル: プラグインの書き込みおよび登録](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) の "トレースログの表示" を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e154b-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="e154b-108">これでエラーを検査できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e154b-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="e154b-109">Microsoft Dynamics 365 Sales にサインインします。</span><span class="sxs-lookup"><span data-stu-id="e154b-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="e154b-110">**設定**ボタン (ギヤ記号) を選択してから、**詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="e154b-111">**設定**メニューで、**カスタマイズ \> プラグイン トレース ログ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="e154b-112">タイプ名として **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** を選択して、エラー詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="e154b-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="e154b-113">デュアル書き込み同期エラーの調査</span><span class="sxs-lookup"><span data-stu-id="e154b-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="e154b-114">テスト中のエラーを検査するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e154b-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="e154b-115">Microsoft Dynamics Lifecycle Services (LCS) にログインします。</span><span class="sxs-lookup"><span data-stu-id="e154b-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="e154b-116">LCS プロジェクトを開いて、デュアル書き込みテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="e154b-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="e154b-117">**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="e154b-118">LCS に表示されるローカル アカウントを使用して、アプリケーション バーチャル マシン (VM) へのリモート デスクトップ接続を実行します。</span><span class="sxs-lookup"><span data-stu-id="e154b-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="e154b-119">イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e154b-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="e154b-120">**アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e154b-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="e154b-121">エラーと詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e154b-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="e154b-122">1 つの Common Data Service 環境をアプリケーションからリンク解除し、別の環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="e154b-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="e154b-123">リンクを更新するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e154b-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="e154b-124">アプリケーション環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="e154b-124">Go to the application environment.</span></span>
2. <span data-ttu-id="e154b-125">データ管理を開きます。</span><span class="sxs-lookup"><span data-stu-id="e154b-125">Open Data Management.</span></span>
3. <span data-ttu-id="e154b-126">**アプリ用 CDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="e154b-127">実行しているすべてのマッピングを選択してから、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="e154b-128">すべてのマッピングを選択してから、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e154b-129">**CustomerV3-Account** テンプレートが選択されている場合、**削除**オプションは利用できません。</span><span class="sxs-lookup"><span data-stu-id="e154b-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="e154b-130">必要に応じて、このテンプレートの選択をクリアします。</span><span class="sxs-lookup"><span data-stu-id="e154b-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="e154b-131">**CustomerV3-Account** は古いプロビジョニングされたテンプレートであり、見込み客から現金化ソリューションで動作します。</span><span class="sxs-lookup"><span data-stu-id="e154b-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="e154b-132">グローバルにリリースされているため、すべてのテンプレートの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e154b-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="e154b-133">**リンク解除の環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e154b-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="e154b-134">**はい**を選択して操作を確認します。</span><span class="sxs-lookup"><span data-stu-id="e154b-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="e154b-135">新しい環境をリンクするには、[インストール ガイド](https://aka.ms/dualwrite-docs) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e154b-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
