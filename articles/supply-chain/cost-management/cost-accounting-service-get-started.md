---
title: 原価会計の使用を開始する
description: このトピックでは、原価計算サービスのライセンスの詳細とインストール手順を説明します。
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276936"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="f5eca-103">原価会計の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="f5eca-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="f5eca-104">このトピックに記載されている機能は、プライベート プレビュー リリースの一部として提供されます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="f5eca-105">このトピックの内容や記載されている機能は変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f5eca-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="f5eca-106">プレビュー リリースの詳細については、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5eca-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="f5eca-107">原価会計サービスを利用することで、設定した原価計算台帳の中で複数の 棚卸し会計を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="f5eca-108">各原価計算台帳を *規則* に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="f5eca-109">規則とは、次のタイプの会計ポリシーの集合です。</span><span class="sxs-lookup"><span data-stu-id="f5eca-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="f5eca-110">原価オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f5eca-110">Cost object</span></span>
- <span data-ttu-id="f5eca-111">入力測定基準</span><span class="sxs-lookup"><span data-stu-id="f5eca-111">Input measurement basis</span></span>
- <span data-ttu-id="f5eca-112">原価フロー仮定</span><span class="sxs-lookup"><span data-stu-id="f5eca-112">Cost flow assumption</span></span>
- <span data-ttu-id="f5eca-113">原価要素</span><span class="sxs-lookup"><span data-stu-id="f5eca-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="f5eca-114">原価会計サービスを有効にした後でも、通常、Microsoft Dynamics 365 Supply Chain Management では棚卸し会計を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="f5eca-115">原価計算サービスはアドインです。</span><span class="sxs-lookup"><span data-stu-id="f5eca-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="f5eca-116">この機能を使用できるようにするには、Microsoft Dynamics Lifecycle Services (LCS) からインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5eca-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f5eca-117">したがって、本番環境で有効にする前に、テスト環境で評価することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="f5eca-118">現在原価会計サービスは、Dynamics 365 Supply Chain Management に組み込まれているすべての原価管理機能に対応していません。</span><span class="sxs-lookup"><span data-stu-id="f5eca-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f5eca-119">したがって、現在使用可能な一連の機能が要件を満たすかどうかを評価することが重要となります。</span><span class="sxs-lookup"><span data-stu-id="f5eca-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="f5eca-120">ライセンス</span><span class="sxs-lookup"><span data-stu-id="f5eca-120">Licensing</span></span>

<span data-ttu-id="f5eca-121">原価会計サービスは、Supply Chain Management に使用できる棚卸し会計の標準機能と共にライセンス供与されます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="f5eca-122">原価会計サービスの使用にあたっては、追加のライセンスを購入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f5eca-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="f5eca-123">アドインのインストール</span><span class="sxs-lookup"><span data-stu-id="f5eca-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5eca-124">原価会計サービスを使用するには、(ワンボックス環境ではなく) LCSを有効にした高可用性環境を用意する必要があります。また、Dynamics 365 Supply Chain Management バージョン 10.0.11 またはそれ以降を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5eca-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="f5eca-125">原価計算サービスを使用するには、次の手順に従って、Supply Chain Management 用の原価計算サービス アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="f5eca-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="f5eca-126">LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f5eca-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="f5eca-127">**プレビュー機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="f5eca-128">プラス記号 (**+**) を選択してください。</span><span class="sxs-lookup"><span data-stu-id="f5eca-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="f5eca-129">**コード** フィールドに、原価会計サービス用のアドインのベータキーを入力します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="f5eca-130">（事前にキーを電子メールで受け取っている必要があります）</span><span class="sxs-lookup"><span data-stu-id="f5eca-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="f5eca-131">**ブロック解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="f5eca-132">サービスを追加する LCS 環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="f5eca-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="f5eca-133">**完全な詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="f5eca-134">**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="f5eca-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="f5eca-135">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="f5eca-136">**原価会計サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="f5eca-137">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="f5eca-138">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-138">Select **Install**.</span></span>

1. <span data-ttu-id="f5eca-139">**環境アドイン** クイックタブに、原価会計サービスがインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="f5eca-140">数分後、状態が **インストール中** から **インストール済** に変わります。</span><span class="sxs-lookup"><span data-stu-id="f5eca-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="f5eca-141">（この変更を表示するには、ページを更新する必要がある場合があります）その時点で、原価会計サービスを使用する準備が整います。</span><span class="sxs-lookup"><span data-stu-id="f5eca-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="f5eca-142">統合を設定する</span><span class="sxs-lookup"><span data-stu-id="f5eca-142">Set up the integration</span></span>

<span data-ttu-id="f5eca-143">原価会計サービスと Dynamics 365 Supply Chain Management の統合を設定するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f5eca-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="f5eca-144">**システム管理 > 機能管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="f5eca-145">**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="f5eca-146">**すべて** タブを開き、*原価会計サービス* という機能を検索します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="f5eca-147">**直ちに有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="f5eca-148">**原価管理 > 原価会計サービス > 設定 > 原価計算サービスパラメータ > 統合パラメータ** へと移動します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="f5eca-149">**アプリケーション ID**  フィールドに、次のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="f5eca-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="f5eca-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="f5eca-151">**データ サービス エンドポイント** フィールドに次の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="f5eca-152">**原価会計サービス エンドポイント** フィールドに次の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5eca-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="f5eca-153">以上で、原価会計サービスを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f5eca-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="f5eca-154">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="f5eca-154">Related resources</span></span>

[<span data-ttu-id="f5eca-155">原価会計サービス ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="f5eca-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
