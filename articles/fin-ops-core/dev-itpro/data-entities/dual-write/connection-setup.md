---
title: デュアル書き込みの設定方法に関するガイダンス
description: このトピックでは、デュアル書き込みの設定でサポートされているシナリオについて説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685668"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="e990d-103">デュアル書き込みの設定方法に関するガイダンス</span><span class="sxs-lookup"><span data-stu-id="e990d-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e990d-104">Finance and Operations 環境と Dataverse 環境との間には、デュアル書き込み接続を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e990d-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="e990d-105">**Finance and Operations 環境** では、**Finance and Operations アプリケーション** の基盤となるプラットフォームを提供します (たとえば、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、および Dynamics 365 Human Resources)。</span><span class="sxs-lookup"><span data-stu-id="e990d-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="e990d-106">**Dataverse 環境** では、**Customer Engagement アプリ** の基盤となるプラットフォームを提供します (Dynamics 365 Sales、Dynamics 365 Customer Service、Dynamics 365 Field Service、Dynamics 365 Marketing、および Dynamics 365 Project Service Automation)。</span><span class="sxs-lookup"><span data-stu-id="e990d-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e990d-107">Dynamics 365 Finance の Human Resources モジュールでは 、デュアル書き込み接続に対応していますが、Dynamics 365 Human Resources アプリでは対応していません。</span><span class="sxs-lookup"><span data-stu-id="e990d-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="e990d-108">この設定のメカニズムは、サブスクリプションや環境によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e990d-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="e990d-109">Finance and Operations アプリの新しいインスタンスの場合、デュアル書き込み接続の設定は Microsoft Dynamics Lifecycle Services (LCS) で開始されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e990d-110">Microsoft Power Platform のライセンスを所有している際は、テナントに無い場合、新しい Dataverse 環境が得られます。</span><span class="sxs-lookup"><span data-stu-id="e990d-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="e990d-111">既存のインスタンス Finance and Operations アプリの場合、デュアル書き込み接続の設定は Finance and Operations環境で開始されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="e990d-112">エンティティでデュアル書き込みを開始する前に、最初の同期を実行して、Finance and Operations アプリと Customer Engagement アプリの両面で既存のデータを処理することができます。</span><span class="sxs-lookup"><span data-stu-id="e990d-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="e990d-113">2 つの環境間でデータを同期する必要がない場合は、初期同期を省略できます。</span><span class="sxs-lookup"><span data-stu-id="e990d-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="e990d-114">初期同期では、既存のデータをひとつのアプリから双方向の別のアプリにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="e990d-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="e990d-115">設定のシナリオには、使用中の環境や環境に含まれるデータのタイプによって、さまざまなシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="e990d-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="e990d-116">サポートされている設定シナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e990d-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="e990d-117">新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="e990d-118">新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="e990d-119">データ付き新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="e990d-120">データ付き新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="e990d-121">既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="e990d-122">既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="e990d-123">新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="e990d-124">データ無しの Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの新しいインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="e990d-125">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="e990d-126">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="e990d-127">Customer Engagement アプリの新しい空のインスタンスがプロビジョニングされ、CRM の主要ソリューションがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="e990d-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="e990d-128">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="e990d-129">テーブル マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="e990d-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="e990d-130">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="e990d-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="e990d-131">新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="e990d-132">データ無しの Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの既存のインスタンス間のデュアル書き込み接続を設定するには、[Lifecycle Services からのデュアル書き込み設定](lcs-setup.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="e990d-133">接続の設定が完了すると、次のアクションが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="e990d-134">新しい空の Finance and Operations 環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="e990d-135">DAT 会社のデータに対して、デュアル書き込み接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="e990d-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="e990d-136">テーブル マップでは、ライブ同期が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="e990d-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="e990d-137">次に、両方の環境について、ライブ データ同期の準備が整います。</span><span class="sxs-lookup"><span data-stu-id="e990d-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="e990d-138">既存の Dataverse データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="e990d-139">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="e990d-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="e990d-140">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="e990d-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="e990d-141">3 文字の国際標準化機構 (ISO) 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="e990d-142">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-143">例へのリンクや代替のアプローチについては、このトピックで後述する[使用例](#example)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="e990d-144">データ付き新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="e990d-145">データ付き Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの新しいインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス](#new-new) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="e990d-146">接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="e990d-147">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e990d-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="e990d-148">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-149">例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="e990d-150">データ付き新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="e990d-151">データ付き Finance and Operations アプリの新しいインスタンスと Customer Engagement アプリの既存のインスタンス間にデュアル書き込み接続を設定するには、このトピック前半の[新しい Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス](#new-existing) セクションにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="e990d-152">接続の設定が完了したら、データを Customer Engagement アプリに同期する場合には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="e990d-153">LCS ページから Finance and Operations アプリを開き、ログインして、**データ管理 \> デュアル書き込み** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e990d-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="e990d-154">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-155">既存の Dataverse データを Finance and Operations アプリに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e990d-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="e990d-156">Finance and Operations アプリに新しい会社を作成します。</span><span class="sxs-lookup"><span data-stu-id="e990d-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="e990d-157">デュアル書き込み接続の設定に会社を追加します。</span><span class="sxs-lookup"><span data-stu-id="e990d-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="e990d-158">3 文字の ISO 会社コードを使用し、Dataverse データを [Bootstrap](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="e990d-159">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-160">例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="e990d-161">既存の Finance and Operations アプリ インスタンスと新しい Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="e990d-162">Finance and Operations アプリの既存インスタンスと Customer Engagement アプリの新規のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で発生します。</span><span class="sxs-lookup"><span data-stu-id="e990d-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="e990d-163">[Finance and Operations アプリから接続を設定します](enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="e990d-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="e990d-164">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-165">例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="e990d-166">既存の Finance and Operations アプリ インスタンスと既存の Customer Engagement アプリ インスタンス</span><span class="sxs-lookup"><span data-stu-id="e990d-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="e990d-167">Finance and Operations アプリの既存インスタンスと Customer Engagement アプリの既存のインスタンス間のデュアル書き込み接続の設定は、Finance and Operation 環境で行います。</span><span class="sxs-lookup"><span data-stu-id="e990d-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="e990d-168">[Finance and Operations アプリから接続を設定します](enable-dual-write.md)。</span><span class="sxs-lookup"><span data-stu-id="e990d-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="e990d-169">既存の Dataverse データを Finance and Operations アプリに同期するには、3 文字の ISO 会社コードを使用して、Dataverse データを [ブートストラップ](bootstrap-company-data.md) にて実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="e990d-170">データを同期するテーブルの **初期同期** 機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e990d-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="e990d-171">例へのリンクや代替のアプローチについては、[使用例](#example)のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="e990d-172">例</span><span class="sxs-lookup"><span data-stu-id="e990d-172">Example</span></span>

<span data-ttu-id="e990d-173">例については、[Customers V3 の有効化—連絡先テーブル マップ](enable-entity-map.md#enable-table-map)を参照してください</span><span class="sxs-lookup"><span data-stu-id="e990d-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="e990d-174">初期同期を実行する必要がある各エンティティのデータ ボリュームに基づく代替的なアプローチについては、[初期同期の考慮事項](initial-sync-guidance.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e990d-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
