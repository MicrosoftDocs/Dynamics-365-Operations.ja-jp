---
title: 割増償却を使用する固定資産の作成
description: 日本では、固定資産は特定の条件下で増加償却額を転記することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27b94e8e8dd11101d4a9a2c6b0fe05a6a9ccb0f8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175148"
---
# <a name="create-a-fixed-asset-with-additional-depreciation"></a><span data-ttu-id="38e4b-103">割増償却を使用する固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="38e4b-103">Create a fixed asset with additional depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38e4b-104">日本では、固定資産は特定の条件下で増加償却額を転記することができます。</span><span class="sxs-lookup"><span data-stu-id="38e4b-104">In Japan, a fixed asset is permitted to post an additional depreciation amount, under certain conditions.</span></span> 



<span data-ttu-id="38e4b-105">この手順を使用して、割増減価償却プロファイルのある固定資産の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-105">Use this procedure to learn how to create a fixed asset with additional depreciation profile.</span></span>



<span data-ttu-id="38e4b-106">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38e4b-106">In order to complete this procedure, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="38e4b-107">これはデモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="38e4b-107">This was created using the demo data company JPMF.</span></span>


## <a name="create-a-fixed-assset-and-assign-an-additional-depreciation-profile-to-it"></a><span data-ttu-id="38e4b-108">固定資産の作成および割増減価償却プロファイルの割り当て</span><span class="sxs-lookup"><span data-stu-id="38e4b-108">Create a fixed assset and assign an additional depreciation profile to it</span></span>
1. <span data-ttu-id="38e4b-109">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-109">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="38e4b-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e4b-110">Click New.</span></span>
3. <span data-ttu-id="38e4b-111">[固定資産グループ] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-111">In the Fixed asset group field, select a value.</span></span>
4. <span data-ttu-id="38e4b-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="38e4b-113">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e4b-113">Click Books.</span></span>
6. <span data-ttu-id="38e4b-114">[減価償却] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-114">Expand the Depreciation section.</span></span>
7. <span data-ttu-id="38e4b-115">[特別減価償却プロファイル] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-115">In the Extraordinary depreciation profile field, enter or select a value.</span></span>
8. <span data-ttu-id="38e4b-116">[特別減価償却] フィールド グループ下で、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-116">under the Extraordinary depreciation field group, enter a date</span></span>
    * <span data-ttu-id="38e4b-117">割増償却は、この日の翌日から開始します。</span><span class="sxs-lookup"><span data-stu-id="38e4b-117">The additional depreciation will start from the next day of this date.</span></span>  
9. <span data-ttu-id="38e4b-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38e4b-118">Click Save.</span></span>
