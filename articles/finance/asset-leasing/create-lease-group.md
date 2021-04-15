---
title: リース グループの作成
description: このトピックでは、リース グループを設定する方法について説明します。 新しいリースを作成するには、リース グループが必要です。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5d5efb02c95d9368fbc178cfd9bcd7ce088d1c66
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816055"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="3ab16-104">リース グループの作成</span><span class="sxs-lookup"><span data-stu-id="3ab16-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ab16-105">このトピックでは、リース グループを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="3ab16-106">新しいリースを作成するには、リース グループが必要です。</span><span class="sxs-lookup"><span data-stu-id="3ab16-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="3ab16-107">リース帳簿は、各リース グループに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="3ab16-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="3ab16-108">リース帳簿は、各リースで作成しなければならない既定の帳簿を決定します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="3ab16-109">**リース転記パラメーター** ページでは、特定のアカウントをリース グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="3ab16-110">リース帳簿を作成し、リース グループを追加する</span><span class="sxs-lookup"><span data-stu-id="3ab16-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="3ab16-111">**資産リース \> 設定 \> リース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="3ab16-112">アクション ウィンドウで **新規** を選択して、リース グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="3ab16-113">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="3ab16-114">新しい行の **リース グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="3ab16-115">**説明** フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="3ab16-116">先ほど入力した情報が、**リースの追加** ページの **リースグループ** フィールドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="3ab16-117">リース グループへの帳簿の関連付け</span><span class="sxs-lookup"><span data-stu-id="3ab16-117">Associate a book with a lease group</span></span>

<span data-ttu-id="3ab16-118">リース グループの作成後は、各グループに帳簿を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="3ab16-119">リースを作成してリースグループに割り当てると、そのリースグループに関連付けられた帳簿ごとに一連のスケジュールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab16-120">帳簿をリース グループに割り当てるには、あらかじめ設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab16-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="3ab16-121">**資産リース \> 設定 \> リース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="3ab16-122">リース グループを選択し、**帳簿** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="3ab16-123">**新規** を選択し、**帳簿タイプ** フィールドで、リース グループに割り当てる帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ab16-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="3ab16-124">リースをさまざまな方法で計上する必要がある場合は、複数の帳簿をリース グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="3ab16-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]