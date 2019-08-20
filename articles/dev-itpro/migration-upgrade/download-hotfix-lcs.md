---
title: Lifecycle Services (LCS) から更新プログラムをダウンロード
description: このトピックでは、期待される更新と、更新を Lifecycle Services (LCS) から取得する方法について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 56171
ms.assetid: 61069cf2-6c3f-4ebc-bbee-b21b1c99626a
ms.search.region: Global
ms.author: amarshall
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68b4130b4604fc20abfaa144cd543f03e0dd46cb
ms.sourcegitcommit: add48ece3864645a89a28327c4add607714befb5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736292"
---
# <a name="get-updates-from-lifecycle-services-lcs"></a><span data-ttu-id="a89fa-103">Lifecycle Services (LCS) から更新プログラムを入手</span><span class="sxs-lookup"><span data-stu-id="a89fa-103">Get updates from Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a89fa-104">このトピックでは、期待される更新と、最新の更新を Lifecycle Services (LCS) を使用して取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-104">This topic covers what updates you should expect to see and how you can get the latest updates using Lifecycle Services (LCS).</span></span>

## <a name="get-updates"></a><span data-ttu-id="a89fa-105">更新プログラムの入手</span><span class="sxs-lookup"><span data-stu-id="a89fa-105">Get updates</span></span>

<span data-ttu-id="a89fa-106">利用可能な更新プログラムを表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="a89fa-106">To view available updates:</span></span>
1. <span data-ttu-id="a89fa-107">資格情報を使用して LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="a89fa-107">Sign in to LCS using your credentials.</span></span>
2. <span data-ttu-id="a89fa-108">LCS プロジェクトで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-108">In the LCS project, select an environment.</span></span>
3. <span data-ttu-id="a89fa-109">**環境** ページで下にスクロールして **利用可能な更新** を表示します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-109">On the **Environment** page, scroll down to see the **Available updates**.</span></span>

## <a name="types-of-updates"></a><span data-ttu-id="a89fa-110">更新のタイプ</span><span class="sxs-lookup"><span data-stu-id="a89fa-110">Types of updates</span></span>

- <span data-ttu-id="a89fa-111">**バイナリ更新プログラム**は、コンパイル済みで累積されています。</span><span class="sxs-lookup"><span data-stu-id="a89fa-111">**Binary updates** are pre-compiled and cumulative.</span></span> <span data-ttu-id="a89fa-112">その後のバイナリ更新には、これまでのすべての更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-112">Every subsequent binary update includes all previous updates.</span></span> <span data-ttu-id="a89fa-113">これらの更新は、開発環境でコンパイルする必要はなく、LCS から非開発環境に直接適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-113">These updates don't have to be compiled in a development environment, and they can be applied directly to a non-development environment from LCS.</span></span>
        
    <span data-ttu-id="a89fa-114">Retail 機能とカスタマイズされた販売時点管理 (POS) のインスタンスを持つ環境を実行している場合は、Retail SDK のパッケージに記載されている追加手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-114">If you're running an environment that has Retail functionality and a customized instance of Cloud point of sale (POS), you must complete the additional steps that are listed under Retail SDK packaging.</span></span> <span data-ttu-id="a89fa-115">Microsoft Dynamics 365 for Retail で、すべての更新プログラムは、アプリケーション モデルの更新プログラムでさえ、バイナリ更新プログラムとしてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-115">For Microsoft Dynamics 365 for Retail, all updates, even updates for application models, are released as binary updates.</span></span>    
    
    <span data-ttu-id="a89fa-116">Microsoft Dynamics 365 for Retail のすべてのバージョン、および Microsoft Dynamics 365 for Finance and Operations バージョン 8.1 以降では、アプリケーション モデルの更新を含むすべての更新はバイナリ更新プログラムとしてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-116">For all versions of Microsoft Dynamics 365 for Retail, and Microsoft Dynamics 365 for Finance and Operations version 8.1 and later, all updates, including updates for application models, are released as binary updates.</span></span>

