---
title: デュアル書き込み設定用にサポートされたシナリオ
description: このトピックでは、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
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
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818599"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="656f8-103">デュアル書き込み設定用にサポートされたシナリオ</span><span class="sxs-lookup"><span data-stu-id="656f8-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="656f8-104">Finance and Operations 環境と Common Data Service 環境との間には、デュアル書き込み接続を設定できます。</span><span class="sxs-lookup"><span data-stu-id="656f8-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="656f8-105">**Finance and Operations 環境** では、**Finance and Operations アプリ** の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail)。</span><span class="sxs-lookup"><span data-stu-id="656f8-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="656f8-106">**Common Data Service 環境**では、**Dynamics 365 のモデル駆動型アプリ**の基盤となるプラットフォームを提供します (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation)。</span><span class="sxs-lookup"><span data-stu-id="656f8-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="656f8-107">Finance and Operations の Human Resources では 、デュアル書き込み接続をサポートしていますが、Dynamics 365 Human Resources アプリではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="656f8-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="656f8-108">この設定のメカニズムは、サブスクリプションおよび環境によって異なります。</span><span class="sxs-lookup"><span data-stu-id="656f8-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="656f8-109">Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="656f8-110">Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Common Data Service 環境が得られます。</span><span class="sxs-lookup"><span data-stu-id="656f8-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="656f8-111">既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="656f8-112">サポートされている設定シナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="656f8-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="656f8-113">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="656f8-114">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="656f8-115">デモ データ付き新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="656f8-116">デモ データ付き新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="656f8-117">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="656f8-118">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="656f8-119">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="656f8-120">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="656f8-121">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="656f8-122">モデル駆動型のアプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="656f8-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="656f8-123">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="656f8-124">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="656f8-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="656f8-125">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="656f8-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a> <span data-ttu-id="656f8-126">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="656f8-127">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの既存インスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="656f8-128">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="656f8-129">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="656f8-130">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="656f8-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="656f8-131">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="656f8-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="656f8-132">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="656f8-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="656f8-133">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="656f8-134">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="656f8-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="656f8-135">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="656f8-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="656f8-136">3 文字の国際標準化機構 (ISO) 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="656f8-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="656f8-137">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="656f8-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a> <span data-ttu-id="656f8-138">デモ データ付きの新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="656f8-139">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-new) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="656f8-140">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="656f8-141">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="656f8-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="656f8-142">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="656f8-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a> <span data-ttu-id="656f8-143">デモ データ付きの新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="656f8-144">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの既存インスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存モデル駆動型アプリ インスタンス](#new-existing) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="656f8-145">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="656f8-146">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="656f8-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="656f8-147">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="656f8-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="656f8-148">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="656f8-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="656f8-149">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="656f8-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="656f8-150">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="656f8-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="656f8-151">3 文字の ISO 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="656f8-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="656f8-152">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="656f8-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a> <span data-ttu-id="656f8-153">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="656f8-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="656f8-154">Finance and Operations アプリの既存インスタンスと Dynamics 365 のモデル駆動型アプリの新規または既存インスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。</span><span class="sxs-lookup"><span data-stu-id="656f8-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="656f8-155">Finance and Operations アプリから接続を設定します。</span><span class="sxs-lookup"><span data-stu-id="656f8-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="656f8-156">既存の Common Data Service データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Common Data Service データを [ブートストラップ](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="656f8-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="656f8-157">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="656f8-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
