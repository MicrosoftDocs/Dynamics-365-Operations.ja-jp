---
title: "Lifecycle Services から更新プログラムをダウンロード"
description: "このチュートリアルを使用して、Lifecycle Services (LCS) から Microsoft Dynamics 365 for Finance and Operations の 修正プログラムをダウンロードします。"
author: AngelMarshall
manager: AnnBe
ms.date: 02/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 56171
ms.assetid: 61069cf2-6c3f-4ebc-bbee-b21b1c99626a
ms.search.region: Global
ms.author: amarshall
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 490fd20aeb93d57f73d6c2a5362acb920e2b891e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="download-updates-from-lifecycle-services"></a><span data-ttu-id="2a2fd-103">Lifecycle Services から更新プログラムをダウンロード</span><span class="sxs-lookup"><span data-stu-id="2a2fd-103">Download updates from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a2fd-104">このチュートリアルを使用して、Microsoft Dynamics Lifecycle Services (LCS) から更新プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-104">Use this tutorial to download updates from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="types-of-updates"></a><span data-ttu-id="2a2fd-105">更新のタイプ</span><span class="sxs-lookup"><span data-stu-id="2a2fd-105">Types of updates</span></span>

- <span data-ttu-id="2a2fd-106">**バイナリ更新プログラム**は、コンパイル済みで累積されています。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-106">**Binary updates** are pre-compiled and cumulative.</span></span> <span data-ttu-id="2a2fd-107">その後のバイナリ更新には、これまでのすべての更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-107">Every subsequent binary update includes all previous updates.</span></span> <span data-ttu-id="2a2fd-108">これらの更新は、開発環境でコンパイルする必要はなく、LCS から非開発環境に直接適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-108">These updates don't have to be compiled in a development environment, and they can be applied directly to a non-development environment from LCS.</span></span>
        
    <span data-ttu-id="2a2fd-109">小売機能とカスタマイズされた販売時点管理 (POS) のインスタンスを持つ環境を実行している場合は、Retail SDK のパッケージに記載されている追加手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-109">If you're running an environment that has retail functionality and a customized instance of Cloud point of sale (POS), you must complete the additional steps that are listed under Retail SDK packaging.</span></span> <span data-ttu-id="2a2fd-110">Microsoft Dynamics 365 for Retail で、すべての更新プログラムは、アプリケーション モデルの更新プログラムでさえ、バイナリ更新プログラムとしてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-110">For Microsoft Dynamics 365 for Retail, all updates, even updates for application models, are released as binary updates.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2a2fd-111">環境がプラットフォーム更新プログラム 4 以上である場合、**すべてのバイナリ更新プログラム**および**プラットフォーム バイナリ更新プログラム**を LCS **環境**ページからダウンロードするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-111">If your environment is on Platform Update 4 and above, you will have the option to download **All binary updates** and **Platform binary updates** from the LCS **Environment** page.</span></span>  
    > - <span data-ttu-id="2a2fd-112">**すべてのバイナリ更新プログラム** タイルには、アプリケーションとプラットフォームのバイナリ アップデートのパッケージの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-112">The **All binary updates** tile includes a combined package of application and platform binary updates.</span></span>  
    > - <span data-ttu-id="2a2fd-113">**プラットフォーム バイナリの更新プログラム** タイルには、最新のプラットフォーム専用の更新プログラムまたは修正プログラムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-113">The **Platform binary updates** tile includes the latest platform only updates or hotfixes.</span></span> 
    

