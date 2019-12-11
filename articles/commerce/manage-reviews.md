---
title: 評価とレビューの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価およびレビューの管理ツールを使用して、評価およびレビューを管理する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698029"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="cb677-103">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="cb677-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cb677-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価およびレビューの管理ツールを使用して、評価およびレビューを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cb677-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="cb677-105">概要</span><span class="sxs-lookup"><span data-stu-id="cb677-105">Overview</span></span>

<span data-ttu-id="cb677-106">Dynamics 365 Commerce は、Microsoft Azure 認知サービスを使用して、俗語を編集することでレビュー テキストを自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="cb677-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="cb677-107">さらに、モデレーターは、評価とレビューの管理ツールを次の手動タスクに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cb677-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="cb677-108">応答するか削除して、レビューをモデレートします。</span><span class="sxs-lookup"><span data-stu-id="cb677-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="cb677-109">顧客の要求に応じて、顧客のレビューを削除します。</span><span class="sxs-lookup"><span data-stu-id="cb677-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="cb677-110">評価とレビューの傾向を分析できるように、すべての製品の評価とレビューのデータを Microsoft Power BI テンプレートに一括インポートします。</span><span class="sxs-lookup"><span data-stu-id="cb677-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="cb677-111">レビューの読み取り</span><span class="sxs-lookup"><span data-stu-id="cb677-111">Read a review</span></span> 