- <span data-ttu-id="a89fa-117">**X++ 更新プログラム**には、アプリケーション モデルの特定のアプリケーション機能への更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-117">**X++ updates** include updates to specific application functionality in application models.</span></span> <span data-ttu-id="a89fa-118">これらの更新は、個別にダウンロードして適用することができます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-118">These updates can be independently downloaded and applied.</span></span> <span data-ttu-id="a89fa-119">環境に適用する特定の X++ 更新プログラムを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-119">You can select specific X++ updates to apply to your environment.</span></span> <span data-ttu-id="a89fa-120">依存 X++ 更新は自動的に選択され、ダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-120">Dependent X++ updates are automatically selected and downloaded.</span></span> <span data-ttu-id="a89fa-121">X++ の更新はソース コードの更新です。</span><span class="sxs-lookup"><span data-stu-id="a89fa-121">X++ updates are source code updates.</span></span> <span data-ttu-id="a89fa-122">非開発環境に適用する前に、X++ の更新を開発者環境でコンパイルし、カスタマイズとマージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-122">Before they can be applied to a non-development environment, X++ updates must be compiled in a developer environment and merged with any customizations.</span></span> <span data-ttu-id="a89fa-123">X++ の更新は Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 以前にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-123">X++ updates apply only to Microsoft Dynamics 365 for Finance and Operations version 8.0 and earlier.</span></span> 


## <a name="update-option-by-product-and-version"></a><span data-ttu-id="a89fa-124">製品とバージョンごとの更新オプション</span><span class="sxs-lookup"><span data-stu-id="a89fa-124">Update option by product and version</span></span>
<span data-ttu-id="a89fa-125">製品とバージョンに基づいて Lifecycle Services とは異なる更新オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-125">Based on your product and version, you will have different update options from Lifecycle Services.</span></span>  

### <a name="dynamics-365-for-retail"></a><span data-ttu-id="a89fa-126">Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="a89fa-126">Dynamics 365 for Retail</span></span> 
- <span data-ttu-id="a89fa-127">**アプリケーション バージョン 8.0 以前** - すべてのアプリケーションとプラットフォームの変更に対する、累積的な結合されたバイナリ更新プログラムである単一のタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-127">**Application version 8.0 and earlier** - There will be a single tile that is a cumulative, combined binary update of all the application and platform changes.</span></span>

- <span data-ttu-id="a89fa-128">**アプリケーション バージョン 8.1 以降** - これは次のセクションで説明するように、Dynamics 365 for Finance and Operations バージョン 8.1 以降と同じ更新オプションが含みます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-128">**Application version 8.1 and later** - This includes the same update options as Dynamics 365 for Finance and Operations for version 8.1 and later, as described in the following section.</span></span>

