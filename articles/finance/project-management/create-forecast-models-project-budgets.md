---
title: プロジェクト予算の予測モデルを作成
description: このトピックでは、残っている予算の予測モデルを作成する方法について説明します。
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321782"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="c143b-103">プロジェクト予算の予測モデルを作成</span><span class="sxs-lookup"><span data-stu-id="c143b-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c143b-104">このトピックでは、残っている予算の予測モデルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c143b-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="c143b-105">予算管理の対象となるプロジェクトでは、元予算と予算残高の 2 種類の予算を使用します。</span><span class="sxs-lookup"><span data-stu-id="c143b-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="c143b-106">プロジェクト予算を作成するときには、**予測モデル** ページで作成された、元予算と予算残高の予測モデルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c143b-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="c143b-107">プロジェクト予算をコミットすると、指定したモデルに基づいたプロジェクト予算が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c143b-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="c143b-108">予算管理に使用される予測モデルは、下位モデルを持つことができず、また、下位モデルとして使用することもできません。</span><span class="sxs-lookup"><span data-stu-id="c143b-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="c143b-109">**プロジェクト管理と会計** > **設定** > **予測**  > **予測モデル** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="c143b-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="c143b-110">**新規** を選択して、新しい予測モデルを作成し、モデルの ID 番号と名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="c143b-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="c143b-111">**停止** オプションを **はい**に設定し、予測モデルの予測行が変更されないように設定します。</span><span class="sxs-lookup"><span data-stu-id="c143b-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="c143b-112">モデルが関連付けられている予測行が一般会計にキャッシュ フロー予測を生成する場合は、**キャッシュフロー予測に含める** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c143b-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="c143b-113">プロジェクト日付を請求日として使用するには、**予測請求日** を **はい** に設定 します。</span><span class="sxs-lookup"><span data-stu-id="c143b-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="c143b-114">**予算タイプ** フィールドで、次のモデル タイプのいずれかを選択します：</span><span class="sxs-lookup"><span data-stu-id="c143b-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="c143b-115">**元の予算**：元の予算が作成され、承認された際にコミットされた当初予算額を使用します。</span><span class="sxs-lookup"><span data-stu-id="c143b-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="c143b-116">**予算残高**：プロジェクトの実施期間中の予算残額を使用します。</span><span class="sxs-lookup"><span data-stu-id="c143b-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="c143b-117">この予測モデルの残高は、実際のトランザクションによって減少し、予算リビジョンによって増加または減少します。</span><span class="sxs-lookup"><span data-stu-id="c143b-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="c143b-118">**繰り越し**：プロジェクトの繰越予算額を使用します。</span><span class="sxs-lookup"><span data-stu-id="c143b-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="c143b-119">繰越は、ある会計年度の未使用の予算額を別の会計年度に移動するために実行するオプションのプロセスです。</span><span class="sxs-lookup"><span data-stu-id="c143b-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="c143b-120">必要に応じて次のオプションを設定します：</span><span class="sxs-lookup"><span data-stu-id="c143b-120">Set the following options as required:</span></span>

   - <span data-ttu-id="c143b-121">プロジェクト日付を請求日として使用するには、**予測請求日** を有効化します。</span><span class="sxs-lookup"><span data-stu-id="c143b-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="c143b-122">仕掛品（WIP）に基づいて予測する場合は、**WIP で予測する** を有効にし、WIP の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="c143b-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="c143b-123">既定の **予算のタイプ** を **なし** のままにすることも、新しいタイプを入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="c143b-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="c143b-124">予算タイプは、レコードを変更した後で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="c143b-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="c143b-125">既定の予算タイプを変更すると、他のすべてのオプションが更新できなくなります。また、この予測モデルを再利用することはできません。</span><span class="sxs-lookup"><span data-stu-id="c143b-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

