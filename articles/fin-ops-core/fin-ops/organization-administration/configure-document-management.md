---
title: ドキュメント管理のコンフィギュレーション
description: このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。
author: jasongre
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 166189aaeaa60ba9d9df9df211bcffe2be7f2850
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111642"
---
# <a name="configure-document-management"></a><span data-ttu-id="85dfe-103">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-103">Configure document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85dfe-104">このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-104">This topic explains how to configure document management (document handling) so that it stores file attachments and notes for records.</span></span> <span data-ttu-id="85dfe-105">これには、この機能に関連する概念および機能に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-105">It includes information about the concepts and features that are involved in this functionality.</span></span>

<span data-ttu-id="85dfe-106">ドキュメントの管理の詳細については、簡単なビデオ [ドキュメント管理](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be) をご視聴ください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-106">To learn more about document management, watch the short [Document Management](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be) video.</span></span>

## <a name="configure-document-types"></a><span data-ttu-id="85dfe-107">ドキュメント タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-107">Configure document types</span></span>

<span data-ttu-id="85dfe-108">ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-108">Document types are used to categorize the documents that you attach to records or the templates that you create.</span></span> <span data-ttu-id="85dfe-109">各ドキュメント タイプは、固有の場所に格納されることができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-109">Each document type can be stored in a unique location.</span></span>

<span data-ttu-id="85dfe-110">ドキュメント タイプの既定のセットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-110">A default set of document types is provided.</span></span> <span data-ttu-id="85dfe-111">これらのドキュメント タイプを使用すると、ファイル、イメージ、メモ、または URL として添付ファイルを分類できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-111">You can use these document types to categorize an attachment as a file, image, note, or URL.</span></span> <span data-ttu-id="85dfe-112">**ファイル** および **画像** の既定のドキュメント タイプは、場所として **Azure ストレージ** を使用するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-112">The **File** and **Image** default document types are configured to use **Azure storage** as the location.</span></span>

<span data-ttu-id="85dfe-113">新しいドキュメント タイプを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="85dfe-113">To create a new document type, follow these steps.</span></span>

1. <span data-ttu-id="85dfe-114">**ドキュメント タイプ** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-114">Go to the **Document types** page.</span></span>
2. <span data-ttu-id="85dfe-115">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-115">Click **New**.</span></span>
3. <span data-ttu-id="85dfe-116">**タイプ** フィールドに、**SharePoint** または **HR** ドキュメントなどの新しいドキュメント タイプの短縮名を入力します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-116">In the **Type** field, enter a short name for the new document type, such as **SharePoint** or **HR Docs**.</span></span>
4. <span data-ttu-id="85dfe-117">**名前** フィールドに、**SharePoint ファイル** または **HR ドキュメント** などの長い名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-117">In the **Name** field, enter a longer name, such as **SharePoint files** or **HR Docs**.</span></span>
5. <span data-ttu-id="85dfe-118">**クラス** フィールドで、ドキュメント タイプの動作を定義するクラスを指定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-118">In the **Class** field, specify a class to define the behavior for the document type:</span></span>

    - <span data-ttu-id="85dfe-119">**ファイルの添付** - ユーザーはファイルを要求されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-119">**Attach file** – The user is prompted for a file.</span></span>
    - <span data-ttu-id="85dfe-120">**URL の添付** - ユーザーは、`https://www.microsoft.com` のように、**メモ** フィールドに URL を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-120">**Attach URL** – The user can enter a URL in the **Notes** field, such as `https://www.microsoft.com`.</span></span> <span data-ttu-id="85dfe-121">**添付ファイル** ページの **開く** ボタンをクリックすると [参照] タブに URL が開きます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-121">The **Open** button on the **Attachments** page will open the URL on a browser tab.</span></span>
    - <span data-ttu-id="85dfe-122">**簡易メモ** – ユーザーは **メモ** フィールドに簡易メモを追加できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-122">**Simple note** – The user can add a simple note in the **Notes** field.</span></span>

6. <span data-ttu-id="85dfe-123">**クラス** フィールドで **ファイルの添付** を指定した場合、**場所** フィールドで使用する記憶域メカニズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-123">If you specified **Attach file** in the **Class** field, in the **Location** field, specify the storage mechanism to use.</span></span>
7. <span data-ttu-id="85dfe-124">**場所** フィールドで **SharePoint** を指定した場合、**SharePoint アドレス** フィールドで Microsoft SharePoint アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-124">If you specified **SharePoint** in the **Location** field, specify the Microsoft SharePoint address in the **SharePoint Address** field.</span></span> <span data-ttu-id="85dfe-125">これを行うには、**編集** ボタン (鉛筆シンボル) をクリックし、**フォルダー選択** ダイアログ ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-125">To do this, click the **Edit** button (pencil symbol) and use the **Folder selection** dialog box.</span></span>

## <a name="configure-sharepoint-storage"></a><span data-ttu-id="85dfe-126">SharePoint 記憶域のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-126">Configure SharePoint storage</span></span>

<span data-ttu-id="85dfe-127">Microsoft SharePoint Online は、ネイティブでサポートされる保存場所の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="85dfe-127">Microsoft SharePoint Online is one of the storage locations that are supported natively.</span></span> <span data-ttu-id="85dfe-128">現在、SharePoint Online だけがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-128">Currently, only SharePoint Online is supported.</span></span> <span data-ttu-id="85dfe-129">オンプレミス SharePoint (ローカル SharePoint サーバー) のサポートは将来追加される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-129">Support for on-premises SharePoint (a local SharePoint server) may be added in the future.</span></span>

<span data-ttu-id="85dfe-130">SharePoint ストレージを使用するには、ドキュメント タイプの **場所** フィールドを **SharePoint** に設定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-130">To use SharePoint storage, set the **Location** field for a document type to **SharePoint**.</span></span> <span data-ttu-id="85dfe-131">その後、**SharePoint アドレス** フィールドに、有効な SharePoint アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-131">Then, in the **SharePoint Address** field, enter a valid SharePoint address.</span></span>

<span data-ttu-id="85dfe-132">SharePoint 記憶域を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-132">To configure SharePoint storage, follow these steps.</span></span>

1. <span data-ttu-id="85dfe-133">**ドキュメント管理パラメータ** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-133">Go to the **Document management parameters** page.</span></span>
2. <span data-ttu-id="85dfe-134">**SharePoint** タブの **既定の SharePoint サーバー** フィールドで、contosoax7.sharepoint.com など、SharePoint サイトに対して自動的に検出されたホスト名を確認します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-134">On the **SharePoint** tab, in the **Default SharePoint server** field, review the host name that was automatically detected for the SharePoint site, such as contosoax7.sharepoint.com.</span></span> <span data-ttu-id="85dfe-135">通常、SharePoint ホスト名は tenantname.sharepoint.com の形式で、そのテナントのアカウントは `user1@tenantname.onmicrosoft.com` の形式で示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-135">Typically, the SharePoint host name is in the form tenantname.sharepoint.com, and accounts on that tenant are in the form `user1@tenantname.onmicrosoft.com`.</span></span>

    <span data-ttu-id="85dfe-136">既定の SharePoint サーバーが指定されていない場合は、通常、テナントの SharePoint サイトが存在しないか、有効な Microsoft 365 ライセンスが現在のユーザー (管理者) に関連付けられていないかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="85dfe-136">Typically, if no default SharePoint server is specified, either there is no SharePoint site for the tenant, or a valid Microsoft 365 license isn't associated with the current user (the admin).</span></span>

