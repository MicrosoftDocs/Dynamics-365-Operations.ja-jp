---
title: 仕訳帳の作成および検証
description: この手順では、仕訳帳と仕訳帳明細行を作成し、検証します。
author: panolte
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72c97c6afb7bbe602fcb7a5e24a1d2a2cd727f6d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832733"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="1c000-103">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="1c000-103">Create and validate journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c000-104">この手順では、仕訳帳と仕訳帳明細行を作成し、検証します。</span><span class="sxs-lookup"><span data-stu-id="1c000-104">This procedure creates and validates journals and journal lines.</span></span> <span data-ttu-id="1c000-105">デモの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1c000-105">You can try this procedure using the USMF demo company.</span></span>  

1. <span data-ttu-id="1c000-106">**総勘定元帳 > 仕訳入力 > 一般仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1c000-106">Go to **General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="1c000-107">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-107">Click **New**.</span></span>
3. <span data-ttu-id="1c000-108">**名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="1c000-108">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1c000-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1c000-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1c000-110">**行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-110">Click **Lines**.</span></span>
6. <span data-ttu-id="1c000-111">**勘定** フィールドに [勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c000-111">In the **Account** field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="1c000-112">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c000-112">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="1c000-113">**借方** または **貸方** 勘定の金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c000-113">Enter an amount for the account as either a **Debit** or **Credit**.</span></span> 
9. <span data-ttu-id="1c000-114">**相手勘定** フィールドに [相手勘定タイプ] に基づいた適切な勘定を入力します。</span><span class="sxs-lookup"><span data-stu-id="1c000-114">In the **Offset account** field, enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="1c000-115">**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-115">Click **Validate**.</span></span>
11. <span data-ttu-id="1c000-116">**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-116">Click **Validate**.</span></span>
12. <span data-ttu-id="1c000-117">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-117">Click **Post**.</span></span>
13. <span data-ttu-id="1c000-118">**伝票** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c000-118">Click **Voucher**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]