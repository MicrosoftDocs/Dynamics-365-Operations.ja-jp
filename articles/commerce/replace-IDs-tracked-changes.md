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
ms.openlocfilehash: 080a97e4fa436392680a62ea232f9881a17c452e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345096"
---
# <a name="replace-user-ids-associated-with-tracked-content-changes"></a>追跡しているコンテンツの変更に関連付いたユーザー ID の置換

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーで追跡しているコンテンツの変更に関連付けられたユーザー ID を置換する方法について説明します。

Dynamics 365 Commerce では、サイト ビルダー オーサリング ツールは、コンテンツ管理システム (CMS) の項目に対して行われた変更を追跡します。 したがって、ドキュメントの変更履歴を表示して、チームがコンテンツで共同作業を行うときに、作業を追跡するのに役立ちます。 追跡された変更にユーザー ID を割り当てるために、システムは Azure Active Directory (Azure AD) ID 管理システムのユーザー ID を使用します。 これらのユーザー ID は、Azure AD が発行する電子メール アドレスでもあります。 Commerce システム管理者は、必要に応じてサイト ビルダーの変更追跡履歴ログのユーザー ID 参照を置き換えることができます。

## <a name="replace-a-user-id-in-site-builder"></a>サイト ビルダーでのユーザー ID の置換

サイト ビルダーでユーザー IDを置換するには、次の手順を実行します。

1. サイトの **ホーム** ページに移動します。
1. 左のナビゲーション ウィンドウで、**テナントの設定** を展開し、**コンテンツ変更の追跡** を選択します。

    ![選択したコンテンツ変更の追跡。](./media/TrackingContentChanges.png)

1. **コンテンツ変更の追跡** ページで、**管理** を選択します。
1. **電子メール アドレスの置換** フィールドに、変更追跡ログから削除するユーザー ID の電子メール アドレスを入力し、**置換** を選択します。 (**置換** を選択する前に、複数の電子メール アドレスを入力することができます。)

    ![[電子メール アドレスの管理] ダイアログ ボックスに入力された電子メール アドレス。](./media/ReplaceEmailAddress.png)

1. **OK** を選択してから、**保存** を選択します。 メッセージ ボックスに、入力したユーザー ID のレコードが更新されたことが通知されます。

> [!NOTE]
> サイト ビルダーは、すべてのユーザー ID の電子メール アドレスを、匿名化されたランダムに生成された文字列に置き換えて、電子メール アドレスへの CMS 参照をすべて削除します。 このアクションは、サイト ビルダー インスタンスに関連付けられた特定の E コマース環境 (テナント) で参照される履歴ログにのみ影響します。

## <a name="additional-resources"></a>追加リソース

[コンプライアンスの概要](compliance-overview.md)

[ユーザー補助機能](accessibility.md)

[Cookie のコンプライアンス](cookie-compliance.md)

[プライバシー ポリシー ページの追加](add-privacy-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
