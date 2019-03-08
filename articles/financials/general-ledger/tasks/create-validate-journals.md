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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c94d992b97e9a2a18299f97c982430f8205cabf2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "329968"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="e48b7-103">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="e48b7-103">Create and validate journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e48b7-104">このタスク ガイドでは、仕訳帳および仕訳帳明細行を作成し、検証します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-104">This task guide creates and validates journals and journal lines.</span></span> <span data-ttu-id="e48b7-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-105">This tasks uses the USMF demo company.</span></span>  



1. <span data-ttu-id="e48b7-106">[総勘定元帳] > [総勘定元帳] > [仕訳入力] > [一般仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-106">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="e48b7-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-107">Click New.</span></span>
3. <span data-ttu-id="e48b7-108">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e48b7-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e48b7-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e48b7-110">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-110">Click Lines.</span></span>
6. <span data-ttu-id="e48b7-111">[勘定] フィールドに [勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-111">In the Account field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="e48b7-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-112">In the Description field, type a value.</span></span>
8. <span data-ttu-id="e48b7-113">借方または貸方勘定の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-113">Enter an amount for the Account in either Debit or Credit.</span></span> <span data-ttu-id="e48b7-114">このタスク ガイドでは、借方金額を想定しています。</span><span class="sxs-lookup"><span data-stu-id="e48b7-114">This task guide is assuming a debit amount.</span></span>
9. <span data-ttu-id="e48b7-115">[相手勘定] フィールドに [相手勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="e48b7-115">In the Offset account field enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="e48b7-116">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-116">Click Validate.</span></span>
11. <span data-ttu-id="e48b7-117">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-117">Click Validate.</span></span>
12. <span data-ttu-id="e48b7-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-118">Click Post.</span></span>
13. <span data-ttu-id="e48b7-119">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48b7-119">Click Voucher.</span></span>

