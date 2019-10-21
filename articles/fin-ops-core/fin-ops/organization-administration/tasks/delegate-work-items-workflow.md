---
title: ワークフローの作業項目をデリゲート
description: 事務所を不在にする予定がある場合や、作業項目を処理できない場合は、自分の作業項目を他のユーザーに委任 (再割り当て) することができます。
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189962"
---
# <a name="delegate-work-items-in-a-workflow"></a>ワークフローの作業項目をデリゲート

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>作業項目の手動委任

個別の作業項目を委任するには、**ワークフロー**メニューの**委任**オプションを選択し、コメントとともに委任されるユーザーを入力します。 これにより、作業項目がユーザーに再度割り当てられ、完了させることができます。

## <a name="automatically-delegate-work-items"></a>作業項目を自動的に委任

不在であることを計画している場合、またはその他の方法で一定期間作業項目に対処できない場合、**ユーザー オプション**ページにて、他のユーザーに新しい作業項目を自動的に委任することができます。

### <a name="set-up-automatic-delegation"></a>自動委任の設定
1. **共通 > 設定 > ユーザー オプション**の順に移動します。
2. **ワークフロー** タブをクリックします。通知セクションが展開されていることを確認します。 他のユーザーに作業項目を自動的に委任するようにシステムをコンフィギュレーションするには、委任ルールを作成して、特定のタイプの作業項目についてその委任条件を指定する必要があります。 委任ルールを作成するには、次の手順に従います。  
3. **追加**をクリックします。
4. **スコープ** フィールドで、オプションを選択します。
    - [すべて] – 割り当てられているすべての作業項目を委任します。
    - [モジュール] – 特定のタイプのワークフローに関連する作業項目のみをデリゲートします。 このオプションを選択する場合は、[名前] フィールドでワークフローのタイプを選択する必要があります。
    - [ワークフロー] – 特定のワークフローに関連する作業項目のみをデリゲートします。 このオプションを選択する場合は、[名前] フィールドでワークフローを選択する必要があります。  
5. **デリゲート** フィールドで、作業項目をデリゲートするユーザーを選択します。 作業項目をいつ委任するかを指定するためには [開始日時] と [終了日時] フィールドを使用します。  
6. **開始日時**フィールドで、日付と時刻を入力します。
7. **終了日時**フィールドに日時を入力します。
8. **有効**チェック ボックスをオンにして、委任ルールを有効化します。 **モジュール**を範囲として選択した場合は、名前フィールドでモジュールを選択する必要があります。 **ワークフロー**を範囲として選択した場合は、特定のワークフローを選択して名前フィールドでデリゲートする必要があります。  
9. **コメント** フィールドに、作業項目を委任する理由を説明するコメントを入力します。

