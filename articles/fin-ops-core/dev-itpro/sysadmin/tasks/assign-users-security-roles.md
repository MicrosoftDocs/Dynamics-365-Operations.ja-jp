---
title: ユーザーのセキュリティ ロールへの割り当て
description: Finance and Operations アプリにアクセスするには、ユーザーをセキュリティ ロールに割り当てる必要があります。
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180970"
---
# <a name="assign-users-to-security-roles"></a>ユーザーのセキュリティ ロールへの割り当て

[!include [task guide banner](../../includes/task-guide-banner.md)]

一般的な能力以外のものを使用する場合は、ユーザーがセキュリティ ロールに割り当てられている必要があります。 この手順では、業務データに基づいてシステム管理者がどのようにしてユーザーを自動的にロールに割り当てられるかについて説明します。 

## <a name="automatically-assign-users-to-roles"></a>ロールへのユーザーの自動割り当て
1. **ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる**に移動します。
2. ツリーで、「会計監修者」を選択します。 ルールを構成するロールを選択します。 この例では、会計監修者を選択します。 
3. **ルールの追加**をクリックして、ドロップ ダイアログを開きます。
4. **クエリの選択**一覧で、目的のレコードを見つけ、選択します。 このルールを使用するには、クエリを選択します。  
5. **メンバーシップ ルール名**一覧で、選択された行のリンクをクリックします。
6. **クエリの編集**をクリックします。 必要に応じてクエリを編集します。  
7. **OK**をクリックします。

## <a name="exclude-users-from-automatic-role-assignment"></a>自動ロール割り当てからのユーザーの除外
1. ページを閉じます。
2. **ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる**に移動します。
3. ツリーで、「会計監修者」を選択します。 ロールを選択します。 この例では、会計監修者を選択します。  
4. **ロールに割り当てられたユーザー** メニューで、**手動でのユーザーの割り当て/除外**を選択します。
5. **ユーザーをロールに割り当てる、またはユーザーをロールから除外する**の一覧で、選択された行をマークします。 ユーザーを選択します。  
6. **アクション ウィンドウ**で、**ロールから除外**を選択します。
    
    **ロールから除外**をクリックして、ロールから選択したユーザーを除外できます。 除外を削除するには、除外を削除するユーザーを選択して**ステータスのリセット**をクリックします。 ユーザーのステータスをリセットして除外を削除した場合、ユーザーのロールが再度自動的に割り当てられます。 ただし、ステータスをリセットした場合、ユーザーはすぐにロールに割り当てられたり、ロールから除外されません。 代わりに、ユーザーは自動ロール割り当てのルールが実行される次回にロールに割り当てられたり、ロールから削除されたりします。  
