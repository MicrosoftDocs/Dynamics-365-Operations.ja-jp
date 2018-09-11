--- 
title: "売上税所轄官庁の設定"
description: "売上税所轄官庁とは、収集された売上税の報告先および支払先です。"
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c3d6ab08c91dba035891509bc5cc33db39a726c2
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="3b9b1-103">売上税所轄官庁の設定</span><span class="sxs-lookup"><span data-stu-id="3b9b1-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b9b1-104">売上税所轄官庁とは、収集された売上税の報告先および支払先です。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="3b9b1-105">売上税を所轄官庁に直接支払うか、売上税所轄官庁用に作成した仕入先を介して支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="3b9b1-106">設定すると、会社は通常の支払業務を行うことで予定どおりに売上税所轄官庁に対して支払を行うことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="3b9b1-107">売上税所轄官庁を仕入先として設定しない場合は、適切な期日に売上税所轄官庁への手動支払を準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="3b9b1-108">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3b9b1-109">[税] > [間接税] > [売上税] > [売上税所轄官庁] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="3b9b1-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-110">Click New.</span></span>
3. <span data-ttu-id="3b9b1-111">[所轄官庁] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="3b9b1-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3b9b1-113">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3b9b1-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3b9b1-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3b9b1-116">国/地域に合ったレポートのレイアウトを選択します (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="3b9b1-117">売上税所轄官庁の要件に合うレポートのレイアウトがない場合は、既定のレイアウトを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="3b9b1-118">支払う税の合計金額の丸め方法を指定するには、丸めフォームおよび丸めフィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="3b9b1-119">すべての丸め誤差は、総勘定元帳で設定した自動トランザクションの勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="3b9b1-120">[丸め] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="3b9b1-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b9b1-121">Click Save.</span></span>


