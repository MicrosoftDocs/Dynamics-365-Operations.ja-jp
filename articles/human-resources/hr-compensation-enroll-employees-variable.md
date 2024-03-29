---
title: 変動報酬プランへの従業員の登録
description: 報酬および福利厚生マネージャーは、従業員の現金および現金以外の報奨を計算する変動報酬プランに従業員を登録できます。
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11f86bfa4bfcece164755bb5d86944e0bed0fff2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692285"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>変動報酬プランへの従業員の登録


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

報酬および福利厚生マネージャーは、従業員の現金および現金以外の報奨を計算する変動報酬プランに従業員を登録できます。 この手順は、変動報酬プランが **登録を有効にする** フィールドで、**はい** を設定することによって作成され、適格性ルールが変動報酬プランに対して作成されていることを前提にしています。 この手順の作成に使用するデモ データの会社は USMF です。 この手順を開始するには、**人事管理** > **作業者** > **従業員** > **報酬** > **変動プラン登録** の順に移動します。

1. **新規** をクリックします。
2. **計画** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * [プラン] ルックアップでは、従業員は適格性ルールに基づいて適格となる変動報酬のみが表示されるようにフィルタ処理されるようになります。  
3. 一覧で、選択された行のリンクをクリックします。
4. **一般** セクションの展開を切り替えます。
5. **有効日** フィールドに日付を入力します。
6. **保存** をクリックします。
7. **上書き** セクションの展開を切り替えます。
    * 選択された変動プランが割合である場合、採用ルールの日付は、従業員の採用日付を上書きするように、必要に応じて設定できます。  
    * 変動プランがある基となるプランのパーセンテージである場合、従業員の報奨率は上書きされます。 変動報酬計画が単位数計画である場合、従業員の単位数は上書きされます。  
    * 従業員に一律の報酬量を与えられれば、金額はここで設定できます。  
8. **組織の上書き** セクションの展開を切り替えます。
    * 従業員の業績を考慮に入力すると、さまざまな部門のパフォーマンス、または従業員の職位に割り当てられた部門以外の部門は、部門上書きできます。 **割合** の列は合計を 100 とする必要があります。  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
