---
title: 固定報酬プランへの従業員の登録
description: 報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688744"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>固定報酬プランへの従業員の登録


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。 この手順は、固定プランが作成され、有効となり、適格性ルールが計画に対して設定されることを前提としています。 この手順の作成に使用するデモ データの会社は USMF です。 手順を開始するには、**人事管理** > **作業者** > **従業員** > **報酬** > **固定プラン** の順に移動します。

1. **新規** をクリックします。
2. **アクション** フィールドに、従業員の報酬の変更について説明する **雇用/再雇用型** の固定報酬アクションを選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. **職位** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
    * 表示されているレベルは、**職位** に割り当てられている **ジョブ** の **報酬** FastTab > **レベル** フィールドを参照しています。 報酬は、従業員に割り当てる前に、ジョブに設定する必要があります。  
6. **プラン** フィールドで、従業員の固定報酬プランを選択します。 **計画** 検索では、**適格性ルール** に基づいて適格となるプランのみが表示されるようにフィルター処理されます。
7. 一覧で、目的のレコードを見つけ、選択します。
    * 報酬の **発効日** と **有効期限** の既定値は、作業者の職位の割り当て開始日および終了日から取得されます。 必要に応じて、これらの日付を調整できます。  
    * 固定報酬プランがステップ計画である場合、従業員に対する正しい支払いレートを含む手順を選択します。 固定報酬プランが段階的またはバンド プランである場合、従業員に対する正しい支払いレートを入力します。 支払レートは、計画の許容設定およびジョブの報酬レベルの最小または最大基準点に対して検証されます。  
8. **OK** をクリックします。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
