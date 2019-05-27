---
title: Lifecycle Services (LCS) から更新プログラムをダウンロード
description: このトピックでは、期待される更新と、更新を Lifecycle Services (LCS) から取得する方法について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 56171
ms.assetid: 61069cf2-6c3f-4ebc-bbee-b21b1c99626a
ms.search.region: Global
ms.author: amarshall
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b396e98326e277ec7cc730e094cc9332d7ac8230
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537402"
---
# <a name="get-updates-from-lifecycle-services-lcs"></a><span data-ttu-id="07dad-103">Lifecycle Services (LCS) から更新プログラムを入手</span><span class="sxs-lookup"><span data-stu-id="07dad-103">Get updates from Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07dad-104">このトピックでは、期待される更新と、更新を Lifecycle Services (LCS) から取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="07dad-104">This topic covers what updates you should expect to see and how you can get the updates from Lifecycle Services (LCS).</span></span>

## <a name="types-of-updates"></a><span data-ttu-id="07dad-105">更新のタイプ</span><span class="sxs-lookup"><span data-stu-id="07dad-105">Types of updates</span></span>

- <span data-ttu-id="07dad-106">**バイナリ更新プログラム**は、コンパイル済みで累積されています。</span><span class="sxs-lookup"><span data-stu-id="07dad-106">**Binary updates** are pre-compiled and cumulative.</span></span> <span data-ttu-id="07dad-107">その後のバイナリ更新には、これまでのすべての更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07dad-107">Every subsequent binary update includes all previous updates.</span></span> <span data-ttu-id="07dad-108">これらの更新は、開発環境でコンパイルする必要はなく、LCS から非開発環境に直接適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="07dad-108">These updates don't have to be compiled in a development environment, and they can be applied directly to a non-development environment from LCS.</span></span>
        
    <span data-ttu-id="07dad-109">小売機能とカスタマイズされた販売時点管理 (POS) のインスタンスを持つ環境を実行している場合は、Retail SDK のパッケージに記載されている追加手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07dad-109">If you're running an environment that has retail functionality and a customized instance of Cloud point of sale (POS), you must complete the additional steps that are listed under Retail SDK packaging.</span></span> <span data-ttu-id="07dad-110">Microsoft Dynamics 365 for Retail で、すべての更新プログラムは、アプリケーション モデルの更新プログラムでさえ、バイナリ更新プログラムとしてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="07dad-110">For Microsoft Dynamics 365 for Retail, all updates, even updates for application models, are released as binary updates.</span></span>    

- <span data-ttu-id="07dad-111">**X++ 更新プログラム**には、アプリケーション モデルの特定のアプリケーション機能への更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07dad-111">**X++ updates** include updates to specific application functionality in application models.</span></span> <span data-ttu-id="07dad-112">これらの更新は、個別にダウンロードして適用することができます。</span><span class="sxs-lookup"><span data-stu-id="07dad-112">These updates can be independently downloaded and applied.</span></span> <span data-ttu-id="07dad-113">環境に適用する特定の X++ 更新プログラムを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="07dad-113">You can select specific X++ updates to apply to your environment.</span></span>  <span data-ttu-id="07dad-114">依存 X++ 更新は自動的に選択され、ダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="07dad-114">Dependent X++ updates are automatically selected and downloaded.</span></span> <span data-ttu-id="07dad-115">X++ の更新はソース コードの更新であり、非開発環境に適用する前に、開発環境でコンパイルして任意のカスタマイズとマージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07dad-115">Any X++ updates are source code updates, before they can be applied to a non-development environment, they must be compiled in a developer environment and merged with any customizations.</span></span> <span data-ttu-id="07dad-116">X++ 更新プログラムは Microsoft Dynamics 365 for Finance and Operations にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-116">X++ updates apply only to Microsoft Dynamics 365 for Finance and Operations.</span></span>   

## <a name="get-updates"></a><span data-ttu-id="07dad-117">更新プログラムの入手</span><span class="sxs-lookup"><span data-stu-id="07dad-117">Get updates</span></span>

