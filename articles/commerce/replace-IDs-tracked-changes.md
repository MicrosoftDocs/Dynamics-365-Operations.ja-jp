---
title: 追跡しているコンテンツの変更に関連付いたユーザー ID の置換
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで追跡しているコンテンツの変更に関連付けられたユーザー ID を置換する方法について説明します。
author: BrianShook
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0a0a9e778e3dbcf86029e5df5811c3a3fe4a4913
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792063"
---
# <a name="replace-user-ids-associated-with-tracked-content-changes"></a><span data-ttu-id="0379b-103">追跡しているコンテンツの変更に関連付いたユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="0379b-103">Replace user IDs associated with tracked content changes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0379b-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで追跡しているコンテンツの変更に関連付けられたユーザー ID を置換する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0379b-104">This topic describes how to replace user IDs that are associated with tracked content changes in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="0379b-105">Dynamics 365 Commerce では、サイト ビルダー オーサリング ツールは、コンテンツ管理システム (CMS) の項目に対して行われた変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="0379b-105">In Dynamics 365 Commerce, the site builder authoring tool tracks changes that are made to items in the content management system (CMS).</span></span> <span data-ttu-id="0379b-106">したがって、ドキュメントの変更履歴を表示して、チームがコンテンツで共同作業を行うときに、作業を追跡するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0379b-106">Therefore, a document change history can be shown to help teams track their efforts when they collaborate on content.</span></span> <span data-ttu-id="0379b-107">追跡された変更にユーザー ID を割り当てるために、システムは Azure Active Directory (Azure AD) ID 管理システムのユーザー ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="0379b-107">To assign user identities to tracked changes, the system uses user IDs from the Azure Active Directory (Azure AD) identity management system.</span></span> <span data-ttu-id="0379b-108">これらのユーザー ID は、Azure AD が発行する電子メール アドレスでもあります。</span><span class="sxs-lookup"><span data-stu-id="0379b-108">These user IDs are also the email addresses that are issued by Azure AD.</span></span> <span data-ttu-id="0379b-109">Commerce システム管理者は、必要に応じてサイト ビルダーの変更追跡履歴ログのユーザー ID 参照を置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="0379b-109">Commerce system admins can replace user ID references in the change tracking history logs in site builder as they require.</span></span>

## <a name="replace-a-user-id-in-site-builder"></a><span data-ttu-id="0379b-110">サイト ビルダーでのユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="0379b-110">Replace a user ID in site builder</span></span>

<span data-ttu-id="0379b-111">サイト ビルダーでユーザー IDを置換するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0379b-111">To replace a user ID in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0379b-112">サイトの **ホーム** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="0379b-112">Go to the **Home** page for your site.</span></span>
1. <span data-ttu-id="0379b-113">左のナビゲーション ウィンドウで、**テナントの設定** を展開し、**コンテンツ変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0379b-113">In the left navigation pane, expand **Tenant Settings**, and then select **Tracking Content Changes**.</span></span>

    ![選択したコンテンツ変更の追跡](./media/TrackingContentChanges.png)

1. <span data-ttu-id="0379b-115">**コンテンツ変更の追跡** ページで、**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0379b-115">On the **Tracking Content Changes** page, select **Manage**.</span></span>
1. <span data-ttu-id="0379b-116">**電子メール アドレスの置換** フィールドに、変更追跡ログから削除するユーザー ID の電子メール アドレスを入力し、**置換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0379b-116">In the **Replace email address** field, enter the user ID email address that should be removed from the change tracking logs, and then select **Replace**.</span></span> <span data-ttu-id="0379b-117">(**置換** を選択する前に、複数の電子メール アドレスを入力することができます。)</span><span class="sxs-lookup"><span data-stu-id="0379b-117">(You can enter multiple email addresses before you select **Replace**.)</span></span>

    ![[電子メール アドレスの管理] ダイアログ ボックスに入力された電子メール アドレス](./media/ReplaceEmailAddress.png)

1. <span data-ttu-id="0379b-119">**OK** を選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0379b-119">Select **OK**, and then select **Save**.</span></span> <span data-ttu-id="0379b-120">メッセージ ボックスに、入力したユーザー ID のレコードが更新されたことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="0379b-120">A message box notifies you that the records for the user IDs that you entered have been updated.</span></span>

> [!NOTE]
> <span data-ttu-id="0379b-121">サイト ビルダーは、すべてのユーザー ID の電子メール アドレスを、匿名化されたランダムに生成された文字列に置き換えて、電子メール アドレスへの CMS 参照をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="0379b-121">Site builder replaces every user ID email address with an anonymized, randomly generated string to remove all CMS references to the email address.</span></span> <span data-ttu-id="0379b-122">このアクションは、サイト ビルダー インスタンスに関連付けられた特定の E コマース環境 (テナント) で参照される履歴ログにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="0379b-122">This action affects only the history logs that are referenced in the specific e-Commerce environment (tenant) that is associated with the site builder instance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0379b-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0379b-123">Additional resources</span></span>

[<span data-ttu-id="0379b-124">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="0379b-124">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="0379b-125">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="0379b-125">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="0379b-126">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="0379b-126">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="0379b-127">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="0379b-127">Add a privacy policy page</span></span>](add-privacy-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
