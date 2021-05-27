---
title: 品質管理テスト機器
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示のテストに使用できるテスト機器を作成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021735"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="83483-103">品質管理テスト機器</span><span class="sxs-lookup"><span data-stu-id="83483-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83483-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質指示のテストに使用できるテスト機器を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83483-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="83483-105">**テスト機器** ページを使用して、品質指示のテストを実行するために使用するデバイスに関する詳細を定義および表示します。</span><span class="sxs-lookup"><span data-stu-id="83483-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="83483-106">テスト機器はオプションです。</span><span class="sxs-lookup"><span data-stu-id="83483-106">Test instruments are optional.</span></span> <span data-ttu-id="83483-107">ただし、品質作業員が、特定のテストの実行にどのデバイスまたはツールを使用する必要があるのかを知るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="83483-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="83483-108">テスト機器の例</span><span class="sxs-lookup"><span data-stu-id="83483-108">Test instrument example</span></span>

<span data-ttu-id="83483-109">電気コンポーネントに対してさまざまなテストを実行しています。</span><span class="sxs-lookup"><span data-stu-id="83483-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="83483-110">一部のテストは、コンポーネントの電圧出力用で、1 つのテストはコンポーネントの温度用であり、もう 1つのテストはコンポーネントの重量用です。</span><span class="sxs-lookup"><span data-stu-id="83483-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="83483-111">各テストの実行には、さまざまなツール、デバイス、または設備が使用されます。</span><span class="sxs-lookup"><span data-stu-id="83483-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="83483-112">たとえば、電圧計は電圧を測定するために使用され、温度計は温度を測定するために使用され、スケールは重量を測定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="83483-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="83483-113">これらの各デバイスをテスト機器として構成し、テスト結果を記録する必要がある測定単位を指定できます。</span><span class="sxs-lookup"><span data-stu-id="83483-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="83483-114">たとえば、電圧計の結果はボルトで記録され、温度計の結果は華氏または摂氏で記録され、スケールの結果はポンドまたはキログラムで記録されます。</span><span class="sxs-lookup"><span data-stu-id="83483-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="83483-115">テスト機器の作成</span><span class="sxs-lookup"><span data-stu-id="83483-115">Create a test instrument</span></span>

1. <span data-ttu-id="83483-116">**在庫管理 \> 設定 \> 品質管理 \> テスト機器** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83483-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="83483-117">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="83483-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="83483-118">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="83483-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="83483-119">**テスト機器** – テスト機器の固有の ID または名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="83483-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="83483-120">**説明** – テスト機器の詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="83483-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="83483-121">**単位** – 機器が測定する結果の単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="83483-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="83483-122">**精度** フィールドは、選択した単位に基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="83483-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="83483-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="83483-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83483-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="83483-124">Additional resources</span></span>

- [<span data-ttu-id="83483-125">品質管理テスト</span><span class="sxs-lookup"><span data-stu-id="83483-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="83483-126">品質管理テスト グループ</span><span class="sxs-lookup"><span data-stu-id="83483-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
