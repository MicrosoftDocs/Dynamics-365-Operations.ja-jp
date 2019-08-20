---
title: 職務分掌の設定
description: 異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3682dbcb72588633fb6b3fe4cbda99f422163a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851266"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="9cc55-103">職務分掌の設定</span><span class="sxs-lookup"><span data-stu-id="9cc55-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cc55-104">異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="9cc55-105">この概念は職務分掌と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="9cc55-106">たとえば、同じ担当者が、商品受入の確認と仕入先への支払処理の両方を実施するのは望ましくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9cc55-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="9cc55-107">職務分掌により、不正のリスクを減らし、エラーや反則を検出できます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="9cc55-108">職務分掌を使用して、内部管理ポリシーを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="9cc55-109">ルールを作成するには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="9cc55-110">この手順を完了するには、システム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cc55-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="9cc55-111">この手順の作成に使用するデモ データの会社は DAT です。</span><span class="sxs-lookup"><span data-stu-id="9cc55-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="9cc55-112">[システム管理] > [セキュリティ] > [職務分掌] > [職務分掌ルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="9cc55-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cc55-113">Click New.</span></span>
3. <span data-ttu-id="9cc55-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9cc55-115">ルールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="9cc55-116">[最初の職務権限] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9cc55-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9cc55-118">ルールによって制御される最初の職務を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="9cc55-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cc55-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9cc55-120">[2 番目の職務権限] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9cc55-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9cc55-122">ルールによって制御される 2 番目の職務を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="9cc55-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cc55-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9cc55-124">[重要度] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="9cc55-125">同じユーザーまたはロールが両方の職務を実行するときに発生するリスクの重要度を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="9cc55-126">[セキュリティ リスク] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="9cc55-127">セキュリティ リスクの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="9cc55-128">[セキュリティ対策] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="9cc55-129">セキュリティ リスクを軽減するために実行するアクションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9cc55-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="9cc55-130">たとえば、プロセスの詳細確認の実施、月次管理確認の実施、または他の部門とのリソースの共有により、リスクを軽減することができます。</span><span class="sxs-lookup"><span data-stu-id="9cc55-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="9cc55-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9cc55-131">Click Save.</span></span>

