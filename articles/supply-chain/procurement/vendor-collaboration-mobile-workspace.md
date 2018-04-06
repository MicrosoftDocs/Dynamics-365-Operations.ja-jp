---
title: "仕入先コラボレーションのモバイル ワークスペース"
description: "このトピックでは、[仕入先コラボレーション] モバイル ワークスペースに関する情報を提供します。 このワークスペースでは、仕入先が、承認のために送信された発注書に関する最新の状態を保つことができるようにします。 新規または更新された発注書および連絡先に関する情報を閲覧することもできます。"
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: bfbc0fdfcff809a7d22362961b9778355ed7317b
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="vendor-collaboration-mobile-workspace"></a><span data-ttu-id="12b50-105">仕入先コラボレーションのモバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="12b50-105">Vendor collaboration mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="12b50-106">このトピックでは、[**仕入先コラボレーション**] モバイル ワークスペースに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="12b50-106">This topic provides information about the **Vendor collaboration** mobile workspace.</span></span> <span data-ttu-id="12b50-107">このワークスペースでは、仕入先が、承認のために送信された発注書に関する最新の状態を保つことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="12b50-107">This workspace helps your vendors stay up to date about the purchase orders that have been sent to them for approval.</span></span> <span data-ttu-id="12b50-108">新規または更新された発注書および連絡先に関する情報を閲覧することもできます。</span><span class="sxs-lookup"><span data-stu-id="12b50-108">They can also view information about new and updated purchase orders and contacts.</span></span>

<span data-ttu-id="12b50-109">このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="12b50-109">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="12b50-110">概要</span><span class="sxs-lookup"><span data-stu-id="12b50-110">Overview</span></span> 
<span data-ttu-id="12b50-111">[仕入先コラボレーション] モバイル ワークスペースでは、仕入先が新しい発注書を常に把握できるようにし、Microsoft Dynamics 365 for Operations の Web クライアントで発注書の表示をしてから対応ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="12b50-111">The **Vendor collaboration** mobile workspace keeps vendors informed about new purchase orders, so that they can view purchase orders and then respond to them in the Microsoft Dynamics 365 for Finance and Operations, web client.</span></span> 

>[!NOTE]
> <span data-ttu-id="12b50-112">モバイル ワークスペースは仕入先コラボレーション Web インターフェイスの置き換えとしてではなく、補足として使用されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-112">The mobile workspace should be used as a supplement to the vendor collaboration web interface, not a replacement for it.</span></span> 

<span data-ttu-id="12b50-113">仕入先は [**仕入先コラボレーション**] モバイル ワークスペースを使用して、仕入先が承認用に送信された新しい発注書を表示できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-113">Your vendors can use the **Vendor collaboration** mobile workspace to view new purchase orders that are sent to them for approval.</span></span> <span data-ttu-id="12b50-114">これには、製品、数量、および配送指定日などの発注書情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-114">It shows purchase order information, such as products, quantities, and requested delivery dates.</span></span> <span data-ttu-id="12b50-115">価格情報も、各仕入先のコンフィギュレーションに応じて使用できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-115">Price information is also available, depending on the configuration of each vendor.</span></span> 

<span data-ttu-id="12b50-116">仕入先としてサインインするユーザーは、どの発注書が応答済みか、およびどの発注書がまだ顧客のアクション待ちかを参照できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-116">A user who signs in as a vendor will see which purchase orders have been responded to, and which purchase orders are still awaiting customer action.</span></span> <span data-ttu-id="12b50-117">たとえば、仕入先が別の出荷日を提案したものの、顧客がまだその日付に同意していないため、発注書が顧客のアクション待ちである場合があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-117">For example, a purchase order might be awaiting customer action because the vendor suggested another delivery date, but the customer hasn't yet agreed to that date.</span></span> <span data-ttu-id="12b50-118">仕入先は、確認済だが未出荷である発注書の一覧も参照することができます。</span><span class="sxs-lookup"><span data-stu-id="12b50-118">The vendor will also see a list of purchase orders that have been confirmed but haven't yet been delivered.</span></span> 

<span data-ttu-id="12b50-119">発注書に応答するために、仕入先は Web クライアントで使用可能な仕入先コラボレーション Web インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-119">To respond to a purchase order, the vendor must use the vendor collaboration web interface that is available in the web client.</span></span> <span data-ttu-id="12b50-120">したがって、仕入先も、ドキュメントの添付ファイル、行ごとの配送先住所、および仕入先に関連付けられている諸費用など、注文に関する詳細情報を得られます。</span><span class="sxs-lookup"><span data-stu-id="12b50-120">There, the vendor can also get more information about the order, such as document attachments, the delivery address per line, and charges that are associated with the vendor.</span></span> 

