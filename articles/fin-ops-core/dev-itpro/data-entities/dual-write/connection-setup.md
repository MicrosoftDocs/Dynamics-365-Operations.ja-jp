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
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172857"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="26108-103">デュアル書き込み設定用にサポートされたシナリオ</span><span class="sxs-lookup"><span data-stu-id="26108-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="26108-104">Finance and Operations 環境と Common Data Service 環境との間には、デュアル書き込み接続を設定できます。</span><span class="sxs-lookup"><span data-stu-id="26108-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="26108-105">**Finance and Operations 環境**では、**Finance and Operations アプリケーション**の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Retail、および Dynamics 365 Human Resources)。</span><span class="sxs-lookup"><span data-stu-id="26108-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="26108-106">**Common Data Service 環境**では、**Dynamics 365 のモデル駆動型アプリ**の基盤となるプラットフォームを提供します (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation)。</span><span class="sxs-lookup"><span data-stu-id="26108-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="26108-107">この設定のメカニズムは、サブスクリプションおよび環境によって異なります。</span><span class="sxs-lookup"><span data-stu-id="26108-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="26108-108">Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。</span><span class="sxs-lookup"><span data-stu-id="26108-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="26108-109">Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Common Data Service 環境が得られます。</span><span class="sxs-lookup"><span data-stu-id="26108-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="26108-110">既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。</span><span class="sxs-lookup"><span data-stu-id="26108-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="26108-111">サポートされている設定シナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="26108-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="26108-112">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="26108-113">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="26108-114">デモ データ付き新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="26108-115">デモ データ付き新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="26108-116">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="26108-117">新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="26108-118">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="26108-119">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="26108-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="26108-120">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="26108-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="26108-121">モデル駆動型のアプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="26108-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="26108-122">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="26108-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="26108-123">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="26108-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="26108-124">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="26108-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a> <span data-ttu-id="26108-125">新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="26108-126">データ無しの Finance and Operations アプリの新しいインスタンスと Dynamics 365 のモデル駆動アプリの既存インスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="26108-127">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="26108-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="26108-128">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="26108-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="26108-129">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="26108-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="26108-130">エンティティ マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="26108-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="26108-131">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="26108-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="26108-132">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="26108-133">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="26108-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="26108-134">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="26108-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="26108-135">3 文字の国際標準化機構 (ISO) 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="26108-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="26108-136">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="26108-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a> <span data-ttu-id="26108-137">デモ データ付きの新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="26108-138">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しいモデル駆動型アプリ インスタンス](#new-new) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="26108-139">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="26108-140">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="26108-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="26108-141">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="26108-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a> <span data-ttu-id="26108-142">デモ データ付きの新しい Finance and Operations アプリ インスタンスと既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="26108-143">デモ データ付き Finance and Operations アプリの新しいインスタンスと Dynamics 365 モデル駆動型アプリの既存インスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存モデル駆動型アプリ インスタンス](#new-existing) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="26108-144">接続の設定が完了したら、デモ データをモデル駆動型のアプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="26108-145">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="26108-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="26108-146">データを同期するエンティティの**初期同期**機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="26108-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="26108-147">既存の Common Data Service データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26108-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="26108-148">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="26108-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="26108-149">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="26108-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="26108-150">3 文字の ISO 会社コードを使用し、Common Data Service データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="26108-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="26108-151">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="26108-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a> <span data-ttu-id="26108-152">既存の Finance and Operations アプリ インスタンスと新規または既存のモデル駆動型アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="26108-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="26108-153">Finance and Operations アプリの既存インスタンスと Dynamics 365 のモデル駆動型アプリの新規または既存インスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。</span><span class="sxs-lookup"><span data-stu-id="26108-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="26108-154">Finance and Operations アプリから接続を設定します。</span><span class="sxs-lookup"><span data-stu-id="26108-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="26108-155">既存の Common Data Service データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Common Data Service データを [ブートストラップ](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="26108-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="26108-156">デュアル書き込みはライブ同期モードになっているため、Common Data Service からのデータは、自動的に Finance and Operations アプリに送られます。</span><span class="sxs-lookup"><span data-stu-id="26108-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
