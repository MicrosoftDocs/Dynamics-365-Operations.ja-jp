---
title: 個人の連絡先適格性オプションのコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources にて、個人の連絡先の適格性オプションをコンフィギュレーションします。 個人の連絡先は、受益者または扶養家族とすることができます。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790887"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="b5ace-104">個人の連絡先適格性オプションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b5ace-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b5ace-105">この記事では、Microsoft Dynamics 365 Human Resources で給付金で使用する個人の連絡先のタイプをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b5ace-106">個人の連絡先は、受益者または扶養家族とすることができます。</span><span class="sxs-lookup"><span data-stu-id="b5ace-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="b5ace-107">**給付金管理** ワーク スペースの **設定** で、**個人の連絡先適格性オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="b5ace-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-108">Select **New**.</span></span>

3. <span data-ttu-id="b5ace-109">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b5ace-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="b5ace-110">Field</span></span> | <span data-ttu-id="b5ace-111">説明</span><span class="sxs-lookup"><span data-stu-id="b5ace-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b5ace-112">**適格性オプション**</span><span class="sxs-lookup"><span data-stu-id="b5ace-112">**Eligibility option**</span></span> | <span data-ttu-id="b5ace-113">適格性オプションを識別する固有の適格性オプション名またはコード。</span><span class="sxs-lookup"><span data-stu-id="b5ace-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="b5ace-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5ace-114">**Description**</span></span> | <span data-ttu-id="b5ace-115">適格性オプションの簡単な説明。</span><span class="sxs-lookup"><span data-stu-id="b5ace-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="b5ace-116">**連絡先適格性コード**</span><span class="sxs-lookup"><span data-stu-id="b5ace-116">**Contact eligibility code**</span></span> | <span data-ttu-id="b5ace-117">個人の適格性オプションを最もよく表しているシステムコードです。</span><span class="sxs-lookup"><span data-stu-id="b5ace-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="b5ace-118">次から選択できます。</span><span class="sxs-lookup"><span data-stu-id="b5ace-118">You can choose from:</span></span> <ul><li><span data-ttu-id="b5ace-119">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="b5ace-119">Relationship</span></span></li><li><span data-ttu-id="b5ace-120">学生</span><span class="sxs-lookup"><span data-stu-id="b5ace-120">Student</span></span></li><li><span data-ttu-id="b5ace-121">規定年齢を超えた被扶養者</span><span class="sxs-lookup"><span data-stu-id="b5ace-121">Overage dependent</span></span></li><li><span data-ttu-id="b5ace-122">規定年齢を過ぎた無効な被扶養者</span><span class="sxs-lookup"><span data-stu-id="b5ace-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="b5ace-123">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="b5ace-123">**Status**</span></span> | <span data-ttu-id="b5ace-124">適格性オプションの状態。</span><span class="sxs-lookup"><span data-stu-id="b5ace-124">The status of the eligibility option.</span></span> <span data-ttu-id="b5ace-125">適格性オプション状態が無効に設定されている場合は、個人の連絡先に対して、その個人連絡先の適格性オプションを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="b5ace-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="b5ace-126">**リレーションシップ**</span><span class="sxs-lookup"><span data-stu-id="b5ace-126">**Relationship**</span></span> | <span data-ttu-id="b5ace-127">個人の連絡先と従業員の関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="b5ace-128">このフィールドは、連絡先の適格性コードがリレーションシップに設定されている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="b5ace-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="b5ace-129">**年齢**</span><span class="sxs-lookup"><span data-stu-id="b5ace-129">**Age**</span></span> | <span data-ttu-id="b5ace-130">給付金プランの受給資格を持つ個人連絡先の最大年齢。</span><span class="sxs-lookup"><span data-stu-id="b5ace-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="b5ace-131">このフィールドは、リレーションシップを選択した場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="b5ace-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="b5ace-132">この年齢は、個人の連絡先の計算された年齢と比較されます。</span><span class="sxs-lookup"><span data-stu-id="b5ace-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="b5ace-133">計算された年齢: (補充日 – 個人連絡先の生年月日 / 365)。</span><span class="sxs-lookup"><span data-stu-id="b5ace-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="b5ace-134">この数値は、常に整数です。</span><span class="sxs-lookup"><span data-stu-id="b5ace-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="b5ace-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5ace-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]