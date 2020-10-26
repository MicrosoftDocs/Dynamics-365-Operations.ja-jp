---
title: 新しい製品の作成
description: このトピックでは、新しい共有製品の作成方法を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a4745fe4fc44f85bcfd388ee573f5a6d0cd8519
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986171"
---
# <a name="create-a-new-product"></a><span data-ttu-id="258e3-103">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="258e3-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="258e3-104">このトピックでは、新しい共有製品の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="258e3-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="258e3-105">これは通常、製品デザイナーが実行します。</span><span class="sxs-lookup"><span data-stu-id="258e3-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="258e3-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="258e3-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="258e3-107">製品の作成</span><span class="sxs-lookup"><span data-stu-id="258e3-107">Create a product</span></span>
1. <span data-ttu-id="258e3-108">ナビゲーション ウィンドウで、**モジュール > 製品情報管理 > 製品 > 製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="258e3-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="258e3-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="258e3-109">Select **New**.</span></span>
3. <span data-ttu-id="258e3-110">**製品番号**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="258e3-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="258e3-111">番号順序が製品番号に対して設定されていない場合は、手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="258e3-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="258e3-112">**製品名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="258e3-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="258e3-113">製品名が検索名の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="258e3-113">The product name defaults to the search name.</span></span> <span data-ttu-id="258e3-114">必要に応じて手動でこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="258e3-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="258e3-115">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="258e3-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="258e3-116">分析コード グループの設定</span><span class="sxs-lookup"><span data-stu-id="258e3-116">Set up dimension groups</span></span>
1. <span data-ttu-id="258e3-117">**分析コード グループ**を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="258e3-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="258e3-118">**保管分析コード グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="258e3-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="258e3-119">保管分析コード グループにより、製品の各トランザクションに入力する必要がある保管分析コードと、在庫で追跡される方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="258e3-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="258e3-120">**追跡用分析コード グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="258e3-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="258e3-121">追跡用分析コード グループにより、製品の各トランザクションに入力する必要がある追跡用分析コードと、在庫で処理される方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="258e3-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="258e3-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="258e3-122">Select **OK**.</span></span>