<span data-ttu-id="12b50-121">特別なセキュリティ ロールを持つ仕入先は、どの連絡担当者が仕入先勘定に登録されているかを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="12b50-121">Vendors that have a special security role can see which contact persons are registered for a vendor account.</span></span> <span data-ttu-id="12b50-122">同じセキュリティロールで、仕入先がすべての送信済ユーザー要求のステータスを表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="12b50-122">The same security role lets a vendor view the status of any user request that has been submitted.</span></span> 

<span data-ttu-id="12b50-123">Web クライアントの仕入先コラボレーション Web インターフェイスは、新しい連絡先の作成および新しいユーザーの要求を送信するために使用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-123">The vendor collaboration web interface in the web client must be used to create new contacts and submit new user requests.</span></span> 

<span data-ttu-id="12b50-124">[**仕入先コラボレーション**] モバイル ワークスペースは、仕入先がこれらのタスクを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="12b50-124">The **Vendor collaboration** mobile workspace lets a vendor perform these tasks:</span></span>

-   <span data-ttu-id="12b50-125">仕入先に送信された新規発注書の表示。</span><span class="sxs-lookup"><span data-stu-id="12b50-125">View new purchase orders that are sent to the vendor.</span></span>
-   <span data-ttu-id="12b50-126">仕入先が応答し、かつ顧客のアクション待ちである発注書の表示。</span><span class="sxs-lookup"><span data-stu-id="12b50-126">View purchase orders that the vendor has responded to, and that are awaiting customer action.</span></span>
-   <span data-ttu-id="12b50-127">確認済だが受入未完了である発注書の表示。</span><span class="sxs-lookup"><span data-stu-id="12b50-127">View purchase orders that have been confirmed but haven't yet been fully received.</span></span>
-   <span data-ttu-id="12b50-128">仕入先の登録されている連絡担当者情報の表示。</span><span class="sxs-lookup"><span data-stu-id="12b50-128">View contact person information that is registered for the vendor account.</span></span> <span data-ttu-id="12b50-129">(このタスクには、追加のセキュリティ ロールが必要です。)</span><span class="sxs-lookup"><span data-stu-id="12b50-129">(This task requires an additional security role.)</span></span>
-   <span data-ttu-id="12b50-130">仕入先により送信されたユーザー要求についての情報の表示し、および要求のステータスに従います。</span><span class="sxs-lookup"><span data-stu-id="12b50-130">View information about a user request that was submitted by the vendor, and follow the status of the request.</span></span> <span data-ttu-id="12b50-131">(このタスクには、追加のセキュリティ ロールが必要です。)</span><span class="sxs-lookup"><span data-stu-id="12b50-131">(This task requires an additional security role.)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="12b50-132">前提条件</span><span class="sxs-lookup"><span data-stu-id="12b50-132">Prerequisites</span></span>
<span data-ttu-id="12b50-133">組織に配置されている Microsoft Dynamics 365 のバージョンによって、前提条件は異なります。</span><span class="sxs-lookup"><span data-stu-id="12b50-133">The prerequisites vary, depending on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="12b50-134">Microsoft Dynamics 365 for Finance and Operations を使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="12b50-134">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span> 
<span data-ttu-id="12b50-135">Microsoft Dynamics 365 for Finance and Operations を組織に配置している場合、システム管理者は [仕入先コラボレーション] モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-135">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Vendor collaboration** mobile workspace.</span></span> <span data-ttu-id="12b50-136">手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12b50-136">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="12b50-137">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="12b50-137">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="12b50-138">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-138">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="12b50-139">前提条件</span><span class="sxs-lookup"><span data-stu-id="12b50-139">Prerequisite</span></span></th>
<th><span data-ttu-id="12b50-140">役割</span><span class="sxs-lookup"><span data-stu-id="12b50-140">Role</span></span></th>
<th><span data-ttu-id="12b50-141">説明</span><span class="sxs-lookup"><span data-stu-id="12b50-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12b50-142">プラットフォーム更新プログラム 3 を使用している場合は、KB 3216943 を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-142">KB 3216943 must be implemented if you're using Platform update 3.</span></span></td>
<td><span data-ttu-id="12b50-143">システム管理者</span><span class="sxs-lookup"><span data-stu-id="12b50-143">System administrator</span></span></td>
<td><span data-ttu-id="12b50-144">プラットフォーム更新プログラム 3 を使用している場合、KB 3216943 はバイナリ更新プログラムです。</span><span class="sxs-lookup"><span data-stu-id="12b50-144">KB 3216943 is a binary update that is required if you're using Platform update 3.</span></span> <span data-ttu-id="12b50-145">この KB を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-145">To implement this KB, the system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="12b50-146">Microsoft Dynamics Lifecycle Services (LCS) から KB 3216943 をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="12b50-146">Download KB 3216943 from Microsoft Dynamics Lifecycle Services (LCS).</span></span></li>
<li><span data-ttu-id="12b50-147">配置可能パッケージとして配信される、バイナリ更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="12b50-147">Install the binary update, which is delivered as a deployable package.</span></span> <span data-ttu-id="12b50-148">配置可能パッケージを適用する方法についての詳しい情報は、<a href="../../dev-itpro/deployment/apply-deployable-package-system.md">適用可能パッケージ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12b50-148">For information about how to apply a deployable package, see <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply a deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12b50-149">KB 4013633 を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-149">KB 4013633 must be implemented.</span></span></td>
<td><span data-ttu-id="12b50-150">システム管理者</span><span class="sxs-lookup"><span data-stu-id="12b50-150">System administrator</span></span></td>
<td><span data-ttu-id="12b50-151">KB 4013633 は、[<strong>手持ち在庫</strong>] モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="12b50-151">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Inventory on-hand</strong> mobile workspace.</span></span> <span data-ttu-id="12b50-152">KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-152">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="12b50-153"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">LCS からメタデータ修正プログラムのダウンロード</a>。</span><span class="sxs-lookup"><span data-stu-id="12b50-153"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from LCS</a>.</span></span></li>
<li><span data-ttu-id="12b50-154"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></span><span class="sxs-lookup"><span data-stu-id="12b50-154"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li><li><span data-ttu-id="12b50-155"><strong>SCMMobile</strong> モデルを含む<a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="12b50-155"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="12b50-156"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="12b50-156"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12b50-157">[<strong>仕入先コラボレーション</strong>] モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-157">The <strong>Vendor collaboration</strong> mobile workspace must be published.</span></span></td><td><span data-ttu-id="12b50-158">システム管理者</span><span class="sxs-lookup"><span data-stu-id="12b50-158">System administrator</span></span></td>
<td><span data-ttu-id="12b50-159">「<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12b50-159">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12b50-160">仕入先のユーザーは、Web クライアントで仕入先コラボレーション Web インターフェイスにアクセスし、仕入先コラボレーション ユーザーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-160">The vendor user must have access to the vendor collaboration web interface in the web client and must set up a vendor collaboration user.</span></span></td><td><span data-ttu-id="12b50-161">購買担当者およびシステム管理者</span><span class="sxs-lookup"><span data-stu-id="12b50-161">Purchasing professionals and the system administrator</span></span></td>
<td><span data-ttu-id="12b50-162">仕入先コラボレーション Web インターフェイスの設定および作業では、以下のトピックでの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="12b50-162">Follow the steps in the following topics to set up and work with the vendor collaboration web interface.</span></span>
<ul>
<li><span data-ttu-id="12b50-163"><a href="vendor-collaboration-work-external-vendors.md">外部仕入先との作業のために仕入先コラボレーションを使用</a></span><span class="sxs-lookup"><span data-stu-id="12b50-163"><a href="vendor-collaboration-work-external-vendors.md">Use vendor collaboration to work with external vendors</a></span></span></li>
<li><span data-ttu-id="12b50-164"><a href="manage-vendor-collaboration-users.md">仕入先コラボレーション ユーザーの管理</a></span><span class="sxs-lookup"><span data-stu-id="12b50-164"><a href="manage-vendor-collaboration-users.md">Manage vendor collaboration users</a></span></span></li>
<li><span data-ttu-id="12b50-165"><a href="set-up-maintain-vendor-collaboration.md">仕入先コラボレーションの設定と管理</a></span><span class="sxs-lookup"><span data-stu-id="12b50-165"><a href="set-up-maintain-vendor-collaboration.md">Set up and maintain vendor collaboration</a></span></span></li>
<li><span data-ttu-id="12b50-166"><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Finance and Operations で仕入先コラボレーションを使用して顧客に対応</a></span><span class="sxs-lookup"><span data-stu-id="12b50-166"><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Use vendor collaboration to work with customers in Finance and Operations</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="12b50-167">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="12b50-167">Download and install the mobile app</span></span>

