---
title: 共有可能かつセキュリティで保護された、URL (ディープ リンク ) を作成
description: フォームおよびレコードへの共有可能かつセキュリティで保護された URL を作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 24321
ms.assetid: 3e49f8eb-d9a8-418c-a73d-687da4ca0c96
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 654cd578ab56a0cbad0c4625cfdbd602f7f564c0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980550"
---
# <a name="create-shareable-secured-urls-deep-links"></a><span data-ttu-id="079e1-103">共有可能かつセキュリティで保護された、URL (ディープ リンク ) を作成</span><span class="sxs-lookup"><span data-stu-id="079e1-103">Create shareable, secured URLs (deep links)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="079e1-104">フォームおよびレコードへの共有可能かつセキュリティで保護された URL を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="079e1-104">Learn how to create shareable, secured URLs to forms and records.</span></span>

<a name="overview"></a><span data-ttu-id="079e1-105">概要</span><span class="sxs-lookup"><span data-stu-id="079e1-105">Overview</span></span>
--------

<span data-ttu-id="079e1-106">URL ジェネレータにより、開発者はルート移動可能な特定のフォームへの共有可能およびセキュリティ保護される URL (ディープ リンクとも呼ばれる) を作成できます。</span><span class="sxs-lookup"><span data-stu-id="079e1-106">The URL Generator enables developers to create shareable and secured URLs (also known as deep links) to specific forms that are root navigable.</span></span> <span data-ttu-id="079e1-107">オプションのデータ コンテキストをフォームに渡すと、フォームを開いた場合にフィルターや固有のデータを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="079e1-107">An optional data context can be passed to the form to display filtered or specific data when the form is opened.</span></span> <span data-ttu-id="079e1-108">URL ジェネレーターにより、レポート、電子メール、および外部アプリケーションへのリンクの埋め込みなどのシナリオが可能になるため、生成されたリンクを使用して移動するだけで、指定されたフォームやデータを迅速かつ容易に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="079e1-108">The URL Generator enables scenarios such as embedding links in reports, email, and external applications, enabling users to quickly and easily locate the specified forms or data by simply navigating using the generated link.</span></span>

### <a name="purpose"></a><span data-ttu-id="079e1-109">目的</span><span class="sxs-lookup"><span data-stu-id="079e1-109">Purpose</span></span>

-   <span data-ttu-id="079e1-110">指定されたインスタンスでのルート移動可能なフォームに移動するために使用できる URL を生成する開発者を支援します。</span><span class="sxs-lookup"><span data-stu-id="079e1-110">Empower developers to generate URLs that can be used to navigate to root navigable forms in a specified instance.</span></span>
-   <span data-ttu-id="079e1-111">必要に応じて、指定されたフォームに移動した際に表示されるデータ コンテキストを指定する開発者を支援します。</span><span class="sxs-lookup"><span data-stu-id="079e1-111">Empower developers to optionally specify a data context that should be displayed when navigating to the specified form.</span></span>
-   <span data-ttu-id="079e1-112">ユーザーが、インターネットにアクセスできる任意のブラウザーから生成された URL を共有、保存、およびアクセスできるよう支援します。</span><span class="sxs-lookup"><span data-stu-id="079e1-112">Empower users to share, save, and access the generated URLs from any browser with Internet access.</span></span>
-   <span data-ttu-id="079e1-113">システム、フォーム、またはデータへの不正アクセスを防ぐために URL を保護します。</span><span class="sxs-lookup"><span data-stu-id="079e1-113">Secure the URLs to prevent unauthorized access to the system, forms, or data.</span></span>
-   <span data-ttu-id="079e1-114">機密性の高いデータまたは改ざんの影響を防ぐために URL を保護します。</span><span class="sxs-lookup"><span data-stu-id="079e1-114">Secure the URLs to prevent exposure of sensitive data or tampering.</span></span>