### <a name="dynamics-365-for-finance-and-operations"></a><span data-ttu-id="a89fa-129">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a89fa-129">Dynamics 365 for Finance and Operations</span></span>
- <span data-ttu-id="a89fa-130">**アプリケーション バージョン 8.1 以降** - バージョン 8.1 以降のすべての更新は、すべてのアプリケーションとプラットフォームの更新の累積的な結合されたバイナリ更新です。</span><span class="sxs-lookup"><span data-stu-id="a89fa-130">**Application version 8.1 and later** - All updates for version 8.1 and later will be a cumulative, combined binary update of all of the application and platform updates.</span></span> <span data-ttu-id="a89fa-131">今回のリリースから、細かい X++ 更新プログラムはなくなります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-131">There will be no granular X++ updates starting with this release.</span></span>  

     <span data-ttu-id="a89fa-132">環境のバージョンと [サービス更新の可用性](../../fin-and-ops/get-started/public-preview-releases.md) に基づいて、環境で利用できる更新プログラムを選択するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-132">Based on your environment version and the [service update availability](../../fin-and-ops/get-started/public-preview-releases.md), you will have the option to choose the updates available to your environment.</span></span> <span data-ttu-id="a89fa-133">各更新オプションは、バージョン番号とビルド番号に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a89fa-133">Each update option is associated with a version number and a build number.</span></span>  

    <span data-ttu-id="a89fa-134">次の更新オプションが 1 つ以上表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-134">You may see one or more of the following update options.</span></span> 

   | <span data-ttu-id="a89fa-135">更新</span><span class="sxs-lookup"><span data-stu-id="a89fa-135">Update</span></span>        | <span data-ttu-id="a89fa-136">説明</span><span class="sxs-lookup"><span data-stu-id="a89fa-136">Description</span></span>           | <span data-ttu-id="a89fa-137">在庫状態</span><span class="sxs-lookup"><span data-stu-id="a89fa-137">Availability</span></span>  |
   | ------------- |-------------| -----|
   | <span data-ttu-id="a89fa-138">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="a89fa-138">Quality update</span></span>      | <span data-ttu-id="a89fa-139">品質更新プログラムは、現在実行している製品バージョンに固有の問題の修正を含む、累積的なロールアップ ビルドです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-139">A quality update is a cumulative, roll-up build that contains fixes for issues that are specific to the    product version that you’re currently running.</span></span> | <span data-ttu-id="a89fa-140">品質の更新は、環境が現在のサービス更新プログラムと同じバージョンを実行している (n) の場合、または現在のサービス更新 (n-1) よりも古いバージョンで環境が実行されている場合に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="a89fa-140">A quality update is available when your environment is running the same version of the current service update (n), or when your environment is running on one version older than the current service update (n-1).</span></span> <span data-ttu-id="a89fa-141">たとえば、現在のサービス更新プログラムがバージョン 10.0.2 の場合、バージョン 10.0.2 を実行している場合、または 1 つ古いバージョン 10.0.1 を実行している場合は、品質の更新を選択するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-141">For example, if the current service update is version 10.0.2, you will have the option to choose a quality update if you’re running version 10.0.2, or if you’re running one version older, which is 10.0.1.</span></span><br><br><span data-ttu-id="a89fa-142">現在のサービス更新プログラムより 2 バージョン以上古いバージョンに、品質の更新プログラムはありません。</span><span class="sxs-lookup"><span data-stu-id="a89fa-142">There will be no quality update available for any version that’s older than 2 versions of the current service update.</span></span> <span data-ttu-id="a89fa-143">最新の状態に保つには、最新のサービス更新プログラムを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-143">You will have to apply the latest service update to stay current.</span></span> |
   | <span data-ttu-id="a89fa-144">サービスの更新</span><span class="sxs-lookup"><span data-stu-id="a89fa-144">Service update</span></span>     | <span data-ttu-id="a89fa-145">サービス更新プログラムは、LCS プロジェクトの更新設定に基づい、現在の顧客環境に自動的に適用されているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-145">A service update is the version currently automatically applied to customer environments based on the LCS project update settings.</span></span><br><br><span data-ttu-id="a89fa-146">サービス更新プログラムは、新しい機能、機能、一般に利用可能な関連する品質更新を含む、累積的なロールアップ ビルドです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-146">A service update is a cumulative, roll-up build that contains new features, functionality, and the related quality update that is generally available.</span></span> | <span data-ttu-id="a89fa-147">環境が自動更新で利用できる現在のサービス更新バージョンに更新されていない場合、サービス更新プログラムが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="a89fa-147">A service update is available if your environment has not been updated to the current service update version available for auto-update.</span></span><br><br><span data-ttu-id="a89fa-148">LCS プロジェクトの更新設定を構成済みの場合、指定されたサンドボックスや運用環境のみが自動更新されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-148">Only the designated sandbox or production environment will be auto-updated if you have configured the update settings for the LCS project.</span></span> <span data-ttu-id="a89fa-149">ただし、現在のサービス更新バージョンを他のサンドボックス環境やクラウド ホスト環境に手動で適用できます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-149">However, you can manually apply the current service update version to other sandbox environments or your cloud-hosted environments.</span></span>|
   | <span data-ttu-id="a89fa-150">今後のサービスの更新</span><span class="sxs-lookup"><span data-stu-id="a89fa-150">Upcoming service update</span></span> | <span data-ttu-id="a89fa-151">次回のサービス更新は、自己更新で一般的に利用可能な最新バージョンです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-151">An upcoming service update is the latest version that is generally available for self-update.</span></span><br><br><span data-ttu-id="a89fa-152">次回のサービス更新プログラムは、新しい機能、機能、一般に利用可能な関連する品質更新を含む、累積的なロールアップ ビルドです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-152">An upcoming service update is a cumulative, roll-up build that contains new features, functionality, and the related quality update that is generally available.</span></span> | <span data-ttu-id="a89fa-153">LCS プロジェクトの更新設定に基づいて Microsoft がこのバージョンの自動適用を開始する約 2 週間前に、次回のサービス更新プログラムが一般的に自己配置可能になります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-153">An upcoming service update will be made generally available for self-deployment approximately 2 weeks prior to when Microsoft starts automatically applying this version based on your update settings for the LCS project.</span></span>|