<span data-ttu-id="12b50-168">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="12b50-168">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="12b50-169">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="12b50-169">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="12b50-170">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="12b50-170">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="12b50-171">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="12b50-171">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="12b50-172">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="12b50-172">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="12b50-173">Microsoft Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="12b50-173">Enter your Microsoft Dynamics 365 URL.</span></span>
4.  <span data-ttu-id="12b50-174">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-174">The first time that you sign in, you’re prompted for your user name and password.</span></span> <span data-ttu-id="12b50-175">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="12b50-175">Enter your credentials.</span></span>
5.  <span data-ttu-id="12b50-176">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-176">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="12b50-177">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-177">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="12b50-178">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="12b50-178">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="use-the-vendor-collaboration-mobile-workspace"></a><span data-ttu-id="12b50-179">仕入先コラボレーションのモバイル ワークスペースを使用します</span><span class="sxs-lookup"><span data-stu-id="12b50-179">Use the Vendor collaboration mobile workspace</span></span>
<span data-ttu-id="12b50-180">[**仕入先コラボレーション**] ワークスペースを選択すると、次のオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-180">When you select the **Vendor collaboration** workspace, you’ll see the following options.</span></span>

![仕入先コラボレーションのモバイル ワークスペース](./media/vendor-collaboration-mobile-app.png)

