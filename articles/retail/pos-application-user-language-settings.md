---
title: 販売時点管理 (POS) アプリケーションおよびユーザー言語の設定
description: このトピックでは、Retail Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "336753"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="0bb31-103">販売時点管理 (POS) アプリケーションおよびユーザー言語の設定</span><span class="sxs-lookup"><span data-stu-id="0bb31-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0bb31-104">このトピックでは、Retail Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0bb31-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="0bb31-105">概要</span><span class="sxs-lookup"><span data-stu-id="0bb31-105">Overview</span></span>

<span data-ttu-id="0bb31-106">Retail Modern POS (MPOS) とクラウド POS は、言語設定と翻訳が店舗とユーザーの設定によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="0bb31-107">たとえば、店舗は顧客にとって英語が最も一般的な地域に位置することができますが、一部の作業者はフランス語の翻訳でアプリケーションを使用することを好みます。</span><span class="sxs-lookup"><span data-stu-id="0bb31-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="0bb31-108">データ言語</span><span class="sxs-lookup"><span data-stu-id="0bb31-108">Data language</span></span>

<span data-ttu-id="0bb31-109">ユーザーの設定にかかわらず、MPOS と Cloud POS は常にストアの言語設定を使用してデータに使用される翻訳を決定します。</span><span class="sxs-lookup"><span data-stu-id="0bb31-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="0bb31-110">これにより、すべてのユーザーと顧客が一貫性のあるエクスペリエンスを確保できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="0bb31-111">データの例は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="0bb31-111">Examples of data include:</span></span>

- <span data-ttu-id="0bb31-112">製品</span><span class="sxs-lookup"><span data-stu-id="0bb31-112">Products</span></span>
- <span data-ttu-id="0bb31-113">属性と値</span><span class="sxs-lookup"><span data-stu-id="0bb31-113">Attributes and values</span></span>
- <span data-ttu-id="0bb31-114">カテゴリ名</span><span class="sxs-lookup"><span data-stu-id="0bb31-114">Category names</span></span>
- <span data-ttu-id="0bb31-115">印刷または電子メール送信されたトランザクション受領書</span><span class="sxs-lookup"><span data-stu-id="0bb31-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="0bb31-116">支払方法名</span><span class="sxs-lookup"><span data-stu-id="0bb31-116">Payment method names</span></span>
- <span data-ttu-id="0bb31-117">ライン ディスプレイ メッセージ</span><span class="sxs-lookup"><span data-stu-id="0bb31-117">Line display messages</span></span>

<span data-ttu-id="0bb31-118">ログインする前にユーザーがわからないため、店舗の言語はメインの POS ログイン画面にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="0bb31-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="0bb31-119">店舗の言語で翻訳が利用できない場合、POS は会社の言語に戻ります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="0bb31-120">店舗の言語設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0bb31-120">Configuring the store's language setting</span></span>

<span data-ttu-id="0bb31-121">店舗の言語設定は、**一般 &gt; 地域の設定 &gt; 言語**の**小売店舗**ページにある**すべての小売店舗**から設定します。</span><span class="sxs-lookup"><span data-stu-id="0bb31-121">The store's language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="0bb31-122">ドロップ ダウンを使用して、各店舗の言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="0bb31-122">Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="0bb31-123">ユーザー インターフェイス言語</span><span class="sxs-lookup"><span data-stu-id="0bb31-123">User interface language</span></span>

<span data-ttu-id="0bb31-124">POS ユーザーの言語設定によって、アプリケーション ユーザー インターフェースで使用される翻訳が決まります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="0bb31-125">これには、データと見なされないすべてのラベル、メニュー、およびリストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0bb31-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="0bb31-126">1 つの例外は POS ボタン グリッドに表示されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="0bb31-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="0bb31-127">ボタン グリッドは翻訳をサポートしていないため、ボタンに定義されているテキストが常に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0bb31-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="0bb31-128">翻訳されたボタンをサポートするには、別々のボタン グリッドをコピーして管理し、必要に応じてそれらをユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="0bb31-129">ユーザーの言語設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0bb31-129">Configuring the user's language setting</span></span>

<span data-ttu-id="0bb31-130">POS ユーザーの言語設定は、**小売 &gt; 言語**の下の**作業者**ページの**すべての作業者**から設定します。</span><span class="sxs-lookup"><span data-stu-id="0bb31-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span> <span data-ttu-id="0bb31-131">メインのプロフィール タブでは設定しません。この設定は POS では使用されません。</span><span class="sxs-lookup"><span data-stu-id="0bb31-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="0bb31-132">ユーザーの言語が設定されていないか、翻訳が使用できない言語に設定されている場合、POS は店舗の言語に戻ります。</span><span class="sxs-lookup"><span data-stu-id="0bb31-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="0bb31-133">[UI l言語]  </span><span class="sxs-lookup"><span data-stu-id="0bb31-133">UI language</span></span>                | <span data-ttu-id="0bb31-134">[データ言語 (製品、受領書フォーマット、ライン ディスプレイなど)]</span><span class="sxs-lookup"><span data-stu-id="0bb31-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0bb31-135">**会社**</span><span class="sxs-lookup"><span data-stu-id="0bb31-135">**Company**</span></span> | <span data-ttu-id="0bb31-136">既定</span><span class="sxs-lookup"><span data-stu-id="0bb31-136">Default</span></span>                    | <span data-ttu-id="0bb31-137">既定</span><span class="sxs-lookup"><span data-stu-id="0bb31-137">Default</span></span>                                                       |
| <span data-ttu-id="0bb31-138">**店舗**</span><span class="sxs-lookup"><span data-stu-id="0bb31-138">**Store**</span></span>   | <span data-ttu-id="0bb31-139">会社を上書き</span><span class="sxs-lookup"><span data-stu-id="0bb31-139">Overrides company</span></span>          | <span data-ttu-id="0bb31-140">会社を上書き</span><span class="sxs-lookup"><span data-stu-id="0bb31-140">Overrides company</span></span>                                             |
| <span data-ttu-id="0bb31-141">**ユーザー**</span><span class="sxs-lookup"><span data-stu-id="0bb31-141">**User**</span></span>    | <span data-ttu-id="0bb31-142">店舗又は会社を上書き</span><span class="sxs-lookup"><span data-stu-id="0bb31-142">Overrides store or company</span></span> | <span data-ttu-id="0bb31-143">なし</span><span class="sxs-lookup"><span data-stu-id="0bb31-143">Never</span></span>                                                         |
