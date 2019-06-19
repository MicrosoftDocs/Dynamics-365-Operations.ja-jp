---
title: ドキュメント管理のコンフィギュレーション
description: このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 05/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d30e451799d012a8c7eab350aa524bc0870190d6
ms.sourcegitcommit: 1bd8d0911a64d56cedaa60a9e5a58f9e13b8c1cf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2019
ms.locfileid: "1616141"
---
# <a name="configure-document-management"></a><span data-ttu-id="65c84-103">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-103">Configure document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65c84-104">このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="65c84-104">This topic explains how to configure document management (document handling) so that it stores file attachments and notes for records.</span></span> <span data-ttu-id="65c84-105">これには、この機能に関連する概念および機能に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="65c84-105">It includes information about the concepts and features that are involved in this functionality.</span></span>

<span data-ttu-id="65c84-106">ドキュメントの管理の詳細については、簡単なビデオ [Dynamics 365 for Finance and Operations でのドキュメント管理](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be)をご視聴ください。</span><span class="sxs-lookup"><span data-stu-id="65c84-106">To learn more about document management, watch the short [Document Management in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be) video.</span></span>

## <a name="configure-document-types"></a><span data-ttu-id="65c84-107">ドキュメント タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-107">Configure document types</span></span>

<span data-ttu-id="65c84-108">ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。</span><span class="sxs-lookup"><span data-stu-id="65c84-108">Document types are used to categorize the documents that you attach to records or the templates that you create.</span></span> <span data-ttu-id="65c84-109">各ドキュメント タイプは、固有の場所に格納されることができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-109">Each document type can be stored in a unique location.</span></span>

<span data-ttu-id="65c84-110">ドキュメント タイプの既定のセットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="65c84-110">A default set of document types is provided.</span></span> <span data-ttu-id="65c84-111">これらのドキュメント タイプを使用すると、ファイル、イメージ、メモ、または URL として添付ファイルを分類できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-111">You can use these document types to categorize an attachment as a file, image, note, or URL.</span></span> <span data-ttu-id="65c84-112">**ファイル** および **画像** の既定のドキュメント タイプは、場所として **Azure ストレージ**を使用するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-112">The **File** and **Image** default document types are configured to use **Azure storage** as the location.</span></span>

<span data-ttu-id="65c84-113">新しいドキュメント タイプを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="65c84-113">To create a new document type, follow these steps.</span></span>

1. <span data-ttu-id="65c84-114">**ドキュメント タイプ**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="65c84-114">Go to the **Document types** page.</span></span>
2. <span data-ttu-id="65c84-115">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65c84-115">Click **New**.</span></span>
3. <span data-ttu-id="65c84-116">**タイプ** フィールドに、**SharePoint** または **HR** ドキュメントなどの新しいドキュメント タイプの短縮名を入力します。</span><span class="sxs-lookup"><span data-stu-id="65c84-116">In the **Type** field, enter a short name for the new document type, such as **SharePoint** or **HR Docs**.</span></span>
4. <span data-ttu-id="65c84-117">**名前**フィールドに、**SharePoint ファイル**または **HR ドキュメント**などの長い名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65c84-117">In the **Name** field, enter a longer name, such as **SharePoint files** or **HR Docs**.</span></span>
5. <span data-ttu-id="65c84-118">**クラス** フィールドで、ドキュメント タイプの動作を定義するクラスを指定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-118">In the **Class** field, specify a class to define the behavior for the document type:</span></span>

    - <span data-ttu-id="65c84-119">**ファイルの添付** - ユーザーはファイルを要求されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-119">**Attach file** – The user is prompted for a file.</span></span>
    - <span data-ttu-id="65c84-120">**URL の添付** - ユーザーは、`http://www.microsoft.com` のように、**メモ**フィールドに URL を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-120">**Attach URL** – The user can enter a URL in the **Notes** field, such as `http://www.microsoft.com`.</span></span> <span data-ttu-id="65c84-121">**添付ファイル** ページの **開く** ボタンをクリックすると [参照] タブに URL が開きます。</span><span class="sxs-lookup"><span data-stu-id="65c84-121">The **Open** button on the **Attachments** page will open the URL on a browser tab.</span></span>
    - <span data-ttu-id="65c84-122">**簡易メモ** – ユーザーは **メモ** フィールドに簡易メモを追加できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-122">**Simple note** – The user can add a simple note in the **Notes** field.</span></span>