4. <span data-ttu-id="85dfe-137">オプション: **SharePoint 接続** のテスト をクリックし、指定された SharePoint ホスト名をテストします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-137">Optional: Click **Test SharePoint connection** to test the specified SharePoint host name.</span></span> <span data-ttu-id="85dfe-138">これでセキュリティとライセンスが正しく機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-138">This verifies that the security and license are working correctly.</span></span> 
5. <span data-ttu-id="85dfe-139">オプション: **SharePoint を開く** をクリックし、指定された SharePoint ホスト名をブラウザーで開きます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-139">Optional: Click **Open SharePoint** to open the specified SharePoint host name in a browser.</span></span> <span data-ttu-id="85dfe-140">これはセキュリティを検証せず、ブラウザのタブで SharePoint パスを開くだけの簡単に検索であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-140">Note that this does not verify security, it just opens the SharePoint path in a browser tab for easy exploration.</span></span>

### <a name="troubleshooting-sharepoint-communication"></a><span data-ttu-id="85dfe-141">SharePoint 通信のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="85dfe-141">Troubleshooting SharePoint communication</span></span>

<span data-ttu-id="85dfe-142">SharePoint 通信は、次の条件が満たされた場合にのみ、現在のユーザーに対して機能します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-142">SharePoint communication works for the current user only if the following conditions are met:</span></span>

- <span data-ttu-id="85dfe-143">Microsoft 365 ライセンスが、ユーザーのアカウントに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-143">A Microsoft 365 license is associated with the user's account.</span></span>
- <span data-ttu-id="85dfe-144">ユーザーは、外部ユーザーではなくテナントの一般的なユーザーです (別のテナントのユーザーなど)。</span><span class="sxs-lookup"><span data-stu-id="85dfe-144">The user is a typical user on the tenant, not an external user (for example, a user from another tenant).</span></span>
- <span data-ttu-id="85dfe-145">テナント用の SharePoint サイト (たとえば、 Contoso.SharePoint.com など) が存在します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-145">There is a SharePoint site for the tenant (for example, Contoso.SharePoint.com).</span></span>
- <span data-ttu-id="85dfe-146">SharePoint サイトでは、**このサイトが検索結果として表示されるのを許可** するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-146">The SharePoint site is configured to **Allow this site to appear in search results**.</span></span>
- <span data-ttu-id="85dfe-147">ユーザーは、ドキュメントが格納されているフォルダにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-147">The user has access to the folder that the document is stored in.</span></span>

<span data-ttu-id="85dfe-148">SharePoint に保存されているドキュメントが開かず、プレビューに表示されない場合は、次の手順に従って問題をトラブルシューティングします:</span><span class="sxs-lookup"><span data-stu-id="85dfe-148">If documents stored in SharePoint don't open or don't display in preview, follow these steps to troubleshoot the issue:</span></span> 

1. <span data-ttu-id="85dfe-149">管理者アカウントに電子メール アカウントが関連付けられていることを確認します (**ユーザー** ページで確認または変更します)。</span><span class="sxs-lookup"><span data-stu-id="85dfe-149">Verify the Admin account has an associated email account (verify or change this in the **User** page).</span></span> <span data-ttu-id="85dfe-150">これが設定されていない場合は、OData Excel アドインを使用して電子メールとプロバイダーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-150">If this isn't set up, you need to add the email and provider  via the OData Excel add-in.</span></span> <span data-ttu-id="85dfe-151">既定では、Excel デザインに電子メール アドレスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-151">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="85dfe-152">ユーザーは、Excel デザインを編集し、すべてのフィールドを追加し、適用、および更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-152">The user needs to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="85dfe-153">完了すると、管理者アカウントを更新できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-153">Once complete, you can update the Admin account.</span></span>

2. <span data-ttu-id="85dfe-154">管理者アカウントに電子メール アカウントが関連付けられたら、Dynamics に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-154">After the Admin account has an associated email account, sign in to Dynamics as the admin.</span></span>

3. <span data-ttu-id="85dfe-155">SharePoint に保存されている添付ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-155">Open an attachment that is stored in SharePoint.</span></span>

4. <span data-ttu-id="85dfe-156">添付ファイル ページおよび構成されている SharePoint フォルダーに対する読み取りアクセス権を持つ別のユーザー アカウントでログインします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-156">Sign in with another user account that has read access to the attachments page and the configured SharePoint folder.</span></span> <span data-ttu-id="85dfe-157">添付ファイルを開いてプレビューすることもできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-157">Verify that they can also open and preview the attachment.</span></span>

## <a name="configure-file-types"></a><span data-ttu-id="85dfe-158">ファイルの種類のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-158">Configure file types</span></span>

<span data-ttu-id="85dfe-159">許可されているファイル拡張子のリストを変更することで、ユーザーがレコードに添付できるファイルの種類を制御できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-159">By modifying the list of file extensions that are allowed, you can control the types of files that users can attach to records.</span></span>

<span data-ttu-id="85dfe-160">ファイル タイプを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="85dfe-160">To specify file types, follow these steps.</span></span>

1. <span data-ttu-id="85dfe-161">**ドキュメント管理パラメータ** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-161">Go to the **Document management parameters** page.</span></span>
2. <span data-ttu-id="85dfe-162">**ファイル タイプ** タブで、既定のファイル タイプを確認します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-162">On the **File types** tab, review the default file types.</span></span>
3. <span data-ttu-id="85dfe-163">ユーザーがレコードに添付できないファイル タイプを削除し、ユーザーがレコードに添付できるファイル タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-163">Remove any file types that users should not be able to attach to records, and add any file types that users should be able to attach to records.</span></span>

## <a name="configure-document-preview"></a><span data-ttu-id="85dfe-164">ドキュメント プレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-164">Configure document preview</span></span>

<span data-ttu-id="85dfe-165">添付ファイルのプレビューには、Microsoft Office Online Server で提供される Web アプリ オープン プラットフォーム インターフェイス (WOPI) を使用します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-165">The attachments preview uses the Web app Open Platform Interface (WOPI) that is provided by Microsoft Office Online Server.</span></span> <span data-ttu-id="85dfe-166">**ドキュメント管理パラメーター** ページの **全般** タブの **Office Web Apps サーバー** フィールドで、添付ファイルのプレビューに使用する Office Online サーバー インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-166">On the **Document management parameters** page, on the **General** tab, in the **Office Web Apps Server** field, specify the Office Online Server instance to use for attachment previews.</span></span> <span data-ttu-id="85dfe-167">既定値は、クラウドベースの WOPI サーバーをポイントする `https://onenote.officeapps.live.com` です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-167">The default value is `https://onenote.officeapps.live.com`, which points to the cloud-based WOPI server.</span></span> 

