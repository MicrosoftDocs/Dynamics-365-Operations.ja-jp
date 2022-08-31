---
title: ライフ イベントの変更の処理
description: この記事では、Microsoft Dynamics 365 Human Resources でライフ イベントの変更を処理する方法について説明します。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3d8fbe0270606688944b4465cb5846b8c8f9900
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323505"
---
# <a name="process-life-event-changes"></a>ライフ イベントの変更の処理

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

2 つのライフ イベント変更における Microsoft Dynamics 365 Human Resourcesのライフ イベント 変更の処理:

- 誕生日の変更
- 適格性ルールにより、有効期限の変更をオーバーライドする 

1. **給付金管理** ワークスペースにて、**処理** の下の **ライフ イベントの変更処理** を選択します。

2. **ライフ イベントの変更処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 登録期間 | ライフ イベントを処理する登録期間が変更されます。 |
   | 法人エンティティ | ライフ イベントを処理する法人が変更されます。 |

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
