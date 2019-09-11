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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873108"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="261ee-103">データ統合のトラブルシューティング ガイド</span><span class="sxs-lookup"><span data-stu-id="261ee-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="261ee-104">Common Data Service のプラグイン トレース ログを有効にし、デュアル書き込みプラグイン エラーの詳細を検査</span><span class="sxs-lookup"><span data-stu-id="261ee-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="261ee-105">デュアル書き込み同期中に問題またはエラーが発生した場合は、これらの手順に従って追跡ログのエラーを検査します。</span><span class="sxs-lookup"><span data-stu-id="261ee-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="261ee-106">エラーを検査する前に、プラグイン トレース ログを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="261ee-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="261ee-107">手順については、[チュートリアル: プラグインの書き込みおよび登録](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) の "トレースログの表示" を参照してください。</span><span class="sxs-lookup"><span data-stu-id="261ee-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="261ee-108">これでエラーを検査できるようになります。</span><span class="sxs-lookup"><span data-stu-id="261ee-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="261ee-109">Microsoft Dynamics 365 for Sales へサインインします。</span><span class="sxs-lookup"><span data-stu-id="261ee-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="261ee-110">**設定**ボタン (ギヤ記号) を選択してから、**詳細設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="261ee-111">**設定**メニューで、**カスタマイズ \> プラグイン トレース ログ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="261ee-112">タイプ名として **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** を選択して、エラー詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="261ee-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="261ee-113">Finance and Operations のデュアル書き込み同期エラーを検査</span><span class="sxs-lookup"><span data-stu-id="261ee-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="261ee-114">テスト中のエラーを検査するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="261ee-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="261ee-115">Microsoft Dynamics Lifecycle Services (LCS) にログインします。</span><span class="sxs-lookup"><span data-stu-id="261ee-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="261ee-116">LCS プロジェクトを開いて、デュアル書き込みテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="261ee-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="261ee-117">**クラウド ホスト環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="261ee-118">LCS に表示されるローカル アカウントを使用して、Dynamics 365 for Finance and Operations バーチャル マシン (VM) へのリモート デスクトップ接続を実行します。</span><span class="sxs-lookup"><span data-stu-id="261ee-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="261ee-119">イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="261ee-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="261ee-120">**アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="261ee-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="261ee-121">エラーと詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="261ee-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="261ee-122">1 つの Common Data Service 環境を Finance and Operations からリンク解除し、別の環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="261ee-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="261ee-123">リンクを更新するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="261ee-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="261ee-124">Finance and Operations 環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="261ee-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="261ee-125">データ管理を開きます。</span><span class="sxs-lookup"><span data-stu-id="261ee-125">Open Data Management.</span></span>
3. <span data-ttu-id="261ee-126">**アプリ用 CDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="261ee-127">実行しているすべてのマッピングを選択してから、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="261ee-128">すべてのマッピングを選択してから、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="261ee-129">**CustomerV3-Account** テンプレートが選択されている場合、**削除**オプションは利用できません。</span><span class="sxs-lookup"><span data-stu-id="261ee-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="261ee-130">必要に応じて、このテンプレートの選択をクリアします。</span><span class="sxs-lookup"><span data-stu-id="261ee-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="261ee-131">**CustomerV3-Account** は古いプロビジョニングされたテンプレートであり、見込み客から現金化ソリューションで動作します。</span><span class="sxs-lookup"><span data-stu-id="261ee-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="261ee-132">グローバルにリリースされているため、すべてのテンプレートの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="261ee-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="261ee-133">**リンク解除の環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="261ee-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="261ee-134">**はい**を選択して操作を確認します。</span><span class="sxs-lookup"><span data-stu-id="261ee-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="261ee-135">新しい環境をリンクするには、[インストール ガイド](https://aka.ms/dualwrite-docs) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="261ee-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
