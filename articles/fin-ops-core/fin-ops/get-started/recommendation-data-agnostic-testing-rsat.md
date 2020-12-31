---
title: Regression Suite Automation Tool を使用したデータ認識不可能テスト
description: このトピックでは、Regression Suite Automation Tool を使用したデータ認識不可能テストに関する推奨事項について説明します。
author: kfend
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7fd1fc4756e74a5d07ffae533b6b9837b960f17a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693753"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a><span data-ttu-id="de7a4-103">Regression Suite Automation Tool を使用したデータ認識不可能テスト</span><span class="sxs-lookup"><span data-stu-id="de7a4-103">Data agnostic testing using the Regression Suite Automation Tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de7a4-104">ERP アプリケーションの機能の検証は、完全にデータ認識不可能ではありませんが、テストをするために複数のフェーズとアプローチがあります。</span><span class="sxs-lookup"><span data-stu-id="de7a4-104">While the functional validation of an ERP application can’t be fully data agnostic, there are multiple phases and approaches for testing.</span></span> <span data-ttu-id="de7a4-105">テスト フェーズには次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-105">These testing phases include:</span></span>  

- <span data-ttu-id="de7a4-106">SysTest フレームワーク</span><span class="sxs-lookup"><span data-stu-id="de7a4-106">SysTest framework</span></span>
- <span data-ttu-id="de7a4-107">ATL フレームワーク</span><span class="sxs-lookup"><span data-stu-id="de7a4-107">ATL frameowrk</span></span>
- <span data-ttu-id="de7a4-108">Regression Suite Automation Tool (RSAT)</span><span class="sxs-lookup"><span data-stu-id="de7a4-108">Regression Suite Automation Tool (RSAT)</span></span>