- <span data-ttu-id="2a2fd-114">**X++ 更新プログラム**には、アプリケーション モデルの特定のアプリケーション機能への更新が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-114">**X++ updates** include updates to specific application functionality in application models.</span></span> <span data-ttu-id="2a2fd-115">これらの更新は、個別にダウンロードして適用することができます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-115">These updates can be independently downloaded and applied.</span></span> <span data-ttu-id="2a2fd-116">環境に適用する特定の X++ 更新プログラムを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-116">You can select specific X++ updates to apply to your environment.</span></span>  <span data-ttu-id="2a2fd-117">依存 X++ 更新は自動的に選択され、ダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-117">Dependent X++ updates are automatically selected and downloaded.</span></span>  <span data-ttu-id="2a2fd-118">X++ の更新はソース コードの更新であり、非開発環境に適用する前に、開発環境でコンパイルして任意のカスタマイズとマージする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-118">Any X++ updates are source code updates, before they can be applied to a non-development environment, they must be compiled in a developer environment and merged with any customizations.</span></span> <span data-ttu-id="2a2fd-119">X++ の更新プログラムは Microsoft Dynamics 365 for Finance and Operations に対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-119">X++ updates apply only to Microsoft Dynamics 365 for Finance and Operations.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a2fd-120">オンライン環境では、**すべての X++ 更新プログラム**タイルおよび**重要な X++ 更新プログラム**タイルの両方を表示します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-120">For online environments, you will see both the **All X++ updates** tile and the **Critical X++ updates** tile.</span></span> <span data-ttu-id="2a2fd-121">重要な X++ 更新プログラムは、**実稼働環境**のテレメトリ データに基づく推奨 KB です。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-121">The Critical X++ updates are recommended KBs that are based on the telemetry data in **your production environment**.</span></span>  
    >
    > <span data-ttu-id="2a2fd-122">X++ 更新プログラムをテストして適用するには、X++ 更新プログラムをダウンロードした後で開発環境に適用して展開可能パッケージを作成し、展開可能パッケージをサンドボックスに適用してから実稼働環境に適用します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-122">To test and apply any X++ updates, after download the X++ updates, apply them in a development environment to build a deployable package, and then apply the deployable package to your sandbox and then production environments.</span></span> 
    >
    > <span data-ttu-id="2a2fd-123">更新の展開に関する詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="2a2fd-123">For more information about deploying updates, see [Apply updates to a cloud environment](../deployment/apply-deployable-package-system.md)</span></span>  

## <a name="download-updates"></a><span data-ttu-id="2a2fd-124">更新プログラムのダウンロード</span><span class="sxs-lookup"><span data-stu-id="2a2fd-124">Download updates</span></span>

<span data-ttu-id="2a2fd-125">利用可能な更新プログラムを表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-125">To view available updates:</span></span>
1. <span data-ttu-id="2a2fd-126">資格情報を使用して LCS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-126">Sign in to LCS by using your credentials.</span></span>
2. <span data-ttu-id="2a2fd-127">LCS プロジェクトで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-127">In the LCS project, select an environment.</span></span>
3. <span data-ttu-id="2a2fd-128">**環境**ページで、**監視**セクションには更新タイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-128">On the **Environment** page, the **Monitoring** section includes update tiles.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="2a2fd-129">Retail で、バイナリ更新プログラムのみに対するタイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-129">For Retail, you will see tile for binary updates only.</span></span> <span data-ttu-id="2a2fd-130">Finance and Operations で、X++ 更新およびバイナリ更新の両方に対するタイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-130">For Finance and Operations, you will see tiles for both X++ updates and binary updates.</span></span> <span data-ttu-id="2a2fd-131">これらの 2 種類の更新は、個別にダウンロードして適用することができます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-131">These two types of updates can be independently downloaded and applied.</span></span> <span data-ttu-id="2a2fd-132">ただし、一部の X++ 更新プログラムはバイナリ更新プログラムに依存し、別のバイナリ更新プログラムは X++ 更新プログラムに依存しています。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-132">However, some X++ updates might depend on binary updates, and some binary updates might depend on X++ updates.</span></span> <span data-ttu-id="2a2fd-133">すべての依存関係は、更新の説明に含まています。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-133">Any dependencies are included in the update description.</span></span>
   
## <a name="download-binary-updates"></a><span data-ttu-id="2a2fd-134">ダウンロード Binary 更新プログラム</span><span class="sxs-lookup"><span data-stu-id="2a2fd-134">Download Binary updates</span></span>

1. <span data-ttu-id="2a2fd-135">**すべてのバイナリ更新プログラム** タイルをクリックすると、アプリケーションおよびプラットフォームのバイナリ アップデートの組み合わせリスト、またはプラットフォームのみのバイナリ アップデートのための**プラットフォーム バイナリ更新プログラム** タイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-135">Click **All binary update** tile to view the combined list of application and platform binary updates, or **Platform binary updates** tile for platform only binary updates.</span></span> 

   ![バイナリ タイル](./media/BinaryUpdateTiles.jpg)

2. <span data-ttu-id="2a2fd-137">**バイナリ更新プログラム**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-137">On the **Binary Updates** page, select **Save Package**.</span></span>

   ![バイナリ パッケージの保存](./media/ReviewAndSaveBinaryPackage.jpg)

3. <span data-ttu-id="2a2fd-139">**更新プログラムの確認と保存**ページで、**パッケージの保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-139">On the **Review and Save Updates** page, select **Save package**.</span></span>

