---
title: セルフサービス配置の FAQ
description: このトピックでは、セルフサービス配置に関してよくある質問に対する回答を示します。
author: rashmansur
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: a14b37eb3a60223c660c992bd2c8cbf9121b10b9
ms.sourcegitcommit: 708b3966b1c2bd4999f528d4a03a89d9bb530616
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100487"
---
# <a name="self-service-deployment-faq"></a><span data-ttu-id="cc8b2-103">セルフサービス配置の FAQ</span><span class="sxs-lookup"><span data-stu-id="cc8b2-103">Self-service deployment FAQ</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="cc8b2-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md)に関してよくある質問に対する回答を示します。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-104">This topic provides answers to some frequently asked questions about [self-service deployment](infrastructure-stack.md).</span></span> <span data-ttu-id="cc8b2-105">シナリオがここにない場合は、[既知の問題](known-issues-new-deployment-experience.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-105">Refer to the [known issues](known-issues-new-deployment-experience.md) list if your scenario is not listed here.</span></span>  

## <a name="why-do-i-see-only-application-version-811-and-platform-update-21-and-above-when-i-try-to-deploy-my-sandbox-environment-using-self-service-deployment"></a><span data-ttu-id="cc8b2-106">セルフサービス配置を使用してサンドボックス環境を配置しようとすると、アプリケーション バージョン 8.1.1 とプラットフォーム更新 21 以上しか表示されないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-106">Why do I see only application version 8.1.1 and Platform update 21 and above when I try to deploy my sandbox environment using self-service deployment?</span></span> 

<span data-ttu-id="cc8b2-107">現時点では、セルフ サービス配置では、アプリケーション バージョン 8.1.1 とプラットフォーム更新 21 以上のみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-107">Currently, self-service deployment supports only application version 8.1.1 with Platform update 21 and above.</span></span>  

## <a name="my-development-environment-is-on-application-version-81-am-i-still-able-to-move-my-customization-to-the-sandbox-environment"></a><span data-ttu-id="cc8b2-108">開発環境では、アプリケーション バージョン 8.1 です。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-108">My development environment is on application version 8.1.</span></span> <span data-ttu-id="cc8b2-109">それでもサンドボックス環境にカスタマイズを移動できますか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-109">Am I still able to move my customization to the sandbox environment?</span></span> 

<span data-ttu-id="cc8b2-110">はい。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-110">Yes.</span></span> <span data-ttu-id="cc8b2-111">アプリケーション バージョン 8.1.1 は、アプリケーション 8.1 と完全に下位互換があります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-111">Application version 8.1.1 is fully backward compatible with application 8.1.</span></span> 

## <a name="what-is-the-minimum-supported-application-and-platform-version-when-trying-to-use-the-self-service-deployment"></a><span data-ttu-id="cc8b2-112">セルフサービス配置を使用する場合、アプリケーションとプラットフォームのサポートされている最小バージョンは何ですか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-112">What is the minimum supported application and platform version when trying to use the self-service deployment?</span></span> 

<span data-ttu-id="cc8b2-113">プラットフォーム更新 20 を搭載したアプリケーション バージョン 8.1 が、最小のサポートされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-113">Application version 8.1 with Platform update 20 is the minimum supported version.</span></span> 

## <a name="what-do-i-do-if-deployment-fails"></a><span data-ttu-id="cc8b2-114">配置が失敗した場合どうしたらよいですか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-114">What do I do if deployment fails?</span></span> 

1. <span data-ttu-id="cc8b2-115">配置を削除してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-115">Delete the deployment.</span></span>  
2. <span data-ttu-id="cc8b2-116">同じ環境名を再利用する場合、5 分待機してからやり直してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-116">If you want to reuse the same environment name, wait 5 minutes and try again.</span></span> <span data-ttu-id="cc8b2-117">それ以外の場合、新しい名前で配置を再実行してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-117">Otherwise, retry deploying with a new name.</span></span> 
3. <span data-ttu-id="cc8b2-118">配置が再度失敗した場合は、サポート チケットを記録してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-118">If deployment fails again, log a Support ticket.</span></span>  

> [!Note]
> <span data-ttu-id="cc8b2-119">Microsoft は、今後のリリースで自動再試行ロジックを追加し、ログを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-119">Microsoft will add automatic retry logic in an upcoming release and make logs available.</span></span> 

## <a name="what-if-my-deployment-fails-with-an-environment-already-exists-error"></a><span data-ttu-id="cc8b2-120">"既に環境が存在する" エラーが発生すると配置はどうなりますか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-120">What if my deployment fails with an “environment already exists” error?</span></span> 

