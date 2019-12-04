---
title: Dynamics 365 - Core HR への Power Apps アプリの埋め込み
description: このトピックでは、Microsoft Power Apps メニュー項目がシステム管理モジュールから消えてしまう問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830212"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="288b8-103">Dynamics 365 - Core HR への Power Apps アプリの埋め込み</span><span class="sxs-lookup"><span data-stu-id="288b8-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="288b8-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="288b8-104">**Issue**</span></span>

<span data-ttu-id="288b8-105">**Power Apps** メニュー項目が**システム管理**モジュールから消えました。</span><span class="sxs-lookup"><span data-stu-id="288b8-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="288b8-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="288b8-106">**Cause**</span></span>

<span data-ttu-id="288b8-107">ユーザー インターフェイス (UI) のデザインが変更され、Microsoft Power Apps が標準の個人用設定モデルに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="288b8-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="288b8-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="288b8-108">**Resolution**</span></span>

<span data-ttu-id="288b8-109">Power Apps が埋め込まれる方法が変更されました。</span><span class="sxs-lookup"><span data-stu-id="288b8-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="288b8-110">Power Apps は個人用設定モデルによって追加されます。</span><span class="sxs-lookup"><span data-stu-id="288b8-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="288b8-111">Power Apps は、Microsoft Dynamics 365 Talent のほとんどすべてのページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="288b8-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="288b8-112">Power Apps を Talent に埋め込む方法の詳細については、[Microsoft Power Apps の埋め込み](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="288b8-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="288b8-113">変更前にアプリを埋め込んだ Power Apps の顧客は、新しいモデルにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="288b8-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="288b8-114">**Power Apps** ボタンは、Talent のほとんどすべてのページの右上隅にあります。</span><span class="sxs-lookup"><span data-stu-id="288b8-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="288b8-115">このボタンを使用して、Power Apps を挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="288b8-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="288b8-116">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="288b8-116">Here is an example.</span></span>

1. <span data-ttu-id="288b8-117">**人事管理\>リンク\>作業者\>従業員**に移動します。</span><span class="sxs-lookup"><span data-stu-id="288b8-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="288b8-118">**Power Apps** ボタンを選択してから、**PowerApp の挿入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="288b8-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps ボタン](media/png.png)

3. <span data-ttu-id="288b8-120">**PowerApp の挿入**ダイアログ ボックスのフィールドを完了します。</span><span class="sxs-lookup"><span data-stu-id="288b8-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![PowerApp の挿入ダイアログ ボックス](media/insert-powerapp.png)

<span data-ttu-id="288b8-122">または、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="288b8-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="288b8-123">ページのアクション ウィンドウの**オプション**タブ上の**個人用設定**グループで、**このフォームのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="288b8-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![オプション タブのグループをパーソナライズする](media/options.png)

    <span data-ttu-id="288b8-125">個人用設定ツール バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="288b8-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="288b8-126">ツール バーで、**挿入\>PowerApp** を選択します。</span><span class="sxs-lookup"><span data-stu-id="288b8-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![個人用設定ツール バーを使用して Power Apps アプリを挿入する](media/powerapp-bar.png)
