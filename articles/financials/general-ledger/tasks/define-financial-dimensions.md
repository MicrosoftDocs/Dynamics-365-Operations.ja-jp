---
title: 財務分析コードの定義
description: このタスク ガイドでは、エンティティがサポートしている財務分析コードとカスタム財務分析コードの追加について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a30872daeeeb6d7d2accb07e9fdbdc84bb8dc5e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846466"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="b9bed-103">財務分析コードの定義</span><span class="sxs-lookup"><span data-stu-id="b9bed-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9bed-104">このタスク ガイドでは、エンティティがサポートしている財務分析コードとカスタム財務分析コードの追加について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="b9bed-105">ガイドでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="b9bed-106">エンティティがサポートする財務分析コードの作成</span><span class="sxs-lookup"><span data-stu-id="b9bed-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="b9bed-107">[総勘定元帳] > [勘定科目表] > [分析コード] > [財務分析コード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b9bed-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-108">Click New.</span></span>
3. <span data-ttu-id="b9bed-109">ユーザー値の使用元フィールドで、財務分析コードの基になるシステム定義のエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-109">In the User values form field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="b9bed-110">[分析コード名] フィールドに財務分析コードを説明する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="b9bed-111">名前はシステムで定義されたエンティティとは異なるものにできますが、特殊文字やスペースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="b9bed-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="b9bed-112">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-112">Click Activate.</span></span>
    * <span data-ttu-id="b9bed-113">財務分析コードを有効にすると、テーブルの財務分析コードの名前を更新し、削除された分析コードを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="b9bed-114">財務分析コードを有効化する前に分析コード値を入力できますが、財務分析コードは有効化されていないと使用できません。</span><span class="sxs-lookup"><span data-stu-id="b9bed-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="b9bed-115">有効化メッセージの [終了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="b9bed-116">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-116">Click Activate.</span></span>
    * <span data-ttu-id="b9bed-117">分析コードを特定の日時にバッチで有効化するようスケジューリングすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="b9bed-118">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-118">Click Dimension values.</span></span>
    * <span data-ttu-id="b9bed-119">分析コード値には会社固有のものがあります。</span><span class="sxs-lookup"><span data-stu-id="b9bed-119">Some dimension values are company specific.</span></span> <span data-ttu-id="b9bed-120">分析コード値リストに会社名が表示されているかどうかによって、会社固有のものかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="b9bed-121">カスタム財務分析コードの作成</span><span class="sxs-lookup"><span data-stu-id="b9bed-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="b9bed-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-122">Close the page.</span></span>
2. <span data-ttu-id="b9bed-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-123">Click New.</span></span>
3. <span data-ttu-id="b9bed-124">[値の使用元] フィールドで、カスタム分析コード を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-124">In the Use values from field, select Custom dimension.</span></span>
4. <span data-ttu-id="b9bed-125">[分析コード名] フィールドに財務分析コードを説明する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="b9bed-126">名前にはスペースや特殊文字を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9bed-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="b9bed-127">また主勘定マスクを指定して、分析コード値に対して入力できる情報の量やタイプを制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="b9bed-128">文字またはハイフンなど、各分析コード値の変化しない文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="b9bed-129">また、分析コード値が作成されるたびに変更される、番号と文字のプレースホルダーとなる番号記号 (#) とアンパサンド (&) を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="b9bed-130">番号のプレースホルダーとして番号記号 (#)、文字のプレースホルダとしてアンパサンド (&) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="b9bed-131">例: 分析コード値を CC という文字と番号 3 桁 (###) に制限する場合は、マスクの書式設定として CC-### と入力します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="b9bed-132">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-132">Click Activate.</span></span>
    * <span data-ttu-id="b9bed-133">財務分析コードを有効にすると、テーブルの財務分析コードの名前を更新し、削除された分析コードを削除します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="b9bed-134">財務分析コードを有効化する前に分析コード値を入力できますが、財務分析コードは有効化されていないと使用できません。</span><span class="sxs-lookup"><span data-stu-id="b9bed-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="b9bed-135">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-135">Click Activate.</span></span>
    * <span data-ttu-id="b9bed-136">分析コードを特定の日時にバッチで有効化するようスケジューリングすることができます。</span><span class="sxs-lookup"><span data-stu-id="b9bed-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="b9bed-137">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-137">Click Dimension values.</span></span>
8. <span data-ttu-id="b9bed-138">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9bed-138">Click New.</span></span>
9. <span data-ttu-id="b9bed-139">[分析コード値] フィールドに財務分析コード値を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="b9bed-140">[説明] フィールドに財務分析コード値を説明する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9bed-140">In the Description field, type a description that describes your financial dimension value.</span></span>

