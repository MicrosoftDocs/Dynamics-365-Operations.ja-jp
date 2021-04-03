---
title: 職位の報告関係の修正
description: この手順は、従業員に対して報告関係を変更する方法を示します。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465393"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="b9144-103">職位の報告関係の修正</span><span class="sxs-lookup"><span data-stu-id="b9144-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="b9144-104">この手順は、従業員に対して報告関係を変更する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b9144-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="b9144-105">報告関係は、ワークフローを通してドキュメントを回覧するときに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9144-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="b9144-106">手順は、追加の階層に従業員を割り当てる方法も示します。</span><span class="sxs-lookup"><span data-stu-id="b9144-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="b9144-107">たとえば、従業員がプロジェクトの監修者への非公式の報告関係を伴うプロジェクト・チームの一員である場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9144-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="b9144-108">追加の報告関係は、さまざまなプロジェクトまたはマトリックスのシナリオに対応する職位に定義できます。</span><span class="sxs-lookup"><span data-stu-id="b9144-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="b9144-109">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b9144-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b9144-110">[人事管理] > [職位] > [職位] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9144-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="b9144-111">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="b9144-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b9144-112">たとえば、「000091」という値を含む [職位] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b9144-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="b9144-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9144-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b9144-114">[報告先職位] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b9144-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="b9144-115">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b9144-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="b9144-116">[報告先職位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9144-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="b9144-117">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9144-117">Click Create.</span></span>
8. <span data-ttu-id="b9144-118">[リレーションシップ] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b9144-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="b9144-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9144-119">Click Add.</span></span>
10. <span data-ttu-id="b9144-120">グリッドの左にあるチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b9144-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="b9144-121">[階層名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9144-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="b9144-122">例 : プロジェクト</span><span class="sxs-lookup"><span data-stu-id="b9144-122">Example: Project</span></span>  
12. <span data-ttu-id="b9144-123">[報告先職位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9144-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="b9144-124">例: 000437</span><span class="sxs-lookup"><span data-stu-id="b9144-124">Example:  000437</span></span>
13. <span data-ttu-id="b9144-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9144-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]