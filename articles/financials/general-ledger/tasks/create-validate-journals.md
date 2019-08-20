---
title: 仕訳帳の作成および検証
description: このタスク ガイドでは、仕訳帳および仕訳帳明細行を作成し、検証します。
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad1399d8ca96b9fdc5d316b6d9de8d9e04af55e8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846514"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="6d9bc-103">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="6d9bc-103">Create and validate journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d9bc-104">このタスク ガイドでは、仕訳帳および仕訳帳明細行を作成し、検証します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-104">This task guide creates and validates journals and journal lines.</span></span> <span data-ttu-id="6d9bc-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-105">This tasks uses the USMF demo company.</span></span>  



1. <span data-ttu-id="6d9bc-106">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-106">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="6d9bc-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-107">Click New.</span></span>
3. <span data-ttu-id="6d9bc-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6d9bc-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6d9bc-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-110">Click Lines.</span></span>
6. <span data-ttu-id="6d9bc-111">[勘定] フィールドに [勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-111">In the Account field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="6d9bc-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-112">In the Description field, type a value.</span></span>
8. <span data-ttu-id="6d9bc-113">借方または貸方勘定の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-113">Enter an amount for the Account in either Debit or Credit.</span></span> <span data-ttu-id="6d9bc-114">このタスク ガイドでは、借方金額を想定しています。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-114">This task guide is assuming a debit amount.</span></span>
9. <span data-ttu-id="6d9bc-115">[相手勘定] フィールドに [相手勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-115">In the Offset account field enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="6d9bc-116">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-116">Click Validate.</span></span>
11. <span data-ttu-id="6d9bc-117">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-117">Click Validate.</span></span>
12. <span data-ttu-id="6d9bc-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-118">Click Post.</span></span>
13. <span data-ttu-id="6d9bc-119">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d9bc-119">Click Voucher.</span></span>

