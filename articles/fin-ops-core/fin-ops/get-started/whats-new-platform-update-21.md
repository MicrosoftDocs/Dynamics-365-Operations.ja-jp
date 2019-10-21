---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 21 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a765a61c-52a3-47c5-b579-68b9249c592b
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform 21
ms.openlocfilehash: e99994c7ed3e930ebf4f25bc312640d51596ac34
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191729"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-21-november-2018"></a><span data-ttu-id="ef73a-104">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="ef73a-104">What's new or changed in Dynamics 365 for Finance and Operations platform update 21 (November 2018)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef73a-105">このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-105">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations platform update 21.</span></span> <span data-ttu-id="ef73a-106">このバージョンは 2018 年 11 月にリリースされ、ビルド番号は 7.0.5073 です。</span><span class="sxs-lookup"><span data-stu-id="ef73a-106">This version was released in November 2018 and has a build number of 7.0.5073.</span></span>

## <a name="dynamics-365-october-18-release-notes"></a><span data-ttu-id="ef73a-107">Dynamics 365 2018 年 10 月リリース ノート</span><span class="sxs-lookup"><span data-stu-id="ef73a-107">Dynamics 365 October '18 release notes</span></span>

<span data-ttu-id="ef73a-108">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="ef73a-108">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="ef73a-109">[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424).</span><span class="sxs-lookup"><span data-stu-id="ef73a-109">[Check out the October '18 release notes](https://go.microsoft.com/fwlink/?linkid=870424).</span></span> <span data-ttu-id="ef73a-110">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-110">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="ef73a-111">バグ修正</span><span class="sxs-lookup"><span data-stu-id="ef73a-111">Bug fixes</span></span>

<span data-ttu-id="ef73a-112">プラットフォーム更新 21 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2033925)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef73a-112">For information about the bug fixes included in each of the updates that are part of Platform update 21, sign in to Lifecycle Services (LCS) and view the [KB article](https://go.microsoft.com/fwlink/?linkid=2033925).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="ef73a-113">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="ef73a-113">Extensibility enhancements</span></span>

<span data-ttu-id="ef73a-114">リリース ノートには、[2018 年 10 月リリースのプラットフォーム拡張機能の 2 番目の波](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility2)に関する情報が含まれています。これは、プラットフォーム更新 21 に付属しています。</span><span class="sxs-lookup"><span data-stu-id="ef73a-114">The Release notes contain information about [the second wave of platform extensibility enhancements for the October 2018 release](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility2), which are coming with Platform update 21.</span></span> <span data-ttu-id="ef73a-115">11 個の拡張機能が詳細に説明されており、ハイライトの 1 つは、標準例外処理を容易にするため、try-finally ブロック内のコマンド メソッド チェーン内に次の呼び出しを配置する新しい機能です。</span><span class="sxs-lookup"><span data-stu-id="ef73a-115">There are eleven enhancements detailed, with one of the highlights being the new ability to put the next call inside a chain of command method within a try-finally block to facilitate standard exception handling.</span></span>

## <a name="transientsqlconnectionerror-x-exception"></a><span data-ttu-id="ef73a-116">TransientSqlConnectionError X++ 例外</span><span class="sxs-lookup"><span data-stu-id="ef73a-116">TransientSqlConnectionError X++ exception</span></span>

<span data-ttu-id="ef73a-117">X++ SQL クエリの実行中、サーバー側で一時的な SQL 接続エラーが発生すると、TransientSqlConnectionError X++ 例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-117">During an X++ SQL query execution, when a transient SQL connection error occurs on the server side, a TransientSqlConnectionError X++ exception will occur.</span></span> <span data-ttu-id="ef73a-118">アプリケーションの要件に応じて、アプリケーションは例外をキャッチして処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef73a-118">Depending on the application requirements, the application should catch and handle the exception.</span></span>

<span data-ttu-id="ef73a-119">この例外は通常、大規模なトランザクションの際に、またはデータベースに大きな処理負荷がかかっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-119">This exception usually occurs during a large transaction or when the database is under a lot of processing pressure.</span></span>

