---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 10 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305210"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 9 月 10 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.138.0**

このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>休暇申請で特定の時刻を許可 (半日数)

休暇を日数で申請できるよう休暇および欠勤を設定する場合、半日の定義も有効化できるようになります。 その後、ユーザーが休暇申請を送信するときに、一日の前半または後半に休暇申請しているのかを指定できます。

既定では、このオプションは無効になっています。 一日の前半または後半に休暇申請する従業員については、人事管理パラメータの**休暇と欠勤**区分でこのオプションを有効にする必要があります。

この機能のセキュリティ権限は、人事管理パラメーターの管理にあります。

## <a name="validation-of-leave-and-absence-entries"></a>休暇と欠勤エントリの検証

休暇の構成方法により、各自の作業日よりも長い休暇申請を送信しようとするする従業員には、警告メッセージが表示されます。 つまり、特定の日に全日以上の休暇を取ろうとすると、警告が表示されます。

この検証は常に有効になっています。 従業員が定義された日のしきい値を超えるたびに、休暇申請の警告を受け取ります。

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>ワークフローの条件付きステートメントの追加フィールド

追加のフィールドが、Core HR でいくつかのワークフローの条件付きステートメントおよびプレースホルダーに追加されました。

次のフィールドが、報酬、退職、および移動ワークフローに追加されました。

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- 配置
- 結合
- 部門
- PositionType
- CompLocation
- 肩書き
- 職務
- JobType
- JobFamily
- JobFunction

次のフィールドが職位ワークフローに追加されました。

- 配置
- 結合
- 部門
- PositionType
- CompLocation
- 肩書き
- 職務
- JobType
- JobFamily
- JobFunction

条件付きステートメントおよびプレースホルダーのフィールドは、前述のワークフローのコンフィギュレーションにアクセスできるすべてのユーザーが利用できます。

## <a name="navigation-to-attract-from-personnel-management"></a>人事管理から Attract への移動

人事管理では、Attract が設定されていない場合、"ここに表示する情報が見つかりませんでした。" というメッセージを表示する代わりに、**採用候補者**セクションで Attract の使用を開始するようユーザーに指示します。

## <a name="other-changes"></a>その他の変更

このリリースには、いくつかの追加のバグ修正が含まれています。

- 契約社員の雇用時には、**報酬**タブは要求/アクション ページで使用できないようにする必要があります。
- 退職申請プロセス中には、すべての必須フィールドにデータが入力されるまで続行できません。
- 人事管理分析上の並べ替え順序と日付表示の問題は、解決されました。
