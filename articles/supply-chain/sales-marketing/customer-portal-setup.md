---
title: 顧客ポータルのインストール、設定、更新
description: このトピックでは、顧客ポータルのライセンスの詳細と設定手順を説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b9d1e742f78254d949dc49fda008d63b8bff4d65
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413982"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="96b86-103">顧客ポータルのインストール、設定、更新</span><span class="sxs-lookup"><span data-stu-id="96b86-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="96b86-104">ライセンス要件</span><span class="sxs-lookup"><span data-stu-id="96b86-104">Licensing requirements</span></span>

<span data-ttu-id="96b86-105">顧客ポータルの実装には、次のライセンスを所有している必要があります :</span><span class="sxs-lookup"><span data-stu-id="96b86-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="96b86-106">**Power Apps ポータル** - このライセンスは、顧客ポータルのホストに必要です。</span><span class="sxs-lookup"><span data-stu-id="96b86-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="96b86-107">ポータルは、使用率に基づいてライセンス供与されます。</span><span class="sxs-lookup"><span data-stu-id="96b86-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="96b86-108">詳細については、[Power Apps ポータルのライセンス要件](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96b86-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="96b86-109">**デュアル書き込み** - Supply Chain Management のエンティティにデュアル書き込みを有効にするには、必要なライセンスを所有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b86-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="96b86-110">詳細については、[デュアル書き込みのシステム要件](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96b86-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="96b86-111">デュアル書き込みと、Power Apps ポータルの依存関係</span><span class="sxs-lookup"><span data-stu-id="96b86-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="96b86-112">顧客ポータルは、次の図に示すように、Power Apps ポータルとデュアル書き込みと依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="96b86-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

![![顧客ポータルの依存関係](media/customer-portal-elements.png "顧客ポータルの依存関係")](media/customer-portal-elements.png "Customer portal dependencies")

<span data-ttu-id="96b86-114">Supply Chain Management の他の機能とは異なり、顧客ポータルのテンプレートは Power Apps ポータルに存在します。</span><span class="sxs-lookup"><span data-stu-id="96b86-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="96b86-115">したがって、顧客ポータルは、Power Apps ポータルやデュアル書き込みのエンティティが提供する機能や能力によって制限されます。</span><span class="sxs-lookup"><span data-stu-id="96b86-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="96b86-116">顧客ポータルを有効化する設定が必要です</span><span class="sxs-lookup"><span data-stu-id="96b86-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="96b86-117">必要なライセンスを確認した後は、デュアル書き込みを設定し、[デュアル書き込みの初回同期](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md)に記載の指示に従って設定することができます。</span><span class="sxs-lookup"><span data-stu-id="96b86-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="96b86-118">デュアル書き込みでは、以下のエンティティ マッピングを有効化してください :</span><span class="sxs-lookup"><span data-stu-id="96b86-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="96b86-119">販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="96b86-119">Sales Order Header</span></span>
- <span data-ttu-id="96b86-120">販売注文の詳細</span><span class="sxs-lookup"><span data-stu-id="96b86-120">Sales Order Details</span></span>
- <span data-ttu-id="96b86-121">アカウント</span><span class="sxs-lookup"><span data-stu-id="96b86-121">Accounts</span></span>
- <span data-ttu-id="96b86-122">連絡先</span><span class="sxs-lookup"><span data-stu-id="96b86-122">Contacts</span></span>
- <span data-ttu-id="96b86-123">製品</span><span class="sxs-lookup"><span data-stu-id="96b86-123">Products</span></span>

<span data-ttu-id="96b86-124">この設定の完了後、顧客ポータル テンプレートを準備できます。</span><span class="sxs-lookup"><span data-stu-id="96b86-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="96b86-125">顧客のポータルを準備する</span><span class="sxs-lookup"><span data-stu-id="96b86-125">Provision the Customer portal</span></span>

<span data-ttu-id="96b86-126">開始する前に、[必要な設定](#required-setup)が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="96b86-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="96b86-127">続いて、以下の手順に従って顧客ポータルを準備します。</span><span class="sxs-lookup"><span data-stu-id="96b86-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="96b86-128">[make.powerapps.com](https://make.powerapps.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="96b86-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="96b86-129">デュアル書き込みを有効化した環境を使用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="96b86-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="96b86-130">**作成** タブにて、画面下にスクロールして **テンプレートから開始する** セクションを選択し、**Supply Chain Management の顧客**という名前のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="96b86-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Supply Chain Management Customer**.</span></span>
4. <span data-ttu-id="96b86-131">画面に表示される指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="96b86-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="96b86-132">プロビジョニングが完了したら、**ホーム** ページの **自分のアプリ** セクションで顧客ポータルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="96b86-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="96b86-133">デュアル書き込みソリューションが、作業をする環境にインストールされていない場合は、エラーメッセージが表示され、顧客ポータルを準備することはできません。</span><span class="sxs-lookup"><span data-stu-id="96b86-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="96b86-134">顧客のポータルを更新する</span><span class="sxs-lookup"><span data-stu-id="96b86-134">Update the Customer portal</span></span>

<span data-ttu-id="96b86-135">後から顧客ポータルにその他機能を追加する場合があります。</span><span class="sxs-lookup"><span data-stu-id="96b86-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="96b86-136">基となるソリューション コンポーネントに行われた変更は、自動的に環境に反映されます。</span><span class="sxs-lookup"><span data-stu-id="96b86-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="96b86-137">ただし、環境内で準備された Webサイトに対しては、構成データに加えられた変更は自動的に反映されません。</span><span class="sxs-lookup"><span data-stu-id="96b86-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="96b86-138">新しいテンプレートからコードを取得し、それをプロビジョニングされた Web サイトにマージすることで、これらの変更を手動で適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b86-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="resources"></a><span data-ttu-id="96b86-139">リソース</span><span class="sxs-lookup"><span data-stu-id="96b86-139">Resources</span></span>

<span data-ttu-id="96b86-140">顧客ポータルを設定してカスタマイズする方法の詳細については、次のドキュメントを参照して基礎となるテクノロジーについて確認してください :</span><span class="sxs-lookup"><span data-stu-id="96b86-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="96b86-141">Power Apps ポータル ドキュメント</span><span class="sxs-lookup"><span data-stu-id="96b86-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="96b86-142">デュアル書き込みのドキュメント</span><span class="sxs-lookup"><span data-stu-id="96b86-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="96b86-143">ポータルを効果的に管理するには、Power Appsポータルと Common Data Service のライフサイクルを理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b86-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="96b86-144">詳細については、次のリソースを参照してください :</span><span class="sxs-lookup"><span data-stu-id="96b86-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="96b86-145">ポータルのライフ サイクルについて</span><span class="sxs-lookup"><span data-stu-id="96b86-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="96b86-146">ポータルのアップグレード</span><span class="sxs-lookup"><span data-stu-id="96b86-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="96b86-147">ポータルの構成の移行</span><span class="sxs-lookup"><span data-stu-id="96b86-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="96b86-148">ソリューションのライフサイクル管理 : Dynamics 365 for Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="96b86-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)