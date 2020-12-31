---
title: 追跡しているコンテンツの変更に関連付いたユーザー ID の置換
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで追跡しているコンテンツの変更に関連付けられたユーザー IDを置換する方法について説明します。
author: BrianShook
manager: annbe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: Dynamics365Operations
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: b306bf7f4311423d92163ce54f528223bec346d9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408714"
---
# <a name="replace-user-ids-associated-with-tracked-content-changes"></a><span data-ttu-id="01c33-103">追跡しているコンテンツの変更に関連付いたユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="01c33-103">Replace user IDs associated with tracked content changes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01c33-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで追跡しているコンテンツの変更に関連付けられたユーザー IDを置換する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="01c33-104">This topic describes how to replace user IDs that are associated with tracked content changes in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="01c33-105">概要</span><span class="sxs-lookup"><span data-stu-id="01c33-105">Overview</span></span>

<span data-ttu-id="01c33-106">Dynamics 365 Commerce では、サイト ビルダー オーサリング ツールは、コンテンツ管理システム (CMS) の項目に対して行われた変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="01c33-106">In Dynamics 365 Commerce, the site builder authoring tool tracks changes that are made to items in the content management system (CMS).</span></span> <span data-ttu-id="01c33-107">したがって、ドキュメントの変更履歴を表示して、チームがコンテンツで共同作業を行うときに、作業を追跡するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="01c33-107">Therefore, a document change history can be shown to help teams track their efforts when they collaborate on content.</span></span> <span data-ttu-id="01c33-108">追跡された変更にユーザー ID を割り当てるために、システムは Azure Active Directory (Azure AD) ID 管理システムのユーザー ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="01c33-108">To assign user identities to tracked changes, the system uses user IDs from the Azure Active Directory (Azure AD) identity management system.</span></span> <span data-ttu-id="01c33-109">これらのユーザー ID は、Azure AD が発行する電子メール アドレスでもあります。</span><span class="sxs-lookup"><span data-stu-id="01c33-109">These user IDs are also the email addresses that are issued by Azure AD.</span></span> <span data-ttu-id="01c33-110">Commerce システム管理者は、必要に応じてサイト ビルダーの変更追跡履歴ログのユーザー ID 参照を置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="01c33-110">Commerce system admins can replace user ID references in the change tracking history logs in site builder as they require.</span></span>

## <a name="replace-a-user-id-in-site-builder"></a><span data-ttu-id="01c33-111">サイト ビルダーでのユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="01c33-111">Replace a user ID in site builder</span></span>

<span data-ttu-id="01c33-112">サイト ビルダーでユーザー IDを置換するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="01c33-112">To replace a user ID in site builder, follow these steps.</span></span>

1. <span data-ttu-id="01c33-113">サイトの **ホーム** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="01c33-113">Go to the **Home** page for your site.</span></span>
1. <span data-ttu-id="01c33-114">左のナビゲーション ウィンドウで、**テナントの設定** を展開し、**コンテンツ変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="01c33-114">In the left navigation pane, expand **Tenant Settings**, and then select **Tracking Content Changes**.</span></span>

    ![選択したコンテンツ変更の追跡](./media/TrackingContentChanges.png)

1. <span data-ttu-id="01c33-116">**コンテンツ変更の追跡** ページで、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="01c33-116">On the **Tracking Content Changes** page, select **Manage**.</span></span>
1. <span data-ttu-id="01c33-117">**電子メール アドレスの置換** フィールドに、変更追跡ログから削除するユーザー ID の電子メール アドレスを入力し、**置換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="01c33-117">In the **Replace email address** field, enter the user ID email address that should be removed from the change tracking logs, and then select **Replace**.</span></span> <span data-ttu-id="01c33-118">(**置換** を選択する前に、複数の電子メール アドレスを入力することができます。)</span><span class="sxs-lookup"><span data-stu-id="01c33-118">(You can enter multiple email addresses before you select **Replace**.)</span></span>

    ![[電子メール アドレスの管理] ダイアログ ボックスに入力された電子メール アドレス](./media/ReplaceEmailAddress.png)

1. <span data-ttu-id="01c33-120">**OK** を選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="01c33-120">Select **OK**, and then select **Save**.</span></span> <span data-ttu-id="01c33-121">メッセージ ボックスに、入力したユーザー ID のレコードが更新されたことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="01c33-121">A message box notifies you that the records for the user IDs that you entered have been updated.</span></span>

> [!NOTE]
> <span data-ttu-id="01c33-122">サイト ビルダーは、すべてのユーザー ID の電子メール アドレスを、匿名化されたランダムに生成された文字列に置き換えて、電子メール アドレスへの CMS 参照をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="01c33-122">Site builder replaces every user ID email address with an anonymized, randomly generated string to remove all CMS references to the email address.</span></span> <span data-ttu-id="01c33-123">このアクションは、サイト ビルダー インスタンスに関連付けられた特定の E コマース環境 (テナント) で参照される履歴ログにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="01c33-123">This action affects only the history logs that are referenced in the specific e-Commerce environment (tenant) that is associated with the site builder instance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01c33-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="01c33-124">Additional resources</span></span>

[<span data-ttu-id="01c33-125">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="01c33-125">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="01c33-126">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="01c33-126">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="01c33-127">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="01c33-127">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="01c33-128">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="01c33-128">Add a privacy policy page</span></span>](add-privacy-page.md)
