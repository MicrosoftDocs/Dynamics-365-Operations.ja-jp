---
title: 経費タイプの設定
description: このトピックでは、資産リースで資産タイプを設定する方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880987"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="d4e22-103">経費タイプの設定</span><span class="sxs-lookup"><span data-stu-id="d4e22-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4e22-104">このトピックでは、資産リースで資産タイプを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="d4e22-105">支払スケジュールによって表されない原価は、*経費原価* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="d4e22-106">このような原価の例としては、税金、一般的な領域保守にかかる費用、保険料などがあります。</span><span class="sxs-lookup"><span data-stu-id="d4e22-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="d4e22-107">管理経費タイプの追加</span><span class="sxs-lookup"><span data-stu-id="d4e22-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="d4e22-108">**資産リース \> 設定 \> 経費タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="d4e22-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-109">Select **New**.</span></span>
3. <span data-ttu-id="d4e22-110">適切なフィールドに、新しい経費タイプと説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="d4e22-111">管理原価に対する勘定の割り当て</span><span class="sxs-lookup"><span data-stu-id="d4e22-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="d4e22-112">次に、勘定を経費タイプに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="d4e22-113">これらの勘定は、経費スケジュール エントリが転記されると借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="d4e22-114">相手勘定は、各リースの **履行費用支払スケジュール** 明細行に対して指定されます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="d4e22-115">**資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d4e22-116">**勘定** タブの **履行費用** クイックタブの **経費タイプ** フィールドで、経費タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="d4e22-117">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-117">Select **Add**.</span></span>
4. <span data-ttu-id="d4e22-118">**帳簿タイプ** フィールドで、管理原価にリンクする帳簿タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4e22-119">同じ経費勘定に複数の帳簿タイプを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="d4e22-120">**勘定コード** フィールドで、この帳簿をどのリースに適用するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="d4e22-121">**すべて** – 帳簿をすべてのリースに適用します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="d4e22-122">**グループ** – 特定のリース グループに帳簿を適用します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="d4e22-123">**テーブル** – 帳簿を特定のリースに適用します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="d4e22-124">**グループ** または **テーブル** を **勘定コード** フィールドで選択した場合、勘定番号またはグループ番号を **勘定/グループ番号** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="d4e22-125">該当するフィールドで、ファイナンス リースの主勘定と、オペレーティング リースの主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4e22-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="d4e22-126">これらの手順を完了したら、選択したリースの **リース詳細** ページに **履行費用支払スケジュール** 明細行を使用して経費を追加できます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="d4e22-127">別の方法として、新しいリースを作成するときに経費を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4e22-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
