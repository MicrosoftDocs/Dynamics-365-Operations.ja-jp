---
title: チーム カレンダーの作成
description: Dynamics 365 Human Resources でチームのカレンダーを表示および作成します。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6dffcb265030922e5134cfab1310027be43d87ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904162"
---
# <a name="view-team-and-company-calendars"></a>チームおよび会社のカレンダーの表示

>[!Important]
>この記事で説明した機能は、現在スタンドアロンの Dynamics 365 Human Resources の顧客が利用できます。 Finance のリリース 10.0.26 以降に、Finance インフラストラクチャの今後のリリースで、一部またはすべての機能を使用できます。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources でチームおよび会社のカレンダーを表示することができます。 チームのカレンダーは、階層行で定義されている直属の部下のみを表示します。

## <a name="view-your-team-calendar-as-an-employee"></a>チーム カレンダーを従業員として表示する

- **従業員セルフサービス** ワークスペースで、**概要** 配下の **チーム休暇カレンダー** を選択します。

## <a name="view-your-team-calendar-as-a-manager"></a>チーム カレンダーをマネージャーとして表示する

1. **従業員セルフサービス** ワークスペースで、**自分のチーム** を選択します。

2. **休暇** を選択し、**休暇管理カレンダーの表示** を選択します。

マネージャーは、**自分のチームの保留中の休暇リクエスト**、**承認済休暇**、および **休暇申請** からチーム カレンダーにアクセスすることもできます。 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>休暇マネージャーのカレンダーを休暇マネージャーとして表示する

> [!NOTE]
> 休暇マネージャーのカレンダーを表示するには、最初に **(プレビュー) 休暇マネージャー** を有効にし、機能管理における休暇機能を管理する必要があります。 プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md)を参照してください。

休暇マネージャー ロールのユーザーは、カレンダーにある休暇申請を確認できます。 以下の手順で、休暇カレンダーにアクセスします。

1. **従業員セルフ サービス** ワークスペースで、**休暇管理** を選択してから **休暇マネージャー カレンダー** を選択します。

2. **日付け** フィールドに希望する日付を入力します。

3. 必要に応じて表示オプションを更新します。

休暇マネージャー カレンダーには、休暇階層内の休暇マネージャーに報告する従業員のすべてのレコードが表示されます。

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

**休暇および欠勤パラメーター** のカレンダー コンフィギュレーションは、使用可能な表示オプションを決定します。

また、 マネージャーまたは部門でカレンダーをフィルター処理することもできます。 基本職位の割り当てによって、これらのフィルターが設定されたときに表示される従業員が決定します。 

> [!IMPORTANT]
> 機能管理で **会社間休暇ビュー機能** を有効にすることができます。 次に、**Human Resources の共有パラメーター** ページでこの機能を有効にして、カレンダーに法人フィルターを表示する必要があります。 詳細については、[休暇および欠勤パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md) を参照してください。
> 
> カレンダーは、法人別にフィルター処理できます。 法人に関係なくすべての従業員を表示するには、フィルター フィールドをクリアしてから、**入力** を選択します。 

カレンダー設定の詳細については、[カレンダー パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md?configure-calendar-parameters) を参照してください。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
