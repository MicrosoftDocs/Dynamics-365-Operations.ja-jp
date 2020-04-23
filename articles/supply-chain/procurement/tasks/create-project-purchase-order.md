---
title: プロジェクト発注書の作成
description: この手順では、プロジェクト発注書の作成方法を説明します。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88fa6298d91398e86e2d83e3163707ff36d9e8d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207764"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="c3cf7-103">プロジェクト発注書の作成</span><span class="sxs-lookup"><span data-stu-id="c3cf7-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3cf7-104">この手順では、プロジェクト発注書の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="c3cf7-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c3cf7-106">[プロジェクト管理および会計] > [プロジェクト] > [すべてのプロジェクト] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="c3cf7-107">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c3cf7-108">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c3cf7-109">[品目作業] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-109">Click Item task.</span></span>
5. <span data-ttu-id="c3cf7-110">[発注書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-110">Click Purchase order.</span></span>
6. <span data-ttu-id="c3cf7-111">[仕入先] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="c3cf7-112">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c3cf7-113">これらの手順は必須ではありませんが、これらは発注書明細行の既定のサイトと倉庫を設定することにより、発注書を簡略化します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="c3cf7-114">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="c3cf7-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-115">Click OK.</span></span>
10. <span data-ttu-id="c3cf7-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="c3cf7-117">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c3cf7-118">これは品目番号または調達カテゴリのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="c3cf7-119">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="c3cf7-120">[プロジェクト] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-120">Click the Project tab.</span></span>
    * <span data-ttu-id="c3cf7-121">販売と原価価格が使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="c3cf7-122">必要であっても使用できない場合は、情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="c3cf7-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3cf7-123">Click Save.</span></span>