<span data-ttu-id="de7a4-109">[![テストの分類ピラミッド](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span><span class="sxs-lookup"><span data-stu-id="de7a4-109">[![Test classification pyramid](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span></span>

## <a name="overview"></a><span data-ttu-id="de7a4-110">概要</span><span class="sxs-lookup"><span data-stu-id="de7a4-110">Overview</span></span>
-   <span data-ttu-id="de7a4-111">**SysTest フレームワーク** – SysTest フレームワークは、単体テストの書き込みに対して信頼性があります。</span><span class="sxs-lookup"><span data-stu-id="de7a4-111">**SysTest framework** – The SysTest framework is reliable for writing unit tests.</span></span> <span data-ttu-id="de7a4-112">単体テストは一般にメソッドまたは関数のテストで、常にデータ認識不可能性があり、テストの一部として提供されている入力データにのみ依存しています。</span><span class="sxs-lookup"><span data-stu-id="de7a4-112">Because unit tests are generally testing a method or function, they should always be data agnostic and dependent only on the input data that is provided as part of the test.</span></span>
-   <span data-ttu-id="de7a4-113">**ATL フレームワーク** – Microsoft には SysTest フレームワークが抽象化された ATL フレームワークがあり、機能テストの書き込みをより簡易で信頼性のあるものにします。</span><span class="sxs-lookup"><span data-stu-id="de7a4-113">**ATL framework** – Microsoft has an ATL framework that is an abstraction on the SysTest framework and makes functional test writing much more simple and reliable.</span></span> <span data-ttu-id="de7a4-114">このフレームワークは、コンポーネント テストまたは簡易な統合テストを書き込むために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-114">This framework should be used for writing component tests or simple integration tests.</span></span>
-   <span data-ttu-id="de7a4-115">**RSAT** – RSAT は、統合テストおよび業務サイクル テストに使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-115">**RSAT** – The RSAT is used for integration tests and business cycle tests.</span></span> <span data-ttu-id="de7a4-116">回帰検証テストとも呼ばれる業務サイクル テストは、既存のデータに依存しています。</span><span class="sxs-lookup"><span data-stu-id="de7a4-116">The business cycle tests, also called the regression validation tests, are dependent on existing data.</span></span> <span data-ttu-id="de7a4-117">ただし、追加要素を考慮した場合、これらのテストがデータ認識不可能になることがあります。</span><span class="sxs-lookup"><span data-stu-id="de7a4-117">However, these tests can become data agnostic if you consider additional factors.</span></span> 

    - <span data-ttu-id="de7a4-118">o 単体テストおよびコンポーネント テストのレベルが低く、完全にデータ認識不可能になる場合 (既存のデータセットに依存していない)、業務サイクルまたは再帰検証テストは一部の既存のデータに依存しています。</span><span class="sxs-lookup"><span data-stu-id="de7a4-118">o Where unit tests and component tests are low level and can fully be data agnostic (not dependent on existing dataset), the business cycle or regression validation tests are dependent on some existing data.</span></span> <span data-ttu-id="de7a4-119">このデータには、設定、コンフィギュレーション設定 (パラメーター)、およびマスター データ (顧客、仕入先、品目など) が含まれますが、トランザクション データは含まれません。</span><span class="sxs-lookup"><span data-stu-id="de7a4-119">This data includes setup, configuration settings (parameters), and master data (customer, vendors, items, etc.), but never transaction data.</span></span> <span data-ttu-id="de7a4-120">テスト中にいずれかが変更中である場合、最終テストの一部として元に戻されることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="de7a4-120">Make sure that during the test, if any of these are being changed, that they are reverted back as part of the final test.</span></span>
    - <span data-ttu-id="de7a4-121">特定のレコードを選択する代わりに、特定の基準に基づいてマスター データを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7a4-121">Select master data based on certain criteria instead of selecting a particular record.</span></span> <span data-ttu-id="de7a4-122">たとえば、分析コード値および有効在庫数に基づいて品目を選択する場合、その値で製品リストをフィルター処理を行い、最初の品目を選択して、未来のテストに使用される番号をコピーします。</span><span class="sxs-lookup"><span data-stu-id="de7a4-122">For example, if you want to select an item based on its dimension values and stock availability, filter the product list with those values, select the first item, and copy the number to be used for future tests.</span></span> <span data-ttu-id="de7a4-123">顧客、仕入先、または品目などの簡易なマスター データ明細行の場合、自動化の一部として作成され、連鎖による未来のテストで使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-123">If it’s a simple master data line such as customer, vendor, or item, it can be created as part of the automation and used in future tests through chaining.</span></span> 
    - <span data-ttu-id="de7a4-124">o 請求書番号などを番号順序で、または =TEXT(NOW(),"yyyymmddhhmm") のような Microsoft Excel の関数により固有識別子入力をします。</span><span class="sxs-lookup"><span data-stu-id="de7a4-124">o Enter the unique identifiers, such as invoice numbers, through the number sequence or by using Microsoft Excel functions such as =TEXT(NOW(),"yyyymmddhhmm").</span></span> <span data-ttu-id="de7a4-125">この関数により、アクションが発生した時間を追跡できるように、毎分固有の番号が提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-125">This function will provide a unique number every minute, which allows you to track when the action happened.</span></span> <span data-ttu-id="de7a4-126">これは、製品受領書番号や仕入先請求書番号などの変数に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="de7a4-126">This can be used for variables such as product receipt numbers and vendor invoice numbers.</span></span> <span data-ttu-id="de7a4-127">これらのテストは、復元を必要とせずに、同じデータベース上で幾度も継続して動作します。</span><span class="sxs-lookup"><span data-stu-id="de7a4-127">These tests continue to work on the same database again and again, without requiring any restoration.</span></span>
    - <span data-ttu-id="de7a4-128">既定のオプションは **自動** であるため、常に環境の **編集モード** を設定して、最初のテスト ケースとして **読み取り** または **編集** を行います。**自動** オプションは常に以前の設定を使用することができ、信頼できないテストを引き起こすことがあります。</span><span class="sxs-lookup"><span data-stu-id="de7a4-128">Always set the **Edit mode** of the environment to **Read** or **Edit** as the first test case because the default option is **Auto**. The **Auto** options always uses the previous setting and can cause unreliable tests.</span></span> 
 
    <span data-ttu-id="de7a4-129">[![オプション ページ、パフォーマンス タブ](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span><span class="sxs-lookup"><span data-stu-id="de7a4-129">[![Options page, Performance tab](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span></span>
 
    - <span data-ttu-id="de7a4-130">一般的な検証の代わりに、特定のトランザクションに対するフィルター処理をした後にのみ検証します。</span><span class="sxs-lookup"><span data-stu-id="de7a4-130">Only validate after you filter on a particular transaction instead of generic validation.</span></span> <span data-ttu-id="de7a4-131">たとえば、レコード数について、検証が他のすべてのトランザクションを除外するように、トランザクション番号またはトランザクション日付に対してフィルター処理を行います。</span><span class="sxs-lookup"><span data-stu-id="de7a4-131">For example, for the number of records, filter for the transaction number or the transaction date so that the validation excludes all other transactions.</span></span> 
    - <span data-ttu-id="de7a4-132">顧客残高または予算チェックを確認している場合、値を先に保存してトランザクション値を追加することにより、固定の予測値を検証する代わりに、予測された結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="de7a4-132">If you are checking a customer balance or budget check, save the value first and then add your transaction value to validate the expected result instead of validating a fixed expected value.</span></span> 
 
