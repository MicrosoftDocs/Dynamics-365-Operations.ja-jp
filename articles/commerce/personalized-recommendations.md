---
title: パーソナライズされた製品推奨事項の有効化
description: このトピックでは、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bdb56a1f45cdea1832bd269502e534efdb207b03
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127908"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="a5898-103">パーソナライズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="a5898-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5898-104">このトピックでは、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5898-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a5898-105">概要</span><span class="sxs-lookup"><span data-stu-id="a5898-105">Overview</span></span>

<span data-ttu-id="a5898-106">Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a5898-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="a5898-107">この方法で、パーソナライズされた推奨事項が顧客エクスペリエンス オンラインおよび販売時点管理 (POS) に組み込まれます。</span><span class="sxs-lookup"><span data-stu-id="a5898-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="a5898-108">個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。</span><span class="sxs-lookup"><span data-stu-id="a5898-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="a5898-109">個人用設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="a5898-109">Personalization prerequisites</span></span>

<span data-ttu-id="a5898-110">パーソナライズされた製品推奨事項を顧客に対して利用可能にする前に、Azure Data Lake Store にストレージを移行したコマース ユーザーに対してのみ、製品推奨事項がサポートされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a5898-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="a5898-111">顧客がパーソナライズした製品推奨事項を受信できるようにする前に、小売業者は [製品推奨事項を有効にする](enable-product-recommendations.md) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a5898-112">製品推奨事項を有効にすることにより、個人用設定も有効になります。</span><span class="sxs-lookup"><span data-stu-id="a5898-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="a5898-113">ただし、個人用設定を無効にすると、他のタイプの製品推奨事項は無効になりません。</span><span class="sxs-lookup"><span data-stu-id="a5898-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="a5898-114">製品推奨事項の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5898-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="a5898-115">個人用設定を有効にする</span><span class="sxs-lookup"><span data-stu-id="a5898-115">Turn on personalization</span></span>

<span data-ttu-id="a5898-116">個人用設定を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a5898-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="a5898-117">**Retail とコマース \> 製品推奨事項 \> 推奨パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5898-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="a5898-118">Retai 共有パラメーターのリストで、**推奨リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5898-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="a5898-119">**個人用設定を有効化する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a5898-119">Set the **Enable personalization** option to **Yes**.</span></span>