> [!NOTE]
> <span data-ttu-id="85dfe-168">次の場合は、指定通りの **Office Web Apps サーバー** フィールドを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-168">For the following situations, you will need to adjust the **Office Web Apps Server** field as specified.</span></span> 
> -  <span data-ttu-id="85dfe-169">中国の環境では、https://onenote.partner.officewebapps.cn を使用します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-169">For environments in China, use https://onenote.partner.officewebapps.cn.</span></span> 
> -  <span data-ttu-id="85dfe-170">Government Commmunity Cloud (GCC) の環境では、https://gb4-onenote.officeapps.live.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-170">For environments in the Government Commmunity Cloud (GCC), use https://gb4-onenote.officeapps.live.com.</span></span>

### <a name="for-a-microsoft-dynamics-365-finance--operations-on-premises-environment"></a><span data-ttu-id="85dfe-171">Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境の場合</span><span class="sxs-lookup"><span data-stu-id="85dfe-171">For a Microsoft Dynamics 365 Finance + Operations (on-premises) environment</span></span>

<span data-ttu-id="85dfe-172">財務 + 運営の規定のクラウドベース WOPI サーバーが、プレビューを提供する添付ファイルを読み込みできません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-172">The default cloud-based WOPI server in Finance + Operations can't read the attachment file to provide a preview.</span></span> <span data-ttu-id="85dfe-173">プレビューが必要な場合は、[オンプレミス Office Online サーバー インスタンスをインストールし](/officeonlineserver/deploy-office-online-server)、それを環境内で構成する必要あります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-173">If previews are required, you must [install an on-premises Office Online Server instance](/officeonlineserver/deploy-office-online-server) and configure it inside the environment.</span></span> <span data-ttu-id="85dfe-174">**Office Web アプリケーション サーバー** フィールドを、インストールされている Office Online Server インスタンスのホスト名に設定し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85dfe-174">Set the **Office Web Apps Server** field to the host name of the installed Office Online Server instance, and then click **Save**.</span></span>

<span data-ttu-id="85dfe-175">プレビューが必要な場合は、**Office Web アプリケーション サーバー** フィールドを `https://localhost` に設定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-175">If previews aren't required, set the **Office Web Apps Server** field to `https://localhost`.</span></span> <span data-ttu-id="85dfe-176">プレビューは、その後は、エラー メッセージではなく、「プレビューを利用できません」というメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-176">The preview will then show the message "No preview available" instead of an error message.</span></span>

### <a name="document-preview-wopi-will-not-work-in-environments-with-an-ip-safe-list-enabled"></a><span data-ttu-id="85dfe-177">ドキュメント プレビュー (WOPI) は、IP セーフ リストが有効になっている環境では機能しません</span><span class="sxs-lookup"><span data-stu-id="85dfe-177">Document preview (WOPI) will not work in environments with an IP safe list enabled</span></span>

<span data-ttu-id="85dfe-178">プレビューを提供する WOPI サービスは、ファイル サービスに接続してファイルを取得してレンダリングすることができないため、ドキュメント プレビュー (WOPI) は、IP セーフ リストが有効になっている環境では動作しません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-178">Document preview (WOPI) will not work in environments with an IP safe list enabled, because the WOPI service that provides the preview will not be able to connect back to the file service to retrieve the file for rendering.</span></span>

## <a name="other-configuration"></a><span data-ttu-id="85dfe-179">他のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-179">Other configuration</span></span>

<span data-ttu-id="85dfe-180">これらのオプションが使用されることはほとんどありませんが、考慮すべきその他のコンフィギュレーション オプションを次に示します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-180">Here are some other configuration options to consider, although these options are rarely used:</span></span>

- <span data-ttu-id="85dfe-181">**ドキュメント管理パラメーター** ページの、**一般** タブで、**ドキュメント テーブルの使用** オプションを使用して、**アクティブ ドキュメント テーブル** 許可リストを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-181">On the **Document management parameters** page, on the **General** tab, you can use the **Use Document Tables** option to enable the **Active document tables** allow list.</span></span> <span data-ttu-id="85dfe-182">このオプションを **はい** に設定すると、他のすべてのテーブルの添付ファイルが無効になります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-182">If you set this option to **Yes**, you disable attachments on all other tables.</span></span> <span data-ttu-id="85dfe-183">したがって、必要なときにのみこのオプションをオンにしてください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-183">Therefore, turn on this option only when it's required.</span></span>
- <span data-ttu-id="85dfe-184">**ドキュメント管理パラメーター** ページの、**全般** タブで、**最大ファイル サイズ(単位: メガバイト)** フィールドを使用して、添付ファイルの最大ファイル サイズを設定できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-184">On the **Document management parameters** page, on the **General** tab, you can use the **Maximum file size in megabytes** field to set the maximum file size for attachments.</span></span> <span data-ttu-id="85dfe-185">SharePoint がドキュメント タイプとして使用される場合、ユーザーは最大ファイル サイズが 262 メガバイトのドキュメントのみをアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-185">Note that when SharePoint is used as a document type, users can only upload a document up to a maximum file size of 262 megabytes.</span></span> 
- <span data-ttu-id="85dfe-186">**オプション** ページ (**設定** \> **ユーザー オプション**) では、**基本設定** タブで、**ドキュメント処理の有効化** オプションを使用して、ドキュメント処理を無効にします (ドキュメント管理)。</span><span class="sxs-lookup"><span data-stu-id="85dfe-186">On the **Options** page (**Settings** \> **User options**), on the **Preferences** tab, you can use the **Enable document handling** option to disable document handling (document management).</span></span>

## <a name="accessing-document-management-attachments"></a><span data-ttu-id="85dfe-187">ドキュメント管理添付ファイルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="85dfe-187">Accessing document management attachments</span></span> 

<span data-ttu-id="85dfe-188">ドキュメント管理は、データを含むほとんどのページのトップにある **添付** ボタンとして、ユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-188">Document management appears to users as the **Attach** button at the top of most pages that contain data.</span></span> <span data-ttu-id="85dfe-189">**添付** ボタンを選択した場合 (または対応するキーボード ショートカット **Ctrl**+**Shift**+**A** を使用した場合)、ページで現在選択されているコントロールのデータ ソースのコンテキストで **添付ファイル** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-189">When you select the **Attach** button (or when you use the corresponding keyboard shortcut, **Ctrl**+**Shift**+**A**), the **Attachments** page is opened in the context of the data source of the control that is currently selected on the page.</span></span> <span data-ttu-id="85dfe-190">このページには、対応するデータ ソースに関連するすべての添付ファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-190">This page shows all the attachments that are related to the corresponding data source.</span></span> 

