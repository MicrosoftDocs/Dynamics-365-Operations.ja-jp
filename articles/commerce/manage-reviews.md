---
title: 評価とレビューの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで評価とレビューを管理する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974009"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="a6b5a-103">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="a6b5a-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6b5a-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで評価とレビューを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="a6b5a-105">概要</span><span class="sxs-lookup"><span data-stu-id="a6b5a-105">Overview</span></span>

<span data-ttu-id="a6b5a-106">Dynamics 365 Commerce は、Microsoft Azure 認知サービスを使用して、俗語を編集することでレビュー テキストを自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="a6b5a-107">さらに、モデレーターは Dynamics 365 Commerce サイト ビルダーを使用して、次の手動タスクを実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="a6b5a-108">応答するか削除して、レビューをモデレートします。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="a6b5a-109">顧客の要求に応じて、顧客のレビューを削除します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="a6b5a-110">評価とレビューの傾向を分析できるように、すべての製品の評価とレビューのデータを Microsoft Power BI テンプレートに一括インポートします。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="a6b5a-111">レビューの読み取り</span><span class="sxs-lookup"><span data-stu-id="a6b5a-111">Read a review</span></span> 

<span data-ttu-id="a6b5a-112">Commerce サイト ビルダーのレビューを読むには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-113">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="a6b5a-114">ページの右上にある検索フィールドを使用して、製品 ID、製品名、またはレビュー テキストで表示されるレビューをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="a6b5a-115">追加のフィルターを使用すると、期間、評価、チャネル、または関連する状態 (停止、回答済、または報告済) によってレビューを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![ホーム ページの管理](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="a6b5a-117">レビューへの応答</span><span class="sxs-lookup"><span data-stu-id="a6b5a-117">Respond to a review</span></span> 

<span data-ttu-id="a6b5a-118">場合によっては、製品を購入した顧客が満足や不満を表明したり、製品の使用方法がわからなかったりすることがあります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="a6b5a-119">モデレーターは、レビューへの応答を投稿できます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="a6b5a-120">この応答は、サイトでレビューと共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="a6b5a-121">Commerce サイト ビルダーでレビューに返信するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-122">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="a6b5a-123">回答を必要とするレビューを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="a6b5a-124">右のプロパティ ウィンドウで、**応答の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="a6b5a-125">応答テキストと、応答者に表示される名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="a6b5a-126">既定の応答者の名前は**モデレーター**です。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="a6b5a-127">完了したら、**応答を投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-127">When you've finished, select **Post response**.</span></span>

![レビューへの応答](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="a6b5a-129">レビューの削除</span><span class="sxs-lookup"><span data-stu-id="a6b5a-129">Take down a review</span></span> 

<span data-ttu-id="a6b5a-130">場合によっては、モデレーターが顧客レビューを削除するための業務上の正当な理由があります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="a6b5a-131">Commerce サイト ビルダーでレビューを削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-132">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="a6b5a-133">削除する必要のあるレビューを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="a6b5a-134">右側のプロパティ ウィンドウで、**レビューの削除**の下の削除の理由を選択して、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="a6b5a-135">顧客の要求に応じて顧客のレビューを削除する</span><span class="sxs-lookup"><span data-stu-id="a6b5a-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="a6b5a-136">顧客は、評価やレビューのデータを E コマースの Web サイトから完全に削除したい場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="a6b5a-137">顧客からの削除依頼を受け取ったモデレーターは、レビュー削除機能を使用して、顧客のデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="a6b5a-138">モデレーターは、顧客のデータを検索して削除するために、顧客がサインインしてレビューを提供するために使用した電子メール アドレスが必要になります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="a6b5a-139">Commerce サイト ビルダーで顧客データを検索したり削除したりするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-140">**ホーム \> レビュー \> 削除**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="a6b5a-141">**電子メール アドレスでユーザーを検索する**ボックスで、顧客の電子メール アドレスを入力して、**検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="a6b5a-142">顧客にレビュー活動 (たとえば、レビューの送信、別の顧客のレビューの有用性に関する投票、または別の顧客のレビューに関するコメント) がある場合、その結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="a6b5a-143">各品目には、**削除**ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="a6b5a-144">削除する必要がある各品目について、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="a6b5a-145">確認が求められたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![顧客データの削除](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="a6b5a-147">データがシステムから完全に削除されるまでに最大 7 日かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="a6b5a-148">モデレーターは、この遅延を顧客に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="a6b5a-149">顧客がアカウント設定で名前を変更した場合、検索結果に複数の項目が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="a6b5a-150">この場合、顧客のデータを完全に削除するには、モデレーターは各品目に対して**削除**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="a6b5a-151">評価とレビューのデータのダウンロード</span><span class="sxs-lookup"><span data-stu-id="a6b5a-151">Download ratings and reviews data</span></span>

<span data-ttu-id="a6b5a-152">Commerce サイト ビルダーを使用すると、モデレーターは評価をインポートして、データを一括してレビューできるため、傾向を分析することができます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="a6b5a-153">基本的なメトリックスを含む Power BI テンプレートが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="a6b5a-154">モデレーターは、このテンプレートを使用して、一括インポートされたデータを接続し、ダッシュボードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="a6b5a-155">カスタム ダッシュボードを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="a6b5a-156">モデレーターは、特定のニーズに合わせて Power BI テンプレートをカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="a6b5a-157">Commerce サイト ビルダーで評価とレビューのデータをダウンロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-158">**ホーム \> レビュー \> レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="a6b5a-159">**レビュー データのダウンロード**を選択し、評価とレビューのデータをコンマ区切り値 (CSV) 形式で一括ダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="a6b5a-160">評価とレビューの傾向を表示する</span><span class="sxs-lookup"><span data-stu-id="a6b5a-160">View ratings and reviews trends</span></span>

<span data-ttu-id="a6b5a-161">モデレーターは、Power BI テンプレートをダウンロードして、ダッシュボードに傾向を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="a6b5a-162">Commerce サイト ビルダーの評価とレビューの傾向を表示するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a6b5a-163">**ホーム \> レビュー \> レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="a6b5a-164">**PowerBI テンプレート**を選択し、テンプレートをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-164">Select **PowerBI template** to download the template.</span></span>

    ![Power BI テンプレートをダウンロードする](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="a6b5a-166">Power BI アプリを使用して、ダウンロードしたテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="a6b5a-167">表示される **Web コンテンツへのアクセス** ダイアログ ボックスを閉じ、表示される更新エラー メッセージを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="a6b5a-168">**ホーム**に移動し、**クエリの編集**を選択し、**データ ソースの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="a6b5a-169">**データ ソースの設定** ダイアログ ボックスで、**ソースの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="a6b5a-170">**URL** フィールドに、前の手順でダウンロードしたレビュー データのパスを入力します (たとえば、**c:\\reviews\\ReviewsData.csv**)。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![コンマ区切り値ダイアログ ボックスの URL フィールド](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="a6b5a-172">**OK** を選択し、**変更の適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="a6b5a-173">データ ソースに変更を適用するには、1 ~ 2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="a6b5a-174">評価とレビューの傾向を表示するには、**傾向シート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6b5a-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![評価とレビューの傾向](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="a6b5a-176">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a6b5a-176">Additional resources</span></span>

[<span data-ttu-id="a6b5a-177">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="a6b5a-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="a6b5a-178">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="a6b5a-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="a6b5a-179">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a6b5a-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="a6b5a-180">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="a6b5a-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