6. <span data-ttu-id="65c84-123">**クラス** フィールドで**ファイルの添付**を指定した場合、**場所**フィールドで使用する記憶域メカニズムを指定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-123">If you specified **Attach file** in the **Class** field, in the **Location** field, specify the storage mechanism to use.</span></span>
7. <span data-ttu-id="65c84-124">**場所** フィールドで **SharePoint** を指定した場合、**SharePoint アドレス** フィールドで Microsoft SharePoint アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-124">If you specified **SharePoint** in the **Location** field, specify the Microsoft SharePoint address in the **SharePoint Address** field.</span></span> <span data-ttu-id="65c84-125">これを行うには、**編集** ボタン (鉛筆シンボル) をクリックし、**フォルダー選択** ダイアログ ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="65c84-125">To do this, click the **Edit** button (pencil symbol) and use the **Folder selection** dialog box.</span></span>

## <a name="configure-sharepoint-storage"></a><span data-ttu-id="65c84-126">SharePoint 記憶域のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-126">Configure SharePoint storage</span></span>

<span data-ttu-id="65c84-127">Microsoft SharePoint Online は、ネイティブでサポートされる保存場所の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="65c84-127">Microsoft SharePoint Online is one of the storage locations that are supported natively.</span></span> <span data-ttu-id="65c84-128">現在、SharePoint Online だけがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="65c84-128">Currently, only SharePoint Online is supported.</span></span> <span data-ttu-id="65c84-129">オンプレミス SharePoint (ローカル SharePoint サーバー) のサポートは将来追加される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="65c84-129">Support for on-premises SharePoint (a local SharePoint server) may be added in the future.</span></span>

<span data-ttu-id="65c84-130">SharePoint ストレージを使用するには、ドキュメント タイプの**場所**フィールドを **SharePoint** に設定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-130">To use SharePoint storage, set the **Location** field for a document type to **SharePoint**.</span></span> <span data-ttu-id="65c84-131">その後、**SharePoint アドレス** フィールドに、有効な SharePoint アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="65c84-131">Then, in the **SharePoint Address** field, enter a valid SharePoint address.</span></span>

<span data-ttu-id="65c84-132">SharePoint 記憶域を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="65c84-132">To configure SharePoint storage, follow these steps.</span></span>

1. <span data-ttu-id="65c84-133">**ドキュメント管理パラメータ**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="65c84-133">Go to the **Document management parameters** page.</span></span>
2. <span data-ttu-id="65c84-134">**SharePoint** タブの**既定の SharePoint サーバー**フィールドで、contosoax7.sharepoint.com など、SharePoint サイトに対して自動的に検出されたホスト名を確認します。</span><span class="sxs-lookup"><span data-stu-id="65c84-134">On the **SharePoint** tab, in the **Default SharePoint server** field, review the host name that was automatically detected for the SharePoint site, such as contosoax7.sharepoint.com.</span></span> <span data-ttu-id="65c84-135">通常、SharePoint ホスト名は tenantname.sharepoint.com の形式で、そのテナントのアカウントは `user1@tenantname.onmicrosoft.com` の形式で示されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-135">Typically, the SharePoint host name is in the form tenantname.sharepoint.com, and accounts on that tenant are in the form `user1@tenantname.onmicrosoft.com`.</span></span>

    <span data-ttu-id="65c84-136">既定の SharePoint サーバーが指定されていない場合は、通常、テナントの SharePoint サイトが存在しないか、有効な Microsoft Office 365 ライセンスが現在のユーザー (管理者) に関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="65c84-136">Typically, if no default SharePoint server is specified, either there is no SharePoint site for the tenant, or a valid Microsoft Office 365 license isn't associated with the current user (the admin).</span></span>