<span data-ttu-id="85dfe-191">**添付** ボタンには、現在選択されているレコードの添付ファイルの数も表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-191">The **Attach** button also shows a count of the attachments for the currently selected record.</span></span> <span data-ttu-id="85dfe-192">したがって、現在のレコードの添付ファイルが存在するかどうかを確認するには、**添付ファイル** ページを開いておく必要はありません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-192">Therefore, you can determine whether there are attachments for the current record without having to open the **Attachments** page.</span></span> <span data-ttu-id="85dfe-193">このボタンでは、0 ～ 9 件の添付ファイルの正確なカウントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-193">The button shows exact counts for zero through nine attachments.</span></span> <span data-ttu-id="85dfe-194">9 つ以上の添付ファイルがある場合、このボタンには、**9+** がカウントとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-194">If there are more than nine attachments, the button shows **9+** as the count.</span></span> <span data-ttu-id="85dfe-195">このようにして、カウントが大きくなると生じる可能性があるパフォーマンスへの影響と視覚的なノイズが減少します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-195">In this way, the performance impact and visual noise that exact larger counts might cause are reduced.</span></span>

### <a name="showing-related-document-attachments"></a><span data-ttu-id="85dfe-196">関連ドキュメントの添付ファイルの表示</span><span class="sxs-lookup"><span data-stu-id="85dfe-196">Showing related document attachments</span></span>
<span data-ttu-id="85dfe-197">バージョン 10.0.12 では、**関連するドキュメントの添付ファイルを表示** 機能により、ドキュメント添付ファイルのエクスペリエンスが次の方法で変更されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-197">In version 10.0.12, the **Show related document attachments** feature changes the document attachment experience in the following ways.</span></span> 

-  <span data-ttu-id="85dfe-198">この機能を有効にする場合、1 つのデータ ソースに関連する添付ファイルだけが **添付ファイル** ページに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-198">When the feature is enabled, the **Attachments** page no longer shows only attachments that are related to a single data source.</span></span> <span data-ttu-id="85dfe-199">代わりに、ユーザーは有効なレコードに関連付けられている、ページ上の他のデータ ソースから添付ファイルを表示してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-199">Instead, users can see and access attachments from other data sources on the pages that are related to the active record.</span></span> <span data-ttu-id="85dfe-200">これを生じさせるため、データ ソースが次の条件を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-200">For this to occur, the data source must:</span></span> 
    -  <span data-ttu-id="85dfe-201">内部結合または外部結合を使用して、親データソースに直接関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-201">Be directly related to the parent data source by means of an inner or outer join.</span></span>
    -  <span data-ttu-id="85dfe-202">基数が 1:1 または 0:1 のアクティブ、遅延、またはパッシブ結合を使用して、親データソースに直接関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-202">Be directly related to the parent data source by means of an active, delayed, or passive join with either 1:1 or 0:1 cardinality.</span></span>

    <span data-ttu-id="85dfe-203">この基準では、ヘッダー レコードでの添付ファイルの表示時に、子コレクション (明細行など) からの添付ファイルの表示が除外されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-203">Note that this criteria excludes showing attachments from child collections (such as lines) when looking at attachments on the header record.</span></span>  

    <span data-ttu-id="85dfe-204">**添付** ボタンの添付ファイルの数についても、この変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-204">The count of attachments on the **Attach** button also reflects this change.</span></span> 

-  <span data-ttu-id="85dfe-205">ユーザーは **添付ファイル** ページの関連するデータ ソース間で、添付ファイルを移動したりコピーしたりできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-205">Users can move and copy attachments between the related data sources on the **Attachments** page.</span></span>

## <a name="document-attachment-history"></a><span data-ttu-id="85dfe-206">ドキュメントの添付ファイルの履歴</span><span class="sxs-lookup"><span data-stu-id="85dfe-206">Document attachment history</span></span>

<span data-ttu-id="85dfe-207">バージョン 10.0.16/プラットフォーム更新プログラム 40 以降、レコードの添付ファイルに対して履歴メカニズムが使用できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-207">Starting in version 10.0.16/Platform update 40, a history mechanism has been made available for record attachments.</span></span> <span data-ttu-id="85dfe-208">これにより、個々の添付ファイルに関連するアクションの監査を組織で管理することができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-208">This allows your organization to maintain an audit of actions related to individual attachments.</span></span> <span data-ttu-id="85dfe-209">特に、添付ファイルが作成された日時、マークされた保留中の削除、復元、削除、または移動、そのアクションを実行したユーザーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-209">In particular, you can see when an attachment was created, marked for pending deletion, restored, deleted, or moved and who performed that action.</span></span> <span data-ttu-id="85dfe-210">添付ファイルの履歴は 10.0.16/プラットフォーム更新プログラム 40 まで維持されないため、そのバージョンよりも前の添付ファイルに対するアクションは使用できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-210">Note that attachment history is not maintained until 10.0.16/Platform update 40, so any actions on attachments prior to that version will not be available.</span></span>  

### <a name="configuration-of-document-attachment-history"></a><span data-ttu-id="85dfe-211">ドキュメントの添付ファイル履歴のコンフィグレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-211">Configuration of document attachment history</span></span>
<span data-ttu-id="85dfe-212">**ドキュメント管理パラメータ** > **一般** > **履歴** > **ドキュメント履歴の有効化** に移動してドキュメントの添付ファイルの履歴を有効 (または無効) にできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-212">Document attachment history can be enabled (or disabled) by going to **Document management parameters** > **General** > **History** > **Enable document history**.</span></span> <span data-ttu-id="85dfe-213">既定の履歴保持期間は 180 日ですが、この値は **履歴を保持する日数** フィールドを使用して必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-213">The default history retention period is 180 days, but this value can be modified as needed using the **Number of days to retain history** field.</span></span> 

### <a name="viewing-an-attachments-history"></a><span data-ttu-id="85dfe-214">添付ファイルの履歴の表示</span><span class="sxs-lookup"><span data-stu-id="85dfe-214">Viewing an attachment's history</span></span>
<span data-ttu-id="85dfe-215">レコード添付ファイルの履歴を表示するには、2 つのエントリ ポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-215">There are two entry points for viewing the history of a record attachment:</span></span>

