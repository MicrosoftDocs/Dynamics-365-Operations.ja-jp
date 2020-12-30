---
title: 職位の報告関係の修正
description: この手順は、従業員に対して報告関係を変更する方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae8ca5b20f331709e9fc1d9ae3b5f350e5c19ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419387"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="4647c-103">職位の報告関係の修正</span><span class="sxs-lookup"><span data-stu-id="4647c-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="4647c-104">この手順は、従業員に対して報告関係を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4647c-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="4647c-105">報告関係は、ワークフローを通してドキュメントを回覧するときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="4647c-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="4647c-106">手順は、追加の階層に従業員を割り当てる方法も示します。</span><span class="sxs-lookup"><span data-stu-id="4647c-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="4647c-107">たとえば、従業員がプロジェクトの監修者への非公式の報告関係を伴うプロジェクト・チームの一員である場合があります。</span><span class="sxs-lookup"><span data-stu-id="4647c-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="4647c-108">追加の報告関係は、さまざまなプロジェクトまたはマトリックスのシナリオに対応する職位に定義できます。</span><span class="sxs-lookup"><span data-stu-id="4647c-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="4647c-109">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="4647c-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4647c-110">[人事管理] > [職位] > [職位] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4647c-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="4647c-111">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="4647c-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4647c-112">たとえば、「000091」という値を含む [職位] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="4647c-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="4647c-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4647c-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4647c-114">[報告先職位] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="4647c-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="4647c-115">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4647c-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="4647c-116">[報告先職位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4647c-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="4647c-117">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4647c-117">Click Create.</span></span>
8. <span data-ttu-id="4647c-118">[リレーションシップ] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="4647c-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="4647c-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4647c-119">Click Add.</span></span>
10. <span data-ttu-id="4647c-120">グリッドの左にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4647c-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="4647c-121">[階層名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4647c-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="4647c-122">例 : プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4647c-122">Example: Project</span></span>  
12. <span data-ttu-id="4647c-123">[報告先職位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4647c-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="4647c-124">例: 000437</span><span class="sxs-lookup"><span data-stu-id="4647c-124">Example:  000437</span></span>
13. <span data-ttu-id="4647c-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4647c-125">Click Save.</span></span>

