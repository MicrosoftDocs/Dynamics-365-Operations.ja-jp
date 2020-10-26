---
title: 製品のバッチ属性の作成
description: この手順では、バッチ属性の作成方法、既定値の範囲の割り当て方法、グループに属性を含める方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8924eedfbb635ca04aa167d7f6c44872fef496fd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986314"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="f12ba-103">製品のバッチ属性の作成</span><span class="sxs-lookup"><span data-stu-id="f12ba-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f12ba-104">この手順では、バッチ属性の作成方法、既定値の範囲の割り当て方法、グループに属性を含める方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="f12ba-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="f12ba-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="f12ba-106">[在庫管理] > [設定] > [バッチ] > [バッチ属性] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="f12ba-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-107">Click New.</span></span>
3. <span data-ttu-id="f12ba-108">[属性] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="f12ba-109">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f12ba-110">[属性タイプ] フィールドで、「属性」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="f12ba-111">この手順では、小数値を有効にするために [小数] タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="f12ba-112">他の属性タイプを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="f12ba-112">You can select other attribute types.</span></span> <span data-ttu-id="f12ba-113">列挙型を選択する場合、ターゲット フィールドに値を入力する前に、列挙型リストで値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12ba-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="f12ba-114">[最小] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="f12ba-115">[最大] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="f12ba-116">[増分] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="f12ba-117">[ターゲット] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="f12ba-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-118">Click Save.</span></span>
11. <span data-ttu-id="f12ba-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f12ba-119">Close the page.</span></span>
12. <span data-ttu-id="f12ba-120">[在庫管理] > [設定] > [バッチ] > [バッチ属性グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="f12ba-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-121">Click New.</span></span>
14. <span data-ttu-id="f12ba-122">[属性グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="f12ba-123">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="f12ba-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-124">Click Save.</span></span>
17. <span data-ttu-id="f12ba-125">[グループ属性] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-125">Click Group attributes.</span></span>
18. <span data-ttu-id="f12ba-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-126">Click New.</span></span>
19. <span data-ttu-id="f12ba-127">[属性] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f12ba-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="f12ba-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f12ba-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="f12ba-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f12ba-130">属性は、いずれかのグループに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f12ba-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="f12ba-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f12ba-131">Click Save.</span></span>
23. <span data-ttu-id="f12ba-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f12ba-132">Close the page.</span></span>

