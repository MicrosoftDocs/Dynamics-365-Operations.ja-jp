--- 
title: "電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するためのデータ モデルを準備する"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96195003c209c56c7ea4cbfec2f3543eb68453ff
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="b4a08-103">電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するためのデータ モデルを準備する</span><span class="sxs-lookup"><span data-stu-id="b4a08-103">Prepare data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4a08-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b4a08-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="b4a08-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b4a08-106">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4a08-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="b4a08-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="b4a08-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="b4a08-108">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="b4a08-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b4a08-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b4a08-110">「Litware, Inc.」を確認します</span><span class="sxs-lookup"><span data-stu-id="b4a08-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="b4a08-111">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b4a08-112">「Litware, Inc.」を選択します</span><span class="sxs-lookup"><span data-stu-id="b4a08-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="b4a08-113">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b4a08-113">provider.</span></span>
3. <span data-ttu-id="b4a08-114">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-114">Click Repositories.</span></span>
    * <span data-ttu-id="b4a08-115">「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="b4a08-116">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="b4a08-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="b4a08-117">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="b4a08-118">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-118">Click Create repository.</span></span>
7. <span data-ttu-id="b4a08-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="b4a08-120">Microsoftが提供する顧客請求書モデル設定を取得する</span><span class="sxs-lookup"><span data-stu-id="b4a08-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b4a08-121">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-121">Click Show filters.</span></span>
2. <span data-ttu-id="b4a08-122">次のフィルターを適用します: 「フィルターオペレーターから始める」を使用して、「名称」フィールドに「運営リソース」のフィルター値を入力します。「フィルターオペレーターから始める」を使用して、「説明」フィールドにフィルター値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="b4a08-123">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-123">Click Show filters.</span></span>
4. <span data-ttu-id="b4a08-124">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-124">Click Open.</span></span>
5. <span data-ttu-id="b4a08-125">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="b4a08-126">モデル設定「顧客請求書モデル」を選択し、インポートします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="b4a08-127">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-127">Click Import.</span></span>
    * <span data-ttu-id="b4a08-128">[選択した設定のバージョン 1 のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="b4a08-129">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-129">Click Yes.</span></span>
8. <span data-ttu-id="b4a08-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4a08-130">Close the page.</span></span>
9. <span data-ttu-id="b4a08-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4a08-131">Close the page.</span></span>
10. <span data-ttu-id="b4a08-132">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="b4a08-133">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="b4a08-134">ドキュメント管理のファイルへのアクセスをサポートするために取得したモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="b4a08-135">Microsoft 提供の設定から取得した顧客請求書モデルの設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="b4a08-136">この設定を使用してドキュメント管理のファイルにアクセスし、このモデルに基づいて作成する電子ドキュメント用にそれらのファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="b4a08-137">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4a08-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b4a08-138">[新規] フィールドで、「名称から取得: 顧客請求書モデル、Microsoft」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="b4a08-139">[名称] フィールドに、「顧客請求書モデル（カスタム）」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4a08-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="b4a08-140">顧客請求書モデル（カスタム）</span><span class="sxs-lookup"><span data-stu-id="b4a08-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="b4a08-141">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4a08-141">Click Create configuration.</span></span>

