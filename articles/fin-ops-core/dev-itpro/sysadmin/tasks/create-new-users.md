---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570524"
---
# <a name="create-new-users"></a>新規ユーザーの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>ユーザーをライセンスに関連付ける (新しいライセンスタイプのみ)
2019 年 10 月に追加された新しいライセンスタイプのいずれかを使用している場合は、ユーザーはライセンスに関連付けられている必要があります。 ライセンスに関連付けられているユーザーは、最初にログインしたときに、ロールを持たないシステムユーザーとして自動的に追加されます。 ライセンスに関連付けられていないユーザーには、警告メッセージが表示されます。

システム管理者は、[Microsoft 365 管理者センター](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)で、[ユーザーにライセンスを割り当てる](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)ことができます。

## <a name="add-a-new-user"></a>新しいユーザーを追加する
1. **システム管理 \> ユーザー \> ユーザー**の順に移動します。
2. アクション ウィンドウで、**新規**を選択します。
3. **ユーザー ID** フィールドに、ユーザーの固有 ID を入力します。 ユーザー ID が必要です。  
4. **ユーザー名**フィールドに、ユーザー名を入力します。  
5. **ドメイン**フィールドに、ユーザーのドメインを入力します。  
6. **エイリアス**フィールドに、ユーザーのエイリアスを入力します。  
7. **法人**フィールドで、目的の会社を選択します。 
8. **ユーザーのロール**クイックタブで、**ロールの割り当て**を選択し、[ユーザーをセキュリティロールに割り当てます。](assign-users-security-roles.md)
9. **OK** を選択します。
10. **保存** を選択します。

## <a name="import-users"></a>ユーザーのインポート
1. アクション ウィンドウで、**ユーザーのインポート**を選択します。
2. 一覧で、選択された行をマークします。
3. **ユーザーのインポート**を選択します。
4. **閉じる**を選択します。

