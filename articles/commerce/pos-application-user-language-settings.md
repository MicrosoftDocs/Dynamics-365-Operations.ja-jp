---
title: 販売時点管理 (POS) アプリケーションおよびユーザー言語の設定
description: このトピックでは、Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bdd03dff359e7c2799eff53b0e999580ce8b1c06
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193106"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="f921e-103">販売時点管理 (POS) アプリケーションおよびユーザー言語の設定</span><span class="sxs-lookup"><span data-stu-id="f921e-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f921e-104">このトピックでは、Modern POS (MPOS) とクラウド POS の言語設定を変更する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f921e-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="f921e-105">概要</span><span class="sxs-lookup"><span data-stu-id="f921e-105">Overview</span></span>
<span data-ttu-id="f921e-106">Modern POS (MPOS) とクラウド POS は、言語設定と翻訳が店舗とユーザーの設定によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f921e-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="f921e-107">たとえば、店舗は顧客にとって英語が最も一般的な地域に位置することができますが、一部の作業者はフランス語の翻訳でアプリケーションを使用することを好みます。</span><span class="sxs-lookup"><span data-stu-id="f921e-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="f921e-108">データ言語</span><span class="sxs-lookup"><span data-stu-id="f921e-108">Data language</span></span>

<span data-ttu-id="f921e-109">ユーザーの設定にかかわらず、MPOS と Cloud POS は常にストアの言語設定を使用してデータに使用される翻訳を決定します。</span><span class="sxs-lookup"><span data-stu-id="f921e-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="f921e-110">これにより、すべてのユーザーと顧客が一貫性のあるエクスペリエンスを確保できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f921e-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="f921e-111">データの例は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="f921e-111">Examples of data include:</span></span>

- <span data-ttu-id="f921e-112">製品</span><span class="sxs-lookup"><span data-stu-id="f921e-112">Products</span></span>
- <span data-ttu-id="f921e-113">属性と値</span><span class="sxs-lookup"><span data-stu-id="f921e-113">Attributes and values</span></span>
- <span data-ttu-id="f921e-114">カテゴリ名</span><span class="sxs-lookup"><span data-stu-id="f921e-114">Category names</span></span>
- <span data-ttu-id="f921e-115">印刷または電子メール送信されたトランザクション受領書</span><span class="sxs-lookup"><span data-stu-id="f921e-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="f921e-116">支払方法名</span><span class="sxs-lookup"><span data-stu-id="f921e-116">Payment method names</span></span>
- <span data-ttu-id="f921e-117">ライン ディスプレイ メッセージ</span><span class="sxs-lookup"><span data-stu-id="f921e-117">Line display messages</span></span>

<span data-ttu-id="f921e-118">ログインする前にユーザーがわからないため、店舗の言語はメインの POS ログイン画面にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="f921e-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="f921e-119">店舗の言語で翻訳が利用できない場合、POS は会社の言語に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f921e-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="f921e-120">店舗の言語設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f921e-120">Configuring the store's language setting</span></span>

<span data-ttu-id="f921e-121">店舗の言語設定は、**一般 &gt; 地域の設定 &gt; 言語** の、**店舗** ページにある **すべての店舗** から設定します。</span><span class="sxs-lookup"><span data-stu-id="f921e-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="f921e-122">ドロップ ダウン リストを使用して、各店舗の言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="f921e-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="f921e-123">ユーザー インターフェイス言語</span><span class="sxs-lookup"><span data-stu-id="f921e-123">User interface language</span></span>

<span data-ttu-id="f921e-124">POS ユーザーの言語設定によって、アプリケーション ユーザー インターフェースで使用される翻訳が決まります。</span><span class="sxs-lookup"><span data-stu-id="f921e-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="f921e-125">これには、データと見なされないすべてのラベル、メニュー、およびリストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f921e-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="f921e-126">1 つの例外は POS ボタン グリッドに表示されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="f921e-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="f921e-127">ボタン グリッドは翻訳をサポートしていないため、ボタンに定義されているテキストが常に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f921e-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="f921e-128">翻訳されたボタンをサポートするには、別々のボタン グリッドをコピーして管理し、必要に応じてそれらをユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f921e-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="f921e-129">ユーザーの言語設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f921e-129">Configuring the user's language setting</span></span>

<span data-ttu-id="f921e-130">POS ユーザーの言語設定は、**Retail とコマース &gt; 言語** の下の、**作業者** ページの **すべての作業者** から設定します。</span><span class="sxs-lookup"><span data-stu-id="f921e-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="f921e-131">メインのプロフィール タブでは設定しません。この設定は POS では使用されません。</span><span class="sxs-lookup"><span data-stu-id="f921e-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="f921e-132">ユーザーの言語が設定されていないか、翻訳が使用できない言語に設定されている場合、POS は店舗の言語に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f921e-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

| &nbsp;      | <span data-ttu-id="f921e-133">[UI l言語]  </span><span class="sxs-lookup"><span data-stu-id="f921e-133">UI language</span></span>                | <span data-ttu-id="f921e-134">[データ言語 (製品、受領書フォーマット、ライン ディスプレイなど)]</span><span class="sxs-lookup"><span data-stu-id="f921e-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f921e-135">**会社**</span><span class="sxs-lookup"><span data-stu-id="f921e-135">**Company**</span></span> | <span data-ttu-id="f921e-136">既定</span><span class="sxs-lookup"><span data-stu-id="f921e-136">Default</span></span>                    | <span data-ttu-id="f921e-137">既定</span><span class="sxs-lookup"><span data-stu-id="f921e-137">Default</span></span>                                                       |
| <span data-ttu-id="f921e-138">**店舗**</span><span class="sxs-lookup"><span data-stu-id="f921e-138">**Store**</span></span>   | <span data-ttu-id="f921e-139">会社を上書き</span><span class="sxs-lookup"><span data-stu-id="f921e-139">Overrides company</span></span>          | <span data-ttu-id="f921e-140">会社を上書き</span><span class="sxs-lookup"><span data-stu-id="f921e-140">Overrides company</span></span>                                             |
| <span data-ttu-id="f921e-141">**ユーザー**</span><span class="sxs-lookup"><span data-stu-id="f921e-141">**User**</span></span>    | <span data-ttu-id="f921e-142">店舗又は会社を上書き</span><span class="sxs-lookup"><span data-stu-id="f921e-142">Overrides store or company</span></span> | <span data-ttu-id="f921e-143">なし</span><span class="sxs-lookup"><span data-stu-id="f921e-143">Never</span></span>                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]