---
title: モバイル アプリ ページのフィールドをクリック可能にする
description: このトピックでは、モバイル アプリ ページのフィールドをカスタマイズして、メール アドレス、電話番号、または URL として表示する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 669ccfbd34090dc04ae666a220af015e71fe5a24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183103"
---
# <a name="make-fields-on-mobile-app-pages-clickable"></a><span data-ttu-id="ceaec-103">モバイル アプリ ページのフィールドをクリック可能にする</span><span class="sxs-lookup"><span data-stu-id="ceaec-103">Make fields on mobile app pages clickable</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="ceaec-104">モバイル アプリ ページのフィールドは、電子メール アドレス、電話番号、または URL として表示されるようにカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-104">The fields on a mobile app page can be customized so that they are shown as email addresses, phone numbers, or URLs.</span></span>

## <a name="email-field"></a><span data-ttu-id="ceaec-105">電子メール フィールド</span><span class="sxs-lookup"><span data-stu-id="ceaec-105">Email field</span></span>
<span data-ttu-id="ceaec-106">ビジネス ロジックを使用することにより、フィールドを電子メール アドレス フィールドとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-106">You can mark a field as an email address field by using business logic.</span></span> <span data-ttu-id="ceaec-107">ユーザーがフィールドをクリックすると、規定のモバイル メール アプリが起動し、フィールド値がアプリにメール アドレスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-107">Then, when a user clicks the field, the default mobile email app starts, and the field value appears as the email address in the app.</span></span>

## <a name="phone-field"></a><span data-ttu-id="ceaec-108">電話番号フィールド</span><span class="sxs-lookup"><span data-stu-id="ceaec-108">Phone field</span></span>
<span data-ttu-id="ceaec-109">ビジネス ロジックを使用することにより、フィールドを電話番号フィールドとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-109">You can mark a field as a phone number field by using business logic.</span></span> <span data-ttu-id="ceaec-110">ユーザーがフィールドをクリックすると、モバイル ダイヤラー アプリが起動し、フィールド値がアプリに電話番号として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-110">Then, when a user clicks the field, the mobile dialer app starts, and the field value appears as the phone number in the app.</span></span>

> [!NOTE]
> <span data-ttu-id="ceaec-111">IOS では、電話番号が無効な場合、携帯電話のダイヤラー アプリが発生しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ceaec-111">On iOS, if the phone number isn't valid, it might not trigger the mobile dialer app.</span></span>

## <a name="url-field"></a><span data-ttu-id="ceaec-112">URL フィールド</span><span class="sxs-lookup"><span data-stu-id="ceaec-112">URL field</span></span>
<span data-ttu-id="ceaec-113">ビジネス ロジックを使用することにより、フィールドを URL フィールドとしてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-113">You can mark a field as a URL field by using business logic.</span></span> <span data-ttu-id="ceaec-114">ユーザーがフィールドをクリックすると、規定のモバイル ブラウザーに URL が開き、アドレス バーにフィールド値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ceaec-114">Then, when a user clicks the field, the URL opens in the default mobile browser, and the field value appears in the address bar.</span></span>

> [!NOTE]
> <span data-ttu-id="ceaec-115">iOS では完全な URL (つまり、<strong>https</strong> などのプロトコルで始まる URL) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ceaec-115">On iOS, you must provide a complete URL (that is, a URL that starts with a protocol, such as <strong>https</strong>).</span></span> <span data-ttu-id="ceaec-116">それ以外の場合、URL はブラウザーで開かれません。</span><span class="sxs-lookup"><span data-stu-id="ceaec-116">Otherwise, the URL isn't opened in the browser.</span></span> <span data-ttu-id="ceaec-117">www.microsoft.com などの URL は機能しません。</span><span class="sxs-lookup"><span data-stu-id="ceaec-117">A URL such as www.microsoft.com doesn't work.</span></span> <span data-ttu-id="ceaec-118">代わりに、URL は `https://www.microsoft.com` で指定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ceaec-118">Instead, the URL must be specified as `https://www.microsoft.com`.</span></span>

## <a name="example"></a><span data-ttu-id="ceaec-119">例</span><span class="sxs-lookup"><span data-stu-id="ceaec-119">Example</span></span>
<span data-ttu-id="ceaec-120">この例では、顧客の電子メール アドレスと電話番号フィールドを、適切な iOS アプリケーションでクリックして開くことができるように設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ceaec-120">This example shows how to configure the customer email address and phone number fields so that they can clicked and opened in the appropriate iOS apps.</span></span>

<span data-ttu-id="ceaec-121">フィールドをカスタマイズする前に、次のイメージに示すように、フィールドをクリックすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ceaec-121">Before the fields are customized, they can't be clicked, as shown in the following image.</span></span>

![変更される前の、顧客の詳細ページ](media/workspace-api/FieldAsURLOriginal.png)

<span data-ttu-id="ceaec-123">フィールドがリンクであることを指定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ceaec-123">Follow these steps to specify that a field is a link.</span></span>

1. <span data-ttu-id="ceaec-124">**appInit** メソッドに次の明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ceaec-124">Add the following lines to the **appInit** method.</span></span> <span data-ttu-id="ceaec-125">**configureControl** メソッドを呼び出して、ページ名とコントロール名を渡します。</span><span class="sxs-lookup"><span data-stu-id="ceaec-125">You call the **configureControl** method, and pass in the page name and control name.</span></span> <span data-ttu-id="ceaec-126">次に、コントロールの **LinkType** 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ceaec-126">You then supply the **LinkType** value for the control.</span></span> <span data-ttu-id="ceaec-127">次の値がサポートされています: **電話**、**電子メール**、および **URL**。</span><span class="sxs-lookup"><span data-stu-id="ceaec-127">The following values are supported: **Telephone**, **Email**, and **Url**.</span></span>

    ```
    metadataService.configureControl('PageName', 'ControlName', { LinkType: 'Telephone' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Email' });
    metadataService.configureControl('PageName', ' ControlName ', { LinkType: 'Url' });
    ```

2. <span data-ttu-id="ceaec-128">モバイル アプリ デザイナーを使用して、更新されたビジネス ロジック ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ceaec-128">Upload the updated business logic file by using the mobile app designer.</span></span>
3. <span data-ttu-id="ceaec-129">モバイル クライアントでワークスペース メタデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="ceaec-129">Update the workspace metadata in the mobile client.</span></span>

<span data-ttu-id="ceaec-130">フィールドはリンクとして表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ceaec-130">The fields now appear as links.</span></span>

![変更後の顧客詳細ページ](media/workspace-api/FieldAsURLFinal.png)