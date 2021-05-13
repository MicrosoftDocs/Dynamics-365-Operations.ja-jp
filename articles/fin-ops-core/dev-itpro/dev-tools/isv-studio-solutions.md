---
title: ISV Studio を使用して、独立系ソフトウェア ベンダー (ISV) パッケージから X++ モジュールをリンク
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
ms.openlocfilehash: a9a6b4618a7184255ed6580805f8af35fbde0b8e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881895"
---
# <a name="link-x-modules-from-independent-software-vendor-isv-packages-by-using-isv-studio"></a><span data-ttu-id="6bf4d-103">ISV Studio を使用して、独立系ソフトウェア ベンダー (ISV) パッケージから X++ モジュールをリンク</span><span class="sxs-lookup"><span data-stu-id="6bf4d-103">Link X++ modules from independent software vendor (ISV) packages by using ISV Studio</span></span>

<span data-ttu-id="6bf4d-104">独立系ソフトウェア ベンダー (ISVs) は、[Microsoft Power Platform ISV Studio](https://docs.microsoft.com/powerapps/developer/data-platform/isv-app-management) を使用して、X++モジュールを登録済みの製品およびソリューションにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-104">Independent software vendors (ISVs) can link their X++ modules to their registered products and solutions by using [Microsoft Power Platform ISV Studio](https://docs.microsoft.com/powerapps/developer/data-platform/isv-app-management).</span></span> <span data-ttu-id="6bf4d-105">リンクにより、ISV は Finance and Operations アプリでのアプリケーションの成功と使用を監視できます。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-105">Linking enables ISV's to monitor the success and usage of their applications in Finance and Operations apps.</span></span>

> [!NOTE]
> <span data-ttu-id="6bf4d-106">X++ から ISV Studio へのリンクが正しく機能するには、顧客ははすべての ISV モデルに正しいソリューション ID を持つ ISV パッケージを展開している必要があり、顧客の環境はバージョン 10.0.16 以降を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-106">For the link from X++ into ISV Studio to work correctly, customers need to have deployed ISV packages with the correct solution ID in all the ISV models, and the customer's environment has to run version 10.0.16 or higher.</span></span>

## <a name="find-the-product-id-in-microsoft-partner-center"></a><span data-ttu-id="6bf4d-107">Microsoft パートナー センターで製品 ID を検索する</span><span class="sxs-lookup"><span data-stu-id="6bf4d-107">Find the product ID in Microsoft Partner Center</span></span>

<span data-ttu-id="6bf4d-108">パートナー センターにサインインし、製品の **オファーの概要** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-108">Sign in to Partner Center and open the **Offer overview** page for your product.</span></span> <span data-ttu-id="6bf4d-109">次の例に示すように、ブラウザの URL バーから製品 ID GUID (グローバル一意識別子) を検索します。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-109">From the browser's URL bar, locate the product ID GUID (global unique identifier), as shown in the following example.</span></span>

```HTTP
https://partner.microsoft.com/en-us/dashboard/commercial-marketplace/offers/<product-ID-GUID>/overview
```

> [!NOTE]
> <span data-ttu-id="6bf4d-110">製品 ID 製品のオファー コードと一致するとは限りませんが、類似している場合があります。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-110">The product ID does not necessarily match the offer code of your product, although they may be similar.</span></span> <span data-ttu-id="6bf4d-111">記述子でオファー コードを使用しても、ISV Studio に対して X++ モジュールを正しく識別できません。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-111">Using the offer code in your descriptors will not correctly identify your X++ modules to ISV Studio.</span></span>

## <a name="update-your-x-model-descriptors"></a><span data-ttu-id="6bf4d-112">X++ モデル記述子の更新</span><span class="sxs-lookup"><span data-stu-id="6bf4d-112">Update your X++ model descriptors</span></span>

<span data-ttu-id="6bf4d-113">ソリューションを構成するすべてのモデルについて、記述子 XML ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-113">For all models that make up your solution, locate the descriptor XML files.</span></span> <span data-ttu-id="6bf4d-114">ソリューションに属しているすべての記述子で、パートナー センターの製品 ID を使用して `SolutionId` タグを更新します。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-114">In every descriptor belonging to the solution, update the `SolutionId` tag with the product ID from partner center.</span></span>

```xml
<AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <!-- XML content -->
    <SolutionId>product-ID-GUID</SolutionId>
</AxModelInfo>
```

<span data-ttu-id="6bf4d-115">再コンパイル後、X++ バイナリには製品 ID が含まれ、Tier2+ サンドボックスまたは実稼働環境に配置された後に ISV Studio にリンクされます。</span><span class="sxs-lookup"><span data-stu-id="6bf4d-115">After you recompile, the X++ binaries will contain the product ID and will link to ISV Studio after they are deployed to a Tier2+ sandbox or production environment.</span></span>