## <a name="security"></a><span data-ttu-id="079e1-115">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="079e1-115">Security</span></span>
### <a name="site-access"></a><span data-ttu-id="079e1-116">サイト アクセス</span><span class="sxs-lookup"><span data-stu-id="079e1-116">Site access</span></span>

<span data-ttu-id="079e1-117">ドメイン/クライアントへのアクセスは、既存のログインおよびSSL メカニズムを通じて制御されます。</span><span class="sxs-lookup"><span data-stu-id="079e1-117">Access to the domain/client is controlled through the existing login and SSL mechanism.</span></span>

### <a name="form-access"></a><span data-ttu-id="079e1-118">フォーム アクセス</span><span class="sxs-lookup"><span data-stu-id="079e1-118">Form access</span></span>
<span data-ttu-id="079e1-119">メニュー項目はセキュリティが施工されているエントリ ポイントなので、フォームへのアクセスはメニュー項目によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="079e1-119">Access to forms is controlled through Menu items, as Menu items are the entry points where security is enforced.</span></span> <span data-ttu-id="079e1-120">ユーザーがアクセス権を持たないメニュー項目を含む URL を使用して移動する場合、メニュー項目のセキュリティにより、フォームが開かれなくなります。</span><span class="sxs-lookup"><span data-stu-id="079e1-120">If a user navigates using a URL that contains a Menu item that the user does not have access to, then the Menu item security will prevent the form from opening.</span></span> <span data-ttu-id="079e1-121">ユーザーは、フォームを開くために必要な権限を持っていないことを示すメッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="079e1-121">The user will receive a message indicating that they do not have the necessary permissions to open the form.</span></span> <span data-ttu-id="079e1-122">ディープ リンクは、ルート ナビゲーションを許可するメニュー項目に対してのみ機能することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="079e1-122">Note that deep links will only work for Menu items that allow root navigation.</span></span>

### <a name="data-access"></a><span data-ttu-id="079e1-123">データ アクセス</span><span class="sxs-lookup"><span data-stu-id="079e1-123">Data access</span></span>

<span data-ttu-id="079e1-124">データへのアクセスは、既存のフォーム レベルのクエリによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="079e1-124">Access to data is controlled through the existing form-level queries.</span></span> <span data-ttu-id="079e1-125">生成された URL を使用してフォームが開かれているとき、そのフォームは既存のフォーム レベルのクエリを実行します。これにより、データへのユーザーのアクセスが制限されます。</span><span class="sxs-lookup"><span data-stu-id="079e1-125">When a form is opened with a generated URL, the form will run its existing form-level queries, which restrict the user's access to data.</span></span> <span data-ttu-id="079e1-126">生成された URL で指定されたデータ コンテキストは、これらのフォーム レベルのクエリが適用された後に消費され、ユーザーに表示されるデータをさらにフィルタリングする場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="079e1-126">The data context that is specified in the generated URL is consumed after these form-level queries are applied, and results only in further filtering of the data displayed to the user.</span></span> <span data-ttu-id="079e1-127">つまり、生成された URL は多くても 1 つのフォームを開いて、フォーム レベルのクエリに基づいてフォームがユーザーに表示するデータすべてを表示できます。</span><span class="sxs-lookup"><span data-stu-id="079e1-127">In short, a generated URL can, at most, open a form and display all of the data that a form would display to the user based on the form-level queries.</span></span> <span data-ttu-id="079e1-128">生成された URL には、生成された URL を使用していない場合にフォームでアクセスできないデータへのアクセスをユーザーに与えることはできません。</span><span class="sxs-lookup"><span data-stu-id="079e1-128">A generated URL cannot grant a user access to data that is otherwise inaccessible on the form when not using the generated URL.</span></span>

## <a name="usage"></a><span data-ttu-id="079e1-129">用途</span><span class="sxs-lookup"><span data-stu-id="079e1-129">Usage</span></span>
<span data-ttu-id="079e1-130">URL ジェネレーターは、次の名前空間の下の X++ からアクセス可能な .NET ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="079e1-130">The URL Generator is a .NET library that is accessible from X++, under the following namespace.</span></span>

