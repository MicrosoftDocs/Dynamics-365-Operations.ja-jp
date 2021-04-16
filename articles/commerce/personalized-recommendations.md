---
title: パーソナライズされた製品推奨事項の有効化
description: このトピックでは、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。
author: bebeale
ms.date: 08/18/2020
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
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804432"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="37f3e-103">パーソナライズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="37f3e-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37f3e-104">このトピックでは、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="37f3e-105">Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="37f3e-106">この方法で、パーソナライズされた推奨事項が顧客エクスペリエンス オンラインおよび販売時点管理 (POS) に組み込まれます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="37f3e-107">個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="37f3e-108">個人用設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="37f3e-108">Personalization prerequisites</span></span>

<span data-ttu-id="37f3e-109">パーソナライズされた製品推奨事項を顧客に対して利用可能にする前に、Azure Data Lake Store にストレージを移行したコマース ユーザーに対してのみ、製品推奨事項がサポートされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="37f3e-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="37f3e-110">顧客がパーソナライズした製品推奨事項を受信できるようにする前に、小売業者は [製品推奨事項を有効にする](enable-product-recommendations.md) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="37f3e-111">製品推奨事項を有効にすることにより、個人用設定も有効になります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="37f3e-112">ただし、個人用設定を無効にすると、他のタイプの製品推奨事項は無効になりません。</span><span class="sxs-lookup"><span data-stu-id="37f3e-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="37f3e-113">製品推奨事項の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37f3e-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="37f3e-114">個人用設定を有効にする</span><span class="sxs-lookup"><span data-stu-id="37f3e-114">Turn on personalization</span></span>

<span data-ttu-id="37f3e-115">個人用設定を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="37f3e-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="37f3e-116">Commerce Headquarters で、**機能管理** を検索します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="37f3e-117">**すべて** を選択して、使用可能な機能の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="37f3e-118">検索ボックスに、**推奨事項** を入力します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="37f3e-119">**個人用設定がされた製品の推奨** 機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="37f3e-120">**個人用設定がされた製品の推奨** プロパティ ペインで、**すぐに有効化する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![個人用設定を有効にする](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="37f3e-122">個人用設定を有効にすると、パーソナライズされた製品推奨事項リストを生成するプロセスが開始します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="37f3e-123">これらのリストを利用可能にし、オンラインおよび POS で表示するまでに、少なくとも 1 日必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="37f3e-124">パーソナライズされたリスト</span><span class="sxs-lookup"><span data-stu-id="37f3e-124">Personalized lists</span></span>

