---
title: タスク記録のセキュリティ診断
description: この記事では、タスクの記録に基づいてセキュリティ許可要件を分析して管理する方法について説明します。
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272523"
---
# <a name="security-diagnostics-for-task-recordings"></a>タスク記録のセキュリティ診断

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>準備

この記事では、タスクの記録に基づいてセキュリティ許可要件を分析して管理する方法について説明します。 この記事のステップを完了する前に、分析する業務プロセスのタスク記録を保持している必要があります。 業務プロセスを記録するには、[タスクレコーダーのリソース](../../user-interface/task-recorder.md)を参照してください。 

## <a name="manage-security-for-a-task-recording"></a>タスク記録のセキュリティ管理

1. **システム管理** > **セキュリティ** > **タスク記録のセキュリティ診断** に移動します。
2. その場所からタスクの記録を開きます。 **この PC から開く** または **Lifecycle Services から開く** を選択し、続いて **閉じる** を選択します。
3. これにより、**セキュリティ メニュー項目の詳細** ページが開きます。このページには、プロセスに必要なセキュリティ オブジェクトの一覧が表示されます。

 > [!NOTE]
 > **アクション** と **出力** のメニュー項目は、一覧には含まれません。

4. **ユーザー ID** フィールドでユーザー を選択します。 ユーザーが一部のメニュー項目に対するアクセス許可を持っていない場合、**不足しているアクセス許可** フィールドが **はい** に更新されます。
  
  ![セキュリティ メニュー項目の詳細ページ。](../media/Security-Menu-Item-Details.png)

5. **参照の追加** を選択すると、欠落して いるアクセス許可を付与するロール、職務、特権などのセキュリティ オブジェクトの一覧が表示されます。
6. リストからセキュリティ オブジェクトを選択します：

    - **ロール** を選択した場合は 、**ユーザーへの役割の追加** を選択します。 **ロールにユーザーを割り当てる** ページが表示され ます。 詳細については、[ユーザーにセキュリティ ロールへを割り当てる](assign-users-security-roles.md)ページを参照してください。
    - **職務** を選択した場合は、**ロールに職務を追加する** を選択し、職務を追加するロールを選択して、**OK** を選択します。
    - **権限** を選択した場合は、**職務に権限を追加する** を選択し、権限を追加する職務を選択して、**OK** を選択します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