4. <span data-ttu-id="65c84-137">オプション: **SharePoint 接続**のテスト をクリックし、指定された SharePoint ホスト名をテストします。</span><span class="sxs-lookup"><span data-stu-id="65c84-137">Optional: Click **Test SharePoint connection** to test the specified SharePoint host name.</span></span>
5. <span data-ttu-id="65c84-138">オプション: **SharePoint を開く**をクリックし、指定された SharePoint ホスト名をブラウザーで開きます。</span><span class="sxs-lookup"><span data-stu-id="65c84-138">Optional: Click **Open SharePoint** to open the specified SharePoint host name in a browser.</span></span>

### <a name="troubleshooting-sharepoint-communication"></a><span data-ttu-id="65c84-139">SharePoint 通信のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="65c84-139">Troubleshooting SharePoint communication</span></span>

<span data-ttu-id="65c84-140">SharePoint 通信は、次の条件が満たされた場合にのみ、現在のユーザーに対して機能します。</span><span class="sxs-lookup"><span data-stu-id="65c84-140">SharePoint communication works for the current user only if the following conditions are met:</span></span>

- <span data-ttu-id="65c84-141">Office 365 ライセンスが、ユーザーのアカウントに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="65c84-141">An Office 365 license is associated with the user's account.</span></span>
- <span data-ttu-id="65c84-142">ユーザーは、外部ユーザーではなくテナントの一般的なユーザーです (別のテナントのユーザーなど)。</span><span class="sxs-lookup"><span data-stu-id="65c84-142">The user is a typical user on the tenant, not an external user (for example, a user from another tenant).</span></span>
- <span data-ttu-id="65c84-143">テナント用の SharePoint サイト (たとえば、Contoso.SharePoint.com など) が存在します。</span><span class="sxs-lookup"><span data-stu-id="65c84-143">There is a SharePoint site for the tenant (for example, Contoso.SharePoint.com).</span></span>

## <a name="configure-file-types"></a><span data-ttu-id="65c84-144">ファイルの種類のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-144">Configure file types</span></span>

<span data-ttu-id="65c84-145">許可されているファイル拡張子のリストを変更することで、ユーザーがレコードに添付できるファイルの種類を制御できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-145">By modifying the list of file extensions that are allowed, you can control the types of files that users can attach to records.</span></span>

<span data-ttu-id="65c84-146">ファイル タイプを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="65c84-146">To specify file types, follow these steps.</span></span>

1. <span data-ttu-id="65c84-147">**ドキュメント管理パラメータ**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="65c84-147">Go to the **Document management parameters** page.</span></span>
2. <span data-ttu-id="65c84-148">**ファイル タイプ**タブで、既定のファイル タイプを確認します。</span><span class="sxs-lookup"><span data-stu-id="65c84-148">On the **File types** tab, review the default file types.</span></span>
3. <span data-ttu-id="65c84-149">ユーザーがレコードに添付できないファイル タイプを削除し、ユーザーがレコードに添付できるファイル タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="65c84-149">Remove any file types that users should not be able to attach to records, and add any file types that users should be able to attach to records.</span></span>

## <a name="configure-document-preview"></a><span data-ttu-id="65c84-150">ドキュメント プレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-150">Configure document preview</span></span>

