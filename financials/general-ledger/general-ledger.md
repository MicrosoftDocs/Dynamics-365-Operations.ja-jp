---
title: "総勘定元帳と財務報告のホーム ページ"
description: "法人の財務レコードを定義および管理するには、一般会計を使用します。 一般会計では借方と貸方のエントリ登録です。 これらのエントリは、勘定科目表に表示される勘定を使用して分類されます。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="b4b70-105">一般会計</span><span class="sxs-lookup"><span data-stu-id="b4b70-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b4b70-106">法人の財務レコードを定義および管理するには、一般会計を使用します。</span><span class="sxs-lookup"><span data-stu-id="b4b70-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b4b70-107">一般会計では借方と貸方のエントリ登録です。</span><span class="sxs-lookup"><span data-stu-id="b4b70-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b4b70-108">これらのエントリは、勘定科目表に表示される勘定を使用して分類されます。</span><span class="sxs-lookup"><span data-stu-id="b4b70-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="b4b70-109">配賦ルールに基づいて、金額を、1 つ以上の勘定または勘定と分析コードの組み合わせに配賦または配分できます。</span><span class="sxs-lookup"><span data-stu-id="b4b70-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b4b70-110">配賦には、固定と変動の 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="b4b70-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b4b70-111">また、勘定科目間のトランザクションを決済し、通貨金額を再評価することもできます。</span><span class="sxs-lookup"><span data-stu-id="b4b70-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b4b70-112">会計年度末には、決算トランザクションを生成し、次の会計年度に使用する勘定を用意します。</span><span class="sxs-lookup"><span data-stu-id="b4b70-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b4b70-113">連結機能を使用すれば、複数の関連する法人の財務結果を 1 つの連結した組織の結果にまとめることができます。</span><span class="sxs-lookup"><span data-stu-id="b4b70-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b4b70-114">関連会社は、同じ Microsoft Dynamics 365 for Finance and Operations データベースに格納することも、別のデータベースに格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="b4b70-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="b4b70-115">消費税</span><span class="sxs-lookup"><span data-stu-id="b4b70-115">Sales tax</span></span>
<span data-ttu-id="b4b70-116">すべての会社は税金を徴収し、さまざまな税務当局に支払います。</span><span class="sxs-lookup"><span data-stu-id="b4b70-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b4b70-117">ルールと税率は国/地域、都道府県、市区郡、および市町村によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b4b70-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="b4b70-118">また、ルールは、税務当局が要件を変更した際に、定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4b70-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b4b70-119">売上税コードには、徴収額と当局への支払額に関する基本的な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b4b70-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b4b70-120">売上税コードの設定時には、徴収する必要のある金額または割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4b70-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b4b70-121">また、トランザクション金額に金額や割合を適用する各種方法も定義します。</span><span class="sxs-lookup"><span data-stu-id="b4b70-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b4b70-122">このセクションのトピックでは、税務当局が定める徴収方法と税率に対して売上税コードを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b4b70-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







