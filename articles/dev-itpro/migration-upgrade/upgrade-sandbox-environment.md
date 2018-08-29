---
title: "サンドボックス環境のアップグレード"
description: "このトピックでは、非実稼働サンドボックス環境またはスタンドアロン サンドボックス環境へのデータ アップグレードを実行する手順について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 03/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 269234
ms.assetid: feb8ca24-e86d-4101-b77f-c04137e176d0
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4b7f144f69348f7a11d7a11a533cf11dbfd508d1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="upgrade-sandbox-environments"></a><span data-ttu-id="3b661-103">サンドボックス環境のアップグレード</span><span class="sxs-lookup"><span data-stu-id="3b661-103">Upgrade sandbox environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b661-104">このトピックでは、標準またはプレミアの承認テスト (第 2 層または第 3 層) 以上のサンドボックス環境でデータ アップグレードを実行する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b661-104">This topic describes the steps for performing a data upgrade on a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher sandbox environment.</span></span>

<span data-ttu-id="3b661-105">一部の環境では、Microsoft サービス エンジニアリング チーム (DSE) がデータのアップグレードを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b661-105">In some environments, the Microsoft Service Engineering Team (DSE) will run the data upgrade for you.</span></span> <span data-ttu-id="3b661-106">詳細については、[Microsoft Dynamics 365 for Finance and Operations の最新の更新への移動の概要](upgrade-latest-update.md#scenario-3-upgrade-to-the-latest-application-release) で「エンド ツー エンドのアップグレード プロセス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-106">For more information, see the end-to-end upgrade process in [Overview of moving to the latest update of Microsoft Dynamics 365 for Finance and Operations](upgrade-latest-update.md#scenario-3-upgrade-to-the-latest-application-release).</span></span>

> [!NOTE]
> <span data-ttu-id="3b661-107">この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</span><span class="sxs-lookup"><span data-stu-id="3b661-107">In this article, we use the term *sandbox* to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b661-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="3b661-108">Prerequisites</span></span>

<span data-ttu-id="3b661-109">独立したソフトウェア ベンダー (ISV) からのカスタマイズやソリューションがある場合は、開始する前に [コード アップグレード](upgrade-latest-update.md#scenario-2-upgrade-your-custom-code) を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b661-109">If you have any customizations or any solutions from independent software vendors (ISVs), you must complete a [code upgrade](upgrade-latest-update.md#scenario-2-upgrade-your-custom-code) before you begin.</span></span> <span data-ttu-id="3b661-110">アップグレードされた配置可能なパッケージを、Microsoft Dynamics Lifecycle Services (LCS) のアセット ライブラリにも用意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b661-110">Your upgraded deployable packages must also be ready in your Asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3b661-111">サンド ボックス環境でアップグレードする前に、開発環境でデータのアップグレードを実行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3b661-111">We strongly recommend that you do the data upgrade in a development environment before you upgrade in a sandbox environment.</span></span> <span data-ttu-id="3b661-112">開発環境でプロセスを修正して再実行するほうが速いです。</span><span class="sxs-lookup"><span data-stu-id="3b661-112">It's much faster to make corrections and rerun the process in a development environment.</span></span> <span data-ttu-id="3b661-113">したがって、まず開発環境で作業することで、アップグレードに必要な全体的な時間を短縮できます。</span><span class="sxs-lookup"><span data-stu-id="3b661-113">Therefore, by working in a development environment first, you can reduce the overall time that is required for the upgrade.</span></span>

## <a name="export-the-database"></a><span data-ttu-id="3b661-114">データベースをエキスポート</span><span class="sxs-lookup"><span data-stu-id="3b661-114">Export the database</span></span>

<span data-ttu-id="3b661-115">Bacpac ファイルにアップグレードする既存のサンド ボックス環境から、データベースをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="3b661-115">Export the database from the existing sandbox environment that you want to upgrade to a bacpac file.</span></span> <span data-ttu-id="3b661-116">詳細については、[後から復元するため Finance and Operations データベースのコピー](../database/copy-operations-database.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-116">For more information, see [Copy a Finance and Operations database to restore later](../database/copy-operations-database.md).</span></span>

### <a name="additional-steps-for-management-reporter"></a><span data-ttu-id="3b661-117">Management Reporter 向け追加手順</span><span class="sxs-lookup"><span data-stu-id="3b661-117">Additional steps for Management Reporter</span></span>

<span data-ttu-id="3b661-118">レポート デザイナーからレポート定義、またはビルディング ブロック グループをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="3b661-118">Export your report definitions, or building block groups, from the Report designer.</span></span> <span data-ttu-id="3b661-119">エクスポートされたファイルを安全な場所に移動し、後でそのファイルを使用してレポート定義を再インポートできます。</span><span class="sxs-lookup"><span data-stu-id="3b661-119">Then move the exported file to a secure location, so that you can use the file later to reimport the report definitions.</span></span> <span data-ttu-id="3b661-120">詳細については、[レポート パーツ グループ](https://msdn.microsoft.com/en-us/library/dn464326.aspx#Exportabuildingblockgroup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-120">For more information, see [Building block group](https://msdn.microsoft.com/en-us/library/dn464326.aspx#Exportabuildingblockgroup).</span></span> <span data-ttu-id="3b661-121">エクスポートしたファイルを安全な場所にコピーまたはアップロードすることで、後に異なった環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b661-121">By copying or uploading the exported file to a secure location, you can import it into a different environment later.</span></span> <span data-ttu-id="3b661-122">詳細については、[Windows の AzCopy からデータの転送](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-122">For more information, see [Transfer data with the AzCopy on Windows](https://azure.microsoft.com/en-gb/documentation/articles/storage-use-azcopy/).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b661-123">Microsoft は、Microsoft Dynamics 365 for Finance and Operations の契約の一部としてストレージ アカウントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="3b661-123">Microsoft doesn't provide a storage account as part of your agreement for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3b661-124">ストレージ アカウントを購入するか、別の Microsoft Azure サブスクリプションからストレージ アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b661-124">You must either purchase a storage account or use a storage account from a separate Microsoft Azure subscription.</span></span>
>
> <span data-ttu-id="3b661-125">Azure 仮想マシン (VM) 上の D ドライブの動作に注意してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-125">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="3b661-126">エクスポートされたビルディング ブロック グループを失う可能性があるため、D ドライブに永続的に格納しようとしないでください。</span><span class="sxs-lookup"><span data-stu-id="3b661-126">Don't try to permanently store your exported building block groups on drive D, because you might lose them.</span></span> <span data-ttu-id="3b661-127">詳細については、[Windows Azure 仮想マシン上のテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-127">For more information, see the [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) blog post.</span></span>

## <a name="redeploy-the-sandbox-environment"></a><span data-ttu-id="3b661-128">サンドボックス環境を再配置</span><span class="sxs-lookup"><span data-stu-id="3b661-128">Redeploy the sandbox environment</span></span>

<span data-ttu-id="3b661-129">LCS 実装プロジェクトでは、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3b661-129">In your LCS implementation project, follow these steps.</span></span>

1. <span data-ttu-id="3b661-130">アップグレードするサンドボックス環境を検索し、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="3b661-130">Find the sandbox environment that you want to upgrade, and delete it.</span></span>

    1. <span data-ttu-id="3b661-131">**環境**ページで、**割り当て解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b661-131">On the **Environment** page, select **Deallocate**.</span></span> <span data-ttu-id="3b661-132">数分後、環境ステータスは、**解除**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3b661-132">After a few minutes, the environment status is updated to **Deallocated**.</span></span>
    2. <span data-ttu-id="3b661-133">**削除** を選択し、環境の名前を入力して削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="3b661-133">Select **Delete**, and then enter the environment name to confirm deletion.</span></span> <span data-ttu-id="3b661-134">数分後、環境が削除されます。</span><span class="sxs-lookup"><span data-stu-id="3b661-134">After a few minutes, the environment is deleted.</span></span>

2. <span data-ttu-id="3b661-135">主要な LCS プロジェクト ページの、**環境**セクションで、削除された環境に配置を要求するためのオプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="3b661-135">On the main LCS project page, in the **Environments** section, the deleted environment shows options for requesting a deployment.</span></span> <span data-ttu-id="3b661-136">オプションを選択し、環境に展開する新しいバージョンを要求します。</span><span class="sxs-lookup"><span data-stu-id="3b661-136">Select an option, and request that a new version be deployed in the environment.</span></span> <span data-ttu-id="3b661-137">環境に配置する必要があるパッケージとして、アセット ライブラリ内のアップグレードされたカスタム配置可能なパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b661-137">Select the upgraded custom deployable packages in your Asset library as the packages that should be deployed in the environment.</span></span>

## <a name="import-the-database"></a><span data-ttu-id="3b661-138">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="3b661-138">Import the database</span></span>

<span data-ttu-id="3b661-139">新しく再配置されたサンドボックス環境に bacpac ファイルからデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="3b661-139">Import the database from a bacpac file into the newly redeployed sandbox environment.</span></span> <span data-ttu-id="3b661-140">詳細については、[後から復元するため Finance and Operations データベースのコピー](../database/copy-operations-database.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b661-140">For more information, see [Copy a Finance and Operations database to restore later](../database/copy-operations-database.md).</span></span>

## <a name="run-the-data-upgrade-package"></a><span data-ttu-id="3b661-141">データ アップグレード パッケージを実行</span><span class="sxs-lookup"><span data-stu-id="3b661-141">Run the data upgrade package</span></span>

<span data-ttu-id="3b661-142">[開発、デモ、またはサンドボックス環境でのデータのアップグレード](upgrade-data-to-latest-update.md) の手順に従って、データ アップグレードの配置可能パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="3b661-142">Run the data upgrade by following the steps in [Upgrade data in development, demo or sandbox environments](upgrade-data-to-latest-update.md).</span></span>


## <a name="deploy-retail-customizations"></a><span data-ttu-id="3b661-143">小売りのカスタマイズを展開する</span><span class="sxs-lookup"><span data-stu-id="3b661-143">Deploy retail customizations</span></span> 

<span data-ttu-id="3b661-144">お客様の環境で、小売チャネル コンポーネントのカスタマイズが必要である場合、データ アップグレード パッケージを実行した後、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)の手順に従って、小売の結合された配置可能パッケージを再適用します。</span><span class="sxs-lookup"><span data-stu-id="3b661-144">If your environment requires customizations for retail channel components, after you run the data upgrade package, follow the steps in [Apply updates to a cloud environment](../deployment/apply-deployable-package-system.md) to re-apply your retail combined deployable package.</span></span>

## <a name="update-additional-components"></a><span data-ttu-id="3b661-145">追加コンポーネントの更新</span><span class="sxs-lookup"><span data-stu-id="3b661-145">Update additional components</span></span>

<span data-ttu-id="3b661-146">追加のコンポーネントが環境で使用される場合は、それらをアップグレードする追加手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b661-146">If any additional components are used in your environment, you might have to complete additional steps to upgrade them.</span></span>

### <a name="additional-steps-for-management-reporter"></a><span data-ttu-id="3b661-147">Management Reporter 向け追加手順</span><span class="sxs-lookup"><span data-stu-id="3b661-147">Additional steps for Management Reporter</span></span>

<span data-ttu-id="3b661-148">「[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)」の手順に従って、Management Reporter データベースをリセットします。</span><span class="sxs-lookup"><span data-stu-id="3b661-148">Reset the Management Reporter database by following the steps in [Resetting the financial reporting data mart after restoring a database](../analytics/reset-financial-reporting-datamart-after-restore.md).</span></span> <span data-ttu-id="3b661-149">その後、以前にエクスポートしたビルディング ブロック グループを再度インポートします。</span><span class="sxs-lookup"><span data-stu-id="3b661-149">Then reimport the building block groups that you exported earlier.</span></span>

## <a name="limitations"></a><span data-ttu-id="3b661-150">制限</span><span class="sxs-lookup"><span data-stu-id="3b661-150">Limitations</span></span>

<span data-ttu-id="3b661-151">更新プロセス中に、Azure Blob Storage に保存されている既存のドキュメント処理のドキュメントは失われます。</span><span class="sxs-lookup"><span data-stu-id="3b661-151">During this upgrade process, you will lose any existing document handling documents that are stored in Azure blob storage.</span></span> <span data-ttu-id="3b661-152">(サンドボックスデータベースをインポートすると、ドキュメントは持ち越されません。) X++ **FileUpload** クラスを使用して BLOB ストレージにドキュメントを配置するカスタムコードがある場合、それらのドキュメントも失われます。</span><span class="sxs-lookup"><span data-stu-id="3b661-152">(When a sandbox database is imported, the documents aren't brought over.) If you have custom code that uses the X++ **FileUpload** class to put documents in blob storage, you will also lose those documents.</span></span>

