---
title: 待機期間のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58d96469fc953c1bbabe8e29bf9df7a8fb4a0589
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092516"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="5f484-103">待機期間のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5f484-103">Configure waiting periods</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5f484-104">Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。</span><span class="sxs-lookup"><span data-stu-id="5f484-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="5f484-105">たとえば、雇用日から 3 か月、各月の最初、または 6 か月です。</span><span class="sxs-lookup"><span data-stu-id="5f484-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="5f484-106">**給付金管理**ワーク スペースの**設定**で、**待機期間**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f484-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="5f484-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f484-107">Select **New**.</span></span>

3. <span data-ttu-id="5f484-108">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f484-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5f484-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="5f484-109">Field</span></span> | <span data-ttu-id="5f484-110">説明</span><span class="sxs-lookup"><span data-stu-id="5f484-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5f484-111">待機コード</span><span class="sxs-lookup"><span data-stu-id="5f484-111">Waiting code</span></span> | <span data-ttu-id="5f484-112">待機期間の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="5f484-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="5f484-113">説明</span><span class="sxs-lookup"><span data-stu-id="5f484-113">Description</span></span> | <span data-ttu-id="5f484-114">待機期間の説明。</span><span class="sxs-lookup"><span data-stu-id="5f484-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="5f484-115">待機方法</span><span class="sxs-lookup"><span data-stu-id="5f484-115">Waiting method</span></span> | <span data-ttu-id="5f484-116">値のドロップ ダウン リストから適切な待機メソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f484-116">Select the appropriate waiting method from the drop down list of values.</span></span> <span data-ttu-id="5f484-117">オプションには、正味、当月、現在の四半期、今年度、および現在の週があります。</span><span class="sxs-lookup"><span data-stu-id="5f484-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="5f484-118">月数</span><span class="sxs-lookup"><span data-stu-id="5f484-118">Months</span></span> | <span data-ttu-id="5f484-119">待機日を計算するために待機メソッドに追加する月数を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f484-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="5f484-120">Days</span><span class="sxs-lookup"><span data-stu-id="5f484-120">Days</span></span> | <span data-ttu-id="5f484-121">待機日を計算するために待機メソッドに追加する日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f484-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="5f484-122">待機日数</span><span class="sxs-lookup"><span data-stu-id="5f484-122">Waiting day</span></span> | <span data-ttu-id="5f484-123">待機日の計算に使用する待機日を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f484-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="5f484-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f484-124">Select **Save**.</span></span>
