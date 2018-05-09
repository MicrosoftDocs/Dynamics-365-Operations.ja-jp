--- 
title: "大量採用プロジェクトの作成"
description: "この手順では、大量雇用プロジェクトを設定するプロセスについて説明します。"
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3ec4f8a998364998909171564135ab6133b301b9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="8ddc1-103">大量採用プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8ddc1-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ddc1-104">この手順では、大量雇用プロジェクトを設定するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="8ddc1-105">リクルーターは大量雇用プロジェクトを使用して、簡単に複数の職位を作成し、多数の作業者をこれらの職位に採用することができます。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="8ddc1-106">この手順を開始するには、[人事管理] > [採用] > [大量雇用プロジェクト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="8ddc1-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8ddc1-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-108">Click New.</span></span>
2. <span data-ttu-id="8ddc1-109">[大量雇用プロジェクト] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="8ddc1-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="8ddc1-111">[プロジェクト開始] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="8ddc1-112">[プロジェクト終了] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="8ddc1-113">[プロジェクトを開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-113">Click Open project.</span></span>
7. <span data-ttu-id="8ddc1-114">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-114">Click Yes.</span></span>
8. <span data-ttu-id="8ddc1-115">[職位を開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-115">Click Create positions.</span></span>
9. <span data-ttu-id="8ddc1-116">[数量] フィールドに、作成する職位の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="8ddc1-117">開始日は、新しい作業者の採用日付になります。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="8ddc1-118">終了日は、新しい作業者の退職日になります。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="8ddc1-119">新しい作業者が従業員または契約者かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="8ddc1-120">[ジョブ] フィールドで、ドロップ ダウン ボタンをクリックして、職位を作成するジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="8ddc1-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8ddc1-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ddc1-123">既定のフルタイム相当値は、選択したジョブから取得されます。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="8ddc1-124">必要に応じて手動でこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="8ddc1-125">必要に応じて、新しい職位の [部門] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="8ddc1-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ddc1-126">Click OK.</span></span>