![更新プログラムの確認と保存](./media/ReviewBinaryPackage.jpg)

4. <span data-ttu-id="2a2fd-141">**資産ライブラリへのパッケージの保存**スライダーから、**名前**および**説明**を入力し、**パッケージの保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-141">From the **Save package to asset library** slider, enter the **Name** and **Description**, and click **Save package**.</span></span>

   ![資産ライブラリへのパッケージの保存](./media/SaveBinaryPackage.jpg)

5. <span data-ttu-id="2a2fd-143">**完了**をクリックし、環境ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-143">Click **Done** to return to environment page.</span></span>

   ![DoneSavingBinaryPackage](./media/DoneSavingBinaryPackage.jpg)
 
6. <span data-ttu-id="2a2fd-145">資産ライブラリに保存されているバイナリ パッケージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-145">You'll see the saved binary package in the asset library.</span></span> 

   ![ViewSavedBinaryPackageInAssetLibrary](./media/ViewSavedBinaryPackageInAssetLibrary.jpg)

## <a name="download-x-updates"></a><span data-ttu-id="2a2fd-147">ダウンロード X++ 更新プログラム</span><span class="sxs-lookup"><span data-stu-id="2a2fd-147">Download X++ updates</span></span>

1. <span data-ttu-id="2a2fd-148">**すべての X++ 更新プログラム** タイルをクリックすると、使用可能なアプリケーションの更新の一覧を環境に表示、または実稼働環境への推奨アプリケーションの更新プログラムの**重要な X++ 更新プログラム**を表示します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-148">Click on **All X++ updates** tile to view the list of available application updates to an environment, or **Critical X++ updates** for recommended application updates to your production environment.</span></span> 

   ![アプリケーション X++ 更新タイル](./media/X++UpdateTiles.jpg)   
  
2. <span data-ttu-id="2a2fd-150">**更新プログラムの追加**ページで、該当するナレッジサポート技術情報 (KB) 番号を選択し、**追加**をクリックし、選択した KB を**ダウンロード パッケージ**に追加します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-150">On the **Add updates** page, select the applicable Knowledge Base (KB) numbers, and then click **Add** to add selected KBs to the **Download package**.</span></span>

    ![X++ の更新プログラムの追加](./media/AddX++Updates.jpg)

    > [!NOTE]
    > <span data-ttu-id="2a2fd-152">X++ の更新プログラムで、この時点で利用可能なすべての更新プログラムをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-152">For X++ updates, you can download all available updates at this point.</span></span> <span data-ttu-id="2a2fd-153">**すべて選択** を選択して **追加** をクリックし、すべての KB を **ダウンロード パッケージ** に追加します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-153">Select **Select all**, and then click **Add** to add all KBs to  the **Download package**.</span></span>

3. <span data-ttu-id="2a2fd-154">**ダウンロード パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-154">Select **Download package**.</span></span>

    ![ダウンロード X++ パッケージ](./media/DownloadX++UpdatePackage.jpg)

4. <span data-ttu-id="2a2fd-156">**修正プログラムの確認とダウンロード**ページで、選択した修正プログラムを確認したり、パッケージを破棄して、修正プログラムの選択に戻ったり、または最終修正プログラムのパッケージをダウンロードしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-156">On the **Review and download hotfixes** page, you can review the hotfixes that you selected, discard the package, return to the hotfix selections, or download the final hotfix package.</span></span>

    ![X++ 更新プログラムの確認とダウンロード](media/ReviewAndDownloadX++Package.jpg)
    
5. <span data-ttu-id="2a2fd-158">パッケージをダウンロードして**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-158">Download the package, and click **Done**.</span></span>
    
    ![downloaded](media/X++UpdatesDownloadBegin.jpg)


## <a name="also-see"></a><span data-ttu-id="2a2fd-160">参照してください。</span><span class="sxs-lookup"><span data-stu-id="2a2fd-160">Also see</span></span>
- [<span data-ttu-id="2a2fd-161">クラウド環境への更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="2a2fd-161">Apply updates to a cloud environment</span></span>](../deployment/apply-deployable-package-system.md)
- [<span data-ttu-id="2a2fd-162">メタデータ修正プログラムのインストール</span><span class="sxs-lookup"><span data-stu-id="2a2fd-162">Install a metadata hotfix</span></span>](./install-metadata-hotfix-package.md) 

