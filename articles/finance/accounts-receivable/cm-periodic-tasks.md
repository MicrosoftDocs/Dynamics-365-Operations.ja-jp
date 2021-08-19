---
title: 定期的な与信管理タスク
description: このトピックでは、顧客の与信限度額を管理するために必要なプロセスの一部である定期処理タスクについて説明します。
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f6b04c28c0f7b5e4d58d464ad45d42478cde4e0ffb584e5afa43c99ebaed7166
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724018"
---
# <a name="periodic-credit-management-tasks"></a>定期与信管理タスク

[!include [banner](../includes/banner.md)]

このトピックでは、顧客の与信限度額を管理するために必要なプロセスの一部である定期処理タスクについて説明します。

## <a name="update-risk-scores"></a>リスク スコアの更新

企業の進化や状況の変化に応じて、特定の顧客に対する与信リスクも変更する可能性があります。 顧客に対して適切な与信限度額を維持するには、各リスク スコアの基準を定期的に確認し、各顧客のスコアを更新する必要があります。 **リスク スコアの更新** ページを使用して、次のスコアを更新することができます (**与信および回収\>定期処理タスク\>与信管理\>リスク スコアの更新**)。 すべてのユーザー定義計算も処理されます。

- **平均支払日数** - このスコアは、顧客が請求書の支払に要する平均日数です。
- **初回購入** - このスコアは、顧客が組織の顧客であった年数を示します。
- **業務年数** - このスコアは、顧客が業務を行った年数です。 **顧客** ページの **業務開始** フィールドの値が使用されます。
- **売掛債権回転日数** - このスコアは、売掛金勘定残高、売上収益、および過去 12 か月間の日数に基づいて計算されます。
- **平均残高** - このスコアは、過去の 12 か月間の売掛金勘定残高に基づいて計算されます。
- **与信管理グループ**、**アカウント ステータス**、および **国** - これらのスコアは、顧客からの情報を使用します。

## <a name="update-customer-balance-statistics"></a>顧客残高統計の更新

**顧客残高統計** の更新プロセスを実行すると、**残高統計の照会** ページに表示される残高統計の計算を更新できます。 この情報は、リスクのスコアと、**顧客** ページの与信統計情報ボックスに表示される値を計算するために使用されます。

プロセスを実行すると、単一の顧客の顧客残高統計が更新されます。 複数の顧客に対してプロセスを実行するバッチ ジョブを設定するには、**残高統計の計算** ページ (**与信管理\>定期処理のタスク\>残高統計の計算**) を使用します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]