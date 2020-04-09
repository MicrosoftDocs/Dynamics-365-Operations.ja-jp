---
title: 圧縮記帳のある固定資産の処分
description: このタスクでは、圧縮記帳のある固定資産の日本での処理方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b871e2cc9456da5b5b48b13ff0d9491a58c6aa1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141537"
---
# <a name="dispose-of-a-fixed-asset-with-reduction-entry"></a><span data-ttu-id="3531e-103">圧縮記帳のある固定資産の処分</span><span class="sxs-lookup"><span data-stu-id="3531e-103">Dispose of a fixed asset with reduction entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3531e-104">このタスクでは、圧縮記帳のある固定資産の日本での処理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3531e-104">Use this task to learn how to dispose of a fixed asset with reduction entry for Japan.</span></span>



<span data-ttu-id="3531e-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3531e-105">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="3531e-106">このタスクは、デモ データ会社 JPMF を使用して完了しました。</span><span class="sxs-lookup"><span data-stu-id="3531e-106">This task was completed using the JPMF demo data company.</span></span>

1. <span data-ttu-id="3531e-107">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3531e-107">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="3531e-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-108">Click New.</span></span>
3. <span data-ttu-id="3531e-109">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3531e-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3531e-110">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-110">Click Lines.</span></span>
5. <span data-ttu-id="3531e-111">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-111">Click Proposals.</span></span>
6. <span data-ttu-id="3531e-112">[処分 - 仕損] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-112">Click Disposal - scrap.</span></span>
7. <span data-ttu-id="3531e-113">処分トランザクションの日付の入力</span><span class="sxs-lookup"><span data-stu-id="3531e-113">Enter the date of disposal transaction</span></span>
8. <span data-ttu-id="3531e-114">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-114">Click Filter.</span></span>
9. <span data-ttu-id="3531e-115">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3531e-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="3531e-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-116">Click OK.</span></span>
11. <span data-ttu-id="3531e-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-117">Click OK.</span></span>
12. <span data-ttu-id="3531e-118">固定資産の処分の経費が転記される主勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="3531e-118">Enter the main accounts where the fixed asset disposal expenses will be posted to.</span></span>
    * <span data-ttu-id="3531e-119">仕訳帳に処分の経費を後で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="3531e-119">You can also choose to enter the disposal expenses later in a journal.</span></span>     <span data-ttu-id="3531e-120">固定資産の主勘定と減価償却累計額の主勘定およびそのほかの関連固定資産勘定は、固定資産の転記プロファイル コンフィギュレーションに従って自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3531e-120">The fixed asset main account and accumulated depreciation main account and other fixed asset related accounts are automatically determined by the configuration in the fixed asset posting profile.</span></span>  
    * <span data-ttu-id="3531e-121">圧縮記帳ドキュメントは、固定資産ドキュメントとは別に処分されます。</span><span class="sxs-lookup"><span data-stu-id="3531e-121">The disposal of reduction entry document is separated from that of the fixed asset.</span></span>  
    * <span data-ttu-id="3531e-122">元の助成金額および累計償却額は、固定資産の転記プロファイルのコンフィギュレーションに従って自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3531e-122">The original subsidy amount and accumulated amortization amount are automatically determined by the configuration in the fixed asset posting profile.</span></span>  
13. <span data-ttu-id="3531e-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3531e-123">Click Post.</span></span>

