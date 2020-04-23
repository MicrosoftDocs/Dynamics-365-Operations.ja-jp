---
title: 倉庫の作業ポリシーの設定 (申請、2016 年 5 月)
description: 倉庫のプロセスは必ずしも倉庫作業を含みません。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62fbf2f44216c300af5e092f5dbd05ef2239321b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216784"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="34346-103">倉庫の作業ポリシーの設定 (申請、2016 年 5 月)</span><span class="sxs-lookup"><span data-stu-id="34346-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34346-104">倉庫のプロセスは必ずしも倉庫作業を含みません。</span><span class="sxs-lookup"><span data-stu-id="34346-104">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="34346-105">作業ポリシーを定義して、原材料のピッキングの作業の作成、および特定の場所での一連の製品に対する完成品のプット アウェイを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="34346-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="34346-106">デモ データの会社 USMF がこの記録の作成に使用されました。</span><span class="sxs-lookup"><span data-stu-id="34346-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="34346-107">このタスク ガイドでは、Dynamics AX アプリケーション 7.0.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="34346-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="34346-108">[倉庫管理] > [設定] > [作業] > [作業ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="34346-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="34346-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-109">Click New.</span></span>
3. <span data-ttu-id="34346-110">[作業ポリシー名] フィールドに、「プット アウェイ作業なし」と入力します。</span><span class="sxs-lookup"><span data-stu-id="34346-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="34346-111">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-111">Click Save.</span></span>
5. <span data-ttu-id="34346-112">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-112">Click Add.</span></span>
6. <span data-ttu-id="34346-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="34346-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="34346-114">[ワーク オーダー タイプ] フィールドで、[完成品のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="34346-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="34346-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-115">Click Add.</span></span>
9. <span data-ttu-id="34346-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="34346-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="34346-117">[ワーク オーダー タイプ] フィールドで、[連産物と副産物のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="34346-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="34346-118">[在庫場所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="34346-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="34346-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-119">Click Add.</span></span>
13. <span data-ttu-id="34346-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="34346-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="34346-121">倉庫の一覧で、「51」を入力します。</span><span class="sxs-lookup"><span data-stu-id="34346-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="34346-122">[場所] フィールドで「001」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="34346-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="34346-123">[製品] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="34346-123">Expand the Products section.</span></span>
17. <span data-ttu-id="34346-124">[製品の選択] フィールドで、[選択済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="34346-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="34346-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-125">Click Add.</span></span>
19. <span data-ttu-id="34346-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="34346-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="34346-127">[品目番号] フィールドで、「L0101」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="34346-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="34346-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34346-128">Click Save.</span></span>

