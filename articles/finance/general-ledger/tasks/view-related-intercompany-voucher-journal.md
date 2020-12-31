---
title: 仕訳帳からの関連する会社間伝票の表示
description: 一般仕訳帳から会社間トランザクションを転記する時、関連する伝票ウィンドウは相殺会社からの伝票を表示します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, SysDataAreaSelectLookup, LedgerTransVoucher, LedgerTransRelatedVouchers
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee8385561f9aadae333c05c6df62de0ad1d39010
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445287"
---
# <a name="view-related-intercompany-voucher-from-journal"></a><span data-ttu-id="b2e1d-103">仕訳帳からの関連する会社間伝票の表示</span><span class="sxs-lookup"><span data-stu-id="b2e1d-103">View related intercompany voucher from journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2e1d-104">一般仕訳帳から会社間トランザクションを転記する時、関連する伝票ウィンドウは相殺会社からの伝票を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-104">The related voucher window shows the voucher from the offset company when posting an intercompany transaction from the general journal.</span></span>


## <a name="post-an-intercompany-journal"></a><span data-ttu-id="b2e1d-105">会社間仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="b2e1d-105">Post an intercompany journal</span></span>
1. <span data-ttu-id="b2e1d-106">[一般仕訳帳] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-106">Go to General journals.</span></span>
2. <span data-ttu-id="b2e1d-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-107">Click New.</span></span>
3. <span data-ttu-id="b2e1d-108">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b2e1d-109">[名前] フィールドで、会社間の仕訳帳名を入力するか、または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-109">In the Name field, enter or select the intercompany journal name.</span></span>
5. <span data-ttu-id="b2e1d-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-110">Click Lines.</span></span>
6. <span data-ttu-id="b2e1d-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-111">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b2e1d-112">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-112">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="b2e1d-113">[説明] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-113">In the Description field, enter or select a value.</span></span>
9. <span data-ttu-id="b2e1d-114">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-114">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b2e1d-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-115">Close the page.</span></span>
11. <span data-ttu-id="b2e1d-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-116">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="b2e1d-117">[相殺会社] フィールドで、相殺会社を入力、または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-117">In the Offset company field, type or select the offset company.</span></span>
13. <span data-ttu-id="b2e1d-118">[相殺会社] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-118">In the Offset company field, enter or select a value.</span></span>
14. <span data-ttu-id="b2e1d-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-119">Close the page.</span></span>
15. <span data-ttu-id="b2e1d-120">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-120">In the Offset account field, specify the desired values.</span></span>
16. <span data-ttu-id="b2e1d-121">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-121">Click Post.</span></span>

## <a name="view-related-intercompany-voucher"></a><span data-ttu-id="b2e1d-122">関連する会社間伝票の表示</span><span class="sxs-lookup"><span data-stu-id="b2e1d-122">View related intercompany voucher</span></span>
1. <span data-ttu-id="b2e1d-123">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-123">Click Voucher.</span></span>
2. <span data-ttu-id="b2e1d-124">[関連する伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-124">Click Related vouchers.</span></span>
3. <span data-ttu-id="b2e1d-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-125">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b2e1d-126">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e1d-126">Click Voucher.</span></span>

