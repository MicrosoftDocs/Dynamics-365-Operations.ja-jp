---
title: 雇用検証 i9 検証
description: 連邦移民改革管理法 (IRCA) により、米国の雇用主は、新しく雇用した従業員の雇用適格性の状態を確認する必要があります。
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmPersonIdentificationNumber, Hcmi9Document
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 544c298f83c4b1838a94aee95ed6038fcc1f4e4f
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850782"
---
# <a name="employment-verification-i9-verification"></a><span data-ttu-id="a978e-103">雇用検証 i9 検証</span><span class="sxs-lookup"><span data-stu-id="a978e-103">Employment verification i9 verification</span></span>

[!include [task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="a978e-104">連邦移民改革管理法 (IRCA) により、米国の雇用主は、新しく雇用した従業員の雇用適格性の状態を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a978e-104">The Immigration Reform and Control Act requires US employers to verify the employment eligibility status of newly hired employees.</span></span> <span data-ttu-id="a978e-105">この手順では、I-9 の検証に必要なドキュメントを記録する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="a978e-105">This procedure will walk you through the steps of recording the necessary documents for I-9 verification.</span></span> <span data-ttu-id="a978e-106">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="a978e-106">Use the USMF company for this procedure.</span></span>

1. <span data-ttu-id="a978e-107">[人事管理] > [作業者] > [従業員] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a978e-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="a978e-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="a978e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a978e-109">たとえば、「Vince」という値を含む [名前] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="a978e-109">For example, filter on the Name field with a value of 'Vince'.</span></span>
3. <span data-ttu-id="a978e-110">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-110">Select the employee.</span></span> <span data-ttu-id="a978e-111">例: Vince Prado</span><span class="sxs-lookup"><span data-stu-id="a978e-111">Example: Vince Prado</span></span>
4. <span data-ttu-id="a978e-112">[個人情報] クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="a978e-112">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="a978e-113">[ID 番号] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-113">Click Identification numbers.</span></span>
6. <span data-ttu-id="a978e-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-114">Click New.</span></span>
7. <span data-ttu-id="a978e-115">記録する ID タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-115">Select the identification type that you are recording.</span></span> <span data-ttu-id="a978e-116">例: パスポート</span><span class="sxs-lookup"><span data-stu-id="a978e-116">Example: Passport</span></span>
8. <span data-ttu-id="a978e-117">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a978e-117">In the Number field, type a value.</span></span>
9. <span data-ttu-id="a978e-118">[基本] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-118">Select Yes in the Primary field.</span></span>
10. <span data-ttu-id="a978e-119">[説明] フィールドに、ID レコードの簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a978e-119">In the Description field, enter a brief description of the identification record..</span></span>
11. <span data-ttu-id="a978e-120">発行機関で、作業者の ID のフォームを発行した機関を選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-120">In the issuing agency select the agency that issued the form of identification to the worker.</span></span> <span data-ttu-id="a978e-121">例: 政府</span><span class="sxs-lookup"><span data-stu-id="a978e-121">Example: Government</span></span>
12. <span data-ttu-id="a978e-122">発行機関が作業者の ID のフォームを発行した日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a978e-122">Enter the date that the issuing agency issued the form of identification to the worker.</span></span> <span data-ttu-id="a978e-123">例: 2011 年 2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a978e-123">Example: 02/15/2011</span></span>
13. <span data-ttu-id="a978e-124">ID のフォームの期限が切れる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a978e-124">Enter the date when the form of identification expires.</span></span> <span data-ttu-id="a978e-125">例: 2021 年 2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a978e-125">Example: 2/15/2021</span></span>
14. <span data-ttu-id="a978e-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-126">Click Save.</span></span>
15. <span data-ttu-id="a978e-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a978e-127">Close the page.</span></span>
16. <span data-ttu-id="a978e-128">[雇用] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-128">Click the Employment tab.</span></span>
17. <span data-ttu-id="a978e-129">[I-9] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-129">Click I-9.</span></span>
18. <span data-ttu-id="a978e-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-130">Click New.</span></span>
19. <span data-ttu-id="a978e-131">[就業資格] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-131">In the Work eligibility field, select an option.</span></span>
    * <span data-ttu-id="a978e-132">従業員が米国の市民権または国籍を持っていない場合は、従業員の居住外国人番号または入国番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a978e-132">If the employee is not a citizen or national of the United States, you must enter the worker's resident alien or admission number.</span></span>  
20. <span data-ttu-id="a978e-133">[GroupListA] オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-133">Select the GroupListA option.</span></span>
    * <span data-ttu-id="a978e-134">選択するリストは、従業員が提出した識別フォームにより決まります。</span><span class="sxs-lookup"><span data-stu-id="a978e-134">The list that you select depends on what form of identification the worker provided.</span></span> <span data-ttu-id="a978e-135">作業者は、リスト A のドキュメントを 1 つ、またはリスト B と C からドキュメントを 1 つ提出する必要があります。たとえば、作業者がパスポートを提示した場合、リスト A を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="a978e-135">A worker must provide one List A document or one document from List B and C. For example, if the worker provided a passport, then List A could be selected.</span></span> <span data-ttu-id="a978e-136">ただし、作業者が運転免許証と社会保障カードのみを提供した場合、リスト B と C を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a978e-136">However, if the worker has only provided their drivers license and social security card, then list B and C must be selected.</span></span>  
21. <span data-ttu-id="a978e-137">[ I-9 ドキュメント タイプ] フィールドで、従業員が提出したドキュメントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-137">In the I-9 document type field, select the type of document that the worker provided.</span></span>
22. <span data-ttu-id="a978e-138">[文章番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a978e-138">In the Document number field, enter or select a value.</span></span>
23. <span data-ttu-id="a978e-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a978e-139">Click Save.</span></span>

