---
title: デュアル書き込み設定用にサポートされたシナリオ
description: このトピックでは、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112472"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="a4c81-103">デュアル書き込み設定用にサポートされたシナリオ</span><span class="sxs-lookup"><span data-stu-id="a4c81-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a4c81-104">Finance and Operations 環境と Common Data Service 環境との間には、デュアル書き込み接続を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="a4c81-105">**Finance and Operations 環境**では、**Finance and Operations アプリケーション**の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail、および Dynamics 365 Human Resources)。</span><span class="sxs-lookup"><span data-stu-id="a4c81-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="a4c81-106">**Common Data Service 環境**では、**Dynamics 365 のモデル駆動型アプリ**の基盤となるプラットフォームを提供します (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation)。</span><span class="sxs-lookup"><span data-stu-id="a4c81-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="a4c81-107">この設定のメカニズムは、サブスクリプションおよび環境によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a4c81-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="a4c81-108">Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a4c81-109">Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Common Data Service 環境が得られます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="a4c81-110">既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="a4c81-111">サポートされている設定シナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a4c81-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="a4c81-112">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="a4c81-113">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="a4c81-114">デモ データ付き新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="a4c81-115">デモ データ付き新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="a4c81-116">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="a4c81-117">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="a4c81-118">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a4c81-119">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a4c81-120">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a4c81-121">モデル駆動型のアプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="a4c81-122">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a4c81-123">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="a4c81-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a4c81-124">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a> <span data-ttu-id="a4c81-125">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="a4c81-126">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの既存インスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="a4c81-127">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="a4c81-128">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="a4c81-129">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="a4c81-130">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="a4c81-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="a4c81-131">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="a4c81-132">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a4c81-133">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4c81-134">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a4c81-135">3 文字の国際標準化機構 (ISO) 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="a4c81-136">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a> <span data-ttu-id="a4c81-137">デモ データ付きの新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="a4c81-138">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-new) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="a4c81-139">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a4c81-140">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a4c81-141">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a> <span data-ttu-id="a4c81-142">デモ データ付きの新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="a4c81-143">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの既存インスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存モデル駆動型アプリ インスタンス](#new-existing) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="a4c81-144">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="a4c81-145">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="a4c81-146">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="a4c81-147">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a4c81-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="a4c81-148">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4c81-149">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="a4c81-150">3 文字の ISO 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a4c81-151">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a> <span data-ttu-id="a4c81-152">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="a4c81-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="a4c81-153">Finance and Operations アプリの既存インスタンスと Dynamics 365 のモデル駆動型アプリの新規または既存インスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="a4c81-154">Finance and Operations アプリから接続を設定します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="a4c81-155">既存の Common Data Service データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Common Data Service データを [ブートストラップ](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="a4c81-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="a4c81-156">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="a4c81-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
