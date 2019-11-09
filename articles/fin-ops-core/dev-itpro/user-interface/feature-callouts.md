---
title: 機能のコールアウト
description: 機能のコールアウトをトリガーして、ユーザーに新しい機能を認識してもらいましょう。
author: jasongre
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-5-31
ms.dyn365.ops.version: Platform update 26
ms.openlocfilehash: 4da3ab6dd87ed97877eb429197e4d5cbf191586e
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578296"
---
# <a name="feature-callouts"></a><span data-ttu-id="b1d49-103">機能のコールアウト</span><span class="sxs-lookup"><span data-stu-id="b1d49-103">Feature callouts</span></span>

[!include [banner](../includes/banner.md)]


## <a name="introduction"></a><span data-ttu-id="b1d49-104">はじめに</span><span class="sxs-lookup"><span data-stu-id="b1d49-104">Introduction</span></span>
<span data-ttu-id="b1d49-105">ドキュメントは新機能の説明に役立ちますが、製品の使用中にユーザーがその機能に遭遇した場合は、これらの新機能について認識を高めることも重要です。</span><span class="sxs-lookup"><span data-stu-id="b1d49-105">While documentation is helpful for explaining new features, it’s also important to raise awareness of these new capabilities as users encounter the feature while using the product.</span></span> <span data-ttu-id="b1d49-106">その結果、機能のコールアウトをプラットフォームの更新プログラム 26 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-106">As a result, feature callouts are available in Platform update 26.</span></span> <span data-ttu-id="b1d49-107">機能のコールアウトを使用して、ユーザーに新しい機能を示して、オプションで機能の詳細を知るためのハイパーリンクをユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-107">You can use feature callouts to point out a new capability to a user and optionally provide a hyperlink for the user to learn more about the feature.</span></span> 

<span data-ttu-id="b1d49-108">このトピックでは、機能のコールアウトの作成に使用される API について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-108">In this topic, the APIs that are used to construct feature callouts are discussed in detail.</span></span>   

<span data-ttu-id="b1d49-109">![ナビゲーション ウィンドウの機能のコールアウトの変更](./media/cli_featureCallout_noLink.png "プラットフォーム更新プログラム 22 でリリースされた、ナビゲーション ウィンドウの機能のコールアウトの変更")</span><span class="sxs-lookup"><span data-stu-id="b1d49-109">![Feature callout for Navigation Pane changes](./media/cli_featureCallout_noLink.png "Feature callout for Navigation Pane changes released in Platform update 22")</span></span>
  
## <a name="the-got-it-button"></a><span data-ttu-id="b1d49-110">"了解" ボタン</span><span class="sxs-lookup"><span data-stu-id="b1d49-110">The "Got it" button</span></span>
<span data-ttu-id="b1d49-111">機能のコールアウトがトリガーされたら、ユーザは **了解** ボタンをただクリックしてポップアップを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-111">When a feature callout is triggered, the user can simply click the **Got it** button to dismiss the popup.</span></span> <span data-ttu-id="b1d49-112">これにより、この機能コールアウトの状態が個人用設定サブシステムに保存され、特定の機能コールアウトが再度トリガーされるのを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-112">This saves the state of this feature callout in the personalization subsystem, which prevents that specific feature callout from being triggered again.</span></span> 

## <a name="resetting-feature-callouts"></a><span data-ttu-id="b1d49-113">機能のコールアウトのリセット</span><span class="sxs-lookup"><span data-stu-id="b1d49-113">Resetting feature callouts</span></span>
<span data-ttu-id="b1d49-114">機能コールアウトの状態が個人用設定に保存されている場合、個人用設定をクリアしても以前に閉じたすべての機能コールアウトの状態は削除されません。</span><span class="sxs-lookup"><span data-stu-id="b1d49-114">Even though the feature callout state is stored in personalization, clearing personalizations will not delete the state of all previously dismissed feature callouts.</span></span> <span data-ttu-id="b1d49-115">代わりに、すべての機能コールアウトをリセットして再び起動するようにする、別のアクションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="b1d49-115">Instead, separate actions have been added to reset all feature callouts so that they fire again.</span></span> <span data-ttu-id="b1d49-116">これらのアクションは、**使用状況データ** ページの **個人用設定** タブ、および **個人設定** ページの **ユーザーごとに管理** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="b1d49-116">These actions are located on the **Personalization** tab on the **Usage data** page as well as on the **Manage per user** tab on the **Personalization** page.</span></span>   

## <a name="disabling-feature-callouts"></a><span data-ttu-id="b1d49-117">機能のコールアウトの無効化</span><span class="sxs-lookup"><span data-stu-id="b1d49-117">Disabling feature callouts</span></span> 
<span data-ttu-id="b1d49-118">管理者は必要に応じて、**クライアント パフォーマンス オプション** ページで **機能のコールアウトを有効化** オプションを使用して、環境に対して機能のコールアウトを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-118">If needed, administrators can turn off feature callouts for an environment using the **Feature callouts enabled** option on the **Client performance options** page.</span></span> 
  
## <a name="implementation-details"></a><span data-ttu-id="b1d49-119">実装詳細</span><span class="sxs-lookup"><span data-stu-id="b1d49-119">Implementation details</span></span>
<span data-ttu-id="b1d49-120">SystemNotificationsWhatsNewManager クラスには、機能のコールアウトをトリガーするための 2 つのバリアント API が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1d49-120">The SystemNotificationsWhatsNewManager class contains two variant APIs for triggering a feature callout.</span></span> 

