---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141928"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="6f393-103">ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)</span><span class="sxs-lookup"><span data-stu-id="6f393-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f393-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="6f393-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6f393-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="6f393-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6f393-106">この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f393-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="6f393-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="6f393-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="6f393-108">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="6f393-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6f393-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f393-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6f393-110">「Litware, Inc.」 であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6f393-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="6f393-111">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f393-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="6f393-112">Litware, Inc. を選択します</span><span class="sxs-lookup"><span data-stu-id="6f393-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="6f393-113">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6f393-113">provider.</span></span>
3. <span data-ttu-id="6f393-114">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-114">Click Repositories.</span></span>
    * <span data-ttu-id="6f393-115">「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="6f393-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="6f393-116">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f393-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="6f393-117">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="6f393-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="6f393-118">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-118">Click Create repository.</span></span>
7. <span data-ttu-id="6f393-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="6f393-120">Microsoft 提供のイントラスタット コンフィギュレーションを取得する</span><span class="sxs-lookup"><span data-stu-id="6f393-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6f393-121">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-121">Click Open.</span></span>
2. <span data-ttu-id="6f393-122">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f393-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="6f393-123">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-123">Click Import.</span></span>
    * <span data-ttu-id="6f393-124">[選択した設定のバージョン1.1のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="6f393-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-125">Click Yes.</span></span>
5. <span data-ttu-id="6f393-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f393-126">Close the page.</span></span>
6. <span data-ttu-id="6f393-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f393-127">Close the page.</span></span>
7. <span data-ttu-id="6f393-128">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f393-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="6f393-129">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="6f393-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="6f393-130">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f393-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

