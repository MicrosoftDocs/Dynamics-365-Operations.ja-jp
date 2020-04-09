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
ms.openlocfilehash: 212227afb21ac1a20d29c33b40f6c44561da14fe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144356"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="8ff30-103">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="8ff30-103">Create and validate journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ff30-104">このタスク ガイドでは、仕訳帳および仕訳帳明細行を作成し、検証します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-104">This task guide creates and validates journals and journal lines.</span></span> <span data-ttu-id="8ff30-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-105">This tasks uses the USMF demo company.</span></span>  



1. <span data-ttu-id="8ff30-106">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-106">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="8ff30-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-107">Click New.</span></span>
3. <span data-ttu-id="8ff30-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8ff30-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8ff30-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8ff30-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-110">Click Lines.</span></span>
6. <span data-ttu-id="8ff30-111">[勘定] フィールドに [勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-111">In the Account field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="8ff30-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-112">In the Description field, type a value.</span></span>
8. <span data-ttu-id="8ff30-113">借方または貸方勘定の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-113">Enter an amount for the Account in either Debit or Credit.</span></span> <span data-ttu-id="8ff30-114">このタスク ガイドでは、借方金額を想定しています。</span><span class="sxs-lookup"><span data-stu-id="8ff30-114">This task guide is assuming a debit amount.</span></span>
9. <span data-ttu-id="8ff30-115">[相手勘定] フィールドに [相手勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ff30-115">In the Offset account field enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="8ff30-116">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-116">Click Validate.</span></span>
11. <span data-ttu-id="8ff30-117">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-117">Click Validate.</span></span>
12. <span data-ttu-id="8ff30-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-118">Click Post.</span></span>
13. <span data-ttu-id="8ff30-119">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ff30-119">Click Voucher.</span></span>