### <a name="addwhatsnewwithactionlink"></a><span data-ttu-id="b1d49-121">AddWhatsNewWithActionLink()</span><span class="sxs-lookup"><span data-stu-id="b1d49-121">AddWhatsNewWithActionLink()</span></span> 
<span data-ttu-id="b1d49-122">新しい製品の機能に関連付けられているドキュメントを開くように構成されている [詳細情報] のリンクを含むコントロールに機能のコールアウトを追加します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-122">Add a feature callout to a control with a "Learn more" link that is configured to open the documentation associated with the new product capability.</span></span>  

#### <a name="parameters"></a><span data-ttu-id="b1d49-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1d49-123">Parameters</span></span>

| <span data-ttu-id="b1d49-124">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1d49-124">Parameter</span></span>     | <span data-ttu-id="b1d49-125">説明</span><span class="sxs-lookup"><span data-stu-id="b1d49-125">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b1d49-126">ruleID</span><span class="sxs-lookup"><span data-stu-id="b1d49-126">ruleID</span></span>        | <span data-ttu-id="b1d49-127">一意の GUID を生成します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-127">Generate a unique GUID.</span></span>                                                    | 
| <span data-ttu-id="b1d49-128">title</span><span class="sxs-lookup"><span data-stu-id="b1d49-128">title</span></span>         | <span data-ttu-id="b1d49-129">(ローカライズ済みの) タイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-129">Provide a (localized) title.</span></span>                                               | 
| <span data-ttu-id="b1d49-130">bodyText</span><span class="sxs-lookup"><span data-stu-id="b1d49-130">bodyText</span></span>      | <span data-ttu-id="b1d49-131">(ローカライズ済みの) 説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-131">Provide a (localized) description.</span></span>                                         | 
| <span data-ttu-id="b1d49-132">targetControl</span><span class="sxs-lookup"><span data-stu-id="b1d49-132">targetControl</span></span> | <span data-ttu-id="b1d49-133">機能のコールアウトを追加するコントロールの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-133">Provide the name of the control you want to attach the feature callout to.</span></span> | 
| <span data-ttu-id="b1d49-134">urlLink</span><span class="sxs-lookup"><span data-stu-id="b1d49-134">urlLink</span></span>       | <span data-ttu-id="b1d49-135">"詳細" リンクをクリックしたときに、新しいタブで開く URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-135">Provide the URL to open in a new tab when the "Learn more" link is clicked.</span></span> <span data-ttu-id="b1d49-136">URL が指定されない場合、"詳細" リンクは表示されません。</span><span class="sxs-lookup"><span data-stu-id="b1d49-136">If a URL is not specified, then a "Learn more" link will not be displayed.</span></span> |


### <a name="addwhatsnew"></a><span data-ttu-id="b1d49-137">AddWhatsNew()</span><span class="sxs-lookup"><span data-stu-id="b1d49-137">AddWhatsNew()</span></span> 
<span data-ttu-id="b1d49-138">機能のコールアウトを [詳細情報] リンクのないコントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-138">Add a feature callout to a control without a "Learn more" link.</span></span> 

#### <a name="parameters"></a><span data-ttu-id="b1d49-139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1d49-139">Parameters</span></span>

| <span data-ttu-id="b1d49-140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1d49-140">Parameter</span></span>     | <span data-ttu-id="b1d49-141">説明</span><span class="sxs-lookup"><span data-stu-id="b1d49-141">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b1d49-142">ruleID</span><span class="sxs-lookup"><span data-stu-id="b1d49-142">ruleID</span></span>        | <span data-ttu-id="b1d49-143">一意の GUID を生成します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-143">Generate a unique GUID.</span></span>                                                    | 
| <span data-ttu-id="b1d49-144">title</span><span class="sxs-lookup"><span data-stu-id="b1d49-144">title</span></span>         | <span data-ttu-id="b1d49-145">(ローカライズ済みの) タイトルを入力します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-145">Provide a (localized) title.</span></span>                                               | 
| <span data-ttu-id="b1d49-146">bodyText</span><span class="sxs-lookup"><span data-stu-id="b1d49-146">bodyText</span></span>      | <span data-ttu-id="b1d49-147">(ローカライズ済みの) 説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-147">Provide a (localized) description.</span></span>                                         | 
| <span data-ttu-id="b1d49-148">targetControl</span><span class="sxs-lookup"><span data-stu-id="b1d49-148">targetControl</span></span> | <span data-ttu-id="b1d49-149">機能のコールアウトを追加するコントロールの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1d49-149">Provide the name of the control you want to attach the feature callout to.</span></span> | 

### <a name="example"></a><span data-ttu-id="b1d49-150">例</span><span class="sxs-lookup"><span data-stu-id="b1d49-150">Example</span></span>
<span data-ttu-id="b1d49-151">次のコードスニペットは、*TestStringControl* というコントロールに関連付けられている機能のコールアウトをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="b1d49-151">The following code snippet will trigger a feature callout attached to the control named *TestStringControl*.</span></span>  

    public void init() 
    {
         super(); 
     
         SystemNotificationsWhatsNewManager::AddWhatsNewWithActionLink(
              MyTestKey, 
              "My title" , 
              "My description", 
              TestStringControl.name(), 
              "http://www.microsoft.com"
         );
    }

## <a name="notes"></a><span data-ttu-id="b1d49-152">摘要</span><span class="sxs-lookup"><span data-stu-id="b1d49-152">Notes</span></span>
-  <span data-ttu-id="b1d49-153">複数の機能のコールアウトを一度に 1 ページに表示できます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-153">Multiple feature callouts can be shown on a page at one time.</span></span>
-  <span data-ttu-id="b1d49-154">機能のコールアウトは、コントロールごとに 1 つのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-154">Only one feature callout is allowed per control.</span></span> <span data-ttu-id="b1d49-155">複数のコールアウトが存在する場合は、最後にトリガーされたものが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1d49-155">If multiple callouts exist, the last one to get triggered will be displayed.</span></span>