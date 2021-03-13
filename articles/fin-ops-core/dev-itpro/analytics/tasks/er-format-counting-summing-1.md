---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)
description: このトピックでは、既に生成されたテキスト出力のデータに基づいて棚卸および集計を行うために電子レポート形式を構成する方法について説明します。 (第 1 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3639b5ac28f8a571642e983906d658dabf05b1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093025"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="9f64d-104">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)</span><span class="sxs-lookup"><span data-stu-id="9f64d-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f64d-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="9f64d-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="9f64d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="9f64d-107">この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f64d-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="9f64d-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="9f64d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="9f64d-109">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="9f64d-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="9f64d-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9f64d-111">「Litware, Inc.」 であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9f64d-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="9f64d-112">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="9f64d-113">Litware, Inc. を選択します</span><span class="sxs-lookup"><span data-stu-id="9f64d-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="9f64d-114">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9f64d-114">provider.</span></span>
3. <span data-ttu-id="9f64d-115">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-115">Click Repositories.</span></span>
    * <span data-ttu-id="9f64d-116">「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="9f64d-117">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9f64d-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="9f64d-118">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="9f64d-119">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-119">Click Create repository.</span></span>
7. <span data-ttu-id="9f64d-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="9f64d-121">Microsoft 提供のイントラスタット コンフィギュレーションを取得する</span><span class="sxs-lookup"><span data-stu-id="9f64d-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="9f64d-122">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-122">Click Open.</span></span>
2. <span data-ttu-id="9f64d-123">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="9f64d-124">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-124">Click Import.</span></span>
    * <span data-ttu-id="9f64d-125">[選択した設定のバージョン1.1のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="9f64d-126">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-126">Click Yes.</span></span>
5. <span data-ttu-id="9f64d-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9f64d-127">Close the page.</span></span>
6. <span data-ttu-id="9f64d-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9f64d-128">Close the page.</span></span>
7. <span data-ttu-id="9f64d-129">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f64d-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="9f64d-130">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="9f64d-131">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f64d-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