<span data-ttu-id="12b50-182">[**仕入先コラボレーション**] ワークスペースには、次のページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="12b50-182">The **Vendor collaboration** workspace includes the following pages.</span></span>

### <a name="contacts"></a><span data-ttu-id="12b50-183">連絡先</span><span class="sxs-lookup"><span data-stu-id="12b50-183">Contacts</span></span>
<span data-ttu-id="12b50-184">**連絡先** ページで、仕入先に設定されているすべての連絡先を表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="12b50-184">The **Contacts** page lets you see all the contacts that have been set up for the vendor account.</span></span> <span data-ttu-id="12b50-185">連絡担当者にエイリアスがある場合、連絡担当者の名前、主な子メール アドレス、およびユーザー エイリアスを表示します。</span><span class="sxs-lookup"><span data-stu-id="12b50-185">It shows the contact person's name, primary email address, and user alias, if the contact person has an alias.</span></span> <span data-ttu-id="12b50-186">このページは連絡担当者のユーザー アカウントが有効かどうかも表示します。</span><span class="sxs-lookup"><span data-stu-id="12b50-186">This page also shows whether the contact person's user account is active.</span></span> <span data-ttu-id="12b50-187">連絡先を選択すると、個人が連絡先となっている法人などの、連絡先の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-187">When you select a contact, you see contact details, such as the legal entities that the person is a contact for.</span></span> <span data-ttu-id="12b50-188">電話番号、代替の電子メール アドレスなどの連絡先情報も表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-188">You also see contact information, such as a telephone number or an alternative email address.</span></span>

### <a name="user-requests"></a><span data-ttu-id="12b50-189">ユーザー要求</span><span class="sxs-lookup"><span data-stu-id="12b50-189">User requests</span></span>
<span data-ttu-id="12b50-190">[**ユーザーの要求**] ページは、仕入先コラボレーション Web インターフェイスから送信した全てのユーザー要求が表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="12b50-190">The **User requests** page lets you see all the user requests that you've submitted via the vendor collaboration web interface.</span></span> <span data-ttu-id="12b50-191">それらの要求のステータスに従うこともできます。</span><span class="sxs-lookup"><span data-stu-id="12b50-191">You can also follow the status of those requests.</span></span> <span data-ttu-id="12b50-192">ユーザー要求を選択すると、要求内容、ユーザーの追加または無効化、セキュリティの変更を表示でき、そのユーザーに対してどのセキュリティ ロールが要求されたかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-192">When you select a user request, you can see what was requested, add or inactivate a user, change security, and see which security roles were requested for the user.</span></span>

