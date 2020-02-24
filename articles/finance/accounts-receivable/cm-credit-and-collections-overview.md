---
title: 与信および回収の概要
description: このトピックでは、与信および回収の機能の概要を示します。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2fdfe05483d577819d64bdf7a4ebfe5d37cd414c
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015287"
---
# <a name="credit-and-collections-overview"></a>与信および回収の概要

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

顧客の与信限度額を管理し、必要に応じて回収活動を行うことができます。

## <a name="credit-management"></a>与信の管理

顧客の与信管理では、作成した与信ルールに基づいて、転記プロセスを通じて与信限度額の管理と販売注文のフロー制御を行うことができます。

与信管理プロセスには、次の手順のいずれかを含めることができます。

- 顧客の与信属性を更新して、顧客の与信価値に関する追加情報を提供します。
- 与信限度額調整を使用して、顧客の与信限度額を作成します。
- 与信限度額調整を使用して、顧客の一時的な与信限度額を作成します。 このように、業務上の要件に基づいて、顧客の与信限度額を一時的に増減することができます。
- 保険や保証に関する情報など、与信限度額に影響を与える可能性のある情報を追加します。
- 顧客間をリンクして 1 つの与信限度額を共有する顧客の与信グループを作成します。
- 顧客にリスク スコアを割り当てた後、スコアを使用して、与信限度額調整を通じて顧客の与信限度額を自動的に生成します。
- リスク、支払条件、与信限度額、期限切れ金額、使用された与信限度額の割合などの要因に基づいて、1 つ以上の転記プロセス中に注文を保留するブロック ルールを作成します。
- 保留中の販売注文の一覧を管理し、保留の理由を確認して、問題を軽減します。
- 販売注文をリリースして、転記プロセスを続けます。
- 与信限度額の変更と販売注文リリースの承認を管理するためのワークフローを設定します。

## <a name="collections-management"></a>回収管理

**回収**ページでは、売掛金勘定回収情報が管理される一元的な表示が提供されます。 回収マネージャーは、この一元的な表示を使用して回収を管理できます。 回収代行業者は、定義済の回収基準を使用して生成された顧客リスト、または**顧客**ページから回収プロセスを開始できます。

回収を設定または作業を開始する前に、次の概念を理解する必要があります:

- 顧客エイジング スナップショットには、特定の時点でのエイジングした残高の情報が含まれます。
- 回収の顧客プールを使用して、作業を整理することができます。
- 回収代行業者は、独自の顧客プールを使用できます。
- リスト ページには、回収の顧客、活動、およびケースが記載されます。
- 顧客の回収情報はすべて、1 つのページにまとめられ、そのページからアクションを実行できます。
- 1 つのステップで、利息や手数料を免除、再開、または取消をすることができます。
- 1 つのステップで、損金処理トランザクションを作成できます。
- 1 つのステップで、預金不足 (NSF) の支払を処理できます。

これらの概念の詳細については、[回収管理の主要概念](./cm-collections-concepts.md)を参照してください。

## <a name="additional-resources"></a>追加リソース

[顧客与信管理パラメーターの設定](./cm-credit-mgmt-setup.md)

[顧客与信管理の設定情報](./cm-setup-information.md)

[顧客の与信管理情報の追加](./cm-add-credit-mgmt-information-customer.md)

[顧客の与信グループ](./cm-customer-credit-groups.md)

[顧客の与信限度額調整](./cm-credit-limit-adjustments.md)

[販売注文の与信保留](./cm-sales-order-credit-holds.md)

[顧客与信管理の定期処理タスク](./cm-periodic-tasks.md)