<span data-ttu-id="ef73a-120">TransientSqlConnectionError 例外は、トランザクション内ではキャッチできません。</span><span class="sxs-lookup"><span data-stu-id="ef73a-120">The TransientSqlConnectionError exception is not catchable within the transaction.</span></span> <span data-ttu-id="ef73a-121">この例外が検出された X++ トランザクションは、例外が発生する前にキャンセルされます (**ttsAbort** を呼び出す)。</span><span class="sxs-lookup"><span data-stu-id="ef73a-121">The X++ transaction that encounters this exception is canceled (calling **ttsAbort**) before the exception occurs.</span></span> <span data-ttu-id="ef73a-122">つまり、汎用 X++ エラー例外ではなく一時的な SQL 接続エラーを特定するためにキャッチ ブロックを使用した後、最上位のトランザクションを再試行するか、新しいセッションでアプリケーション コード ロジックを再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef73a-122">This means that you need to use the catch block to identify the transient SQL connection error instead of a generic X++ error exception, and then retry the outermost transaction or retry application code logic in a new session.</span></span> <span data-ttu-id="ef73a-123">この例外は、一時的なサーバーの障害時にアプリケーションの設計を許可します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-123">This exception allows the application to be designed for transient server failures.</span></span>

<span data-ttu-id="ef73a-124">アプリケーション トランザクションの処理に時間がかかる場合、複数の増分遅延を使用して TransientSqlConnectionError 例外をキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-124">If an application transaction takes a long time to process, you can use multiple incremental delays to catch the TransientSqlConnectionError exception.</span></span> <span data-ttu-id="ef73a-125">新しいセッションでアプリケーション コードを再実行すると、例外をキャッチした後に成功する可能性が最も高くなります。</span><span class="sxs-lookup"><span data-stu-id="ef73a-125">Retrying your application code in a new session is most likely to succeed after you have caught the exception.</span></span>

