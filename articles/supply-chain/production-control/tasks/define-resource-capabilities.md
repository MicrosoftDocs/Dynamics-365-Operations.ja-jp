---
title: リソース能力の定義
description: リソースの能力は、リソースがどのような工程を行えるかを示します。
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0940883d0e9edf56e61b5ecd817062aac5e0f8a6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "340157"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="9bc17-103">リソース能力の定義</span><span class="sxs-lookup"><span data-stu-id="9bc17-103">Define resource capabilities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9bc17-104">リソースの能力は、リソースがどのような工程を行えるかを示します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="9bc17-105">スケジューリング中に、それぞれの職務や工程の要件と、利用可能なリソースの能力とを照合します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="9bc17-106">このタスク ガイドでは、能力の作成、およびリソースへの割り当て方法を確認できます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="9bc17-107">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9bc17-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="9bc17-108">リソース能力の作成</span><span class="sxs-lookup"><span data-stu-id="9bc17-108">Create a resource capability</span></span>
1. <span data-ttu-id="9bc17-109">[リソース能力] に移動します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="9bc17-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9bc17-110">Click New.</span></span>
3. <span data-ttu-id="9bc17-111">[能力] フィールドで、リソース能力の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="9bc17-112">ある工程について、能力 ID を使用すると、工程の実行にその能力を持つリソースが必要であることを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="9bc17-113">[説明] フィールドに、能力の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="9bc17-114">リソースへの能力の割り当て</span><span class="sxs-lookup"><span data-stu-id="9bc17-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="9bc17-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9bc17-115">Click Add.</span></span>
2. <span data-ttu-id="9bc17-116">[リソース] フィールドで、リソースの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="9bc17-117">リソースの能力は、1 つ以上のリソースに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="9bc17-118">[有効期限] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9bc17-119">限られた期間だけリソースに能力があることを指定する場合にも、このフィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="9bc17-120">[優先順位] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="9bc17-121">職務および工程をスケジュールするとき、優先順位によってリソースを選択するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="9bc17-122">これを選択し、かつ 2 つ以上のリソースが期日までに職務や工程を行うことができる場合、要求能力に応じて優先順位の最も低いリソースが選択されます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="9bc17-123">[レベル] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9bc17-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="9bc17-124">ジョブや工程が特定の機能を要求することを指定する場合は、必要な最低レベルを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="9bc17-125">能力レベルを使用すると、同じ職務を遂行することができるリソースについて、速度、強み、サイズなどの違いによる区別を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9bc17-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

