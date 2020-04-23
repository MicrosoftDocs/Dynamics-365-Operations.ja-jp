---
title: 待機期間のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: adb7842231e8092398b240a2f017c28821b13ee1
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229582"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="c3ed7-103">待機期間のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c3ed7-103">Configure waiting periods</span></span>

<span data-ttu-id="c3ed7-104">Microsoft Dynamics 365 Human Resources では、待機日は、給付金プランに使用するマイルストーンを確立します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="c3ed7-105">たとえば、雇用日から 3 か月、各月の最初、または 6 か月です。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="c3ed7-106">**給付金管理**ワーク スペースの**設定**で、**待機期間**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="c3ed7-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-107">Select **New**.</span></span>

3. <span data-ttu-id="c3ed7-108">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c3ed7-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="c3ed7-109">Field</span></span> | <span data-ttu-id="c3ed7-110">説明</span><span class="sxs-lookup"><span data-stu-id="c3ed7-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c3ed7-111">**待機コード**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-111">**Waiting code**</span></span> | <span data-ttu-id="c3ed7-112">待機期間の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="c3ed7-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-113">**Description**</span></span> | <span data-ttu-id="c3ed7-114">待機期間の説明。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="c3ed7-115">**待機方法**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-115">**Waiting method**</span></span> | <span data-ttu-id="c3ed7-116">値のドロップダウン リストから適切な待機メソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="c3ed7-117">オプションには、正味、当月、現在の四半期、今年度、および現在の週があります。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="c3ed7-118">**月数**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-118">**Months**</span></span> | <span data-ttu-id="c3ed7-119">待機日を計算するために待機メソッドに追加する月数を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="c3ed7-120">**日**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-120">**Days**</span></span> | <span data-ttu-id="c3ed7-121">待機日を計算するために待機メソッドに追加する日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="c3ed7-122">**待機日数**</span><span class="sxs-lookup"><span data-stu-id="c3ed7-122">**Waiting day**</span></span> | <span data-ttu-id="c3ed7-123">待機日の計算に使用する待機日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="c3ed7-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3ed7-124">Select **Save**.</span></span>