<span data-ttu-id="65c84-151">添付ファイルのプレビューには、Microsoft Office Online Server で提供される Web アプリ オープン プラットフォーム インターフェイス (WOPI) を使用します。</span><span class="sxs-lookup"><span data-stu-id="65c84-151">The attachments preview uses the Web app Open Platform Interface (WOPI) that is provided by Microsoft Office Online Server.</span></span> <span data-ttu-id="65c84-152">**ドキュメント管理パラメーター** ページの**全般**タブの **Office Web Apps サーバー** フィールドで、添付ファイルのプレビューに使用する Office Online サーバー インスタンスを指定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-152">On the **Document management parameters** page, on the **General** tab, in the **Office Web Apps Server** field, specify the Office Online Server instance to use for attachment previews.</span></span> <span data-ttu-id="65c84-153">既定値は [`https://onenote.officeapps.live.com`] です。</span><span class="sxs-lookup"><span data-stu-id="65c84-153">The default value is `https://onenote.officeapps.live.com`.</span></span> <span data-ttu-id="65c84-154">この値は、クラウド ベースの WOPI サーバーを指しています。</span><span class="sxs-lookup"><span data-stu-id="65c84-154">This value points to the cloud-based WOPI server.</span></span>

### <a name="for-an-on-premises-environment"></a><span data-ttu-id="65c84-155">オンプレミス環境について</span><span class="sxs-lookup"><span data-stu-id="65c84-155">For an on-premises environment</span></span>

<span data-ttu-id="65c84-156">環境がオンプレミス上にあるとき、既定のクラウド ベースの WOPI サーバーは添付ファイルを読み込んでプレビューを提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="65c84-156">When an environment is on-premises, the default cloud-based WOPI server can't read the attachment file to provide a preview.</span></span> <span data-ttu-id="65c84-157">プレビューが必要な場合は、[オンプレミス Office Online サーバー インスタンスをインストールし](https://technet.microsoft.com/library/jj219455.aspx)、それを環境内で構成する必要あります。</span><span class="sxs-lookup"><span data-stu-id="65c84-157">If previews are required, you must [install an on-premises Office Online Server instance](https://technet.microsoft.com/library/jj219455.aspx) and configure it inside the environment.</span></span> <span data-ttu-id="65c84-158">**Office Web アプリケーション サーバー** フィールドを、インストールされている Office Online Server インスタンスのホスト名に設定し、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65c84-158">Set the **Office Web Apps Server** field to the host name of the installed Office Online Server instance, and then click **Save**.</span></span>

<span data-ttu-id="65c84-159">プレビューが必要な場合は、**Office Web アプリケーション サーバー** フィールドを `https://localhost` に設定します。</span><span class="sxs-lookup"><span data-stu-id="65c84-159">If previews aren't required, set the **Office Web Apps Server** field to `https://localhost`.</span></span> <span data-ttu-id="65c84-160">プレビューは、その後は、エラー メッセージではなく、「プレビューを利用できません」というメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="65c84-160">The preview will then show the message "No preview available" instead of an error message.</span></span>

## <a name="other-configuration"></a><span data-ttu-id="65c84-161">他のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65c84-161">Other configuration</span></span>

<span data-ttu-id="65c84-162">これらのオプションが使用されることはほとんどありませんが、考慮すべきその他のコンフィギュレーション オプションを次に示します。</span><span class="sxs-lookup"><span data-stu-id="65c84-162">Here are some other configuration options to consider, although these options are rarely used:</span></span>

