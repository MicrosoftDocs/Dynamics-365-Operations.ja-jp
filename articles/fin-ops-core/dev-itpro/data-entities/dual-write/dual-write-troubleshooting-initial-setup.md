---
title: 初期セットアップ中の問題のトラブルシューティング
description: このトピックでは、デュアル書き込み統合の初期設定中に発生する問題を修正するために役立つ情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: cfbc1ab3ef6d47f6ec2d8ca4ca4b8940784e6e49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129984"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="5c453-103">初期セットアップ中の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5c453-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="5c453-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c453-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="5c453-105">このトピックでは、 デュアル書き込み統合の初期設定を行う際に、発生する可能性がある問題を修正するトラブルシューティングに特化した情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c453-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c453-106">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c453-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="5c453-107">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="5c453-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="5c453-108">Finance and Operations アプリを Dataverse にリンクさせることはできません。</span><span class="sxs-lookup"><span data-stu-id="5c453-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="5c453-109">**デュアル書き込みの設定に必要なロール:** Finance and Operations アプリと Dataverse 両方のシステム管理者権限。</span><span class="sxs-lookup"><span data-stu-id="5c453-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="5c453-110">一般的には、 **Dataverseへのリンク設定** ページで発生するエラーは、設定が不完全な場合やアクセス権限の問題が原因で発生するします。</span><span class="sxs-lookup"><span data-stu-id="5c453-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="5c453-111">次の図に示すように、**Dataverseへのリンク設定** ページで正常性チェック全体が合格になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5c453-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="5c453-112">正常性チェック全体で合格しない限りは、デュアル書き込みをリンクすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5c453-112">You can't link dual-write unless the whole health check passes.</span></span>

![正常性チェックの成功](media/health_check.png)

<span data-ttu-id="5c453-114">Azure AD 環境と Finance and Operations 環境えおリンクするには、Dataverse テナント管理者の資格情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="5c453-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="5c453-115">環境をリンクした後、ユーザーはアカウントの資格情報を使用してログインし、既存のテーブル マップを更新できます。</span><span class="sxs-lookup"><span data-stu-id="5c453-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="5c453-116">Dataverse ページへのリンクを開いた際のエラー</span><span class="sxs-lookup"><span data-stu-id="5c453-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="5c453-117">**問題の解決に必要な資格情報：** Azure ADテナント管理者</span><span class="sxs-lookup"><span data-stu-id="5c453-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="5c453-118">Finance and Operations アプリで **Dataverseへのリンク** を開いた際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c453-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="5c453-119">*応答状態コードが成功とならない: 404 (Not Found)。*</span><span class="sxs-lookup"><span data-stu-id="5c453-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="5c453-120">このエラーは、同意の手順が完了していない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="5c453-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="5c453-121">同意の手順が完了しているかどうかを検証するには、Azure AD テナント管理者のアカウントを使用して portal.Azure.com にログインし、ID **33976c19-1db5-4c02-810e-c243db79efde** を持つサードパーティ製のアプリが Azure AD **エンタープライズ アプリケーション** のリストに表示されるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5c453-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="5c453-122">これが存在しない場合は、アプリの同意をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c453-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="5c453-123">アプリへの同意をするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5c453-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="5c453-124">管理者の資格情報を使用して、次のURLを開きます。</span><span class="sxs-lookup"><span data-stu-id="5c453-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="5c453-125">同意を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c453-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="5c453-126">ご利用のテナントで ID **33976c19-1db5-4c02-810e-c243db79efde** が含まれているアプリのインストールに同意していることを示す場合は、**同意する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c453-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="5c453-127">このアプリは、Dataverse および Finance and Operations アプリをリンクするために必要となります。</span><span class="sxs-lookup"><span data-stu-id="5c453-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="5c453-128">この手順に問題がある場合は、ブラウザーを incognito モード（Google Chrome の場合）または InPrivate モード（Microsoft Edge の場合）で開きます。</span><span class="sxs-lookup"><span data-stu-id="5c453-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="5c453-129">会社のデータとデュアル書き込みのチームがリンク設定中に正しく設定されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="5c453-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="5c453-130">デュアル書き込みが正常に機能するように、設定時に選択した会社は Dataverse 環境で作成されます。</span><span class="sxs-lookup"><span data-stu-id="5c453-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="5c453-131">既定では、これらの会社は読み取り専用となっており、**IsDualWriteEnable** プロパティは **True** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5c453-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="5c453-132">さらに、既定の所有権を持つ業務部門の所有者とチームが作成され、会社名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5c453-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="5c453-133">マッピングを有効にする前に、既定のチームの所有者が指定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5c453-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="5c453-134">**会社 (CDM\_Company)** テーブルを検索するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5c453-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="5c453-135">Dynamics 365 のモデル駆動型のアプリで、右上隅のフィルターを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c453-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="5c453-136">ドロップダウン リストにて、**会社** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c453-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="5c453-137">結果を表示するには、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c453-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="5c453-138">デュアル書き込みの構成時にリンクしていた会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c453-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="5c453-139">**既定の所有チーム** 列に値が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5c453-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="5c453-140">次の図では、**既定の所有チーム** 列が **USMF デュアル書き込み** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5c453-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![既定の所有チームを確認する](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="5c453-142">デュアル書き込み対してにリンク可能な、リーガル テーブルまたは会社数の制限を確認する</span><span class="sxs-lookup"><span data-stu-id="5c453-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="5c453-143">マッピングを有効化した際に、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c453-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="5c453-144">*デュアル書き込みエラー: プラグインの登録に失敗しました：\[（プロジェクト DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea のパーティション マッピングを取得できません。エラー DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea で許容されるマッピングの最大パーティション数を超過超しました）\]、1 つまたは複数のエラーが発生しました。*</span><span class="sxs-lookup"><span data-stu-id="5c453-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="5c453-145">現在のところ、環境をリンク可能なリーガル テーブルの制限は、約 40 件です。</span><span class="sxs-lookup"><span data-stu-id="5c453-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="5c453-146">このエラーは、マッピングを有効化する際に発生し、環境間で 40 以上のリーガル テーブルがリンクされている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="5c453-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>
