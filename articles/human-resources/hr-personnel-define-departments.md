---
title: 新しい部門の定義
description: 部門は、販売または会計など、事業の機能領域を表す作業単位です。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06b93e9b7bd4d68aa5d6f6c377991963e37579ae
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464407"
---
# <a name="define-new-departments"></a><span data-ttu-id="1ec08-103">新しい部門の定義</span><span class="sxs-lookup"><span data-stu-id="1ec08-103">Define new departments</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="1ec08-104">部門は、販売または会計など、事業の機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="1ec08-104">Departments are operating units that represent a functional area of a business, such as sales or accounting.</span></span> <span data-ttu-id="1ec08-105">多くの会社には、事業内のさまざまな部門を表示する組織階層があります。</span><span class="sxs-lookup"><span data-stu-id="1ec08-105">Many companies have organizational hierarchies that display the various departments within a business.</span></span> <span data-ttu-id="1ec08-106">この手順では、部門を作成し、作成した部門を組織内の部門階層に追加するプロセスを説明します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-106">This procedure walks through the process of creating departments, and adding those departments to an organizations departmental hierarchy.</span></span> <span data-ttu-id="1ec08-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="1ec08-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1ec08-108">[人事管理] > [部門] > [部門] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-108">Go to Human resources > Departments > Departments.</span></span>
2. <span data-ttu-id="1ec08-109">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1ec08-109">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="1ec08-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1ec08-111">例: プロジェクトの請求書作成</span><span class="sxs-lookup"><span data-stu-id="1ec08-111">Example: Project billing</span></span>  
4. <span data-ttu-id="1ec08-112">[メモ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-112">In the Memo field, type a value.</span></span>
    * <span data-ttu-id="1ec08-113">例: プロジェクトの請求書作成</span><span class="sxs-lookup"><span data-stu-id="1ec08-113">Example: Project billing</span></span>  
5. <span data-ttu-id="1ec08-114">[マネージャー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-114">In the Manager field, enter or select a value.</span></span>
    * <span data-ttu-id="1ec08-115">例: Jodi Christiansen</span><span class="sxs-lookup"><span data-stu-id="1ec08-115">Example: Jodi Christiansen</span></span>  
6. <span data-ttu-id="1ec08-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-116">Click Save.</span></span>
7. <span data-ttu-id="1ec08-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1ec08-117">Close the page.</span></span>
8. <span data-ttu-id="1ec08-118">[人事管理] > [部門] > [部門階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-118">Go to Human resources > Departments > Department hierarchy.</span></span>
9. <span data-ttu-id="1ec08-119">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-119">Click Edit.</span></span>
10. <span data-ttu-id="1ec08-120">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-120">Click Insert.</span></span>
11. <span data-ttu-id="1ec08-121">[部門] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-121">Click Department.</span></span>
12. <span data-ttu-id="1ec08-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ec08-123">例: プロジェクトの請求書作成</span><span class="sxs-lookup"><span data-stu-id="1ec08-123">Example: Project billing</span></span>  
13. <span data-ttu-id="1ec08-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-124">Click OK.</span></span>
14. <span data-ttu-id="1ec08-125">[発行] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ec08-125">Click Publish to open the drop dialog.</span></span>
15. <span data-ttu-id="1ec08-126">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-126">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="1ec08-127">部門の階層を公開する際、変更をいつ有効にするかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1ec08-127">When publishing the department hierarchy, you can select when to make the changes effective.</span></span> <span data-ttu-id="1ec08-128">変更を将来の日付にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1ec08-128">Changes can be future dated.</span></span> <span data-ttu-id="1ec08-129">たとえば、次の会計年度の期首に追加の部門を追加することがわかっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="1ec08-129">For example, you may know that at the beginning of your fiscal year you will be adding an additional department.</span></span> <span data-ttu-id="1ec08-130">会計年度の期首に有効日を設定すれば、階層の変更はその日付に有効になります。</span><span class="sxs-lookup"><span data-stu-id="1ec08-130">You can set your effective date to the beginning of the fiscal year, and the changes to the hierarchy will be effective on that date.</span></span>  
16. <span data-ttu-id="1ec08-131">[変更の説明] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ec08-131">In the Describe changes field, type a value.</span></span>
17. <span data-ttu-id="1ec08-132">[発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec08-132">Click Publish.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]