```xpp
Microsoft.Dynamics.AX.Framework.Utilities.UrlHelper.UrlGenerator
```

#### <a name="requirements"></a><span data-ttu-id="079e1-131">必要量</span><span class="sxs-lookup"><span data-stu-id="079e1-131">Requirements</span></span>

<span data-ttu-id="079e1-132">URL ジェネレーターは、アクティブなユーザー セッションまたはバッチ処理で、AOS 上で実行されているコードから使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079e1-132">The URL Generator must be used from code running on the AOS, in an active user session or batch process.</span></span> <span data-ttu-id="079e1-133">この要件は、URL を生成するインスタンスに固有の暗号化によるセキュリティで保護することができます。</span><span class="sxs-lookup"><span data-stu-id="079e1-133">This requirement ensures that the URL can be secured through encryption specific to the instance that generates the URL.</span></span> <span data-ttu-id="079e1-134">少なくとも、作業 URL を生成するために次の情報を指定して URL ジェネレータに渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="079e1-134">At a minimum, the following information must be specified and passed to the URL Generator in order to generate a working URL.</span></span>

-   <span data-ttu-id="079e1-135">**ホスト URL**</span><span class="sxs-lookup"><span data-stu-id="079e1-135">**Host URL**</span></span>
    -   <span data-ttu-id="079e1-136">インスタンスの Web ルートの URL。</span><span class="sxs-lookup"><span data-stu-id="079e1-136">The URL of the web root for the instance.</span></span> <span data-ttu-id="079e1-137">例: https://ax.dynamics.contoso.com/</span><span class="sxs-lookup"><span data-stu-id="079e1-137">For example: https://ax.dynamics.contoso.com/</span></span>
-   <span data-ttu-id="079e1-138">**メニュー項目の表示**の AOT 名</span><span class="sxs-lookup"><span data-stu-id="079e1-138">AOT name of the **Menu Item Display**</span></span>
    -   <span data-ttu-id="079e1-139">フォームを開くために使用するメニュー項目の表示。</span><span class="sxs-lookup"><span data-stu-id="079e1-139">The menu item display to be used to open the form.</span></span>
-   <span data-ttu-id="079e1-140">**パーティション**</span><span class="sxs-lookup"><span data-stu-id="079e1-140">**Partition**</span></span>
    -   <span data-ttu-id="079e1-141">要求に使用するパーティション。</span><span class="sxs-lookup"><span data-stu-id="079e1-141">The partition to use for the request.</span></span>
-   <span data-ttu-id="079e1-142">**会社**</span><span class="sxs-lookup"><span data-stu-id="079e1-142">**Company**</span></span>
    -   <span data-ttu-id="079e1-143">要求に使用する会社。</span><span class="sxs-lookup"><span data-stu-id="079e1-143">The company to use for the request.</span></span>

#### <a name="example"></a><span data-ttu-id="079e1-144">例</span><span class="sxs-lookup"><span data-stu-id="079e1-144">Example</span></span>

```xpp
// gets the generator instance
var generator     = new Microsoft.Dynamics.AX.Framework.Utilities.UrlHelper.UrlGenerator();
var currentHost   = new System.Uri(UrlUtility::getUrl());
generator.HostUrl = currentHost.GetLeftPart(System.UriPartial::Authority);
generator.Company = curext();
generator.MenuItemName = <menu item name>;
generator.Partition = getCurrentPartition(); 

// repeat this segment for each datasource to filter
var requestQueryParameterCollection = generator.RequestQueryParameterCollection;
requestQueryParameterCollection.AddRequestQueryParameter(
    <datasource name>,
    <field1>, <value1>,
    <field2>, <value2>,
    <field3>, <value3>,
    <field4>, <value4>,
    <field5>, <value5>
);

System.Uri fullURI = generator.GenerateFullUrl();

// to get the encoded URI, use the following code
fullURI.AbsoluteUri
```