- <span data-ttu-id="65c84-163">**ドキュメント管理パラメーター**ページの、**一般**タブで、**ドキュメント テーブルの使用**オプションを使用して、**アクティブ ドキュメント テーブル**許可リストを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-163">On the **Document management parameters** page, on the **General** tab, you can use the **Use Document Tables** option to enable the **Active document tables** allow list.</span></span> <span data-ttu-id="65c84-164">このオプションを**はい**に設定すると、他のすべてのテーブルの添付ファイルが無効になります。</span><span class="sxs-lookup"><span data-stu-id="65c84-164">If you set this option to **Yes**, you disable attachments on all other tables.</span></span> <span data-ttu-id="65c84-165">したがって、必要なときにのみこのオプションをオンにしてください。</span><span class="sxs-lookup"><span data-stu-id="65c84-165">Therefore, turn on this option only when it's required.</span></span>
- <span data-ttu-id="65c84-166">**ドキュメント管理パラメーター**ページの、**全般**タブで、**最大ファイル サイズ(単位: メガバイト)** フィールドを使用して、添付ファイルの最大ファイル サイズを設定できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-166">On the **Document management parameters** page, on the **General** tab, you can use the **Maximum file size in megabytes** field to set the maximum file size for attachments.</span></span> <span data-ttu-id="65c84-167">ユーザーがファイルを提供する機能は、構成ファイルで環境に対して設定されているファイル サイズ制限でも制限されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="65c84-167">Note that the ability of users to provide files is also constrained by the file size limit that is set for the environment in configuration files.</span></span> <span data-ttu-id="65c84-168">これらの設定ファイルは、クライアント ページから変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="65c84-168">These configuration files can't be changed via a client page.</span></span>
- <span data-ttu-id="65c84-169">**オプション** ページ (**設定** \> **ユーザー オプション**) では、**基本設定** タブで、**ドキュメント処理の有効化** オプションを使用して、ドキュメント処理を無効にします (ドキュメント管理)。</span><span class="sxs-lookup"><span data-stu-id="65c84-169">On the **Options** page (**Settings** \> **User options**), on the **Preferences** tab, you can use the **Enable document handling** option to disable document handling (document management).</span></span>

## <a name="accessing-document-management-attachments"></a><span data-ttu-id="65c84-170">ドキュメント管理添付ファイルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="65c84-170">Accessing document management attachments</span></span> 

<span data-ttu-id="65c84-171">ドキュメント管理は、データ ソースを含む殆どのフォームのトップにある**添付**ボタン (キーボード ショートカット: **Ctrl**+**Shift**+**A**) として、ユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-171">Document management appears to users as the **Attach** button (keyboard shortcut: **Ctrl**+**Shift**+**A**) at the top of most forms that contain data sources.</span></span> <span data-ttu-id="65c84-172">**添付**ボタンをクリックすると、フォーム上で現在選択されているコントロールのデータ ソースのコンテキストで**添付ファイル** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="65c84-172">Clicking the **Attach** button will open the **Attachments** form in the context of the data source of the currently selected control on the form.</span></span>

<span data-ttu-id="65c84-173">**添付** ボタンには、現在選択されているレコードの添付ファイルの数も表示されるため、ユーザーはそのフォームを開かなくても、現在のレコードに添付ファイルがあるかどうかを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-173">The **Attach** button will also show a count of attachments for the currently selected record, so the user can see whether there are attachments on the current record without opening that form.</span></span> <span data-ttu-id="65c84-174">カウントには 0 ～ 9、次に 9+ が表示され、パフォーマンスの影響と大きなカウントの決定と表示の視覚的ノイズが制限されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-174">The count will show 0-9, and then 9+ to limit the performance impact and visual noise of determining and showing larger counts.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="65c84-175">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="65c84-175">Frequently asked questions</span></span>

### <a name="what-is-the-difference-between-document-handling-and-document-management"></a><span data-ttu-id="65c84-176">ドキュメント処理とドキュメント管理の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="65c84-176">What is the difference between document handling and document management?</span></span>

<span data-ttu-id="65c84-177">ドキュメント処理とドキュメント管理の違いはありません。</span><span class="sxs-lookup"><span data-stu-id="65c84-177">There is no difference between document handling and document management.</span></span> <span data-ttu-id="65c84-178">両方とも同じ機能を示します。</span><span class="sxs-lookup"><span data-stu-id="65c84-178">Both terms refer to the same functionality.</span></span> <span data-ttu-id="65c84-179">異なるバージョンの製品では、異なる用語が使用されています。</span><span class="sxs-lookup"><span data-stu-id="65c84-179">Different terms are used in different versions of the product.</span></span>

### <a name="what-is-the-difference-between-document-management-and-print-management"></a><span data-ttu-id="65c84-180">ドキュメント処理と印刷管理の違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="65c84-180">What is the difference between document management and print management?</span></span>

<span data-ttu-id="65c84-181">ドキュメント管理では、メモ、ドキュメント、および他のファイルを追加し記録できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-181">Document management lets you add notes, documents, and other files to records.</span></span>

