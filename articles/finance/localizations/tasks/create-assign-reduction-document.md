---
title: 政府助成金の圧縮記帳ドキュメントの作成および割り当て
description: 日本では、圧縮記帳ドキュメントとは、政府助成金によって支援された固定資産に添えるドキュメントのことです。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetReductionEntryProfile_JP, AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0b3cd8a964c1edad721789fc80b53e39d7c022c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145256"
---
# <a name="create-and-assign-a-reduction-entry-document-for-a-government-grant-subsidy"></a><span data-ttu-id="3da49-103">政府助成金の圧縮記帳ドキュメントの作成および割り当て</span><span class="sxs-lookup"><span data-stu-id="3da49-103">Create and assign a reduction entry document for a government grant subsidy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3da49-104">日本では、圧縮記帳ドキュメントとは、政府助成金によって支援された固定資産に添えるドキュメントのことです。</span><span class="sxs-lookup"><span data-stu-id="3da49-104">For Japan, a reduction entry document is a document that you can attach to a fixed asset that is sponsored using a government subsidy.</span></span> <span data-ttu-id="3da49-105">圧縮記帳の証明書には、圧縮記帳メソッド、減価償却の方法、理由、有効性、補助金のしきい値など、政府補助金に関する詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3da49-105">The reduction entry certificate contains the details about the government subsidy, such as the reduction entry method, depreciation convention, reason, validity, and subsidy threshold.</span></span>



<span data-ttu-id="3da49-106">圧縮記帳ドキュメントの詳細は、圧縮記帳金額を計算および転記するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="3da49-106">The details of the reduction entry document are used to calculate and post reduction entry amounts.</span></span>



<span data-ttu-id="3da49-107">このタスクを使用して、圧縮記帳ドキュメントの作成方法および固定資産への適用方法を把握します。</span><span class="sxs-lookup"><span data-stu-id="3da49-107">Use this task to learn how to create reduction entry documents and assign it to a fixed asset.</span></span>



<span data-ttu-id="3da49-108">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3da49-108">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="3da49-109">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="3da49-109">This task uses the JPMF demo company data.</span></span>


## <a name="create-a-new-reduction-entry-document"></a><span data-ttu-id="3da49-110">新しい圧縮記帳ドキュメントの作成</span><span class="sxs-lookup"><span data-stu-id="3da49-110">Create a new reduction entry document</span></span>
1. <span data-ttu-id="3da49-111">[固定資産] > [定期処理タスク] > [圧縮記帳] > [圧縮記帳の文書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3da49-111">Go to Fixed assets > Periodic tasks > Reduction entries > Reduction entry documents.</span></span>
2. <span data-ttu-id="3da49-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3da49-112">Click New.</span></span>
3. <span data-ttu-id="3da49-113">[圧縮記帳] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3da49-113">In the Reduction entry document field, type a value.</span></span>
4. <span data-ttu-id="3da49-114">[圧縮記帳のタイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3da49-114">In the Reduction entry type field, select an option.</span></span>
    * <span data-ttu-id="3da49-115">政府助成金の仕訳入力方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="3da49-115">Select a method to journalize the government grant.</span></span>  
5. <span data-ttu-id="3da49-116">[減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3da49-116">In the Depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="3da49-117">このフィールドは、[圧縮記帳のタイプ] フィールドで [積立金方式] を選択した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3da49-117">This field is available only if you select Reserve in the Reduction entry type field.</span></span>     <span data-ttu-id="3da49-118">減価償却方法は、固定資産に使用する方法と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3da49-118">Depreciation convention should be the same as the one used for the fixed asset.</span></span>  
    * <span data-ttu-id="3da49-119">助成金の原因、失効日、政府助成金最高額の最大レートなどの追加情報を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="3da49-119">You can choose to record some extra information such as subsidies reason, valid from, valid to, max percentage rate of max amount of the government grant subsidy.</span></span>  
    * <span data-ttu-id="3da49-120">[助成金の償却] タブで、固定資産の償却およびそれに関連する助成金について政府から要求された条件を入力できます。</span><span class="sxs-lookup"><span data-stu-id="3da49-120">Under the Retirement of subsidies tab, you can enter terms that required by the government upon the retirement of the fixed asset and its related subsidies.</span></span> <span data-ttu-id="3da49-121">この情報は、固定資産を廃棄するかどうか、または廃棄する場合にその時期はいつかを知りたいときに参照されます。</span><span class="sxs-lookup"><span data-stu-id="3da49-121">This information is referred to if and when you dispose of the fixed asset.</span></span>  
6. <span data-ttu-id="3da49-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3da49-122">Click Save.</span></span>

## <a name="assign-the-reduction-entry-document-to-a-fixed-asset-book"></a><span data-ttu-id="3da49-123">固定資産帳簿への圧縮記帳ドキュメントの割り当て</span><span class="sxs-lookup"><span data-stu-id="3da49-123">Assign the reduction entry document to a fixed asset book</span></span>
1. <span data-ttu-id="3da49-124">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3da49-124">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="3da49-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3da49-125">Click New.</span></span>
    * <span data-ttu-id="3da49-126">支援された資産がシステムに既に入力されている場合、既存の固定資産の編集を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="3da49-126">You can also choose to edit an existing fixed asset if the sponsored asset is already entered in the system.</span></span>  
3. <span data-ttu-id="3da49-127">[固定資産グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3da49-127">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="3da49-128">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3da49-128">Click Books.</span></span>
5. <span data-ttu-id="3da49-129">クイック フィルターを使用して、目的の帳簿を除外します。</span><span class="sxs-lookup"><span data-stu-id="3da49-129">Use the quick filter to filter out the desired book.</span></span>
6. <span data-ttu-id="3da49-130">[圧縮記帳] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3da49-130">In the Reduction entry document field, type a value.</span></span>
7. <span data-ttu-id="3da49-131">ドキュメントの日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3da49-131">Enter the document date.</span></span>
8. <span data-ttu-id="3da49-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3da49-132">Click Save.</span></span>

