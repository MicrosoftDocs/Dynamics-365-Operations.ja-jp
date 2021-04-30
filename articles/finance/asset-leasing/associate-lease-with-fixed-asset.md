---
title: 固定資産へをリースに関連付ける
description: このトピックでは、既存の固定資産を新しいリースに関連付ける方法について説明します。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 02a17b8c995e8aa97384d8b855afb688324017d6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881351"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="a7882-103">固定資産へをリースに関連付ける</span><span class="sxs-lookup"><span data-stu-id="a7882-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7882-104">このトピックでは、既存の固定資産を新しいリースに関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7882-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="a7882-105">固定資産とリースを関連付けた場合、当初認識時使用権資産 (ROU) の値は固定資産の取得原価となります。</span><span class="sxs-lookup"><span data-stu-id="a7882-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="a7882-106">固定資産とリースを関連付ける前に、固定資産に固定資産のレコードを作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7882-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="a7882-107">**リースの概要** ページで、リースを作成し、このリースに資産をリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7882-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="a7882-108">[リースの追加またはコピー](add-lease.md)に記載の手順に従い、リースを追加します。</span><span class="sxs-lookup"><span data-stu-id="a7882-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="a7882-109">**リースの追加** ページの **固定資産番号** フィールドで、まだ取得されていない資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="a7882-110">**帳簿** を選択し、支払スケジュールを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7882-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="a7882-111">**当初認識** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="a7882-112">**資産リース仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="a7882-113">リースの当初認識仕訳入力は、通常は使用権資産に借方に転記される金額の固定資産の借方に転記します。</span><span class="sxs-lookup"><span data-stu-id="a7882-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="a7882-114">以上で、固定資産のトランザクション タイプと帳簿を表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a7882-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="a7882-115">**仕訳帳の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="a7882-116">仕訳帳エントリの個々の明細行を表示するには、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="a7882-117">資産が含まれている仕訳帳明細行を選択し、**固定資産** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7882-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="a7882-118">**固定資産** タブには、トランザクション タイプと帳簿が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7882-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="a7882-119">既定では、**トランザクション タイプ** フィールドは **取得** に設定され、**帳簿** フィールドは固定資産の現在の帳簿に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a7882-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="a7882-120">当初認識仕訳帳入力を転記すると、トランザクションは固定資産の取得トランザクションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7882-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="a7882-121">トランザクション テーブルを表示するには、**固定資産 \> 固定資産 \> 固定資産** に移動し、適切な資産を選択して、**評価額** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="a7882-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="a7882-122">当初認識仕訳入力で、指定された固定資産の取得取引が作成されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7882-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="a7882-123">固定資産の標準減価償却機能を使用して、固定資産を減価償却できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a7882-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="a7882-124">減価償却方法の詳細については、[減価償却方法](../fixed-assets/depreciation-methods-conventions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7882-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a7882-125">固定資産をリースに関連付けると、資産リースの **資産の減価償却** ボタンと **リースの減損** ボタンが無効になります。</span><span class="sxs-lookup"><span data-stu-id="a7882-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="a7882-126">固定資産からの資産減価償却およびリースの減損トランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a7882-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="a7882-127">**資産トランザクション** ボタンをクリックすると、"照会" フォームが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="a7882-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="a7882-128">固定資産で **資産トランザクション** の照会フォームを開くことも可能です。</span><span class="sxs-lookup"><span data-stu-id="a7882-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