<span data-ttu-id="65c84-182">印刷管理では選択したレポートの印刷設定を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-182">Print management lets you control print settings for selected reports.</span></span> <span data-ttu-id="65c84-183">印刷設定には、コピー数、印刷先、およびレポートに含めることができる多言語テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="65c84-183">Print settings include the number of copies, the printer destination, and the multilanguage text that can be included on the report.</span></span> <span data-ttu-id="65c84-184">詳細については、[Document Reporting Services の概要](../../dev-itpro/analytics/document-reporting-services.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65c84-184">For more information, see [Document Reporting Services overview](../../dev-itpro/analytics/document-reporting-services.md).</span></span>

### <a name="what-is-the-difference-between-document-types-and-file-types"></a><span data-ttu-id="65c84-185">ドキュメント タイプとファイル タイプの違いは何ですか。</span><span class="sxs-lookup"><span data-stu-id="65c84-185">What is the difference between document types and file types?</span></span>

<span data-ttu-id="65c84-186">ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。</span><span class="sxs-lookup"><span data-stu-id="65c84-186">Document types are used to categorize the documents that you attach to records or the templates that you create.</span></span> <span data-ttu-id="65c84-187">各ドキュメント タイプは、固有の場所に格納されることができます。</span><span class="sxs-lookup"><span data-stu-id="65c84-187">Each document type can be stored in a unique location.</span></span> <span data-ttu-id="65c84-188">ドキュメント タイプのテーブルの名前は DocuType です。</span><span class="sxs-lookup"><span data-stu-id="65c84-188">The table for document types is named DocuType.</span></span>

<span data-ttu-id="65c84-189">ファイル タイプには、Microsoft Word ドキュメントおよび画像が含まれます。</span><span class="sxs-lookup"><span data-stu-id="65c84-189">File types include Microsoft Word documents and images.</span></span> <span data-ttu-id="65c84-190">ファイル タイプは、.txt、.png、.doc、.xlsx、または .pdf などのファイルの拡張子で表されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-190">A file type is denoted by the extension of the file, such as .txt, .png, .doc, .xlsx, or .pdf.</span></span>

### <a name="does-document-management-integrate-with-office-365"></a><span data-ttu-id="65c84-191">ドキュメント管理は Office 365 と統合されますか。</span><span class="sxs-lookup"><span data-stu-id="65c84-191">Does document management integrate with Office 365?</span></span>

<span data-ttu-id="65c84-192">はい。</span><span class="sxs-lookup"><span data-stu-id="65c84-192">Yes.</span></span> <span data-ttu-id="65c84-193">SharePoint 記憶域はネイティブでサポートされ、ドキュメント タイプの保管場所として選択できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-193">SharePoint storage is supported natively and can be selected as the storage location for a document type.</span></span> <span data-ttu-id="65c84-194">さらに、任意の URL アドレス指定可能なファイルを **URL** ドキュメント タイプ経由で添付できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-194">In addition, any URL addressable file can be made an attachment via the **URL** document type.</span></span>

### <a name="how-does-the-default-storage-location-for-document-management-change-in-on-premises-environments"></a><span data-ttu-id="65c84-195">オンプレミス環境では、ドキュメント管理の既定の保管場所はどのように変更されますか？</span><span class="sxs-lookup"><span data-stu-id="65c84-195">How does the default storage location for Document Management change in on-premises environments?</span></span>

<span data-ttu-id="65c84-196">オンプレミス環境の場合、添付ファイルの Azure Blob ストレージ プロバイダーはファイル フォルダー ストレージ プロバイダーに置き換えられ、添付ファイルはクラウドに格納される代わりにオンプレミスに保存されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-196">For on-premises environments, the Azure Blob storage provider for attachments is replaced by a file folder storage provider so that attachments are kept on-premise instead of being stored in the cloud.</span></span> <span data-ttu-id="65c84-197">したがって、添付ファイルの既定の保管場所はファイル フォルダとなります。</span><span class="sxs-lookup"><span data-stu-id="65c84-197">Therefore, the default storage location for attachments is a file folder.</span></span>

