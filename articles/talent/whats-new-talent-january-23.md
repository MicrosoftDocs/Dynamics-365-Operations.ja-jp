---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2019 年 1 月 23 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 135be837a82af8cee22d83c015a78da3b89b7978
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305096"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2019 年 1 月 23 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.2121**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="changes"></a>変更

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>新規固定報酬レコードの作成時に、従業員の固定報酬のインポートは機能しません
インポート時の報酬レベルを取得するために、従業員固定報酬のエンティティに変更が加えられました。 このリリースより前は、レベルが必要であることを示すメッセージが表示されていました。

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>休暇申請ダイアログ ボックスから最小残高フィールドを削除します
**最小残高**フィールドは、**休暇申請**ダイアログ ボックスから削除されました。 この変更は、休暇要求可能なすべての領域に影響します。

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>報酬レベルのデータ アップグレードはすべてのシナリオで更新されません
固定報酬プランの報酬レベルを更新するための変更が行われました。 この変更により、従業員に割り当てられたジョブの固定プランに対する報酬レベルが設定されます。

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>給与情報の変更ページではシステム管理者としてログインする時のみ使用できます
この変更により、給与管理者のロールを持つ従業員は、その職位の**変更のタイムライン > 変更の管理**ページ上の給与情報にアクセスできるようになります。

### <a name="job-fields-default-to-positions"></a>ジョブ フィールドを職位に設定
ある職位でジョブを変更すると、ジョブ フィールドはその職位に設定されます。 既定値をそのまま使用するか、またはそれらのフィールドの既存の値をそのまま使用するかを選択できるよう警告メッセージが表示されます。

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>猶予期間およびカレンダーは、将来採用される従業員には表示されません。
この変更により、**猶予期間**および**カレンダー** フィールドが**変更の管理**ページに追加され、将来および過去の従業員のデータデータ入力が可能になりました。

### <a name="platform-update-23"></a>プラットフォーム update 23
マイナーなバグ修正は、プラットフォーム更新プログラム 23 の一部として含まれています。 詳細については、[新機能および変更された機能 Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (1月2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23) を参照してください。 
