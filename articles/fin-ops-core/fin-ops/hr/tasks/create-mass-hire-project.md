---
title: 大量採用プロジェクトの作成
description: この手順では、大量雇用プロジェクトを設定するプロセスについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea0f4638a968d2aecf4e3bb27acbd19e6455a8b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190629"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="3ee94-103">大量採用プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="3ee94-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ee94-104">この手順では、大量雇用プロジェクトを設定するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="3ee94-105">リクルーターは大量雇用プロジェクトを使用して、簡単に複数の職位を作成し、多数の作業者をこれらの職位に採用することができます。</span><span class="sxs-lookup"><span data-stu-id="3ee94-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="3ee94-106">この手順を開始するには、[人事管理] > [採用] > [大量雇用プロジェクト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="3ee94-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="3ee94-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3ee94-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-108">Click New.</span></span>
2. <span data-ttu-id="3ee94-109">[大量雇用プロジェクト] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="3ee94-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="3ee94-111">[プロジェクト開始] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="3ee94-112">[プロジェクト終了] フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="3ee94-113">[プロジェクトを開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-113">Click Open project.</span></span>
7. <span data-ttu-id="3ee94-114">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-114">Click Yes.</span></span>
8. <span data-ttu-id="3ee94-115">[職位を開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-115">Click Create positions.</span></span>
9. <span data-ttu-id="3ee94-116">[数量] フィールドに、作成する職位の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="3ee94-117">開始日は、新しい作業者の採用日付になります。</span><span class="sxs-lookup"><span data-stu-id="3ee94-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="3ee94-118">終了日は、新しい作業者の退職日になります。</span><span class="sxs-lookup"><span data-stu-id="3ee94-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="3ee94-119">新しい作業者が従業員または契約者かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="3ee94-120">[ジョブ] フィールドで、ドロップ ダウン ボタンをクリックして、職位を作成するジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="3ee94-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="3ee94-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ee94-123">既定のフルタイム相当値は、選択したジョブから取得されます。</span><span class="sxs-lookup"><span data-stu-id="3ee94-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="3ee94-124">必要に応じて手動でこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3ee94-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="3ee94-125">必要に応じて、新しい職位の [部門] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ee94-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="3ee94-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3ee94-126">Click OK.</span></span>