### <a name="if-i-accidentally-delete-an-attachment-stored-in-azure-blob-storage-can-it-be-restored"></a><span data-ttu-id="65c84-198">誤って Azure Blob Storage に格納されている添付ファイルを削除した場合、復元できますか。</span><span class="sxs-lookup"><span data-stu-id="65c84-198">If I accidentally delete an attachment stored in Azure Blob storage, can it be restored?</span></span>

<span data-ttu-id="65c84-199">Azure Blob Storage に格納されている添付ファイルが誤って削除された場合は、完全に削除されたことになり、ファイルへの参照情報も削除されてしまうため、復元や修復することができません。</span><span class="sxs-lookup"><span data-stu-id="65c84-199">If an attachment stored in Azure Blob storage is accidentally deleted, it cannot be restored or recovered because it has been permanently deleted and the reference to it has also been deleted.</span></span>

### <a name="is-the-database-information-about-attachments-stored-separately-from-the-attachments-themselves"></a><span data-ttu-id="65c84-200">添付ファイルに関するデータベースの情報は、添付ファイルそのものとは別の場所に保存されていますか？</span><span class="sxs-lookup"><span data-stu-id="65c84-200">Is the database information about attachments stored separately from the attachments themselves?</span></span>

<span data-ttu-id="65c84-201">添付ファイルの情報はDocuRefテーブルおよびDocuViewテーブルに格納されています。</span><span class="sxs-lookup"><span data-stu-id="65c84-201">Record attachment information is stored in the DocuRef and DocuView tables.</span></span> <span data-ttu-id="65c84-202">DocuRefテーブルは、主に添付ファイルに関する情報を保持しています。</span><span class="sxs-lookup"><span data-stu-id="65c84-202">The DocuRef table is the record that represents the attachment.</span></span> <span data-ttu-id="65c84-203">DocuRefの情報は、DocuViewレコードに関連付けられている情報と連携しています。</span><span class="sxs-lookup"><span data-stu-id="65c84-203">The DocuRef record points to the record being attached to and to a DocuView record.</span></span> <span data-ttu-id="65c84-204">DocuRefテーブルは、添付ファイルを保持しています。</span><span class="sxs-lookup"><span data-stu-id="65c84-204">The DocuView record points to the file that is the attachment.</span></span> <span data-ttu-id="65c84-205">ファイルはデータベースの外に保存されるため、バックアップから復元するなどのデータベース上の操作は添付ファイルに関するデータベース情報のみに作用し、添付ファイルそのものには作用しません。</span><span class="sxs-lookup"><span data-stu-id="65c84-205">Files are stored outside the database, therefore any database operations, like restoring from backup, will only affect the database information about the attachment, not the attachment file itself.</span></span>

### <a name="can-attachments-be-stored-in-the-database"></a><span data-ttu-id="65c84-206">添付ファイルをデータベースに保存できますか。</span><span class="sxs-lookup"><span data-stu-id="65c84-206">Can attachments be stored in the database?</span></span>

<span data-ttu-id="65c84-207">一連番号</span><span class="sxs-lookup"><span data-stu-id="65c84-207">No.</span></span> <span data-ttu-id="65c84-208">既定では、添付ファイルは Azure Blob Storage に格納されます。</span><span class="sxs-lookup"><span data-stu-id="65c84-208">By default, attachments are stored in Azure Blob storage.</span></span>

### <a name="what-are-the-main-differences-between-azure-blob-storage-and-database-storage"></a><span data-ttu-id="65c84-209">Azure Blob Storage とデータベース ストレージの主な相違点は何ですか。</span><span class="sxs-lookup"><span data-stu-id="65c84-209">What are the main differences between Azure Blob storage and database storage?</span></span>