<span data-ttu-id="07dad-118">利用可能な更新プログラムを表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="07dad-118">To view available updates:</span></span>
1. <span data-ttu-id="07dad-119">資格情報を使用して LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="07dad-119">Sign in to LCS using your credentials.</span></span>
2. <span data-ttu-id="07dad-120">LCS プロジェクトで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="07dad-120">In the LCS project, select an environment.</span></span>
3. <span data-ttu-id="07dad-121">**環境**ページで、**監視**セクションには更新タイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="07dad-121">On the **Environment** page, the **Monitoring** section includes update tiles.</span></span> 

## <a name="types-of-tiles"></a><span data-ttu-id="07dad-122">タイルのタイプ</span><span class="sxs-lookup"><span data-stu-id="07dad-122">Types of tiles</span></span>

<span data-ttu-id="07dad-123">タイルには次の 4 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="07dad-123">There are 4 different types of tiles:</span></span> 
1. <span data-ttu-id="07dad-124">**すべての X++ 更新プログラム** - このタイルには、Microsoft によりリリースされるすべての細かい X++ 更新プログラムが表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-124">**All X++ updates** - This tile shows all the granular X++ updates released by Microsoft.</span></span> 
2. <span data-ttu-id="07dad-125">**重要な X++ 更新プログラム** - このタイルには、実稼働環境のテレメトリ データに基づく推奨 KB が表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-125">**Critical X++ updates** - This tile shows recommended KBs that are based on the telemetry data in your production environment.</span></span> <span data-ttu-id="07dad-126">このタイルには、*生産環境*のみ表示され、更新プログラムのサブセットは環境に推奨される **すべての X++ 更新プログラム** の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-126">This tile will only show *Production environments* and a subset of the updates shown under the **All X++ updates** tile that are recommended for your environments.</span></span> 
3. <span data-ttu-id="07dad-127">**すべてのバイナリ更新プログラム** - このタイルには、アプリケーションとプラットフォームの両方の結合された累積的バイナリ アップデートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-127">**All binary updates** - This tile shows a combined cumulative binary update for both the Application and Platform.</span></span>
4. <span data-ttu-id="07dad-128">**プラットフォーム バイナリ更新プログラム** - このタイルには、プラットフォーム バイナリ更新プログラムのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-128">**Platform binary updates** - This tile shows only the Platform binary updates.</span></span> <span data-ttu-id="07dad-129">プラットフォームだけを更新する場合は、このタイルから更新を取得できます。</span><span class="sxs-lookup"><span data-stu-id="07dad-129">If you want to update only the platform, you can get the update from this tile.</span></span> 

<span data-ttu-id="07dad-130">製品およびバージョンによっては、タイルの表示が異なります。</span><span class="sxs-lookup"><span data-stu-id="07dad-130">Depending on the product and version, the tiles you see will differ.</span></span>

- <span data-ttu-id="07dad-131">**Dynamics 365 for Retail** - Dynamics 365 for Retail を展開したユーザーには、すべてのアプリケーションとプラットフォーム変更が結合された累積的バイナリ更新プログラムである 1 つのタイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-131">**Dynamics 365 for Retail** - Customers that have Dynamics 365 for Retail deployed will see a single tile that is a cumulative combined binary update of all the application and platform changes.</span></span> 

