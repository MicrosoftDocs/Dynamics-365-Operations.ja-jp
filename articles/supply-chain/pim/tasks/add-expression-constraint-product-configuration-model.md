---
title: 製品コンフィギュレーション モデルへ式の制約の追加
description: この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547151"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="e9868-103">製品コンフィギュレーション モデルへ式の制約の追加</span><span class="sxs-lookup"><span data-stu-id="e9868-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9868-104">この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="e9868-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="e9868-105">ユーザーが金属の前グリルを選択した場合は、コーナーの保護をスピーカーに適用する必要があることを義務付ける方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="e9868-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="e9868-106">その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9868-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="e9868-107">式の制約の作成</span><span class="sxs-lookup"><span data-stu-id="e9868-107">Create an expression constraint</span></span>
1. <span data-ttu-id="e9868-108">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="e9868-109">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="e9868-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e9868-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e9868-111">この例では、ハイエンド スピーカー モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9868-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="e9868-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e9868-113">[制約] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e9868-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="e9868-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-114">Click Add.</span></span>
7. <span data-ttu-id="e9868-115">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-115">Click Create.</span></span>
8. <span data-ttu-id="e9868-116">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9868-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="e9868-117">式の入力</span><span class="sxs-lookup"><span data-stu-id="e9868-117">Enter expression</span></span>
1. <span data-ttu-id="e9868-118">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-118">Click Edit expression.</span></span>
    * <span data-ttu-id="e9868-119">この段階で、タスク記録のユーザー インターフェイスのロックを解除する場合、制約式の構築のため、IntelliSense と記号のリストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9868-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="e9868-120">ConstraintBody フィールドで、「Implies[FrontGrill=="Metal", CornerProtection]」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e9868-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="e9868-121">この式ロジックの状態 : [前グリル] が金属の場合、角の保護オプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9868-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="e9868-122">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-122">Click Validate.</span></span>
    * <span data-ttu-id="e9868-123">検証機能は、制約式に対して実行され、構文エラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9868-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="e9868-124">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-124">Click Close.</span></span>
5. <span data-ttu-id="e9868-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9868-125">Click OK.</span></span>

