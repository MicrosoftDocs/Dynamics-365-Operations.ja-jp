---
title: 小売トランザクションを編集するために Excel ブックを作成する
description: このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Excel ブックを作成する方法について説明します。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a2d41dd0470a4abae1a8238be8f1549fb094a026
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795742"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="dab5f-103">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="dab5f-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dab5f-104">このトピックでは、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Excel ブックを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dab5f-105">概要</span><span class="sxs-lookup"><span data-stu-id="dab5f-105">Overview</span></span>

<span data-ttu-id="dab5f-106">事前定義された Excel テンプレートがあり、顧客はシステムのさまざまな部分からアクセスでき、小売トランザクションを編集および監査するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="dab5f-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="dab5f-107">ただし、顧客は、この目的のためにカスタムの Excel ブックを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dab5f-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="dab5f-108">Excel ブックの作成と構成</span><span class="sxs-lookup"><span data-stu-id="dab5f-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="dab5f-109">小売トランザクションを編集できるように、Excel ブックを作成して構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dab5f-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="dab5f-110">Excel を開き、空白のブックを作成します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="dab5f-111">**挿入** タブで **個人用アドイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="dab5f-112">右ウィンドウで、**サーバー情報の追加** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="dab5f-113">サーバーの URL を入力して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dab5f-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="dab5f-114">「アプレットの登録が見つかりません」というエラー メッセージが表示された場合は、次の手順に従って問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="dab5f-115">Commerce で、**システム管理 \> 設定 \> Office アプリのパラメータ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="dab5f-116">**アプリケーション パラメータ** クイックタブで **アプリのパラメーターの初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="dab5f-117">確認のメッセージボックスで **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="dab5f-118">**登録済みアプレット** クイックタブで **アプレットの登録の初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="dab5f-119">必要に応じて前の 3 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="dab5f-120">**デザイン** を選択してから **テーブルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="dab5f-121">変更する必要のあるデータに基づいて、編集のために Excel ブックに追加する必要があるエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="dab5f-122">次のテーブルを参照として使用します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="dab5f-123">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="dab5f-123">Transaction type</span></span> | <span data-ttu-id="dab5f-124">使用するデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="dab5f-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="dab5f-125">現金売りトランザクション、オンライン注文、非同期顧客注文、非同期顧客見積</span><span class="sxs-lookup"><span data-stu-id="dab5f-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="dab5f-126">トランザクション (監査可能)、販売トランザクション (監査可能)、支払トランザクション (監査可能)、税金トランザクション (監査可能)、割引トランザクション (監査可能)、諸費用トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="dab5f-127">銀行入金</span><span class="sxs-lookup"><span data-stu-id="dab5f-127">Bank drop</span></span> | <span data-ttu-id="dab5f-128">トランザクション (監査可能)、銀行入支払/入金トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="dab5f-129">金庫保管</span><span class="sxs-lookup"><span data-stu-id="dab5f-129">Safe drop</span></span> | <span data-ttu-id="dab5f-130">トランザクション (監査可能)、金庫保管支払/入金トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="dab5f-131">支払/入金申告</span><span class="sxs-lookup"><span data-stu-id="dab5f-131">Tender declaration</span></span> | <span data-ttu-id="dab5f-132">トランザクション (監査可能)、支払/入金申告トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="dab5f-133">収入、経費</span><span class="sxs-lookup"><span data-stu-id="dab5f-133">Income, Expense</span></span> | <span data-ttu-id="dab5f-134">トランザクション (監査可能)、収入/経費トランザクション (監査可能)、支払トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="dab5f-135">開始金額の申告、支払/入金の削除、釣銭入力、釣銭支払/入金、請求書の支払、顧客預金</span><span class="sxs-lookup"><span data-stu-id="dab5f-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="dab5f-136">トランザクション (監査可能)、支払トランザクション (監査可能)</span><span class="sxs-lookup"><span data-stu-id="dab5f-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="dab5f-137">各 Excel ブックにデータ エンティティを 1 つだけ追加することが重要です。</span><span class="sxs-lookup"><span data-stu-id="dab5f-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="dab5f-138">また、鍵の記号でマークされているすべてのフィールドを、関連するブックに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dab5f-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="dab5f-139">ブックを構成した後、必要なフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="dab5f-140">ファイル内のすべてのワークシートに同じフィルターを適用してください。</span><span class="sxs-lookup"><span data-stu-id="dab5f-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="dab5f-141">Excel ファイルに大量のデータを読み込まないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="dab5f-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="dab5f-142">そうしない場合、パフォーマンスが影響を受けたり、Excel とシステムの速度が低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dab5f-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="dab5f-143">ファイルのフィルターとして、常に "会社" と "明細書番号" または "トランザクション番号" を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="dab5f-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="dab5f-144">フィルターを構成した後、**更新** を選択してデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="dab5f-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="dab5f-145">必要なデータを編集し、公開します。</span><span class="sxs-lookup"><span data-stu-id="dab5f-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="dab5f-146">**公開** ボタンを使用できない場合、一部の重要なフィールドが Excel ブックに追加されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="dab5f-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dab5f-147">追加リソース</span><span class="sxs-lookup"><span data-stu-id="dab5f-147">Additional resources</span></span>

[<span data-ttu-id="dab5f-148">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="dab5f-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="dab5f-149">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="dab5f-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="dab5f-150">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="dab5f-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="dab5f-151">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="dab5f-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]