- <span data-ttu-id="07dad-132">**Dynamics 365 for Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="07dad-132">**Dynamics 365 for Finance and Operations**</span></span> 
   1. <span data-ttu-id="07dad-133">アプリケーションのバージョン 8.1 以降 - 今回のリリースから、サービス更新プログラムの **1 つのタイル**が表示されます。カスタマイズはすべて拡張機能を通じて行われ、コードのオーバーレイがないためです。</span><span class="sxs-lookup"><span data-stu-id="07dad-133">Application version 8.1 onwards - Starting with this release, you will see a **single tile** for service updates because any customizations are done via extensions and there is no code overlayering.</span></span> <span data-ttu-id="07dad-134">このタイルは、すべてのアプリケーションとプラットフォームの変更の結合された累積的バイナリ アップデートです。</span><span class="sxs-lookup"><span data-stu-id="07dad-134">This tile will be a cumulative combined binary update of all the application and platform changes.</span></span> <span data-ttu-id="07dad-135">今回のリリースから、細かい X++ 更新プログラムはなくなります。</span><span class="sxs-lookup"><span data-stu-id="07dad-135">There will be no granular X++ updates starting with this release.</span></span> <span data-ttu-id="07dad-136">すべてのものは累積的な更新になります。</span><span class="sxs-lookup"><span data-stu-id="07dad-136">Everything will be a cumulative update.</span></span> 
 
   2. <span data-ttu-id="07dad-137">プラットフォーム更新 4 以上を持つアプリケーションのバージョン 7.x または 8.0: この組み合わせを使用するユーザーには、上記の 4 つのタイルがすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-137">Application version 7.x or 8.0 with Platform update 4 or higher - For customers that are on this combination, you will see all the 4 tiles listed above.</span></span> <span data-ttu-id="07dad-138">今回のリリースでは、まだ細かい X++ 更新があります。</span><span class="sxs-lookup"><span data-stu-id="07dad-138">This release will still have the granular X++ updates.</span></span> <span data-ttu-id="07dad-139">プラットフォーム更新 4 以降、プラットフォーム モジュールではオーバーレイヤーが許可されません。つまり、**プラットフォーム バイナリ更新プログラム** タイルを使用して、累積的な更新としてプラットフォーム更新プログラムを提供できます。</span><span class="sxs-lookup"><span data-stu-id="07dad-139">Starting with Platform update 4, no overlayering is allowed on the platform modules, which means that the **Platform binary updates** tile is available to provide the platform updates as a cumulative update.</span></span> 

  3. <span data-ttu-id="07dad-140">プラットフォーム更新 3 以下を持つアプリケーション バージョン 7.x - この組み合わせを使用するユーザーには、3 つのタイル **すべての X++ 更新**、**重要な X++ 更新**、および **すべてのバイナリ更新プログラム** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-140">Application version 7.x with Platform update 3 or lower - For customers that are on this combination, you will see 3 tiles - **All X++ updates**, **Critical X++ updates**, and **All binary updates**.</span></span> <span data-ttu-id="07dad-141">このリリース プラットフォームは引き続きオーバーレイヤーされるため、**プラットフォーム バイナリ更新プログラム** タイルはありません。</span><span class="sxs-lookup"><span data-stu-id="07dad-141">Because this release platform can still be overlayered, there is no **Platform binary updatess** tile.</span></span> 
  > [!NOTE]
    > <span data-ttu-id="07dad-142">今回のリリースを使用している場合、できるだけ早くアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="07dad-142">If you are on this release, you need to upgrade as soon as possible.</span></span> 
   
## <a name="download-binary-updates"></a><span data-ttu-id="07dad-143">バイナリ更新プログラムのダウンロード</span><span class="sxs-lookup"><span data-stu-id="07dad-143">Download binary updates</span></span>

1. <span data-ttu-id="07dad-144">**すべてのバイナリ更新プログラム** タイルをクリックして、アプリケーションおよびプラットフォームのバイナリ アップデートの組み合わせリストを表示するか、またはプラットフォームのみのバイナリ アップデートのための**プラットフォーム バイナリ更新プログラム** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="07dad-144">Click the **All binary update** tile to view the combined list of application and platform binary updates, or click the **Platform binary updates** tile for platform only binary updates.</span></span> 

   ![バイナリ タイル](./media/BinaryUpdateTiles.jpg)

2. <span data-ttu-id="07dad-146">**バイナリ更新プログラム**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="07dad-146">On the **Binary updates** page, select **Save package**.</span></span>

   ![バイナリ パッケージの保存](./media/ReviewAndSaveBinaryPackage.jpg)

3. <span data-ttu-id="07dad-148">**更新プログラムの確認と保存**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="07dad-148">On the **Review and save updates** page, select **Save package**.</span></span>

![更新プログラムの確認と保存](./media/ReviewBinaryPackage.jpg)

4. <span data-ttu-id="07dad-150">**資産ライブラリへのパッケージの保存**スライダーで、**名前**および**説明**を入力し、**パッケージの保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07dad-150">On the **Save package to asset library** slider, enter the **Name** and **Description**, and click **Save package**.</span></span>

   ![資産ライブラリへのパッケージの保存](./media/SaveBinaryPackage.jpg)