### <a name="purchase-orders-ready-for-review"></a><span data-ttu-id="12b50-193">確認準備済発注書</span><span class="sxs-lookup"><span data-stu-id="12b50-193">Purchase orders ready for review</span></span>
<span data-ttu-id="12b50-194">[**確認準備済発注書**] ページは、顧客が送信したが未反応のままであるすべての発注書を表示します。</span><span class="sxs-lookup"><span data-stu-id="12b50-194">The **Purchase orders ready for review** page lets you see all the purchase orders that the customer has sent, but that haven't yet been responded to.</span></span> <span data-ttu-id="12b50-195">どの製品が要求され、いつそれらの製品が出荷されるべきかのような注文に関する選択された情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-195">You can view selected information about the order, such as which products were requested and when those products should be delivered.</span></span> <span data-ttu-id="12b50-196">価格情報も、仕入先のコンフィギュレーションに応じて使用できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-196">Price information is also available, depending on the configuration of the vendor.</span></span>

<span data-ttu-id="12b50-197">発注書にメモや添付ファイルがあるかどうかも確認できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-197">You can also see whether the purchase order has notes or attachments.</span></span> <span data-ttu-id="12b50-198">ただし、メモと添付ファイルを開くには、Web クライアントでの仕入先コラボレーション Web インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-198">However, to open notes and attachments, you must use vendor collaboration web interface in the web client.</span></span> <span data-ttu-id="12b50-199">詳細を含む全ての行をまとめて表示するには [**発注書明細行**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="12b50-199">Select **Purchase order line** to see all the lines together with their details.</span></span> <span data-ttu-id="12b50-200">各明細行では、インジケーターは、メモや添付ファイルがあるか、または配送先住所がヘッダーに示されている配送先住所とは異なるかどうかを表示します。</span><span class="sxs-lookup"><span data-stu-id="12b50-200">For each line, an indicator will show whether there are notes or attachments, or whether the delivery address differs from the delivery address that is shown on the header.</span></span>

<span data-ttu-id="12b50-201">発注書に対応するために、Web クライアントで仕入先コラボレーション Web インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-201">To respond to the purchase order, you must use the vendor collaboration web interface in the web client.</span></span>

### <a name="awaiting-customer-action"></a><span data-ttu-id="12b50-202">顧客のアクション待ち</span><span class="sxs-lookup"><span data-stu-id="12b50-202">Awaiting customer action</span></span>
<span data-ttu-id="12b50-203">[**顧客のアクション待ち**] ページでは、ユーザーまたは仕入先コラボレーションにアクセスし応答できる別の社員が、発注書を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="12b50-203">The **Awaiting customer action** page lets you find purchase orders that you or another person in your company who has access to vendor collaboration has responded to.</span></span> <span data-ttu-id="12b50-204">顧客が発注書において以下のアクションのうちの 1 つを実行する必要がある場合にのみ、発注書がこのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-204">The purchase orders are visible in this list only if the customer must take one of the following actions on the purchase order:</span></span>

-   <span data-ttu-id="12b50-205">発注書が却下された場合、顧客は元の注文を更新するか、またはキャンセルして再度送信するかのいずれかをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-205">If the purchase order was rejected, the customer must either update or cancel the original order, and then send it again.</span></span> <span data-ttu-id="12b50-206">発注書が再度送信されると、[**顧客のアクション待ち**] ページで表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="12b50-206">When the purchase order is sent again, it no longer appears on the **Awaiting customer action** page.</span></span>
-   <span data-ttu-id="12b50-207">発注書の変更が受け入れられると、顧客は元の注文を更新し確認のために再送信するか、または要求された変更ごとに注文を更新してすぐに確定するかのいずれかをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-207">If the purchase order was accepted with changes, the customer must either update the original order and then send it again for review, or update the order per the requested changes and then confirm it immediately.</span></span> <span data-ttu-id="12b50-208">どちらの場合も、発注書は [**顧客のアクション待ち**] ページで表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="12b50-208">In both cases, the purchase order no longer appears on the **Awaiting customer action** page.</span></span>
-   <span data-ttu-id="12b50-209">発注書が受入済になってもまだ [**顧客のアクション待ち**] ページに表示されている場合は、受入れのときに発注書が自動的に確定されていません。</span><span class="sxs-lookup"><span data-stu-id="12b50-209">If the purchase order was accepted but still appears on the **Awaiting customer action** page, the purchase order wasn't automatically confirmed when it was accepted.</span></span> <span data-ttu-id="12b50-210">現在購買担当者が、注文の状態を [**確認済**] に変更するのを待機しています。</span><span class="sxs-lookup"><span data-stu-id="12b50-210">It's now waiting for a purchasing agent to change the order status to **Confirmed**.</span></span> <span data-ttu-id="12b50-211">通常、仕入先が注文を受け入れるとすぐに、発注書は顧客と仕入先間の契約としてみなされます。</span><span class="sxs-lookup"><span data-stu-id="12b50-211">Typically, a purchase order is considered an agreement between the customer and the vendor as soon as the vendor accepts the order.</span></span> <span data-ttu-id="12b50-212">したがって、[**確認済**] ステータスへの更新は、通常は単なる形式的なものです。</span><span class="sxs-lookup"><span data-stu-id="12b50-212">Therefore, the update to **Confirmed** status is usually just a formality.</span></span>

<span data-ttu-id="12b50-213">発注書を選択する場合、対応に関する追加詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-213">When you select a purchase order, additional details appear about the response.</span></span> <span data-ttu-id="12b50-214">すべての明細行について、行の詳細と対応を表示できます。</span><span class="sxs-lookup"><span data-stu-id="12b50-214">You can see the line details and response for every line.</span></span> <span data-ttu-id="12b50-215">行のステータスで、次のうちのどの対応がなされたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="12b50-215">The line status shows which of the following responses has been given:</span></span>

-   <span data-ttu-id="12b50-216">承認済</span><span class="sxs-lookup"><span data-stu-id="12b50-216">Accepted</span></span>
-   <span data-ttu-id="12b50-217">拒否済</span><span class="sxs-lookup"><span data-stu-id="12b50-217">Rejected</span></span>
-   <span data-ttu-id="12b50-218">変更内容承認済</span><span class="sxs-lookup"><span data-stu-id="12b50-218">Accepted with changes</span></span>
-   <span data-ttu-id="12b50-219">代替済 / 代替</span><span class="sxs-lookup"><span data-stu-id="12b50-219">Substituted/Substitute</span></span>
-   <span data-ttu-id="12b50-220">スケジュール / スケジュール明細行に分割</span><span class="sxs-lookup"><span data-stu-id="12b50-220">Split into schedule/Schedule line</span></span>

<span data-ttu-id="12b50-221">[**配送中**] フィールドが [**はい**] または [**いいえ**] のいずれかに設定されて、明細行が配送されるかどうかを示すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="12b50-221">Note that the **Delivering** field is set to either **Yes** or **No** to indicate whether the lines will be delivered.</span></span> <span data-ttu-id="12b50-222">明細行が配送されない場合の以下の理由。</span><span class="sxs-lookup"><span data-stu-id="12b50-222">A line might not be delivered because for the following reasons:</span></span>

- <span data-ttu-id="12b50-223">明細行が却下されました。</span><span class="sxs-lookup"><span data-stu-id="12b50-223">The line was rejected.</span></span>
- <span data-ttu-id="12b50-224">代用が行われたので、元の明細行の受注済み注文としての配送予定はありません。</span><span class="sxs-lookup"><span data-stu-id="12b50-224">A substitution was made, and the original line isn't expected to be delivered as requested in the received order.</span></span>
- <span data-ttu-id="12b50-225">明細行が複数のスケジュール明細行に分割され、元の明細行の受注済注文としての配送予定はありません。</span><span class="sxs-lookup"><span data-stu-id="12b50-225">The line was split into multiple schedule lines, and the original line isn't expected to be delivered as requested in the received order.</span></span>

<span data-ttu-id="12b50-226">注文明細行の対応に加えた変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-226">Any changes that have been made to the order line response are shown.</span></span> <span data-ttu-id="12b50-227">ただし、アップロードされたメモと添付ファイルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="12b50-227">However, uploaded notes and attachments aren't shown.</span></span> <span data-ttu-id="12b50-228">メモと添付ファイルを開くには、Web クライアントで仕入先コラボレーション Web インターフェイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12b50-228">To view notes and attachments, you must use the vendor collaboration web interface in the web client.</span></span>

### <a name="open-confirmed-orders"></a><span data-ttu-id="12b50-229">確認済みのオープン注文</span><span class="sxs-lookup"><span data-stu-id="12b50-229">Open confirmed orders</span></span>
<span data-ttu-id="12b50-230">顧客によって発注書が確認されると、(発注書の状態が [**確認済**] に変更される)、確定済受注の公開に表示されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-230">When the purchase order is confirmed by the customer (that is, the status of the purchase order is changed to **Confirmed**), it appears in the open confirmed order.</span></span> <span data-ttu-id="12b50-231">これは、顧客が受領済に登録されるまでリストに保持されます。</span><span class="sxs-lookup"><span data-stu-id="12b50-231">It will remain in the list until it's registered as received by the customer.</span></span>

