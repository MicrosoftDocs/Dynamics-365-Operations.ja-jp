---
title: 製品コンフィギュレーション モデルへ式の制約の追加
description: この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920884"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="59f51-103">製品コンフィギュレーション モデルへ式の制約の追加</span><span class="sxs-lookup"><span data-stu-id="59f51-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59f51-104">この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="59f51-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="59f51-105">ユーザーが金属の前グリルを選択した場合は、コーナーの保護をスピーカーに適用する必要があることを義務付ける方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="59f51-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="59f51-106">その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="59f51-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="59f51-107">式の制約の作成</span><span class="sxs-lookup"><span data-stu-id="59f51-107">Create an expression constraint</span></span>

1. <span data-ttu-id="59f51-108">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="59f51-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="59f51-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="59f51-110">この例では、ハイエンド スピーカー モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="59f51-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="59f51-111">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="59f51-112">**制約** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="59f51-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="59f51-113">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-113">Select **Add**.</span></span>
7. <span data-ttu-id="59f51-114">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-114">Select **Create**.</span></span>
8. <span data-ttu-id="59f51-115">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59f51-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="59f51-116">式の入力</span><span class="sxs-lookup"><span data-stu-id="59f51-116">Enter expression</span></span>

1. <span data-ttu-id="59f51-117">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="59f51-118">この段階で、タスク記録のユーザー インターフェイスのロックを解除する場合、制約式の構築のため、IntelliSense と記号のリストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="59f51-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="59f51-119">**ConstraintBody** フィールドで、「Implies[FrontGrill=="Metal", CornerProtection] 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="59f51-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="59f51-120">この式ロジックの状態 : [前グリル] が金属の場合、角の保護オプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59f51-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="59f51-121">**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-121">Select **Validate**.</span></span>
    * <span data-ttu-id="59f51-122">検証機能は、制約式に対して実行され、構文エラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="59f51-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="59f51-123">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-123">Select **Close**.</span></span>
5. <span data-ttu-id="59f51-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59f51-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]