1. <span data-ttu-id="cb677-112">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="cb677-113">ページの右上にある検索フィールドを使用して、製品 ID、製品名、またはレビュー テキストで表示されるレビューをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="cb677-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="cb677-114">追加のフィルターを使用すると、期間、評価、チャネル、または関連する状態 (停止、回答済、または報告済) によってレビューを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="cb677-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![ホーム ページの管理](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="cb677-116">レビューへの応答</span><span class="sxs-lookup"><span data-stu-id="cb677-116">Respond to a review</span></span> 

<span data-ttu-id="cb677-117">場合によっては、製品を購入した顧客が満足や不満を表明したり、製品の使用方法がわからなかったりすることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb677-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="cb677-118">モデレーターは、レビューへの応答を投稿できます。</span><span class="sxs-lookup"><span data-stu-id="cb677-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="cb677-119">この応答は、サイトでレビューと共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb677-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="cb677-120">レビューに応答するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb677-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="cb677-121">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="cb677-122">回答を必要とするレビューを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="cb677-123">右のプロパティ ウィンドウで、**応答の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="cb677-124">応答テキストと、応答者に表示される名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb677-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="cb677-125">既定の応答者の名前は**モデレーター**です。</span><span class="sxs-lookup"><span data-stu-id="cb677-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="cb677-126">完了したら、**応答を投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-126">When you've finished, select **Post response**.</span></span>

![レビューへの応答](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="cb677-128">レビューの削除</span><span class="sxs-lookup"><span data-stu-id="cb677-128">Take down a review</span></span> 

<span data-ttu-id="cb677-129">場合によっては、モデレーターが顧客レビューを削除するための業務上の正当な理由があります。</span><span class="sxs-lookup"><span data-stu-id="cb677-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="cb677-130">レビューを削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb677-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="cb677-131">**ホーム \> レビュー \> 管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="cb677-132">削除する必要のあるレビューを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="cb677-133">右側のプロパティ ウィンドウで、削除の理由を選択し、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="cb677-134">顧客の要求に応じて顧客のレビューを削除する</span><span class="sxs-lookup"><span data-stu-id="cb677-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="cb677-135">顧客は、評価やレビューのデータを E コマースの Web サイトから完全に削除したい場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb677-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="cb677-136">顧客からの削除依頼を受け取ったモデレーターは、レビュー削除機能を使用して、顧客のデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="cb677-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="cb677-137">モデレーターは、顧客のデータを検索して削除するために、顧客がサインインしてレビューを提供するために使用した電子メール アドレスが必要になります。</span><span class="sxs-lookup"><span data-stu-id="cb677-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="cb677-138">顧客データを検索して削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb677-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="cb677-139">**ホーム \> レビュー \> 削除**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="cb677-140">**電子メール アドレスでユーザーを検索する**のフィールドで、顧客の電子メール アドレスを入力し、**検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="cb677-141">顧客にレビュー活動 (たとえば、レビューの送信、別の顧客のレビューの有用性に関する投票、または別の顧客のレビューに関するコメント) がある場合、その結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb677-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="cb677-142">各品目には、**削除**ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="cb677-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="cb677-143">削除する必要がある各品目について、**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="cb677-144">確認が求められたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![顧客データの削除](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="cb677-146">データがシステムから完全に削除されるまでに最大 7 日かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb677-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="cb677-147">モデレーターは、この遅延を顧客に通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb677-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="cb677-148">顧客がアカウント設定で名前を変更した場合、検索結果に複数の項目が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="cb677-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="cb677-149">この場合、顧客のデータを完全に削除するには、モデレーターは各品目に対して**削除**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb677-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="cb677-150">評価とレビューのデータのダウンロード</span><span class="sxs-lookup"><span data-stu-id="cb677-150">Download ratings and reviews data</span></span>

<span data-ttu-id="cb677-151">評価とレビューのモデレーション ツールを使用すると、モデレーターは評価とレビューのデータを一括インポートして、傾向を分析することができます。</span><span class="sxs-lookup"><span data-stu-id="cb677-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="cb677-152">基本的なメトリックスを含む Power BI テンプレートが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="cb677-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="cb677-153">モデレーターは、このテンプレートを使用して、一括インポートされたデータを接続し、ダッシュボードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cb677-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="cb677-154">カスタム ダッシュボードを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cb677-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="cb677-155">モデレーターは、特定のニーズに合わせて Power BI テンプレートをカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb677-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="cb677-156">評価とレビューのデータをダウンロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb677-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="cb677-157">**ホーム \> レビュー \> レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="cb677-158">**レビュー データをダウンロード**を選択し、評価とレビューのデータをコンマ区切り値 (CSV) 形式で一括ダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="cb677-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="cb677-159">評価とレビューの傾向を表示する</span><span class="sxs-lookup"><span data-stu-id="cb677-159">View ratings and reviews trends</span></span>

<span data-ttu-id="cb677-160">モデレーターは、Power BI テンプレートをダウンロードして、ダッシュボードに傾向を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="cb677-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="cb677-161">評価とレビューの傾向を表示するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb677-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="cb677-162">**ホーム \> レビュー \> レポート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb677-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="cb677-163">**PowerBI テンプレート**を選択し、テンプレートをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="cb677-163">Select **PowerBI template** to download the template.</span></span>

    ![Power BI テンプレートをダウンロードする](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="cb677-165">Power BI アプリを使用して、ダウンロードしたテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="cb677-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="cb677-166">表示される **Web コンテンツへのアクセス** ダイアログ ボックスを閉じ、表示される更新エラー メッセージを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cb677-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="cb677-167">**ホーム**に移動し、**クエリの編集**を選択し、**データ ソースの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="cb677-168">**データ ソースの設定** ダイアログ ボックスで、**ソースの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="cb677-169">**URL** フィールドに、前の手順でダウンロードしたレビュー データのパスを入力します (たとえば、**c:\\reviews\\ReviewsData.csv**)。</span><span class="sxs-lookup"><span data-stu-id="cb677-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![コンマ区切り値ダイアログ ボックスの URL フィールド](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="cb677-171">**OK** を選択し、**変更の適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="cb677-172">データ ソースに変更を適用するには、1 ~ 2 分かかります。</span><span class="sxs-lookup"><span data-stu-id="cb677-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="cb677-173">評価とレビューの傾向を表示するには、**傾向シート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb677-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![評価とレビューの傾向](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="cb677-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cb677-175">Additional resources</span></span>

[<span data-ttu-id="cb677-176">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="cb677-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="cb677-177">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="cb677-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="cb677-178">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cb677-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="cb677-179">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="cb677-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
