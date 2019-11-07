---
title: 派生テスト ケース
description: このトピックでは、Regression Suite Automation Tool を使用して、複数のコンフィギュレーションで同じテスト ケースを実行する方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d485eb8088af8a962e32ab0eb42232e49b5e78d2
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570537"
---
# <a name="derived-test-cases"></a><span data-ttu-id="48c62-103">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="48c62-103">Derived test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48c62-104">Regression Suite Automation Tool を使用すると、複数のコンフィギュレーションで同じテスト ケースを実行できます。</span><span class="sxs-lookup"><span data-stu-id="48c62-104">The Regression suite automation tool lets you execute the same test case with multiple configurations.</span></span> <span data-ttu-id="48c62-105">これを行うには、Regression Suite Automation Tool でテストケースを選択し、 **新規 > 派生テストケースの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48c62-105">To do this, select a test case in the Regression suite automation tool and then select **New > Create Derived Test Case**.</span></span> <span data-ttu-id="48c62-106">これにより、 Azure DevOps に子テスト ケースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="48c62-106">This creates a child test case in Azure DevOps.</span></span> <span data-ttu-id="48c62-107">結果として派生したテスト ケースは、 Azure DevOps の親テスト ケースにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="48c62-107">The resulting derived test case is linked to its parent test case in Azure DevOps.</span></span> <span data-ttu-id="48c62-108">Excel パラメーター ファイルが添付されていますが、記録ファイルはありません。</span><span class="sxs-lookup"><span data-stu-id="48c62-108">It has an Excel parameters file attached but no recording file.</span></span> <span data-ttu-id="48c62-109">派生したテスト ケースは、選択した **派生** 列と同じテスト スイートの下の Regression Suite Automation Tool グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="48c62-109">The derived test case will appear in the Regression suite automation tool grid under the same test suite with the **Derived** column selected.</span></span> <span data-ttu-id="48c62-110">派生したテスト ケースには、親テスト ケースに数字の接尾語が付いた名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="48c62-110">Derived test cases are named after their parent test case with a numeric suffix.</span></span>

<span data-ttu-id="48c62-111">次の図では、 **仕入先の作成** というテスト ケースから派生テスト ケースが作成されています。</span><span class="sxs-lookup"><span data-stu-id="48c62-111">In the following image, a derived test case has been created from a test case called **Create Vendor**.</span></span>

![仕入先の作成という名前のテスト ケースから作成された派生テスト ケースの例](media/derived-test-case.png)
 
<span data-ttu-id="48c62-113">派生テスト ケースは、 Azure DevOps で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="48c62-113">The derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="48c62-114">これは、 **仕入先の作成 テスト** ケースの子品目であり、特別なキーワード **RSAT: DerivedTestSteps** でタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="48c62-114">It is a child item of the **Create Vendor** test case and is tagged with the special keyword **RSAT:DerivedTestSteps**.</span></span>

![自動的に作成された派生テスト ケースの例](media/derived-1.png)
 
<span data-ttu-id="48c62-116">派生テスト ケースを実行 (再生) すると、親テスト ケースの記録と Excel パラメーター ファイルのコピーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="48c62-116">When you run (play back) a derived test case, it will use the recording of its parent test case and its own copy of the Excel parameters file.</span></span> <span data-ttu-id="48c62-117">これにより、複数の記録を維持することなく、異なるパラメーターで同じテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="48c62-117">This will allow you to run the same test with different parameters without the need to maintain more than one recording.</span></span>

<span data-ttu-id="48c62-118">派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="48c62-118">A derived test case does not need to be part of the same test suite as its parent test case.</span></span> <span data-ttu-id="48c62-119">他のスイートに移動できます。</span><span class="sxs-lookup"><span data-stu-id="48c62-119">You can move it to another suite.</span></span>