- <span data-ttu-id="a89fa-154">**プラットフォーム 更新プログラム 4 以降がインストールされたアプリケーション バージョン 7.x または 8.0** - このリリースは引き続き細かい X++ の更新を含みます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-154">**Application version 7.x or 8.0 with Platform update 4 or later** - This release will still have the granular X++ updates.</span></span> <span data-ttu-id="a89fa-155">プラットフォーム更新 4 以降、プラットフォーム モジュールではオーバーレイヤーが許可されません。つまり、**プラットフォーム バイナリ更新プログラム** タイルを使用して、累積的な更新としてプラットフォーム更新プログラムを提供できます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-155">Starting with Platform update 4, no overlayering is allowed on the platform modules, which means that the **Platform binary updates** tile is available to provide the platform updates as a cumulative update.</span></span>
 
   <span data-ttu-id="a89fa-156">この組み合わせの顧客には、次のタイルが表示されます:</span><span class="sxs-lookup"><span data-stu-id="a89fa-156">For customers that are on this combination, you will see the following tiles:</span></span> 
   - <span data-ttu-id="a89fa-157">**すべての X++ 更新プログラム** - このタイルには、Microsoft によりリリースされるすべての細かい X++ 更新プログラムが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-157">**All X++ updates** - This tile shows all the granular X++ updates released by Microsoft.</span></span> 
        
   - <span data-ttu-id="a89fa-158">**重要な X++ 更新プログラム** - このタイルには、実稼働環境のテレメトリ データに基づく推奨 KB が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-158">**Critical X++ updates** - This tile shows recommended KBs that are based on the telemetry data in your production environment.</span></span> <span data-ttu-id="a89fa-159">このタイルは実稼働環境のみを表示し、更新プログラムのサブセットは環境に推奨される **すべての X++ 更新プログラム** タイルの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-159">This tile will only show Production environments and a subset of the updates shown under the **All X++ updates** tile that are recommended for your environments.</span></span> 
        
   - <span data-ttu-id="a89fa-160">**すべてのバイナリ更新プログラム** - このタイルには、アプリケーションとプラットフォームの両方に対する、結合された累積的バイナリ更新プログラムが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-160">**All binary updates** - This tile shows a combined, cumulative binary update for both the Application and Platform.</span></span>
        
   - <span data-ttu-id="a89fa-161">**プラットフォーム バイナリ更新プログラム** - このタイルには、プラットフォーム バイナリ更新プログラムのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-161">**Platform binary updates** - This tile shows only the Platform binary updates.</span></span> <span data-ttu-id="a89fa-162">プラットフォームだけを更新する場合は、このタイルから更新を取得できます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-162">If you want to update only the platform, you can get the update from this tile.</span></span> 

- <span data-ttu-id="a89fa-163">**プラットフォーム更新 3 以前を持つアプリケーション バージョン 7.x** - この組み合わせを使用するユーザーには、**すべての X++ 更新**、**重要な X++ 更新**、**すべてのバイナリ更新プログラム** の 3 つのタイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-163">**Application version 7.x with Platform update 3 or earlier** - For customers that are on this combination, you will see 3 tiles: **All X++ updates**, **Critical X++ updates**, and **All binary updates**.</span></span> <span data-ttu-id="a89fa-164">このリリース プラットフォームは引き続きオーバーレイヤーされるため、**プラットフォーム バイナリ更新プログラム** タイルはありません。</span><span class="sxs-lookup"><span data-stu-id="a89fa-164">Because this release platform can still be overlayered, there is no **Platform binary updates** tile.</span></span>
   
    > [!NOTE]
    > <span data-ttu-id="a89fa-165">今回のリリースを使用している場合、できるだけ早くアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89fa-165">If you are on this release, you need to upgrade as soon as possible.</span></span> 

  
## <a name="download-binary-updates"></a><span data-ttu-id="a89fa-166">バイナリ更新プログラムのダウンロード</span><span class="sxs-lookup"><span data-stu-id="a89fa-166">Download binary updates</span></span>
<span data-ttu-id="a89fa-167">バイナリ更新をダウンロードするには、LCS で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-167">To download binary updates, follow these steps in LCS.</span></span>

1. <span data-ttu-id="a89fa-168">品質更新プログラム、サービス更新プログラム、すべてのバイナリ更新プログラム、プラットフォーム バイナリ更新プログラムなど、バイナリ更新オプションのいずれかを選択して、アプリケーションとプラットフォーム バイナリ更新プログラムの組み合わせリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-168">Select any of the binary update options, including Quality update, Service update, All binary updates, and Platform binary updates to view the combined list of application and platform binary updates.</span></span> 
  
