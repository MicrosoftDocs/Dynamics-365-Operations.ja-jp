---
title: 固定資産の作成
description: このトピックでは、固定資産リスト ページから新しい固定資産レコードを作成する方法について説明します。
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817104"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="29b14-103">固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="29b14-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29b14-104">このトピックでは、**固定資産** リスト ページから新しい固定資産レコードを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="29b14-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="29b14-105">固定資産グループに割り当てられている番号順序に基づいて、システムが自動的に資産番号を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="29b14-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="29b14-106">固定資産テンプレートを使用して Microsoft Excel アドインで資産をインポートする場合、または別のインポート ジョブを使用する場合は、システムが固定資産レコードを自動的に作成し、資産番号を増加させます。</span><span class="sxs-lookup"><span data-stu-id="29b14-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="29b14-107">資産レコードを手動で作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29b14-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="29b14-108">**ナビゲーション ウィンドウ \> モジュール \> 固定資産 \> 固定資産 \> 固定資産** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29b14-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="29b14-109">**アクション ウィンドウ** で、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29b14-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="29b14-110">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="29b14-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="29b14-111">**固定資産パラメーター** および **固定資産グループ** で **固定資産の自動採番機能** を有効にした場合、**番号** は既定になります。</span><span class="sxs-lookup"><span data-stu-id="29b14-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="29b14-112">そうでない場合、固定資産を識別する固有番号を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29b14-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="29b14-113">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="29b14-114">この資産について業務に必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="29b14-115">**アクション ウィンドウ** で、**帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29b14-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="29b14-116">**取得日付** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="29b14-117">**取得価格** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="29b14-118">この帳簿に業務上必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="29b14-119">残りの帳簿に業務上必要な追加情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="29b14-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="29b14-120">Close the page.</span></span>

<span data-ttu-id="29b14-121">Excel アドインを使用して、または **データ管理** ワークスペースからインポート ジョブを実行することによって、固定資産をインポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="29b14-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="29b14-122">インポートを実行する前に、テンプレートの必須フィールドの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29b14-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="29b14-123">Excel アドインのテンプレートに固定資産番号を定義していない場合、またはデータ管理で、インポートした資産ごとに固定資産番号が作成され、それぞれの番号順序が自動的に増やされます。</span><span class="sxs-lookup"><span data-stu-id="29b14-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="29b14-124">ただし、テンプレートで資産をインポートして資産番号を定義した場合、番号順序は自動的に **増えません**。</span><span class="sxs-lookup"><span data-stu-id="29b14-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="29b14-125">この場合、管理者が手動で番号順序を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29b14-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="29b14-126">Excel アドインのテンプレートで固定資産番号を定義した場合は、定義されている固定資産番号が使用され、番号順序が増加します。</span><span class="sxs-lookup"><span data-stu-id="29b14-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="29b14-127">減価償却を転記 すると、**帳簿** ページで  **サービスの開始** と **減価償却の実行日** フィールドがロックされます。</span><span class="sxs-lookup"><span data-stu-id="29b14-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="29b14-128">また、どちらのフィールドもデータ エンティティから更新されます。</span><span class="sxs-lookup"><span data-stu-id="29b14-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="29b14-129">トランザクションが関連付けられた帳簿に転記されている場合や、新たに作成された固定資産が仕訳帳明細行に入力済で転記されていない場合、固定資産レコードは削除されません。</span><span class="sxs-lookup"><span data-stu-id="29b14-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]