<span data-ttu-id="cc8b2-121">削除したばかりの配置の環境名を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-121">You may be trying to reuse the environment name of a deployment that you just deleted.</span></span> <span data-ttu-id="cc8b2-122">配置を再試行する前に、5 ～ 10分間待ってください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-122">Wait 5–10 minutes before retrying the deployment.</span></span> 

## <a name="i-dont-have-remote-desktop-access-to-my-sandbox-environment-how-do-i-perform-critical-actions-that-require-remote-desktop-access-today"></a><span data-ttu-id="cc8b2-123">サンドボックス環境へのリモート デスクトップ アクセス権がありません。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-123">I don't have Remote Desktop access to my sandbox environment.</span></span> <span data-ttu-id="cc8b2-124">現在リモート デスクトップ アクセスを必要とする重大なアクションはどうすれば実行できますか?</span><span class="sxs-lookup"><span data-stu-id="cc8b2-124">How do I perform critical actions that require Remote Desktop access today?</span></span>

<span data-ttu-id="cc8b2-125">Microsoft リモート デスクトップ アクセスはなくなりますが、引き続きレベル 2 以上のサンドボックス環境を操作できます。ここで説明している共通の重要なアクションを実行するために使用できる、セルフサービスの機能とツールが Microsoft により用意されているためです。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-125">Although you will no longer have Microsoft Remote Desktop access, you can continue to operate your Tier 2+ sandbox environments, because Microsoft is providing self-service capabilities and tools that you can use to perform the common critical actions that are described here.</span></span>

### <a name="access-the-azure-sql-database"></a><span data-ttu-id="cc8b2-126">Azure SQL データベースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="cc8b2-126">Access the Azure SQL database</span></span>
<span data-ttu-id="cc8b2-127">次の手順に従って、Microsoft Azure SQL データベースにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-127">You can access the Microsoft Azure SQL database by following these steps.</span></span>

1. <span data-ttu-id="cc8b2-128">LCS から、SQL Management Studio を使用して Azure SQL データベースに接続するために使用するコンピューターの IP アドレスをホワイトリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-128">From LCS, whitelist the IP address of the machine that you will use to connect to the Azure SQL database using SQL Management Studio.</span></span>
2. <span data-ttu-id="cc8b2-129">LCS を使用して、データベース資格情報を参照するアクセスを要求します。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-129">Use LCS to request access to see the database credentials.</span></span> <span data-ttu-id="cc8b2-130">アクセスを要求する理由を提示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-130">You must provide a reason for requesting access.</span></span> 

<span data-ttu-id="cc8b2-131">要求を送信するとすぐに自動的に承認されます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-131">As soon as you submit the request, it's automatically approved.</span></span> <span data-ttu-id="cc8b2-132">1 分または 2 分以内に、LCS 環境の詳細ページでデータベース アクセスの資格情報を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-132">Within a minute or two, you will be able to see the database access credentials on the LCS environment details page.</span></span> <span data-ttu-id="cc8b2-133">SQL データベースに接続するために資格情報を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-133">You can use the credentials to connect to the SQL database.</span></span>

> [!NOTE]
> <span data-ttu-id="cc8b2-134">資格情報は 8 時間有効です。その後、有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-134">The credentials are valid for eight hours, and then they will expire.</span></span> <span data-ttu-id="cc8b2-135">資格情報の有効期限後、もう一度アクセス権を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-135">After the credentials expire, you will have to request access again.</span></span> 

### <a name="access-log-files"></a><span data-ttu-id="cc8b2-136">ログ ファイルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="cc8b2-136">Access log files</span></span>
<span data-ttu-id="cc8b2-137">すべてのログ ファイルは、LCS 環境監視ページの**活動**タブから表示してダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-137">You can view and download all log files from the **Activity** tab on the LCS environment monitoring page.</span></span>

### <a name="use-perfmon-tools"></a><span data-ttu-id="cc8b2-138">perfmon ツールを使用する</span><span class="sxs-lookup"><span data-stu-id="cc8b2-138">Use perfmon tools</span></span>
<span data-ttu-id="cc8b2-139">リモート デスクトップを使用できなくなるため、パフォーマンスの問題を診断するために perfmon.exe を使用できなくなりますが、LCS を通じて CPU およびメモリ消費の重要な稼働状態メトリックを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-139">Although you can no longer use Remote Desktop and then use perfmon.exe to diagnose performance issues, you can monitor critical health metrics for CPU and memory consumption through LCS.</span></span> <span data-ttu-id="cc8b2-140">さらに、事前定義されたクエリをオンデマンドで実行でき、レベル 2 以上の環境でのパフォーマンスの問題を軽減するために事前に定義されたアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-140">In addition, you can run predefined queries on demand, and you can run predefined actions to mitigate performance issues on your Tier 2+ environments.</span></span> 

