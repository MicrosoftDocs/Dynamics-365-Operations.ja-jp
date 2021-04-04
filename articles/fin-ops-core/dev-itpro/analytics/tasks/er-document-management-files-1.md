---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 1 部 - データ モデルの準備)
description: このトピックでは、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 1 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35bffd6d3688a9887fcdaf4edbd89c344cb9b18d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559800"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="10404-104">ER ドキュメント管理ファイルを形式出力で使用する (第 1 部 - データ モデルの準備)</span><span class="sxs-lookup"><span data-stu-id="10404-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10404-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="10404-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="10404-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="10404-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="10404-107">この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10404-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="10404-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="10404-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="10404-109">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="10404-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="10404-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="10404-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="10404-111">「Litware, Inc.」を確認します</span><span class="sxs-lookup"><span data-stu-id="10404-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="10404-112">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="10404-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="10404-113">「Litware, Inc.」を選択します</span><span class="sxs-lookup"><span data-stu-id="10404-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="10404-114">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="10404-114">provider.</span></span>
3. <span data-ttu-id="10404-115">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-115">Click Repositories.</span></span>

    <span data-ttu-id="10404-116">「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="10404-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="10404-117">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="10404-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="10404-118">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="10404-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="10404-119">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-119">Click Create repository.</span></span>
7. <span data-ttu-id="10404-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="10404-121">Microsoftが提供する顧客請求書モデル設定を取得する</span><span class="sxs-lookup"><span data-stu-id="10404-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="10404-122">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-122">Click Show filters.</span></span>
2. <span data-ttu-id="10404-123">次のフィルターを適用します: 「フィルターオペレーターから始める」を使用して、「名称」フィールドに「運営リソース」のフィルター値を入力します。「フィルターオペレーターから始める」を使用して、「説明」フィールドにフィルター値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10404-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="10404-124">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-124">Click Show filters.</span></span>
4. <span data-ttu-id="10404-125">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-125">Click Open.</span></span>
5. <span data-ttu-id="10404-126">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="10404-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="10404-127">モデル設定「顧客請求書モデル」を選択し、インポートします。</span><span class="sxs-lookup"><span data-stu-id="10404-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="10404-128">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-128">Click Import.</span></span>

    <span data-ttu-id="10404-129">[選択した設定のバージョン 1 のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="10404-130">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-130">Click Yes.</span></span>
8. <span data-ttu-id="10404-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="10404-131">Close the page.</span></span>
9. <span data-ttu-id="10404-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="10404-132">Close the page.</span></span>
10. <span data-ttu-id="10404-133">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="10404-134">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="10404-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="10404-135">ドキュメント管理のファイルへのアクセスをサポートするために取得したモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="10404-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="10404-136">Microsoft 提供の設定から取得した顧客請求書モデルの設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="10404-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="10404-137">この設定を使用してドキュメント管理のファイルにアクセスし、このモデルに基づいて作成する電子ドキュメント用にそれらのファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="10404-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="10404-138">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="10404-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="10404-139">[新規] フィールドで、「名称から取得: 顧客請求書モデル、Microsoft」を入力します。</span><span class="sxs-lookup"><span data-stu-id="10404-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="10404-140">[名称] フィールドに、「顧客請求書モデル（カスタム）」を入力します。</span><span class="sxs-lookup"><span data-stu-id="10404-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="10404-141">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10404-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]