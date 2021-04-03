---
title: 職務分掌の設定
description: 異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562500"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="2c08f-103">職務分掌の設定</span><span class="sxs-lookup"><span data-stu-id="2c08f-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c08f-104">異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="2c08f-105">この概念は職務分掌と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="2c08f-106">たとえば、同じ担当者が、商品受入の確認と仕入先への支払処理の両方を実施するのは望ましくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2c08f-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="2c08f-107">職務分掌により、不正のリスクを減らし、エラーや反則を検出できます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="2c08f-108">職務分掌を使用して、内部管理ポリシーを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="2c08f-109">ルールを作成するには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="2c08f-110">この手順を完了するには、システム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c08f-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="2c08f-111">**システム管理** > **セキュリティ** > **職務分掌**  > **職務分掌ルール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="2c08f-112">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c08f-112">Click **New**.</span></span>
3. <span data-ttu-id="2c08f-113">**名前** フィールドに、ルールの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="2c08f-114">**最初の職務権限** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2c08f-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c08f-116">ルールによって制御される最初の職務を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="2c08f-117">**2 番目の職務権限** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="2c08f-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c08f-119">ルールによって制御される 2 番目の職務を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="2c08f-120">**重要度** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="2c08f-121">同じユーザーまたはロールが両方の職務を実行するときに発生するリスクの重要度を選択します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="2c08f-122">**セキュリティ リスク** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="2c08f-123">セキュリティ リスクの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="2c08f-124">**セキュリティ対策** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="2c08f-125">セキュリティ リスクを軽減するために実行するアクションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c08f-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="2c08f-126">たとえば、プロセスの詳細確認の実施、月次管理確認の実施、または他の部門とのリソースの共有により、リスクを軽減することができます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="2c08f-127">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2c08f-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="2c08f-128">職務の分離に関するルールへの準拠は、ルールを作成する際には検証されません。</span><span class="sxs-lookup"><span data-stu-id="2c08f-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="2c08f-129">既存のロールの競合を作成するルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2c08f-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="2c08f-130">既存のユーザー ロールの割り当てが、新しいルールと競合している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2c08f-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="2c08f-131">ルールを作成または変更した後で、コンプライアンスを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c08f-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="2c08f-132">詳細については、[職務分掌の競合の識別と解決](identify-resolve-conflicts-segregation-duties.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="2c08f-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]