<span data-ttu-id="37f3e-125">推奨事項サービスでは、コンピューター生成された既存のリストの個人用設定を許可することに加え、オンラインと POS の両方で製品検索エクスペリエンスを個人用設定を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="37f3e-126">個人用設定を有効にした後、小売業者はパーソナライズされた "おすすめ" オンライン リストを、または POS 端末で "顧客への推奨" リストを買い物客に表示できます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="37f3e-127">さらに、小売業者は既存の製品推奨事項リストに個人用設定を適用し、認証されたユーザーに対する一般データ保護規則 (GDPR) のオプトアウト エクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="37f3e-128">個人用設定を無効にすると、これらの機能も無効になります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="37f3e-129">オンラインの "おすすめ" リスト</span><span class="sxs-lookup"><span data-stu-id="37f3e-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="37f3e-130">"おすすめ" リストは、認証されたユーザーが推奨製品の個人用設定リストを表示する、人為的知能の機械学習 (AI-ML) リストです。</span><span class="sxs-lookup"><span data-stu-id="37f3e-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="37f3e-131">このリストは、ユーザーのオムニチャネル購買履歴に基づいています。</span><span class="sxs-lookup"><span data-stu-id="37f3e-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="37f3e-132">ユーザーがより多くの購買を行うと、カスタマイズされた推奨が動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="37f3e-133">このタイプのリストは、カテゴリのフィルター処理もサポートしているため、小売業者はナビゲーション階層に基づいておすすめの上位を表示できます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="37f3e-134">E コマース ページに "おすすめ" リストが表示される前に、次のユーザー要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="37f3e-135">ユーザーがサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-135">Users must be signed in.</span></span> <span data-ttu-id="37f3e-136">匿名ユーザーには、パーソナライズされた推奨事項は表示されません。</span><span class="sxs-lookup"><span data-stu-id="37f3e-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="37f3e-137">ユーザーは、自分のアカウントで少なくとも 1 つ購入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="37f3e-138">ユーザーは、パーソナライズされた推奨事項の受信をオプトインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f3e-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="37f3e-139">次の図は、オンライン ストア ページの "おすすめ" リストの例を示します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![オンラインのおすすめリスト](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="37f3e-141">POS の "顧客への推奨" リスト</span><span class="sxs-lookup"><span data-stu-id="37f3e-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="37f3e-142">クライアンテリング エクスペリエンスを向上させるため、小売業者は、コンテキスト "顧客への推奨" リストを追加することにより、既存の顧客詳細ページをパーソナライズできます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="37f3e-143">次の図は、POS 端末の "顧客への推奨" リストの例を示します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS の顧客への推奨リスト](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="37f3e-145">既存の推奨リストへの個人用設定の適用</span><span class="sxs-lookup"><span data-stu-id="37f3e-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="37f3e-146">小売業者は、既存の推奨リストに "新規"、"トレンド"、"ベスト セラー"、"人気製品"、"よく一緒に購入される製品" などの個人用設定を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="37f3e-147">既存のリストに対して個人用設定が適用されると、サインインしたユーザーが以前に購入した品目がそれらのリストから削除されます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="37f3e-148">匿名ユーザーおよびパーソナライズされた推奨事項の受信をオプトアウトしたユーザーの両方については、既存のリストの既定バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="37f3e-149">したがって、小売業者は個別のページ エクスペリエンスを手動で管理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="37f3e-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="37f3e-150">たとえば、サインインしたユーザーが、次の図にある "トレンド - 既定" のリストに表示されている黒色のウォッチと茶色の作業ブーツを既に購入しました。</span><span class="sxs-lookup"><span data-stu-id="37f3e-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="37f3e-151">したがって、"トレンド - 個人用設定" リストに示すように、ユーザーにはそれらの製品の代わりに新しい製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![個人用設定の適用](./media/applypersonalization.png)

<span data-ttu-id="37f3e-153">コマース サイト ビルダーの既存の推奨リストに個人用設定を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="37f3e-154">製品収集モジュールを含む既存のサイト ビルダー ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="37f3e-155">左のナビゲーション ウィンドウで、製品収集モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="37f3e-156">右のナビゲーション ウィンドウの、**製品** で、リストを選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="37f3e-157">**製品リストのコンフィギュレーションの選** ダイアログ ボックスの、**タイプ** で、リスト タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="37f3e-158">**個人用設定を適用** チェック ボックスを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![トレンド リストへの個人用設定の適用](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="37f3e-160">ページを保存し、編集を終了してから、公開します。</span><span class="sxs-lookup"><span data-stu-id="37f3e-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="37f3e-161">ページを公開した後、サインインしているユーザーにはパーソナライズされたトレンド リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="37f3e-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37f3e-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="37f3e-162">Additional resources</span></span>

[<span data-ttu-id="37f3e-163">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="37f3e-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="37f3e-164">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="37f3e-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="37f3e-165">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="37f3e-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="37f3e-166">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="37f3e-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="37f3e-167">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="37f3e-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="37f3e-168">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="37f3e-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="37f3e-169">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="37f3e-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="37f3e-170">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="37f3e-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="37f3e-171">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="37f3e-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="37f3e-172">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="37f3e-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="37f3e-173">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="37f3e-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
