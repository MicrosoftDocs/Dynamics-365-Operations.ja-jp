---
title: 作業指示書へのエラーの追加
description: このトピックでは、資産管理における作業指示書へのエラー登録を追加する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875761"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="3fb4e-103">作業指示書へのエラーの追加</span><span class="sxs-lookup"><span data-stu-id="3fb4e-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3fb4e-104">エラー デザイナーで設定されたエラーを作業指示書に追加できます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="3fb4e-105">作業指示書で選択された資産には、1 つ以上のエラー レコードが接続されている資産タイプが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="3fb4e-106">設定の詳細については、[エラー管理](../setup-for-work-orders/fault-management.md) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="3fb4e-107">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3fb4e-108">一覧で、エラー登録を行う作業指示書を選択し、**資産エラー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="3fb4e-109">**現象**クイック タブの、**明細行の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="3fb4e-110">**エラー** フィールドには、エラー番号が連番で自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="3fb4e-111">**エラー現象**フィールドで該当する現象を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="3fb4e-112">**エラー領域**と**エラー タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="3fb4e-113">**エラー日付**フィールドには、現在の日付が自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="3fb4e-114">必要に応じて、別の日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="3fb4e-115">**選択した現象の原因**クイック タブで、問題の原因を説明する明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="3fb4e-116">**選択した現象の救済**クイック タブで、問題の実行可能なソリューションを説明する明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="3fb4e-117">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-117">Click **Save**.</span></span>

![図 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="3fb4e-119">資産エラーの表示</span><span class="sxs-lookup"><span data-stu-id="3fb4e-119">View asset faults</span></span>

<span data-ttu-id="3fb4e-120">**資産エラー**の一覧では、資産に登録されているすべてのエラーの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="3fb4e-121">**資産管理** > **照会** > **資産エラー** > **資産エラー**の順にクリックして、一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="3fb4e-122">資産エラー レポートの印刷</span><span class="sxs-lookup"><span data-stu-id="3fb4e-122">Print asset fault report</span></span>

<span data-ttu-id="3fb4e-123">**すべての資産**リスト ページから、すべてのエラー登録を表示する資産エラー レポートおよびエラー統計のグラフィックな概要を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="3fb4e-124">**資産管理**  >  **共通**  >  **資産**  >  **全資産**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="3fb4e-125">**資産**リストで、印刷するエラー レポートの資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="3fb4e-126">**一般**タブ > **レポート セクション**で、**資産エラー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="3fb4e-127">特定の期間を挿入するか、エラー タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="3fb4e-128">**OK** をクリックしてレポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="3fb4e-129">**資産管理** > **レポート** > **資産** > **資産エラー**の順にクリックして、複数の資産または資産タイプに対するエラー レポートを印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="3fb4e-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

