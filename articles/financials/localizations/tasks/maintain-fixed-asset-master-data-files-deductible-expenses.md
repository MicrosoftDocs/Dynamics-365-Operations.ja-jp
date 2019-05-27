---
title: 損金の固定資産マスター データ ファイルの管理
description: このタスクでは、損金の固定資産マスター データの保守を行います。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup,  AssetTable, AssetBook
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41d436194dfdf94cf8a3ad889e610e151fc35c90
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560999"
---
# <a name="maintain-fixed-asset-master-data-files-for-deductible-expenses"></a><span data-ttu-id="839fa-103">損金の固定資産マスター データ ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="839fa-103">Maintain fixed-asset master data files for deductible expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="839fa-104">このタスクでは、損金の固定資産マスター データの保守を行います。</span><span class="sxs-lookup"><span data-stu-id="839fa-104">This task walks you through maintaining fixed asset master data files for deductible expenses.</span></span>



<span data-ttu-id="839fa-105">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="839fa-105">This task was created using the demo data company JPMF.</span></span>


## <a name="setups-in-fixed-asset-groups"></a><span data-ttu-id="839fa-106">固定資産グループの設定</span><span class="sxs-lookup"><span data-stu-id="839fa-106">Setups in Fixed asset groups</span></span>
1. <span data-ttu-id="839fa-107">[固定資産] > [設定] > [固定資産グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="839fa-107">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="839fa-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-108">Click New.</span></span>
3. <span data-ttu-id="839fa-109">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="839fa-109">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="839fa-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="839fa-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="839fa-111">[固定資産の自動採番] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="839fa-111">Select Yes in the Autonumber fixed assets field.</span></span>
6. <span data-ttu-id="839fa-112">番号順序コードを選択して、固定資産番号を自動生成します。</span><span class="sxs-lookup"><span data-stu-id="839fa-112">Select a number sequence code to autogenerate the fixed asset number.</span></span>
7. <span data-ttu-id="839fa-113">新しい固定資産の既定の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="839fa-113">Select the default  location for new fixed assets.</span></span>
8. <span data-ttu-id="839fa-114">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-114">Click Books.</span></span>
9. <span data-ttu-id="839fa-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-115">Click New.</span></span>
10. <span data-ttu-id="839fa-116">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="839fa-116">In the Book field, type a value.</span></span>
    * <span data-ttu-id="839fa-117">例: 200RED_CUR</span><span class="sxs-lookup"><span data-stu-id="839fa-117">Example: 200RED_CUR</span></span>  
11. <span data-ttu-id="839fa-118">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="839fa-118">Expand the General section.</span></span>
    * <span data-ttu-id="839fa-119">オプションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="839fa-119">Configure the options.</span></span>  
    * <span data-ttu-id="839fa-120">各オプションの詳細については、他の情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="839fa-120">Refer other materials for the details of each of the options.</span></span>  
12. <span data-ttu-id="839fa-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-121">Click Save.</span></span>
13. <span data-ttu-id="839fa-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-122">Click New.</span></span>
14. <span data-ttu-id="839fa-123">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="839fa-123">In the Book field, type a value.</span></span>
    * <span data-ttu-id="839fa-124">例: 250NDB_TAX</span><span class="sxs-lookup"><span data-stu-id="839fa-124">Example: 250NDB_TAX</span></span>  
15. <span data-ttu-id="839fa-125">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="839fa-125">Expand the General section.</span></span>
    * <span data-ttu-id="839fa-126">オプションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="839fa-126">Configure the options.</span></span>  
    * <span data-ttu-id="839fa-127">各オプションの詳細については、他の情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="839fa-127">Refer other materials for the details of each of the options.</span></span>  
16. <span data-ttu-id="839fa-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-128">Click Save.</span></span>

## <a name="creation-of-fixed-asset"></a><span data-ttu-id="839fa-129">固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="839fa-129">Creation of Fixed asset</span></span>
1. <span data-ttu-id="839fa-130">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="839fa-130">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="839fa-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-131">Click New.</span></span>
3. <span data-ttu-id="839fa-132">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="839fa-132">In the Fixed asset group field, type a value.</span></span>
    * <span data-ttu-id="839fa-133">作成した固定資産グループを使用するか、BUIL-M を使用できます。</span><span class="sxs-lookup"><span data-stu-id="839fa-133">You can use the fixed asset group that you have just created, or you can use BUIL-M.</span></span>  
4. <span data-ttu-id="839fa-134">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="839fa-134">Click Books.</span></span>
    * <span data-ttu-id="839fa-135">帳簿が自動的に作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="839fa-135">Verify that the books were created automatically.</span></span>  