![個人用設定を有効にする](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="a5898-121">個人用設定を有効にすると、パーソナライズされた製品推奨事項リストを生成するプロセスが開始します。</span><span class="sxs-lookup"><span data-stu-id="a5898-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="a5898-122">これらのリストを利用可能にし、オンラインおよび POS で表示するまでに、少なくとも 1 日必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="a5898-123">パーソナライズされたリスト</span><span class="sxs-lookup"><span data-stu-id="a5898-123">Personalized lists</span></span>

<span data-ttu-id="a5898-124">推奨事項サービスでは、コンピューター生成された既存のリストの個人用設定を許可することに加え、オンラインと POS の両方で製品検索エクスペリエンスを個人用設定を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="a5898-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="a5898-125">個人用設定を有効にした後、小売業者はパーソナライズされた "おすすめ" オンライン リストを、または POS 端末で "顧客への推奨" リストを買い物客に表示できます。</span><span class="sxs-lookup"><span data-stu-id="a5898-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="a5898-126">さらに、小売業者は既存の製品推奨事項リストに個人用設定を適用し、認証されたユーザーに対する一般データ保護規則 (GDPR) のオプトアウト エクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="a5898-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="a5898-127">個人用設定を無効にすると、これらの機能も無効になります。</span><span class="sxs-lookup"><span data-stu-id="a5898-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="a5898-128">オンラインの "おすすめ" リスト</span><span class="sxs-lookup"><span data-stu-id="a5898-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="a5898-129">"おすすめ" リストは、認証されたユーザーが推奨製品の個人用設定リストを表示する、人為的知能の機械学習 (AI-ML) リストです。</span><span class="sxs-lookup"><span data-stu-id="a5898-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="a5898-130">このリストは、ユーザーのオムニチャネル購買履歴に基づいています。</span><span class="sxs-lookup"><span data-stu-id="a5898-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="a5898-131">ユーザーがより多くの購買を行うと、カスタマイズされた推奨が動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a5898-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="a5898-132">このタイプのリストは、カテゴリのフィルター処理もサポートしているため、小売業者はナビゲーション階層に基づいておすすめの上位を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a5898-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="a5898-133">E コマース ページに "おすすめ" リストが表示される前に、次のユーザー要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="a5898-134">ユーザーがサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-134">Users must be signed in.</span></span> <span data-ttu-id="a5898-135">匿名ユーザーには、パーソナライズされた推奨事項は表示されません。</span><span class="sxs-lookup"><span data-stu-id="a5898-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="a5898-136">ユーザーは、自分のアカウントで少なくとも 1 つ購入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="a5898-137">ユーザーは、パーソナライズされた推奨事項の受信をオプトインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5898-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="a5898-138">次の図は、オンライン ストア ページの "おすすめ" リストの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a5898-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![オンラインのおすすめリスト](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="a5898-140">POS の "顧客への推奨" リスト</span><span class="sxs-lookup"><span data-stu-id="a5898-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="a5898-141">クライアンテリング エクスペリエンスを向上させるため、小売業者は、コンテキスト "顧客への推奨" リストを追加することにより、既存の顧客詳細ページをパーソナライズできます。</span><span class="sxs-lookup"><span data-stu-id="a5898-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="a5898-142">次の図は、POS 端末の "顧客への推奨" リストの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a5898-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS の顧客への推奨リスト](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="a5898-144">既存の推奨リストへの個人用設定の適用</span><span class="sxs-lookup"><span data-stu-id="a5898-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="a5898-145">小売業者は、既存の推奨リストに "新規"、"トレンド"、"ベスト セラー"、"人気製品"、"よく一緒に購入される製品" などの個人用設定を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="a5898-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="a5898-146">既存のリストに対して個人用設定が適用されると、サインインしたユーザーが以前に購入した品目がそれらのリストから削除されます。</span><span class="sxs-lookup"><span data-stu-id="a5898-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="a5898-147">匿名ユーザーおよびパーソナライズされた推奨事項の受信をオプトアウトしたユーザーの両方については、既存のリストの既定バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5898-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="a5898-148">したがって、小売業者は個別のページ エクスペリエンスを手動で管理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a5898-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="a5898-149">たとえば、サインインしたユーザーが、次の図にある "トレンド - 既定" のリストに表示されている黒色のウォッチと茶色の作業ブーツを既に購入しました。</span><span class="sxs-lookup"><span data-stu-id="a5898-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="a5898-150">したがって、"トレンド - 個人用設定" リストに示すように、ユーザーにはそれらの製品の代わりに新しい製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5898-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![個人用設定の適用](./media/applypersonalization.png)

<span data-ttu-id="a5898-152">コマース サイト ビルダーの既存の推奨リストに個人用設定を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a5898-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a5898-153">製品収集モジュールを含む既存のサイト ビルダー ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a5898-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="a5898-154">左のナビゲーション ウィンドウで、製品収集モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5898-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="a5898-155">右のナビゲーション ウィンドウの、**製品**で、リストを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5898-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="a5898-156">**製品リストのコンフィギュレーションの選**ダイアログ ボックスの、**タイプ**で、リスト タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5898-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="a5898-157">**個人用設定を適用**チェック ボックスを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5898-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![トレンド リストへの個人用設定の適用](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="a5898-159">ページを保存し、編集を終了してから、公開します。</span><span class="sxs-lookup"><span data-stu-id="a5898-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="a5898-160">ページを公開した後、サインインしているユーザーにはパーソナライズされたトレンド リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5898-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5898-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a5898-161">Additional resources</span></span>

[<span data-ttu-id="a5898-162">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="a5898-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a5898-163">Dynamics 365 Commerce 環境での ADLS の有効化</span><span class="sxs-lookup"><span data-stu-id="a5898-163">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a5898-164">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="a5898-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a5898-165">カスタマイズされた製品推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="a5898-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a5898-166">E コマース サイトへの推奨リストの追加</span><span class="sxs-lookup"><span data-stu-id="a5898-166">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a5898-167">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="a5898-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a5898-168">トランザクション画面への推奨設定の追加</span><span class="sxs-lookup"><span data-stu-id="a5898-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a5898-169">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="a5898-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a5898-170">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="a5898-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a5898-171">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="a5898-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a5898-172">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a5898-172">Product recommendations FAQ</span></span>](faq-recommendations.md)
