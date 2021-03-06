---
title: チーム カレンダーの作成
description: Dynamics 365 Human Resources でチームのカレンダーを表示および作成します。
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cedff4031c6455b446af9c56a770a00f3b2efc80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052100"
---
# <a name="view-team-and-company-calendars"></a>チームおよび会社のカレンダーの表示

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources でチームおよび会社のカレンダーを表示することができます。 チームのカレンダーは、階層行で定義されている直属の部下のみを表示します。

## <a name="view-your-team-calendar-as-an-employee"></a>チーム カレンダーを従業員として表示する

1. **従業員セルフサービス** ワークスペースで、**概要** 配下の **チーム休暇カレンダー** を選択します。

## <a name="view-your-team-calendar-as-a-manager"></a>チーム カレンダーをマネージャーとして表示する

1. **従業員セルフサービス** ワークスペースで、**自分のチーム** を選択します。

2. **休暇** を選択し、**休暇管理カレンダーの表示** を選択します。

マネージャーは、**自分のチームの保留中の休暇リクエスト**、**承認済休暇**、および **休暇申請** からチーム カレンダーにアクセスすることもできます。 

## <a name="view-a-company-calendar"></a>会社のカレンダーの表示

人事管理ロール内のユーザーは、会社のカレンダーを表示できます。 会社のカレンダーにはすべての従業員が表示されます。 既定では、カレンダーにはその日の日付に 28 日を加えた日付が表示されますが、日付範囲を変更することもできます。 また、**名前**、**個人番号**、および **休暇タイプ** で、カレンダーをフィルター処理することもできます。

1. **休暇** ワークスペースで、**リンク** を選択します。

2. **休暇カレンダー** を選択します。

人事管理ロールは、**休暇および欠勤申請**、**承認済休暇**、および **休暇申請** から会社のカレンダーにアクセスすることもできます。 

カレンダーには、追加のフィルターとオプションが含まれています。 すべてのカレンダーには、次の表示オプションがあります:

- 承認済の申請
- 保留中の要求数
- 休暇申請のある従業員
- 休暇申請のない従業員
- 従業員の誕生日
- 休暇申請 
- 休暇申請

休暇および欠勤パラメータのカレンダー コンフィギュレーションは、使用可能な表示オプションを決定します。

また、 マネージャーまたは部門でカレンダーをフィルター処理することもできます。 基本職位の割り当てによって、これらのフィルターが設定されたときに表示される従業員が決定します。 

>[!IMPORTANT]
>現在、会社全体の休暇と欠勤の表示はプレビューで表示します。 **サンドボックス** 環境で有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。<br><br>
>次に、**人事管理の共有パラメーター** で機能を有効にして、カレンダーに法人フィルターを表示する必要があります。 詳細については、[休暇および欠勤パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md) を参照してください。<br><br>
>カレンダーは、法人別にフィルター処理できます。 法人に関係なくすべての従業員を表示する場合は、[フィルター] ボックスのチェックを外し、[入力] を選択します。 

カレンダー設定の詳細については、[カレンダー パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md?configure-calendar-parameters) を参照してください。



[!INCLUDE[footer-include](../includes/footer-banner.md)]