<span data-ttu-id="ef73a-126">詳細については、[SQL 接続エラー X++ 例外](../../dev-itpro/dev-ref/sql-connection-error.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef73a-126">For more information, see [SQL connection error X++ exception](../../dev-itpro/dev-ref/sql-connection-error.md).</span></span>

## <a name="sticky-default-actions-in-grids"></a><span data-ttu-id="ef73a-127">グリッド内の既定の付箋アクション</span><span class="sxs-lookup"><span data-stu-id="ef73a-127">Sticky default actions in grids</span></span>

<span data-ttu-id="ef73a-128">Finance and Operations の多くのグリッドで*既定のアクション*が定義されています。</span><span class="sxs-lookup"><span data-stu-id="ef73a-128">Many grids in Finance and Operations have a defined *default action*.</span></span> <span data-ttu-id="ef73a-129">これは、すべての行の値がハイパーリンクとして表示されるグリッド内の 1 つの列です。それに対して、その他の列ではアクティブな行の値だけがハイパーリンクとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-129">This is a single column in the grid where the value in every row always appears as a hyperlink, as opposed to other columns where only the value in the active row appears as a hyperlink.</span></span> <span data-ttu-id="ef73a-130">この既定のアクションは常に、ユーザー個人設定が適用される前に、グリッド内の最初のテキスト列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-130">This default action always appears on the first textual column in a grid before any user personalization is applied.</span></span> <span data-ttu-id="ef73a-131">たとえば、以下の **顧客** 一覧の **アカウント** 列を考えます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-131">For example, consider the **Account** column in the **Customer** list below.</span></span>

<span data-ttu-id="ef73a-132">![顧客リスト](media/customerGrid.png "顧客リスト")</span><span class="sxs-lookup"><span data-stu-id="ef73a-132">![Customer list](media/customerGrid.png "Customer list")</span></span>

<span data-ttu-id="ef73a-133">プラットフォーム更新 21 から利用可能な **既定の付箋アクション** 機能は、列の順序または表示設定を変更する個人用設定が適用された後に、既定のアクション列がグリッドのどこに表示されるかを制御します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-133">The **sticky default action** feature, which is available starting in Platform update 21, controls where the default action column appears in the grid after personalizations that change the order or visibility of columns are applied.</span></span>

<span data-ttu-id="ef73a-134">既定の付箋アクションをオフにすると (プラットフォーム更新 21 より前で既定のアクションがどのように動作したかに対応します)、既定のアクション ハイパーリンクが、個人用設定の適用後に最初のテキスト列に表示される列に変更されます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-134">With sticky default actions off, which corresponds to how default actions work prior to Platform update 21, the default action hyperlink would change to whatever column is the first textual column after personalizations are applied.</span></span> <span data-ttu-id="ef73a-135">たとえば、**アカウント** 列をグリッドの 4 番目の列に移動する場合 (または **アカウント** 列を非表示にした場合)、既定のアクションを表すハイパーリンクは **名前** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-135">For example, if you move the **Account** column to be fourth column in the grid (or alternatively if you hide the **Account** column), the hyperlink representing the default action moves to the **Name** column.</span></span>

<span data-ttu-id="ef73a-136">![既定の付箋アクションがオフ](media/stickyDAOff.png "既定の付箋アクションがオフになると、[アカウント] 列が最初の列に移動されない場合、[名前] 列が既定のアクション列になります。")</span><span class="sxs-lookup"><span data-stu-id="ef73a-136">![Sticky default actions off](media/stickyDAOff.png "With sticky default actions off, the Name column becomes the default action column if the Account column is moved to not be the first column.")</span></span>

<span data-ttu-id="ef73a-137">既定の付箋アクションがオンになると、既定のアクション ハイパーリンクは、フォームに適用される個人用設定に関係なく同じ列になります。</span><span class="sxs-lookup"><span data-stu-id="ef73a-137">With sticky default actions on, the default action hyperlink will be on the same column regardless of any personalizations applied to the form.</span></span> <span data-ttu-id="ef73a-138">つまり、この顧客リストについて、**アカウント** 列が移動されるか非表示になるか関係なく、**アカウント** 列は引き続き既定のアクション列です。</span><span class="sxs-lookup"><span data-stu-id="ef73a-138">This means that for this customer list, the **Account** column will continue to be the default action column regardless of whether the **Account** column is moved or hidden.</span></span>

<span data-ttu-id="ef73a-139">![既定の付箋アクションがオフ](media/stickyDAOn.png "既定の付箋アクションがオンになると、[アカウント] 列は個人用設定にかかわらず既定のアクション列です。")</span><span class="sxs-lookup"><span data-stu-id="ef73a-139">![Sticky default actions off](media/stickyDAOn.png "With sticky default actions on, the Account column is still the default action column despite any personalizations.")</span></span>

<span data-ttu-id="ef73a-140">プラットフォーム更新 21 では、既定の付箋アクション機能がオフですが、システム管理者が環境で有効にできます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-140">With Platform update 21, the sticky default action feature is off, but a system administrator can turn it on for an environment.</span></span> <span data-ttu-id="ef73a-141">この機能を有効にするには、**システム管理** で **クライアント パフォーマンス オプション** ページに移動し、**既定の付箋アクションを有効にする** オプションを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-141">To turn on this feature, go to the **Client performance options** page under **System administration** and find the **Enable sticky default action** option.</span></span>

## <a name="batch-active-periods"></a><span data-ttu-id="ef73a-142">バッチ アクティブ期間</span><span class="sxs-lookup"><span data-stu-id="ef73a-142">Batch active periods</span></span>

<span data-ttu-id="ef73a-143">プラットフォーム更新 21 のリリースでは、バッチ ジョブがいつ実行されるかの制御の追加レベルが使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ef73a-143">With the release of Platform update 21, an additional level of control over when batch jobs execute is now available.</span></span> <span data-ttu-id="ef73a-144">以前は、一定の時間数または特定の日付までの 1 時間ごとにバッチ ジョブが実行されるようにスケジュールすることのみ可能でした。</span><span class="sxs-lookup"><span data-stu-id="ef73a-144">Previously, it was only possible to schedule a batch job to execute every hour for a specified number of hours or until a given date.</span></span> <span data-ttu-id="ef73a-145">管理者は、次のシナリオなど、追加のアクティブ期間の情報を指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ef73a-145">Administrators can now provide information for an additional active period, such as in the following scenarios:</span></span>

- <span data-ttu-id="ef73a-146">バッチ グループ内のジョブが実行を開始できる期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-146">Specify time ranges during which jobs within a batch group can start execution.</span></span>
- <span data-ttu-id="ef73a-147">営業時間外にのみバッチ ジョブを実行する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-147">Select to only run batch jobs outside of office hours.</span></span>
- <span data-ttu-id="ef73a-148">アクティブ期間内で任意の回数の繰り返しを設定します。</span><span class="sxs-lookup"><span data-stu-id="ef73a-148">Set the recurrence for anytime within the active period.</span></span> <span data-ttu-id="ef73a-149">たとえば、管理者は、午後 6 時から午前 8 時の間のみ、毎時間バッチ ジョブを実行することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ef73a-149">For example, your administrator might select to run the batch jobs every hour, but only between the hours of 6:00 PM and 8:00 AM.</span></span>

<span data-ttu-id="ef73a-150">詳細については、「[バッチ アクティブ期間](../../dev-itpro/sysadmin/activeperiod.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef73a-150">For more information, see [Batch active period](../../dev-itpro/sysadmin/activeperiod.md).</span></span>