<span data-ttu-id="65c84-210">データベース ストレージは Azure SQL データベースです。</span><span class="sxs-lookup"><span data-stu-id="65c84-210">Database storage is Azure SQL Database.</span></span> <span data-ttu-id="65c84-211">ファイル ストレージは Azure Blob Storage です。</span><span class="sxs-lookup"><span data-stu-id="65c84-211">File storage is Azure Blob storage.</span></span> <span data-ttu-id="65c84-212">Azure Blob Storage はよりシンプルで安価です。</span><span class="sxs-lookup"><span data-stu-id="65c84-212">Azure Blob storage is simpler and much less expensive.</span></span>

### <a name="how-much-storage-do-we-get-for-azure-blob-storage"></a><span data-ttu-id="65c84-213">Azure Blob Storage にどのくらいストレージを確保できますか。</span><span class="sxs-lookup"><span data-stu-id="65c84-213">How much storage do we get for Azure Blob storage?</span></span>

<span data-ttu-id="65c84-214">詳細については [ライセンス ガイド](https://mbs.microsoft.com/Files/public/365/Dynamics365LicensingGuide.pdf) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65c84-214">That information is in the [licensing guide](https://mbs.microsoft.com/Files/public/365/Dynamics365LicensingGuide.pdf).</span></span> <span data-ttu-id="65c84-215">現在、40 ギガバイト (GB) のストレージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-215">Currently, you get 40 gigabytes (GB) of storage.</span></span>

### <a name="what-is-the-cost-for-additional-storage"></a><span data-ttu-id="65c84-216">追加ストレージの費用はいくらですか。</span><span class="sxs-lookup"><span data-stu-id="65c84-216">What is the cost for additional storage?</span></span>

<span data-ttu-id="65c84-217">追加ストレージのコストは変動しますが [標準の Azure ストレージ費用](https://azure.microsoft.com/pricing/details/storage/page-blobs/) と同様です。</span><span class="sxs-lookup"><span data-stu-id="65c84-217">The cost for additional storage varies, but it's similar to the [standard Azure costs for storage](https://azure.microsoft.com/pricing/details/storage/page-blobs/).</span></span> <span data-ttu-id="65c84-218">すなわち、費用はおよそ GB あたり $0.05 です。</span><span class="sxs-lookup"><span data-stu-id="65c84-218">In other words, the cost is about $0.05 per GB.</span></span>

### <a name="how-can-we-learn-how-much-storage-weve-already-used"></a><span data-ttu-id="65c84-219">既に使用しているストレージの量を確認する方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="65c84-219">How can we learn how much storage we've already used?</span></span>

<span data-ttu-id="65c84-220">データベースやファイル ストレージの制限に近づいた場合は、積極的なコミュニケーションが必要になります。</span><span class="sxs-lookup"><span data-stu-id="65c84-220">There will be proactive communications when you're approaching your database and file storage limits.</span></span> <span data-ttu-id="65c84-221">ただし、Microsoft Dynamics Lifecycle Services (LCS) は一部の情報を提供し、追加情報のサポート要求をログに記録できます。</span><span class="sxs-lookup"><span data-stu-id="65c84-221">However, Microsoft Dynamics Lifecycle Services (LCS) provides some information, and you can log support requests for additional information.</span></span> 

### <a name="is-there-an-option-to-export-all-document-attachments-from-the-system"></a><span data-ttu-id="65c84-222">すべてのドキュメントの添付ファイルをシステムからエクスポートするか選択できますか。</span><span class="sxs-lookup"><span data-stu-id="65c84-222">Is there an option to export all document attachments from the system?</span></span>

<span data-ttu-id="65c84-223">添付ファイルをエクスポートできますが、標準の添付ファイル エンティティが存在しないため、その機能は標準の機能ではありません。</span><span class="sxs-lookup"><span data-stu-id="65c84-223">Although attachments can be exported, that capability isn't a standard capability, because there isn't a standard attachment entity.</span></span> <span data-ttu-id="65c84-224">特定のビジネス ドキュメントやレコードに対する添付ファイルを提供するエンティティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65c84-224">Entities that provide attachments for a specific business document or record must be built.</span></span>