5. <span data-ttu-id="07dad-152">**完了**をクリックし、環境ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="07dad-152">Click **Done** to return to environment page.</span></span>

   ![DoneSavingBinaryPackage](./media/DoneSavingBinaryPackage.jpg)
 
6. <span data-ttu-id="07dad-154">資産ライブラリに保存されているバイナリ パッケージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="07dad-154">You'll see the saved binary package in the asset library.</span></span> 

   ![ViewSavedBinaryPackageInAssetLibrary](./media/ViewSavedBinaryPackageInAssetLibrary.jpg)

## <a name="download-x-updates"></a><span data-ttu-id="07dad-156">ダウンロード X++ 更新プログラム</span><span class="sxs-lookup"><span data-stu-id="07dad-156">Download X++ updates</span></span>

1. <span data-ttu-id="07dad-157">**すべての X++ 更新プログラム** タイルをクリックして、使用可能なアプリケーションの更新の一覧を環境に表示するか、または実稼働環境への推奨アプリケーションの更新プログラムの**重要な X++ 更新プログラム**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="07dad-157">Click the **All X++ updates** tile to view the list of available application updates to an environment, or click the **Critical X++ updates** tile for recommended application updates to your production environment.</span></span> 

   ![アプリケーション X++ 更新タイル](./media/X++UpdateTiles.jpg)   
  
2. <span data-ttu-id="07dad-159">**更新プログラムの追加**ページで、該当するナレッジサポート技術情報 (KB) 番号を選択し、**追加**をクリックし、選択した KB を**ダウンロード パッケージ**に追加します。</span><span class="sxs-lookup"><span data-stu-id="07dad-159">On the **Add updates** page, select the applicable Knowledge Base (KB) numbers, and then click **Add** to add selected KBs to the **Download package**.</span></span>

    ![X++ の更新プログラムの追加](./media/AddX++Updates.jpg)

    > [!NOTE]
    > <span data-ttu-id="07dad-161">X++ の更新プログラムで、この時点で利用可能なすべての更新プログラムをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="07dad-161">For X++ updates, you can download all available updates at this point.</span></span> <span data-ttu-id="07dad-162">**すべて選択** をクリックして **追加** をクリックし、すべての KB を **ダウンロード パッケージ** に追加します。</span><span class="sxs-lookup"><span data-stu-id="07dad-162">Click **Select all**, and then click **Add** to add all KBs to  the **Download package**.</span></span>

3. <span data-ttu-id="07dad-163">**ダウンロード パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07dad-163">Select **Download package**.</span></span>

    ![ダウンロード X++ パッケージ](./media/DownloadX++UpdatePackage.jpg)

4. <span data-ttu-id="07dad-165">**修正プログラムの確認とダウンロード**ページで、選択した修正プログラムを確認したり、パッケージを破棄して、修正プログラムの選択に戻ったり、または最終修正プログラムのパッケージをダウンロードしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="07dad-165">On the **Review and download hotfixes** page, you can review the hotfixes that you selected, discard the package, return to the hotfix selections, or download the final hotfix package.</span></span>

    ![X++ 更新プログラムの確認とダウンロード](media/ReviewAndDownloadX++Package.jpg)
    
5. <span data-ttu-id="07dad-167">パッケージをダウンロードして**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07dad-167">Download the package, and click **Done**.</span></span>
    
    ![downloaded](media/X++UpdatesDownloadBegin.jpg)

## <a name="additional-resources"></a><span data-ttu-id="07dad-169">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="07dad-169">Additional resources</span></span>
- [<span data-ttu-id="07dad-170">クラウド環境への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="07dad-170">Apply updates to a cloud environment</span></span>](../deployment/apply-deployable-package-system.md)
- [<span data-ttu-id="07dad-171">メタデータ修正プログラムのインストール</span><span class="sxs-lookup"><span data-stu-id="07dad-171">Install a metadata hotfix</span></span>](./install-metadata-hotfix-package.md) 