- <span data-ttu-id="85dfe-216">特定のレコードの添付ファイル確認するときは (詳細については [ドキュメント管理添付ファイルへのアクセス](configure-document-management.md#accessing-document-management-attachments) セクションを参照してください)、アクション ウィンドウの **ドキュメント履歴** ボタンを選択すると **添付ファイル** ページで現在の添付ファイル セットの履歴を表示できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-216">When you are looking at the attachments for a specific record (see the [Accessing document management attachments](configure-document-management.md#accessing-document-management-attachments) section for more details), you can view the history for the current set of attachments on the **Attachments** page by selecting the **Document history** button in the Action pane.</span></span>   
- <span data-ttu-id="85dfe-217">管理者は、**ドキュメント管理パラメータ** ページの **履歴** セクションで **ドキュメント履歴** ボタンを選択できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-217">Administrators can select the **Document history** button in the **History** section of the **Document management parameters** page.</span></span> <span data-ttu-id="85dfe-218">このアクションは、システム内のすべての添付ファイルの一覧を表示する **ドキュメント履歴** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-218">This action opens the **Document history** page, which shows a list of all attachments in the system.</span></span> <span data-ttu-id="85dfe-219">その後、任意のレコードをドリルダウンして選択した添付ファイルの詳細な履歴を確認します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-219">You can then drill into any record to see the detailed history for the selected attachment.</span></span>  

## <a name="attachment-recovery"></a><span data-ttu-id="85dfe-220">添付ファイルの回復</span><span class="sxs-lookup"><span data-stu-id="85dfe-220">Attachment recovery</span></span>

<span data-ttu-id="85dfe-221">プラットフォーム更新プログラム 29 では、添付ファイルの回復機能が追加され、設定された期間内に回復されるレコードの添付ファイルのごみ箱が提供されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-221">In Platform update 29, an attachment recovery feature has been added that provides a recycle bin for record attachments to be recovered within a configured period of time.</span></span>

### <a name="configuration-of-attachment-recovery"></a><span data-ttu-id="85dfe-222">添付ファイルの復元のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="85dfe-222">Configuration of attachment recovery</span></span>

<span data-ttu-id="85dfe-223">**ドキュメント管理パラメータ** > **一般** >  **遅延削除** > **遅延削除の有効化** に移動して添付ファイルの回復を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-223">Attachment recovery can be enabled by going to **Document management parameters** > **General** >  **Deferred deletion** > **Deferred deletion enabled**.</span></span> <span data-ttu-id="85dfe-224">**削除を延期する日数** のデフォルトは 30 日ですが、必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-224">The default for **Number of days to defer deletion** is 30 days but can be changed as needed.</span></span> <span data-ttu-id="85dfe-225">**削除を延期する日数** 値がゼロの場合、削除された添付ファイルが無期限に回復可能であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-225">If the **Number of days to defer deletion** value is zero, this means that the deleted attachments will be recoverable for an indefinite period.</span></span> 

<span data-ttu-id="85dfe-226">添付ファイルの回復を有効にすると、この名前のバッチジョブが作成されます: "保存期間の終了に達した削除済み参照のスキャン"。</span><span class="sxs-lookup"><span data-stu-id="85dfe-226">After attachment recovery is enabled, a batch job with this name will be created, "Scans for deleted references which have reached the end of their retention period".</span></span> <span data-ttu-id="85dfe-227">このバッチ ジョブは **削除を延期する日数** を使用して、**削除されたデータと時間** に基づいて削除された添付ファイルを保持する期間を決定します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-227">This batch job will use the **Number of days to defer deletion** to determine how long to retain a deleted attachment based on the **Deleted data and time**.</span></span>

### <a name="deleting-attachments-when-attachment-recovery-is-active"></a><span data-ttu-id="85dfe-228">添付ファイルの回復がアクティブな場合の添付ファイルの削除</span><span class="sxs-lookup"><span data-stu-id="85dfe-228">Deleting attachments when attachment recovery is active</span></span>

<span data-ttu-id="85dfe-229">ユーザーが添付ファイルを削除すると通知がメッセージ センターに追加され、削除の確認と削除が意図されていない場合にアクションを取り消すオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-229">When a user deletes an attachment, a notification will be added to the Message Center to provide confirmation of the deletion and an option to undo to the action if the deletion was unintended.</span></span>

<span data-ttu-id="85dfe-230">テーブル拡張サポートが組み込まれているため、**DocuRef** や **DocuValue** テーブルの拡張やカスタム フィールド値は保持されリカバリが可能です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-230">Table extension support has been built-in, so that any extension or custom field values on the **DocuRef** or **DocuValue** tables will be retained to enable their recovery.</span></span> 

### <a name="recovering-attachments"></a><span data-ttu-id="85dfe-231">添付ファイルの回復</span><span class="sxs-lookup"><span data-stu-id="85dfe-231">Recovering attachments</span></span>

<span data-ttu-id="85dfe-232">添付ファイルの回復が有効な場合、添付ファイルは次の 3 つの方法のいずれかで回復できます:</span><span class="sxs-lookup"><span data-stu-id="85dfe-232">When attachment recovery is enabled, attachments can be recovered in one of three ways:</span></span>
1. <span data-ttu-id="85dfe-233">削除した後すぐに、ユーザーは **添付ファイルを削除しました** 通知の [元に戻す] リンクを使用できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-233">Immediately after deletion, the user can use the undo link in the **Attachment deleted** notification.</span></span>
2. <span data-ttu-id="85dfe-234">**添付ファイル** ページで **削除済み添付ファイル** ボタンを使用して、特定のレコードで回復できる削除された添付ファイルのリストにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-234">On the **Attachments** page, a **Deleted attachments** button provides access to the list of deleted attachments that can be recovered for a particular record.</span></span> <span data-ttu-id="85dfe-235">削除された添付ファイルは、確認のために開いたり、完全に削除したり、復元できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-235">The deleted attachments can be opened for review, permanently deleted, or restored.</span></span>
3. <span data-ttu-id="85dfe-236">**システム管理** > **照会** で **削除済み添付ファイル** ページから削除された添付ファイルのリストへのアクセスが提供され、任意のレコードに回復できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-236">In **System administration** > **Inquiries**, the **Deleted attachments** page provides access to the list of deleted attachments that can be recovered for any record.</span></span> <span data-ttu-id="85dfe-237">削除された添付ファイルは、確認のために開いたり、完全に削除したり、復元できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-237">The deleted attachments can be opened for review, permanently deleted, or restored.</span></span>

## <a name="scanning-attachments-for-viruses-and-malicious-code"></a><span data-ttu-id="85dfe-238">添付ファイルでのウイルスおよび悪意のあるコードのスキャン</span><span class="sxs-lookup"><span data-stu-id="85dfe-238">Scanning attachments for viruses and malicious code</span></span>
<span data-ttu-id="85dfe-239">添付ファイルを操作するときに、ウイルスや悪意のあるコードを探すためのファイルをスキャンしたいかもしれません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-239">When you work with attachments, you might want to scan the files for viruses and malicious code.</span></span> <span data-ttu-id="85dfe-240">したがって、バージョン10.0.12 以降では、ユーザーが添付ファイルを操作するときに、選択したファイル スキャン ソフトウェアでファイル アップロード プロセスに統合できるように、拡張ポイントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-240">Therefore, in version 10.0.12 and later, extension points are available so that customers can integrate with the file scanning software of their choice when they work with attachments.</span></span> <span data-ttu-id="85dfe-241">ファイルのアップロードに同様の拡張点も利用可能です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-241">A similar extension point is also available for file upload.</span></span> <span data-ttu-id="85dfe-242">詳細については、[ファイルのアップロード コントロール](../../dev-itpro/user-interface/file-upload-control.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-242">For more information, see [File upload control](../../dev-itpro/user-interface/file-upload-control.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85dfe-243">初期状態では、Finance and Operations アプリはファイルのウイルスや悪意のあるコードをスキャンせず、ファイルをスキャンするための特定のソフトウェアはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-243">Out of the box, Finance and Operations apps don't scan files for viruses and malicious code, and we don't recommend specific software for file scanning.</span></span> <span data-ttu-id="85dfe-244">代わりに、お客様は、独自のファイル スキャン ソフトウェアを選択し、ファイルのスキャンにソフトウェアまたはサービスを使用できるように適切なコードをデリゲート ハンドラーに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-244">Instead, customers are responsible for choosing their own file scanning software, and for adding the appropriate code to the delegate handlers so that they can use the software or service of their choice to scan files.</span></span>

<span data-ttu-id="85dfe-245">**Docu** クラスでは、次の 2 つのデリゲートが公開されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-245">The **Docu** class exposes the following two delegates.</span></span> <span data-ttu-id="85dfe-246">これらのデリゲートに対して、ドキュメントのスキャンを目的としてハンドラーを実装できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-246">Handlers can be implemented for these delegates for document scanning purposes:</span></span>

- <span data-ttu-id="85dfe-247">**Docu.delegateScanDocument()** – このデリゲートによって、新しいドキュメント添付ファイルがアップロードされたときに、またはユーザーが既存の添付ファイルをプレビューまたはダウンロードしようとしたときに、ファイル スキャン ロジックが適用されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-247">**Docu.delegateScanDocument()** – This delegate applies the file scanning logic when a new document attachment is uploaded, or when a user tries to preview or download an existing attachment.</span></span> <span data-ttu-id="85dfe-248">スキャン サービスによってファイルが悪質であると判断された場合、対応するアクションは失敗します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-248">The corresponding action will fail if the scanning service determines that the file is malicious.</span></span>
-  <span data-ttu-id="85dfe-249">**Docu.delegateScanDeletedDocument()**: このデリゲートによって、ユーザーがファイルをプレビューまたはダウンロードしようとしたときに、ファイルのスキャン ロジックが添付ファイルのごみ箱ドキュメントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-249">**Docu.delegateScanDeletedDocument()** – This delegate applies the file scanning logic to documents in the attachments recycle bin when a user tries to preview or download a file.</span></span> <span data-ttu-id="85dfe-250">スキャン サービスによってファイルが悪質であると判断された場合、対応するアクションは失敗します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-250">The corresponding action will fail if the scanning service determines that the file is malicious.</span></span>

### <a name="implementation-details"></a><span data-ttu-id="85dfe-251">実装詳細</span><span class="sxs-lookup"><span data-stu-id="85dfe-251">Implementation details</span></span>
<span data-ttu-id="85dfe-252">次の **ScanDocuments** クラスの例は、2 つのハンドラーの定型コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-252">The following example of the **ScanDocuments** class shows boilerplate code for the two handlers.</span></span> <span data-ttu-id="85dfe-253">デリゲートのハンドラーを実装する方法の一般情報については、[要求または応答シナリオの EventHandlerResult クラス](../../dev-itpro/dev-tools/event-handler-result-class.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-253">For general information about how to implement handlers for delegates, see [EventHandlerResult classes in request or response scenarios](../../dev-itpro/dev-tools/event-handler-result-class.md).</span></span>

```xpp
    public final class ScanDocuments
    {

        [SubscribesTo(classStr(Docu), staticDelegateStr(Docu, delegateScanDocument))]
        public static void Docu_delegateScanDocument(DocuRef _docuRef, EventHandlerRejectResult _validationResult)
        {
            if (!ScanDocuments::scanDocument(_docuRef))
            {
                _validationResult.reject();
            }
        }

        [SubscribesTo(classStr(Docu), staticDelegateStr(Docu, delegateScanDeletedDocument))]
        public static void Docu_delegateScanDeletedDocument(DocuDeletedRef _docuDeletedRef, EventHandlerRejectResult _validationResult)
        {
            if (!ScanDocuments::scanDeletedDocument(_docuDeletedRef))
            {
                _validationResult.reject();
            }
        }

        private static boolean scanDocument(DocuRef _docuRef)
        {
            /*
            Custom implementation required for connecting to a scanning service
            If document scanning process found an issue, return false; otherwise, return true;
            */
            return true;
        }

        private static boolean scanDeletedDocument(DocuDeletedRef _docuDeletedRef)
        {
            /*
            Custom implementation required for connecting to a scanning service
            If document scanning process found an issue, return false; otherwise, return true;
            */
            return true;
        }

    }
```

## <a name="developer-specifying-valid-content-types-when-attaching-documents-programmatically"></a><span data-ttu-id="85dfe-254">[開発者] ドキュメントをプログラムで関連付ける際の有効なコンテンツのタイプを指定</span><span class="sxs-lookup"><span data-stu-id="85dfe-254">[Developer] Specifying valid content types when attaching documents programmatically</span></span>

<span data-ttu-id="85dfe-255">`DocumentManagement` クラスからの次の API を使用すると、開発者は関連付けるファイルのファイル コンテンツ タイプ (MIME タイプ) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-255">The following APIs from the `DocumentManagement` class allow developers to specify the file content type (MIME type) of the file being attached.</span></span> 
-  <span data-ttu-id="85dfe-256">attachFileToCommon()</span><span class="sxs-lookup"><span data-stu-id="85dfe-256">attachFileToCommon()</span></span>
-  <span data-ttu-id="85dfe-257">attachFile()</span><span class="sxs-lookup"><span data-stu-id="85dfe-257">attachFile()</span></span>
-  <span data-ttu-id="85dfe-258">attachFileToDocuRef()</span><span class="sxs-lookup"><span data-stu-id="85dfe-258">attachFileToDocuRef()</span></span>

<span data-ttu-id="85dfe-259">このファイル コンテンツ タイプが正しく指定されていない場合、関連付けられているドキュメントが予期した動作をしない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-259">If this file content type is not specified correctly, the attached document may not behave as expected.</span></span> <span data-ttu-id="85dfe-260">このため、これらの API を使用する場合は、次のいずれかのアクション コースを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-260">For this reason, if you use these APIs you should consider one of the following courses of action:</span></span>  

-  <span data-ttu-id="85dfe-261">先行する API のいづれかで、`_fileContentType` パラメーターの **null** を渡します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-261">Pass **null** for the `_fileContentType` parameter in any of the preceeding APIs.</span></span> <span data-ttu-id="85dfe-262">これにより、ファイル名から正しいコンテンツ タイプを推定できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-262">Doing so allows the correct content type to be inferred from the file name.</span></span> 
-  <span data-ttu-id="85dfe-263">`_fileContentType` パラメータを含めない次のいずれかの方法で切り替えます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-263">Switch to using one of the following methods that doesn't include a `_fileContentType` parameter.</span></span> <span data-ttu-id="85dfe-264">これにより、誤ったファイル コンテンツ タイプを受け渡す可能性が回避されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-264">This is to avoid the possibility of passing incorrect file content types.</span></span>
    -  <span data-ttu-id="85dfe-265">attachFileToCommon() を置き換える **attachFileForRecord()**</span><span class="sxs-lookup"><span data-stu-id="85dfe-265">**attachFileForRecord()**, which replaces attachFileToCommon()</span></span>
    -  <span data-ttu-id="85dfe-266">attachFile() を置き換える **attachFileForReference()**</span><span class="sxs-lookup"><span data-stu-id="85dfe-266">**attachFileForReference()**, which replaces attachFile()</span></span>
    -  <span data-ttu-id="85dfe-267">attachFileToDocuRef() を置き換える **attachFileForDocuRefRecord()**</span><span class="sxs-lookup"><span data-stu-id="85dfe-267">**attachFileForDocuRefRecord()**, which replaces attachFileToDocuRef()</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="85dfe-268">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="85dfe-268">Frequently asked questions</span></span>

### <a name="what-is-the-difference-between-document-handling-and-document-management"></a><span data-ttu-id="85dfe-269">ドキュメント処理とドキュメント管理の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-269">What is the difference between document handling and document management?</span></span>

<span data-ttu-id="85dfe-270">ドキュメント処理とドキュメント管理の違いはありません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-270">There is no difference between document handling and document management.</span></span> <span data-ttu-id="85dfe-271">両方とも同じ機能を示します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-271">Both terms refer to the same functionality.</span></span> <span data-ttu-id="85dfe-272">異なるバージョンの製品では、異なる用語が使用されています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-272">Different terms are used in different versions of the product.</span></span>

### <a name="what-is-the-difference-between-document-management-and-print-management"></a><span data-ttu-id="85dfe-273">ドキュメント処理と印刷管理の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-273">What is the difference between document management and print management?</span></span>

<span data-ttu-id="85dfe-274">ドキュメント管理では、メモ、ドキュメント、および他のファイルを追加し記録できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-274">Document management lets you add notes, documents, and other files to records.</span></span>

<span data-ttu-id="85dfe-275">印刷管理では選択したレポートの印刷設定を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-275">Print management lets you control print settings for selected reports.</span></span> <span data-ttu-id="85dfe-276">印刷設定には、コピー数、印刷先、およびレポートに含めることができる多言語テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-276">Print settings include the number of copies, the printer destination, and the multilanguage text that can be included on the report.</span></span> <span data-ttu-id="85dfe-277">詳細については、 [ドキュメント レポーティング サービス](../../dev-itpro/analytics/document-reporting-services.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-277">For more information, see [Document Reporting Services](../../dev-itpro/analytics/document-reporting-services.md).</span></span>

### <a name="what-is-the-difference-between-document-types-and-file-types"></a><span data-ttu-id="85dfe-278">ドキュメント タイプとファイル タイプの違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-278">What is the difference between document types and file types?</span></span>

<span data-ttu-id="85dfe-279">ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。</span><span class="sxs-lookup"><span data-stu-id="85dfe-279">Document types are used to categorize the documents that you attach to records or the templates that you create.</span></span> <span data-ttu-id="85dfe-280">各ドキュメント タイプは、固有の場所に格納されることができます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-280">Each document type can be stored in a unique location.</span></span> <span data-ttu-id="85dfe-281">ドキュメント タイプのテーブルの名前は DocuType です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-281">The table for document types is named DocuType.</span></span>

<span data-ttu-id="85dfe-282">ファイル タイプには、Microsoft Word ドキュメントおよび画像が含まれます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-282">File types include Microsoft Word documents and images.</span></span> <span data-ttu-id="85dfe-283">ファイル タイプは、.txt、.png、.doc、.xlsx、または .pdf などのファイルの拡張子で表されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-283">A file type is denoted by the extension of the file, such as .txt, .png, .doc, .xlsx, or .pdf.</span></span>

### <a name="does-document-management-integrate-with-microsoft-365"></a><span data-ttu-id="85dfe-284">ドキュメント管理は Microsoft 365 と統合されますか?</span><span class="sxs-lookup"><span data-stu-id="85dfe-284">Does document management integrate with Microsoft 365?</span></span>

<span data-ttu-id="85dfe-285">はい。</span><span class="sxs-lookup"><span data-stu-id="85dfe-285">Yes.</span></span> <span data-ttu-id="85dfe-286">SharePoint 記憶域はネイティブでサポートされ、ドキュメント タイプの保管場所として選択できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-286">SharePoint storage is supported natively and can be selected as the storage location for a document type.</span></span> <span data-ttu-id="85dfe-287">さらに、任意の URL アドレス指定可能なファイルを **URL** ドキュメント タイプ経由で添付できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-287">In addition, any URL addressable file can be made an attachment via the **URL** document type.</span></span>

### <a name="what-is-the-default-storage-location-for-attachments-in-finance--operations-environments"></a><span data-ttu-id="85dfe-288">Finance + Operations 環境での添付ファイルの既定の保管場所はどこですか?</span><span class="sxs-lookup"><span data-stu-id="85dfe-288">What is the default storage location for attachments in Finance + Operations environments?</span></span>

<span data-ttu-id="85dfe-289">既定では、添付ファイルは製品クラウド オファリングの一部として、自動的に Azure Blob 記憶域に保存されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-289">By default, attachments are saved in Azure Blob storage automatically as part of the product cloud offering.</span></span>

### <a name="if-i-accidentally-delete-an-attachment-stored-in-azure-blob-storage-can-it-be-restored"></a><span data-ttu-id="85dfe-290">誤って Azure Blob Storage に格納されている添付ファイルを削除した場合、復元できますか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-290">If I accidentally delete an attachment stored in Azure Blob storage, can it be restored?</span></span>

<span data-ttu-id="85dfe-291">Azure Blob Storage に格納されている添付ファイルが誤って削除された場合は、完全に削除されたことになり、ファイルへの参照情報も削除されてしまうため、復元や修復することができません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-291">If an attachment stored in Azure Blob storage is accidentally deleted, it cannot be restored or recovered because it has been permanently deleted and the reference to it has also been deleted.</span></span>

### <a name="is-the-database-information-about-attachments-stored-separately-from-the-attachments-themselves"></a><span data-ttu-id="85dfe-292">添付ファイルに関するデータベースの情報は、添付ファイルそのものとは別の場所に保存されていますか？</span><span class="sxs-lookup"><span data-stu-id="85dfe-292">Is the database information about attachments stored separately from the attachments themselves?</span></span>

<span data-ttu-id="85dfe-293">添付ファイルの情報はDocuRefテーブルおよびDocuViewテーブルに格納されています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-293">Record attachment information is stored in the DocuRef and DocuView tables.</span></span> <span data-ttu-id="85dfe-294">DocuRefテーブルは、主に添付ファイルに関する情報を保持しています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-294">The DocuRef table is the record that represents the attachment.</span></span> <span data-ttu-id="85dfe-295">DocuRefの情報は、DocuViewレコードに関連付けられている情報と連携しています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-295">The DocuRef record points to the record being attached to and to a DocuView record.</span></span> <span data-ttu-id="85dfe-296">DocuRefテーブルは、添付ファイルを保持しています。</span><span class="sxs-lookup"><span data-stu-id="85dfe-296">The DocuView record points to the file that is the attachment.</span></span> <span data-ttu-id="85dfe-297">ファイルはデータベースの外に保存されるため、バックアップから復元するなどのデータベース上の操作は添付ファイルに関するデータベース情報のみに作用し、添付ファイルそのものには作用しません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-297">Files are stored outside the database, therefore any database operations, like restoring from backup, will only affect the database information about the attachment, not the attachment file itself.</span></span>

### <a name="can-attachments-be-stored-in-the-database"></a><span data-ttu-id="85dfe-298">添付ファイルをデータベースに保存できますか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-298">Can attachments be stored in the database?</span></span>

<span data-ttu-id="85dfe-299">一連番号</span><span class="sxs-lookup"><span data-stu-id="85dfe-299">No.</span></span> <span data-ttu-id="85dfe-300">既定では、添付ファイルは Azure Blob Storage に格納されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-300">By default, attachments are stored in Azure Blob storage.</span></span>

### <a name="what-are-the-main-differences-between-azure-blob-storage-and-database-storage"></a><span data-ttu-id="85dfe-301">Azure Blob Storage とデータベース ストレージの主な相違点は何ですか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-301">What are the main differences between Azure Blob storage and database storage?</span></span>

<span data-ttu-id="85dfe-302">データベース ストレージは Azure SQL データベースです。</span><span class="sxs-lookup"><span data-stu-id="85dfe-302">Database storage is Azure SQL Database.</span></span> <span data-ttu-id="85dfe-303">ファイル ストレージは Azure Blob Storage です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-303">File storage is Azure Blob storage.</span></span> <span data-ttu-id="85dfe-304">Azure Blob Storage はよりシンプルで安価です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-304">Azure Blob storage is simpler and much less expensive.</span></span>

### <a name="how-much-storage-do-we-get-for-azure-blob-storage"></a><span data-ttu-id="85dfe-305">Azure Blob Storage にどのくらいストレージを確保できますか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-305">How much storage do we get for Azure Blob storage?</span></span>

<span data-ttu-id="85dfe-306">詳細については [ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-306">That information is in the [licensing guide](https://go.microsoft.com/fwlink/?LinkId=866544).</span></span> <span data-ttu-id="85dfe-307">現在、40 ギガバイト (GB) のストレージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-307">Currently, you get 40 gigabytes (GB) of storage.</span></span>

### <a name="what-is-the-cost-for-additional-storage"></a><span data-ttu-id="85dfe-308">追加ストレージの費用はいくらですか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-308">What is the cost for additional storage?</span></span>

<span data-ttu-id="85dfe-309">追加ストレージのコストは変動しますが [標準の Azure ストレージ費用](https://azure.microsoft.com/pricing/details/storage/page-blobs/) と同様です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-309">The cost for additional storage varies, but it's similar to the [standard Azure costs for storage](https://azure.microsoft.com/pricing/details/storage/page-blobs/).</span></span> <span data-ttu-id="85dfe-310">すなわち、費用はおよそ GB あたり $0.05 です。</span><span class="sxs-lookup"><span data-stu-id="85dfe-310">In other words, the cost is about $0.05 per GB.</span></span>

### <a name="how-can-we-learn-how-much-storage-weve-already-used"></a><span data-ttu-id="85dfe-311">既に使用しているストレージの量を確認する方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-311">How can we learn how much storage we've already used?</span></span>

<span data-ttu-id="85dfe-312">データベースやファイル ストレージの制限に近づいた場合は、積極的なコミュニケーションが必要になります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-312">There will be proactive communications when you're approaching your database and file storage limits.</span></span> <span data-ttu-id="85dfe-313">ただし、Microsoft Dynamics Lifecycle Services (LCS) は一部の情報を提供し、追加情報のサポート要求をログに記録できます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-313">However, Microsoft Dynamics Lifecycle Services (LCS) provides some information, and you can log support requests for additional information.</span></span> 

### <a name="is-there-an-option-to-export-all-document-attachments-from-the-system"></a><span data-ttu-id="85dfe-314">すべてのドキュメントの添付ファイルをシステムからエクスポートするか選択できますか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-314">Is there an option to export all document attachments from the system?</span></span>

<span data-ttu-id="85dfe-315">添付ファイルをエクスポートできますが、標準の添付ファイル エンティティが存在しないため、その機能は標準の機能ではありません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-315">Although attachments can be exported, that capability isn't a standard capability, because there isn't a standard attachment entity.</span></span> <span data-ttu-id="85dfe-316">特定のビジネス ドキュメントやレコードに対する添付ファイルを提供するエンティティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-316">Entities that provide attachments for a specific business document or record must be built.</span></span>

### <a name="how-can-attachments-be-extracted-from-the-system"></a><span data-ttu-id="85dfe-317">どのようにシステムから添付ファイルを抽出できますか。</span><span class="sxs-lookup"><span data-stu-id="85dfe-317">How can attachments be extracted from the system?</span></span>

<span data-ttu-id="85dfe-318">添付ファイルを抽出するには、特定のビジネス ドキュメントやレコードに対する添付ファイル エンティティが作成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-318">To extract attachments, an Attachments entity must be built for a specific business document or record.</span></span> <span data-ttu-id="85dfe-319">各レコード タイプの ID が異なるため、標準の添付ファイル エンティティがありません。</span><span class="sxs-lookup"><span data-stu-id="85dfe-319">There isn't a standard attachment entity because the identity for each record type is different.</span></span> <span data-ttu-id="85dfe-320">添付ファイル エンティティを作成する方法については、**AOT > データモデル > データ エンティティ** ノードの下にある "添付ファイル" を検索して、アプリケーション エクスプローラーの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85dfe-320">To learn how to build an Attachments entity, you can find examples in the Application explorer by searching for "Attachment" under the **AOT > Data Model > Data Entities** node.</span></span>

### <a name="how-does-the-document-preview-work-for-attachments-stored-in-sharepoint"></a><span data-ttu-id="85dfe-321">SharePoint に保存された添付ファイルにおけるドキュメント プレビューのしくみ。</span><span class="sxs-lookup"><span data-stu-id="85dfe-321">How does the document preview work for attachments stored in SharePoint?</span></span>

<span data-ttu-id="85dfe-322">ファイルは、WOPI サービスによって現在のユーザーのアクセス許可を使用して SharePoint から取得されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-322">The files are retrieved from SharePoint using the current user permissions by the WOPI service.</span></span> <span data-ttu-id="85dfe-323">これらのファイルは、ドキュメント プレビューを表示するために HTML で表示されます。</span><span class="sxs-lookup"><span data-stu-id="85dfe-323">Those files are then rendered in HTML to provide a document preview.</span></span> <span data-ttu-id="85dfe-324">つまり、現在のユーザーは、ファイルをプレビューしたり開いたりするためにファイルにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="85dfe-324">This means that the current user needs access to the files to be able to preview them or open them.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
