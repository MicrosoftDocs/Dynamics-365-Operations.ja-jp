---
title: パーソナライズされた推奨事項のオプト アウト
description: このトピックでは、顧客が Microsoft Dynamics 365 Commerce でパーソナライズされた推奨事項を受け取ることができるようにする方法について説明します。
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7d0f505ce49bc9be0d027cbb0d636c9de0600b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804456"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="4beaf-103">パーソナライズされた推奨事項のオプトアウト</span><span class="sxs-lookup"><span data-stu-id="4beaf-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4beaf-104">このトピックでは、顧客が Microsoft Dynamics 365 Commerce でパーソナライズされた推奨事項を受け取ることができるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4beaf-105">アカウントの作成時、新規顧客はパーソナライズされた推奨事項を受け取るように自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="4beaf-106">ただし、Dynamics 365 Commerce は、ユーザーがこれらの推奨事項のオプト アウトを選択したり、個人データの処理を制限したりできるようにするさまざまな方法を、小売業者に提供しています。</span><span class="sxs-lookup"><span data-stu-id="4beaf-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="4beaf-107">パーソナライズされた推奨事項の受信をオプト アウトした認証済ユーザーは、ただちにパーソナライズされたリストを見ることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="4beaf-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="4beaf-108">また、パーソナライズのために収集された個人データは、パーソナライズされた推奨モデルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="4beaf-109">パーソナライズされた製品推奨事項の詳細については、[パーソナライズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4beaf-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="4beaf-110">小売業者がオプトアウト エクスペリエンスを実装する方法</span><span class="sxs-lookup"><span data-stu-id="4beaf-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="4beaf-111">小売業者がオプトアウト エクスペリエンスを実装する方法は、3 つあります。</span><span class="sxs-lookup"><span data-stu-id="4beaf-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="4beaf-112">ユーザーに代わってオプト アウトする</span><span class="sxs-lookup"><span data-stu-id="4beaf-112">Opting out on behalf of users</span></span>

<span data-ttu-id="4beaf-113">Commerce バック オフィスのアカウント管理では、小売業者はユーザーに代わってオプト アウトを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="4beaf-114">バックオフィスのホームページから、**すべての顧客** を検索します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="4beaf-115">顧客を検索して選択し、**小売** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![小売クイックタブ](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="4beaf-117">**プライバシー** で、**個人用設定を無効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![プライバシー設定](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="4beaf-119">**保存** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="4beaf-120">モジュールベースのオプトアウト エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="4beaf-120">Module-based opt-out experience</span></span>

<span data-ttu-id="4beaf-121">小売業者は、認証済ユーザーがパーソナライズされた推奨事項を自分でオプト アウトできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="4beaf-122">このオプトアウト エクスペリエンスを提供するには、顧客アカウント プロファイル ページにユーザーのオプトアウト モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="4beaf-123">カスタムの拡張機能</span><span class="sxs-lookup"><span data-stu-id="4beaf-123">Custom extensions</span></span>

<span data-ttu-id="4beaf-124">小売業者は、ユーザーのオプトアウト エクスペリエンスを管理するための独自の拡張機能を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="4beaf-125">詳細については、[Retail サーバー API](e-commerce-extensibility/call-retail-server-apis.md) および [オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4beaf-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="4beaf-126">認証済ユーザーに代わって、パーソナライズされた推奨事項データのデジタル コピーを取得する</span><span class="sxs-lookup"><span data-stu-id="4beaf-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="4beaf-127">顧客は、個人データのデジタル コピーを取得して、その推奨結果をエクスポートして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="4beaf-128">顧客がこの情報を要求した場合、小売業者は、顧客の顧客 ID に基づいて、Retail Server のアプリケーション プログラミング インターフェイス (API) を呼び出す、カスタマイズされた拡張機能を作成し、**おすすめ** リストからすべての結果をクエリする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4beaf-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="4beaf-129">その後、結果をコンマ区切り値 (CSV) 形式でエクスポートして、顧客と共有することができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="4beaf-130">次の例は、小売業者がこのタスクを実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4beaf-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="4beaf-131">小売業者は、ユーザーに代わって個人的な推奨事項データを取得するカスタム拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="4beaf-132">モジュールの作成、既存のモジュールの複製、Retail Server API の呼び出し、データ アクションの呼び出しの詳細については、[オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4beaf-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="4beaf-133">カスタム拡張機能は、**推奨を取得** のコア データ アクションに対する呼び出しを行い、リストの要件に基づいて必要な情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="4beaf-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="4beaf-134">**おすすめ** リストの場合は、拡張機能によって、正しいリスト名と顧客 ID がデータ アクションに渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4beaf-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="4beaf-135">カスタム拡張機能を作成する 1 つの方法として、推奨結果を返すために使用される既存の製品収集モジュールを複製する方法があります。</span><span class="sxs-lookup"><span data-stu-id="4beaf-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="4beaf-136">この既存のモジュールを複製することによって、小売業者は既存のコードを変更し、推奨結果を CSV ファイルにエクスポートする新しいボタンを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="4beaf-137">詳細については、[モジュール ライブラリ モジュールの複製](e-commerce-extensibility/clone-starter-module.md) および [製品収集モジュール](product-collection-module-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4beaf-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="4beaf-138">Retail Server API ライブラリの完全表示については、[Retail Server の顧客およびコンシューマー API](dev-itpro/retail-server-customer-consumer-api.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4beaf-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="4beaf-139">カスタム拡張機能が作成されると、小売業者は、認証済ユーザーの固有の顧客 ID に基づいて、すべての推奨結果の CSV ファイルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="4beaf-140">小売業者は、パーソナライズされた推奨製品リストを含むエクスポートされた CSV ファイルを、認証済ユーザーと共有することができます。</span><span class="sxs-lookup"><span data-stu-id="4beaf-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4beaf-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4beaf-141">Additional resources</span></span>

[<span data-ttu-id="4beaf-142">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="4beaf-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4beaf-143">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="4beaf-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4beaf-144">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="4beaf-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4beaf-145">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="4beaf-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4beaf-146">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="4beaf-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="4beaf-147">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="4beaf-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4beaf-148">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="4beaf-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4beaf-149">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="4beaf-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4beaf-150">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="4beaf-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4beaf-151">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="4beaf-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4beaf-152">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4beaf-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
