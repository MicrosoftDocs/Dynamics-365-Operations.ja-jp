---
title: Attract および Onboard からのデータのエクスポート
description: Dynamics 365 Talent - Attract および Onboard からデータをエクスポートします。
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975937"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="4e9d8-103">Attract および Onboard からのデータのエクスポート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e9d8-104">[Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard アプリの廃止](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) で発表された通り、Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard は、2022 年 2 月 1 日に廃止されます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="4e9d8-105">別の製品への移行を支援するために、両方のアプリでデータエクスポート機能を使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="4e9d8-106">Attract からのデータのエクスポート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-106">Export data from Attract</span></span>

<span data-ttu-id="4e9d8-107">環境へのアクセスを制限することなく、データをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="4e9d8-108">テスト目的で、またはデータ構造を理解するために、この操作を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="4e9d8-109">移行する準備ができたら、この手順の後の指示に従って、Attract 環境に対するアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="4e9d8-110">必ずデータを再度エクスポートしてください。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="4e9d8-111">[https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4e9d8-112">**データのエクスポート**で、**データのエクスポートを要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="4e9d8-113">Attract からのデータ エクスポートの要求</span><span class="sxs-lookup"><span data-stu-id="4e9d8-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="4e9d8-114">**要求は処理中**メッセージボックスが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4e9d8-115">エクスポートのサイズによっては、データのエクスポートに最大で 20 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4e9d8-116">エクスポートが完了したら、横にある**ダウンロード** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="4e9d8-117">すべてのデータ エクスポートは 7 日間実行でき、この時点で**ダウンロード** リンクの有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="4e9d8-118">ダウンロードには、Attract データを含む .zip ファイルが含まれており、以下のフォルダーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="4e9d8-119">フォルダー名</span><span class="sxs-lookup"><span data-stu-id="4e9d8-119">Folder name</span></span> | <span data-ttu-id="4e9d8-120">説明</span><span class="sxs-lookup"><span data-stu-id="4e9d8-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="4e9d8-121">管理者設定</span><span class="sxs-lookup"><span data-stu-id="4e9d8-121">Admin settings</span></span> | <span data-ttu-id="4e9d8-122">Attract 管理センターのコンフィギュレーション。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="4e9d8-123">候補者</span><span class="sxs-lookup"><span data-stu-id="4e9d8-123">Candidates</span></span> | <span data-ttu-id="4e9d8-124">職務または人材プールに追加された全候補者。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="4e9d8-125">電子メール テンプレート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-125">Email templates</span></span> | <span data-ttu-id="4e9d8-126">環境に対してコンフィギュレーションされたすべての電子メール テンプレート。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="4e9d8-127">ジョブ オファー パッケージ テンプレート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-127">Job offer package templates</span></span> | <span data-ttu-id="4e9d8-128">作成されたすべてのジョブ オファー パッケージ テンプレートと、それに関連付けられているコンフィギュレーション。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="4e9d8-129">ジョブ オファー ルール セット</span><span class="sxs-lookup"><span data-stu-id="4e9d8-129">Job offer rule sets</span></span> |  <span data-ttu-id="4e9d8-130">オファー管理のためにアップロードされたすべてのルール セット ファイル。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="4e9d8-131">ジョブ オファー テンプレート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-131">Job offer templates</span></span> | <span data-ttu-id="4e9d8-132">環境に対して作成されたすべてのジョブ オファー ドキュメント テンプレート。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="4e9d8-133">求人</span><span class="sxs-lookup"><span data-stu-id="4e9d8-133">Job openings</span></span> | <span data-ttu-id="4e9d8-134">作成されたすべてのジョブ。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-134">All created jobs.</span></span> <span data-ttu-id="4e9d8-135">削除されたジョブはエクスポートされません。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="4e9d8-136">サブフォルダーには、候補者のアプリケーションが含まれており、候補者のアプリケーション添付ファイルのサブフォルダーと、該当する場合はオファー パッケージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="4e9d8-137">求人テンプレート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-137">Job opening templates</span></span> | <span data-ttu-id="4e9d8-138">環境に対してコンフィギュレーションされたジョブ プロセス テンプレート。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="4e9d8-139">人材プール</span><span class="sxs-lookup"><span data-stu-id="4e9d8-139">Talent pools</span></span> | <span data-ttu-id="4e9d8-140">作成された人材プール、貢献者リスト、および人材プールの候補者リスト。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="4e9d8-141">作業者</span><span class="sxs-lookup"><span data-stu-id="4e9d8-141">Workers</span></span> | <span data-ttu-id="4e9d8-142">環境に存在するすべての作業者のリスト、およびそのロール。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="4e9d8-143">(ルート フォルダー)</span><span class="sxs-lookup"><span data-stu-id="4e9d8-143">(root folder)</span></span> | <span data-ttu-id="4e9d8-144">データ構造フィールドを説明する JSON スキーマ ファイル。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="4e9d8-145">Attract へのアクセスの制限</span><span class="sxs-lookup"><span data-stu-id="4e9d8-145">Restrict access to Attract</span></span>

<span data-ttu-id="4e9d8-146">移行する準備ができたら、非管理者の Attract 環境へのアクセスを制限し、データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="4e9d8-147">Attract 環境へのアクセスの制限は永続的で、元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="4e9d8-148">管理者以外のユーザーが継続して環境にアクセスできるようにする場合は、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="4e9d8-149">[https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4e9d8-150">非管理者による Attract 環境へのアクセスを制限するには、**このアプリへのアクセスの制限**で、**今すぐアクセスを制限**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="4e9d8-151">アクセスを制限すると、転記済の有効なジョブもすべて無転記になります。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="4e9d8-152">非管理者の Attract へのアクセスの制限</span><span class="sxs-lookup"><span data-stu-id="4e9d8-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="4e9d8-153">**これは永続的な変更です**という警告が表示された場合は、**アクセスの制限**を選択して、この環境に対して管理者以外のユーザーを完全に制限します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="4e9d8-154">この手順を完了する準備ができていない場合は、**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="4e9d8-155">アクセス制限が永続的な変更であるという警告</span><span class="sxs-lookup"><span data-stu-id="4e9d8-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="4e9d8-156">管理者は、Attract 環境へのアクセスを制限した後に、データ エクスポート ページと個人レポート ページに継続してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="4e9d8-157">Onboard からデータをエクスポート</span><span class="sxs-lookup"><span data-stu-id="4e9d8-157">Export data from Onboard</span></span>

<span data-ttu-id="4e9d8-158">準備が整ったら、テンプレート、ガイド、および候補者データを Onboard からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="4e9d8-159">[https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport) に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="4e9d8-160">**データのエクスポート**で、**データのエクスポートを要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="4e9d8-161">Onboard からのデータ エクスポートの要求</span><span class="sxs-lookup"><span data-stu-id="4e9d8-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="4e9d8-162">**要求は処理中**メッセージボックスが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4e9d8-163">エクスポートのサイズによっては、データのエクスポートに最大で 20 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4e9d8-164">エクスポートが完了したら、横にある**ダウンロード** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="4e9d8-165">Onboard からのデータ エクスポートのダウンロード</span><span class="sxs-lookup"><span data-stu-id="4e9d8-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="4e9d8-166">データ エクスポートは 7 日間使用できます。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-166">Your data export is available for seven days.</span></span> <span data-ttu-id="4e9d8-167">7 日後に**ダウンロード** リンクの有効期限が切れ、データを再度ダウンロードする必要がある場合は、新しいエクスポートを要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="4e9d8-168">新しいデータ エクスポートを開始すると、新しいエクスポートが成功した後に既存のダウンロードが期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="4e9d8-169">ダウンロードは、次の内容を含む .zip ファイルです。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="4e9d8-170">Word 文書形式の Onboard テンプレートを含む**テンプレート** フォルダー。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="4e9d8-171">Word 文書形式の Onboard ガイドを含む**ガイド** フォルダー。</span><span class="sxs-lookup"><span data-stu-id="4e9d8-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e9d8-172">参照</span><span class="sxs-lookup"><span data-stu-id="4e9d8-172">See also</span></span>

[<span data-ttu-id="4e9d8-173">Dynamics 365 Talent: Attract および Dynamics 365 Talent: Onboard アプリの廃止</span><span class="sxs-lookup"><span data-stu-id="4e9d8-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)