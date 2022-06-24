---
title: レート変更の処理
description: この記事では、Microsoft Dynamics 365 Human Resources で給付金レートの変更を処理する方法について説明します。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09714c70cb00b1a1b5dbd4613bbd70ff11d35cb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882956"
---
# <a name="process-rate-changes"></a>レート変更の処理


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、新規または既存の給付金プランが適格性ルール設定に変更がある場合、Microsoft Dynamics 365 Human Resources で給付金レートの変更を処理する方法について説明します。 新しい適格性ルールが作成されてプランに割り当てられる場合、新しい適格性オプションに基づいて作業者はプランが適格な状態になっているかどうかをチェックするために、システムが作業者の適格性を再実行するように求められます。 

1. **給付金管理** ワークスペースにて、**処理** の下の **レート変更の更新処理** を選択します。

2. **給付金レートの更新処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **登録期間** | レート変更を処理する登録期間。 |

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
