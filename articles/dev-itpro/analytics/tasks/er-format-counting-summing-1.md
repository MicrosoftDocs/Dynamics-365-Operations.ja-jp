--- 
title: "棚卸および集計を行うための形式を作成する"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7613b78d4a9ab63f5be9773a8699fe3ed94636eb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="3afad-103">棚卸および集計を行うための形式を作成する</span><span class="sxs-lookup"><span data-stu-id="3afad-103">Create format for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3afad-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。</span><span class="sxs-lookup"><span data-stu-id="3afad-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3afad-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="3afad-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3afad-106">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3afad-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="3afad-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="3afad-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="3afad-108">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="3afad-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="3afad-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3afad-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="3afad-110">Litware, Inc. を確認します</span><span class="sxs-lookup"><span data-stu-id="3afad-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="3afad-111">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3afad-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="3afad-112">Litware, Inc. を選択します</span><span class="sxs-lookup"><span data-stu-id="3afad-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="3afad-113">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3afad-113">provider.</span></span>
3. <span data-ttu-id="3afad-114">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-114">Click Repositories.</span></span>
    * <span data-ttu-id="3afad-115">「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="3afad-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="3afad-116">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="3afad-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="3afad-117">[設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3afad-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="3afad-118">[リポジトリの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-118">Click Create repository.</span></span>
7. <span data-ttu-id="3afad-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="3afad-120">Microsoft 提供のイントラスタット コンフィギュレーションを取得する</span><span class="sxs-lookup"><span data-stu-id="3afad-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="3afad-121">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-121">Click Open.</span></span>
2. <span data-ttu-id="3afad-122">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="3afad-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="3afad-123">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-123">Click Import.</span></span>
    * <span data-ttu-id="3afad-124">[選択した設定のバージョン1.1のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="3afad-125">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-125">Click Yes.</span></span>
5. <span data-ttu-id="3afad-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3afad-126">Close the page.</span></span>
6. <span data-ttu-id="3afad-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3afad-127">Close the page.</span></span>
7. <span data-ttu-id="3afad-128">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3afad-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="3afad-129">ツリーで、「Intrastat model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="3afad-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="3afad-130">ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。</span><span class="sxs-lookup"><span data-stu-id="3afad-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


