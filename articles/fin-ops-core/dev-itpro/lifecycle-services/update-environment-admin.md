---
title: 環境管理者の更新
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) の財務と運用アプリ環境で環境管理者を変更する方法について説明します。
author: laneswenka
ms.date: 05/10/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-03-05
ms.openlocfilehash: ed5971ad4337091abf8261a1cd0045f92e3377d4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103379"
---
# <a name="update-the-environment-administrator"></a>環境管理者の更新

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) で財務と運用アプリ環境を作成する場合、構成オプションの 1 つで環境管理者としてユーザーを選択する必要があります。 このユーザーは、財務と運用アプリでシステム管理者ロールが割り当てられている既定の **管理者** ユーザー レコードに関連付けられている電子メール アカウントになります。

管理者ユーザーは、システム バッチ ジョブを実行する場合など、アプリのいくつかの場面で重要な役割を果たします。 これらのジョブは管理者特権で実行する必要があります。 組織を去るとユーザーの Azure Active Directory (Azure AD) アカウントは無効になるので、これらのユーザーは会社の通常のユーザーには関連付けできません。

ただし、管理者ユーザー アカウントが Azure AD で無効になることがあり、アプリの **管理者** ユーザー レコードを変更する方法がないことがわかっています。 以前は、この問題がサポート チケットを介して手動でサポートされましたが、現在は LCS のセルフサービス アクションが実行されています。

## <a name="change-the-environment-administrator-account"></a>環境管理者アカウントの変更

環境管理者を変更するには、LCS プロジェクトのプロジェクト所有者である必要があります。

1. LCS でプロジェクトに移動し、環境の詳細ページを開きます。
2. **管理 \> 更新管理者の更新** を選択します
3. 表示されるダイアログ ボックスで、LCS プロジェクトから別のプロジェクト所有者または環境管理者ユーザーを選択します。
4. **保存** を選択します。

> [!IMPORTANT]
> 環境管理者アカウントを変更すると、ターゲットの財務と運用アプリ環境でダウンタイムが発生します。 したがって、この機能は、組織のダウンタイムをスケジュールした後にのみ適切な方法で使用します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

