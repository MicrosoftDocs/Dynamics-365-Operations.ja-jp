---
title: h本社で顧客操作の同期を監査する
description: この記事では、サイトユーザーの問題を修正するのに役立つ Microsoft Dynamics 365 Commerce headquarters での顧客操作の同期を監査する方法について説明します。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691089"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>h本社で顧客操作の同期を監査する

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事では、サイトユーザーの問題を修正するのに役立つ Microsoft Dynamics 365 Commerce headquarters での顧客操作の同期を監査する方法について説明します。

組織で顧客を非同期に作成および編集する機能が採用され始める中、サイト管理者は、サイト ユーザーの要求またはプロセスの失敗に基づいて、操作を表示およびトラブルシューティングする方法が必要になります。 このような場合は、サイト管理者がセルフサービス モデルを使用して、顧客の作成と操作の編集を監査し、失敗を修正できる必要があります。

## <a name="customer-synchronization-status"></a>顧客の同期の状態

顧客管理の非同期モードとその対応する機能をオプトインした場合、Commerce headquarters の管理者は、**P-ジョブ**、**非同期モードからの顧客とビジネス パートナーの同期** ジョブ、**1010** ジョブの定期的なバッチ ジョブを作成およびスケジュールする必要があります。これにより、非同期顧客が Commerce headquarters で同期顧客に変換されます。 顧客管理操作の同期は、これらのジョブが実行されるたびに行われます。 詳細については、[顧客作成モードを非同期化する](async-customer-mode.md) を参照してください。

ビジネス所有者は、次の操作を実行できます。

- サイト ユーザーのすべての作成/編集操作を表示します。 詳細には、ステータスやタイム スタンプが含まれます。
- 顧客テーブルのフィールドおよび値を使用して監査ログを絞り込み、操作をフィルタ処理します。
- ステータスの詳細と共に変更の簡単な説明を表示して、高レベルの運用について理解します。
- 失敗の場合は、問題のあるフィールドを編集および修正し、特定の顧客操作を保存して同期します。

### <a name="elements-on-the-customer-synchronization-status-page"></a>顧客同期ステータス ページの要素

すべての非同期操作のリストを表示するには、Commerce Headquarters で **Commerce と Retail \> 顧客 \> 顧客同期ステータス** に移動します。 次の図は、**顧客同期ステータス** ページの例を示しています。

![Commerce Headquarters の顧客同期ステータス ページ。](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

既定では、**顧客同期ステータス** ページの左側の顧客同期操作の一覧に次の列が表示されます。

- チャネル名
- 顧客アカウント
- 非同期の顧客アカウント
- 操作のタイムスタンプ
- 顧客の同期ステータス

ページの右上隅には、**顧客勘定**、**小売の同期操作**、**顧客の同期ステータス**、**既知の前回のエラー** の値などの顧客勘定の詳細が表示されます。

**変更の説明** セクションには、実行された顧客管理操作のタイプ (顧客作成、勘定の更新、同期に失敗した詳細など) の説明が含されます。

**顧客属性** セクションには、すべての顧客属性と、古い値と新しい値を示すグリッドが表示されます。 このセクションは、変更した顧客属性値を変更して修正プログラムを修正し、再度同期する場合に、このセクションを編集できます。