2. <span data-ttu-id="a89fa-169">**バイナリ更新プログラム**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-169">On the **Binary updates** page, select **Save package**.</span></span>
   
   > [!NOTE]
   > <span data-ttu-id="a89fa-170">保存するサポート技術情報 (KB) の記事を選択できません。これは、バイナリ更新プログラムですべての KB が更新パッケージに自動的に保存されるためです。</span><span class="sxs-lookup"><span data-stu-id="a89fa-170">You will not be able to select Knowledge Base (KB) articles to be saved because binary updates will automatically save all KBs in an update package.</span></span>        
   
   ![バイナリ パッケージの保存](./media/ReviewAndSaveBinaryPackage.jpg)

3. <span data-ttu-id="a89fa-172">**更新プログラムの確認と保存**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-172">On the **Review and save updates** page, select **Save package**.</span></span>

4. <span data-ttu-id="a89fa-173">**資産ライブラリへのパッケージの保存** で **名前** と **説明** を入力し、**パッケージの保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-173">In the **Save package to asset library**, enter the **Name** and **Description**, and select **Save package**.</span></span>

5. <span data-ttu-id="a89fa-174">環境ページに戻るには **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-174">Select **Done** to return to the environment page.</span></span>
 
6. <span data-ttu-id="a89fa-175">資産ライブラリに保存されているバイナリ パッケージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-175">You'll see the saved binary package in the asset library.</span></span> 

## <a name="download-x-updates"></a><span data-ttu-id="a89fa-176">ダウンロード X++ 更新プログラム</span><span class="sxs-lookup"><span data-stu-id="a89fa-176">Download X++ updates</span></span>
<span data-ttu-id="a89fa-177">X++ 更新プログラムをダウンロードするには、LCS で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-177">To download X++ updates, follow these steps in LCS.</span></span> 

1. <span data-ttu-id="a89fa-178">**すべての X++ 更新プログラム** タイルを選択して、環境で使用可能なアプリケーション更新のリストを表示するか、実稼働環境に推奨されるアプリケーション更新の **重要な X++ 更新プログラム** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-178">Select the **All X++ updates** tile to view the list of available application updates for an environment, or select the **Critical X++ updates** tile for the application updates that are recommended for your production environment.</span></span> 

   ![アプリケーション X++ 更新タイル](./media/X++UpdateTiles.jpg)   
  
2. <span data-ttu-id="a89fa-180">**更新プログラムの追加** ページで、該当するサポート技術情報 (KB) 番号を選択し、次に **追加** を選択して、選択した KB をダウンロード パッケージに追加します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-180">On the **Add updates** page, select the applicable Knowledge Base (KB) numbers, and then select **Add** to add selected KBs to the download package.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a89fa-181">X++ の更新プログラムで、この時点で利用可能なすべての更新プログラムをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-181">For X++ updates, you can download all available updates at this point.</span></span> <span data-ttu-id="a89fa-182">**すべて選択** をクリックし **追加** をクリックして、ダウンロード パッケージにすべての KB を追加します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-182">Click **Select all**, and then click **Add** to add all KBs to the download package.</span></span>

3. <span data-ttu-id="a89fa-183">**ダウンロード パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-183">Select **Download package**.</span></span>

4. <span data-ttu-id="a89fa-184">**修正プログラムの確認とダウンロード**ページで、選択した修正プログラムを確認したり、パッケージを破棄して、修正プログラムの選択に戻ったり、または最終修正プログラムのパッケージをダウンロードしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a89fa-184">On the **Review and download hotfixes** page, you can review the hotfixes that you selected, discard the package, return to the hotfix selections, or download the final hotfix package.</span></span>
    
5. <span data-ttu-id="a89fa-185">パッケージをダウンロードして **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a89fa-185">Download the package, and select **Done**.</span></span>
   

## <a name="additional-resources"></a><span data-ttu-id="a89fa-186">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a89fa-186">Additional resources</span></span>
- [<span data-ttu-id="a89fa-187">クラウド環境への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="a89fa-187">Apply updates to a cloud environment</span></span>](../deployment/apply-deployable-package-system.md)
- [<span data-ttu-id="a89fa-188">メタデータ修正プログラムのインストール</span><span class="sxs-lookup"><span data-stu-id="a89fa-188">Install a metadata hotfix</span></span>](./install-metadata-hotfix-package.md) 
