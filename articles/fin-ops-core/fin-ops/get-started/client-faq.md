---
title: クライアント FAQ
description: この記事じゃ、Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fe6da2575b7de866de614ad399c8ad5c0110d9a
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798502"
---
# <a name="client-faq"></a><span data-ttu-id="88dde-103">クライアント FAQ</span><span class="sxs-lookup"><span data-stu-id="88dde-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88dde-104">この記事じゃ、Finance and Operations クライアントについてよく寄せられる質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="88dde-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="88dde-105">なぜ記号が読み込まれないのですか。</span><span class="sxs-lookup"><span data-stu-id="88dde-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="88dde-106">ブラウザーのセキュリティ設定が、記号を正しく読み込むことを妨げている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="88dde-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="88dde-107">この問題を解決するには、次の手順を試してください。</span><span class="sxs-lookup"><span data-stu-id="88dde-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="88dde-108">Internet Explorer でこの問題が発生する場合、**ツール** をクリックしてから、**インターネット オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88dde-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="88dde-109">[インターネット オプション] ダイアログ ボックスの **プライバシー** タブで **レベルのカスタマイズ** をクリックし、**フォントのダウンロード** オプションが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88dde-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="88dde-110">それ以外の場合は、信頼済サイトのリストにアプリ サイトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88dde-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="88dde-111">Dynamics AX 2012 のリボンがありません。</span><span class="sxs-lookup"><span data-stu-id="88dde-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="88dde-112">[アクション ウィンドウ] のタブを常時開いておくことはできますか。</span><span class="sxs-lookup"><span data-stu-id="88dde-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="88dde-113">近々この機能を搭載する予定です。</span><span class="sxs-lookup"><span data-stu-id="88dde-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="88dde-114">ユーザーはアクション ウィンドウのタブを常時開いておくかどうか選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="88dde-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="88dde-115">それ以外の場合は、使用していないときはタブは折りたたまれ、ページの画面スペースがより広くなります。</span><span class="sxs-lookup"><span data-stu-id="88dde-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="88dde-116">右クリックしたときに、ときどき異なるショートカットメニューが表示されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="88dde-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="88dde-117">編集可能なフィールドで (またはテキストが選択されている場合に) 右クリックすると、ブラウザーのショートカット メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88dde-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="88dde-118">このメニューから、**切り取り**、**コピー**、**貼り付け** コマンドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="88dde-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="88dde-119">ショートカット メニューにこれらのコマンドを埋め込むことはできません。セキュリティ上の理由から、ブラウザーは、システムのクリップボードにプログラムからアクセスすることを許可していないためです。</span><span class="sxs-lookup"><span data-stu-id="88dde-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="88dde-120">読み取り専用コントロールのフィールド ラベルや値を右クリックすると、ショートカット メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88dde-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="88dde-121">キーボードでのアクセスを容易にするために、ショートカット メニューを開く機能にキーボード ショートカットを実装する予定です。</span><span class="sxs-lookup"><span data-stu-id="88dde-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="88dde-122">詳細の表示機能はありますか。</span><span class="sxs-lookup"><span data-stu-id="88dde-122">Where is the View details functionality?</span></span>

<span data-ttu-id="88dde-123">**詳細の表示** オプションが、いくつかの方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="88dde-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="88dde-124">コントロールに **詳細の表示** 機能がある場合、およびコントロールに値がある場合、その値はハイパーリンクとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="88dde-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="88dde-125">ハイパーリンクをクリックすると、詳細を含むページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="88dde-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="88dde-126">また、**詳細の表示** はショートカット メニューのオプションです。</span><span class="sxs-lookup"><span data-stu-id="88dde-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="88dde-127">右クリックしたときに、いつショートカット メニューが表示されるかについては、前のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88dde-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>
