---
title: 派生テスト ケース
description: このトピックでは、Regression Suite Automation Tool を使用して、複数のコンフィギュレーションで同じテスト ケースを実行する方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bbb7911fcb79202790ec2c56ce5b2f1de3dd093
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036600"
---
# <a name="derived-test-cases"></a><span data-ttu-id="21385-103">派生テスト ケース</span><span class="sxs-lookup"><span data-stu-id="21385-103">Derived test cases</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21385-104">Regression Suite Automation Tool (RSAT) を使用すると、複数のテスト ケースを使用して同じタスク記録を使用できるので、異なるデータ構成を使用してタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="21385-104">The Regression suite automation tool (RSAT) lets you use the same task recording with multiple test cases, so that you can run a task with different data configurations.</span></span> <span data-ttu-id="21385-105">Regression Suite Automation Tool でテストケースを選択し、**新規 > 派生テスト ケースの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="21385-105">Select a test case in the Regression suite automation tool and then select **New > Create Derived Test Case**.</span></span> <span data-ttu-id="21385-106">これにより、 Azure DevOps に子テスト ケースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="21385-106">This creates a child test case in Azure DevOps.</span></span> <span data-ttu-id="21385-107">結果として派生したテスト ケースは、 Azure DevOps の親テスト ケースにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="21385-107">The resulting derived test case is linked to its parent test case in Azure DevOps.</span></span> <span data-ttu-id="21385-108">Excel パラメーター ファイルが添付されていますが、記録ファイルはありません。</span><span class="sxs-lookup"><span data-stu-id="21385-108">It has an Excel parameters file attached but no recording file.</span></span> <span data-ttu-id="21385-109">派生したテスト ケースは、選択した **派生** 列と同じテスト スイートの下の Regression Suite Automation Tool グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="21385-109">The derived test case will appear in the Regression suite automation tool grid under the same test suite with the **Derived** column selected.</span></span> <span data-ttu-id="21385-110">既定では、派生したテスト ケースに、親テスト ケースと数値の接尾語に基づいた名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="21385-110">By default, derived test cases are named after their parent test case with a numeric suffix.</span></span>

<span data-ttu-id="21385-111">次の図では、**販売注文の作成と検証 - v2** という名前のテスト ケースからの派生テスト ケースが作成されています。</span><span class="sxs-lookup"><span data-stu-id="21385-111">In the following image, a derived test case has been created from a test case named **Create a Sales Order and Validate - v2**.</span></span> <span data-ttu-id="21385-112">(Azure DevOps の) 派生テスト ケースに **販売注文の作成と検証 - v2 (検証に失敗)** という名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="21385-112">The derived test case has been renamed (in Azure DevOps) to **Create a Sales Order and Validate - v2 (Fail validation)**.</span></span>

![派生テスト ケースの例](media/derived-test-case.png)

<span data-ttu-id="21385-114">Azure DevOps において、派生テスト ケースは **販売注文の作成と検証 - v2** テスト ケースの子項目であり、特別なキーワード **RSAT:DerivedTestSteps** でタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="21385-114">In Azure DevOps, a derived test case is a child item of the **Create a Sales Order and Validate - v2** test case and is tagged with the special keyword **RSAT:DerivedTestSteps**.</span></span>

![自動的に作成された派生テスト ケースの例](media/derived-1.png)

<span data-ttu-id="21385-116">派生テスト ケースを実行すると、親テスト ケースの記録と Excel パラメーター ファイルのコピーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="21385-116">When you run a derived test case, it will use the recording of its parent test case and its own copy of the Excel parameters file.</span></span> <span data-ttu-id="21385-117">これにより、複数の記録を維持することなく、異なるパラメーターで同じテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="21385-117">This will allow you to run the same test with different parameters without the need to maintain more than one recording.</span></span>

<span data-ttu-id="21385-118">派生テスト ケースは、親テスト ケースと同じテスト スイートの一部である必要はなく、他のスイートで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="21385-118">A derived test case does not need to be part of the same test suite as its parent test case, and you can use it in another suite.</span></span> <span data-ttu-id="21385-119">派生テスト ケースの名前を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="21385-119">You can also rename a derived test case.</span></span> <span data-ttu-id="21385-120">派生テスト ケースの Excel パラメーター ファイルを編集して、親テスト ケースとは異なるユーザー、会社、または異なる入力や検証パラメーターで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="21385-120">You can edit the Excel parameters file of a derived test case to run it with a different user, a different company, or with different input and validation parameters than its parent test case.</span></span>