### <a name="access-self-service-logs"></a><span data-ttu-id="cc8b2-141">セルフサービス ログにアクセスする</span><span class="sxs-lookup"><span data-stu-id="cc8b2-141">Access self-service logs</span></span>
<span data-ttu-id="cc8b2-142">LCS を通じて環境で実行されるセルフサービス操作に関連するすべてのログは、LCS からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-142">All logs that are related to self-service operations that are performed on the environment through LCS are available for download from LCS.</span></span> <span data-ttu-id="cc8b2-143">これらのセルフサービス操作には、配置、処理、およびデータベースの移動が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-143">These self-service operations include deployment, servicing, and database movement.</span></span> <span data-ttu-id="cc8b2-144">LCS 環境履歴ページからログ フォルダーをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-144">You can download the log folders from the LCS environment history page.</span></span>

### <a name="turn-maintenance-mode-onoff"></a><span data-ttu-id="cc8b2-145">メンテナンス モードのオン/オフを切り替える</span><span class="sxs-lookup"><span data-stu-id="cc8b2-145">Turn Maintenance mode on/off</span></span>
<span data-ttu-id="cc8b2-146">2019 年 1 月リリースから、LCS でのセルフサービスの操作によって環境内のメンテナンス モードをオン/オフできるようになります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-146">Starting in the January 2019 release, you will be able to turn Maintenance mode in your environment on and off through a self-service action in LCS.</span></span>

### <a name="restart-services"></a><span data-ttu-id="cc8b2-147">サービスをリセット</span><span class="sxs-lookup"><span data-stu-id="cc8b2-147">Restart services</span></span>
<span data-ttu-id="cc8b2-148">2019 年 1 月リリース以降、LCS のセルフサービス アクションによりサービスを再起動できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-148">Starting in the January 2019 release, you will able to restart services through a self-service action in LCS.</span></span>

### <a name="configure-the-regression-suite-automation-tool"></a><span data-ttu-id="cc8b2-149">Regression Suite Automation Tool を構成する</span><span class="sxs-lookup"><span data-stu-id="cc8b2-149">Configure the Regression suite automation tool</span></span>
<span data-ttu-id="cc8b2-150">マイクロソフトは、リモート デスクトップを使用しなくても wif.config ファイルの証明書サムネイルを更新できるようにするツールを作成中です。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-150">Microsoft is working on tooling that will let you update certificate thumbprints in the wif.config file without having to use Remote Desktop.</span></span> <span data-ttu-id="cc8b2-151">このツールは、2019 年 2 月にリリースされる予定です。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-151">This tooling is scheduled for release in February 2019.</span></span> <span data-ttu-id="cc8b2-152">それより前に Regression Suite Automation Tool を使用する必要がある場合は、サポート リクエストを記録してください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-152">If you must use the Regression suite automation tool before then, log a support request.</span></span>

## <a name="i-must-perform-one-of-the-critical-actions-that-are-listed-earlier-in-this-topic-but-the-self-service-feature-isnt-yet-available-how-do-i-get-help"></a><span data-ttu-id="cc8b2-153">このトピックの前方に一覧表示されている重大なアクションのいずれかを実行する必要がありますが、セルフサービス機能はまだ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-153">I must perform one of the critical actions that are listed earlier in this topic, but the self-service feature isn't yet available.</span></span> <span data-ttu-id="cc8b2-154">ヘルプを表示する方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-154">How do I get help?</span></span>

<span data-ttu-id="cc8b2-155">サポート チケットを記録すると、Microsoft が環境でのアクションの実行をお手伝いします。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-155">Log a support ticket, and Microsoft will help you perform the action on your environment.</span></span>

## <a name="i-dont-have-remote-desktop-access-to-my-sandbox-environment-and-the-critical-action-that-i-must-perform-isnt-listed-in-this-topic-how-do-i-get-help"></a><span data-ttu-id="cc8b2-156">サンドボックス環境にリモート デスクトップ アクセスがなく、実行する必要がある重要なアクションがこのトピックに挙げられていません。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-156">I don't have Remote Desktop access to my sandbox environment, and the critical action that I must perform isn't listed in this topic.</span></span> <span data-ttu-id="cc8b2-157">ヘルプを表示する方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-157">How do I get help?</span></span>

<span data-ttu-id="cc8b2-158">重要なアクションのこのトピックの前方に掲載されていない場合、このトピックにコメントを追加するかドキュメンテーション バグを記録すると、Microsoft が要求に対応します。</span><span class="sxs-lookup"><span data-stu-id="cc8b2-158">If your critical action isn't listed earlier in this topic, add a comment to this topic or log a documentation bug, and Microsoft will address your requirement.</span></span>
