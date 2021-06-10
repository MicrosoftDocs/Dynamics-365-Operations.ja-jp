---
title: ISV Studio を使用した ISV パッケージからの X++ モジュールのリンク
description: このトピックでは、ISV Studio を使用した X++ パッケージのリンクについて説明します。
author: jorisdg
ms.date: 04/08/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c6c39f7baa0b76492f4db85bc6f04787a487d71
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093906"
---
# <a name="link-x-modules-from-isv-packages-by-using-isv-studio"></a><span data-ttu-id="9e33e-103">ISV Studio を使用した ISV パッケージからの X++ モジュールのリンク</span><span class="sxs-lookup"><span data-stu-id="9e33e-103">Link X++ modules from ISV packages by using ISV Studio</span></span>

<span data-ttu-id="9e33e-104">独立系ソフトウェア ベンダー (ISVs) は、[Microsoft Power Platform ISV Studio](/powerapps/developer/data-platform/isv-app-management) を使用して、X++モジュールを登録済みの製品およびソリューションにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="9e33e-104">Independent software vendors (ISVs) can link their X++ modules to their registered products and solutions by using [Microsoft Power Platform ISV Studio](/powerapps/developer/data-platform/isv-app-management).</span></span> <span data-ttu-id="9e33e-105">リンクにより、ISV は Finance and Operations アプリでのアプリケーションの成功と使用を監視できます。</span><span class="sxs-lookup"><span data-stu-id="9e33e-105">Linking enables ISV's to monitor the success and usage of their applications in Finance and Operations apps.</span></span>

> [!NOTE]
> <span data-ttu-id="9e33e-106">X++ から ISV Studio へのリンクが正常に機能するには、顧客がすべての ISV モデルに正しいソリューション ID を持つ ISV パッケージを配置している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e33e-106">For the link from X++ into ISV Studio to work correctly, customers need to have deployed ISV packages with the correct solution ID in all the ISV models.</span></span> <span data-ttu-id="9e33e-107">また、顧客の環境はバージョン 10.0.16 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e33e-107">The customer's environment also has to be version 10.0.16 or higher.</span></span>

## <a name="find-the-product-id-in-microsoft-partner-center"></a><span data-ttu-id="9e33e-108">Microsoft パートナー センターで製品 ID を検索する</span><span class="sxs-lookup"><span data-stu-id="9e33e-108">Find the product ID in Microsoft Partner Center</span></span>

<span data-ttu-id="9e33e-109">パートナー センターにサインインし、製品の **オファーの概要** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e33e-109">Sign in to Partner Center and open the **Offer overview** page for your product.</span></span> <span data-ttu-id="9e33e-110">次の例に示すように、ブラウザの URL バーから製品 ID グローバル一意識別子 (GUID) を検索します。</span><span class="sxs-lookup"><span data-stu-id="9e33e-110">From the browser's URL bar, locate the product ID globally unique identifier (GUID), as shown in the following example.</span></span>

```HTTP
https://partner.microsoft.com/dashboard/commercial-marketplace/offers/<product-ID-GUID>/overview
```

> [!NOTE]
> <span data-ttu-id="9e33e-111">製品 ID 製品のオファー コードと一致するとは限りませんが、類似している場合があります。</span><span class="sxs-lookup"><span data-stu-id="9e33e-111">The product ID does not necessarily match the offer code of your product, although they may be similar.</span></span> <span data-ttu-id="9e33e-112">記述子でオファー コードを使用しても、ISV Studio に対して X++ モジュールを正しく識別できません。</span><span class="sxs-lookup"><span data-stu-id="9e33e-112">Using the offer code in your descriptors will not correctly identify your X++ modules to ISV Studio.</span></span>

## <a name="update-your-x-model-descriptors"></a><span data-ttu-id="9e33e-113">X++ モデル記述子の更新</span><span class="sxs-lookup"><span data-stu-id="9e33e-113">Update your X++ model descriptors</span></span>

<span data-ttu-id="9e33e-114">ソリューションを構成するすべてのモデルについて、記述子 XML ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="9e33e-114">For all models that make up your solution, locate the descriptor XML files.</span></span> <span data-ttu-id="9e33e-115">ソリューションに属しているすべての記述子で、パートナー センターの製品 ID を使用して `SolutionId` タグを更新します。</span><span class="sxs-lookup"><span data-stu-id="9e33e-115">For every descriptor that belongs to a solution, update the `SolutionId` tag with the product ID from Partner Center.</span></span>

:::code language="xml" source="code/descriptor.xml" highlight="19,20":::

<span data-ttu-id="9e33e-116">再コンパイル後、X++ バイナリには製品 ID が含まれ、Tier 2+ サンドボックスまたは実稼働環境に配置された後に ISV Studio にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="9e33e-116">After you recompile, the X++ binaries will contain the product ID and will link to ISV Studio after they are deployed to a Tier 2+ sandbox or production environment.</span></span>
