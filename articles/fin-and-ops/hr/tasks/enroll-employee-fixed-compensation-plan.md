--- 
title: "固定報酬プランへの従業員の登録"
description: "報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。"
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88630311a4326508fa69a8938fa216f1a45ba089
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>固定報酬プランへの従業員の登録

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。 この手順は、固定プランが作成され、有効となり、適格性ルールが計画に対して設定されることを前提としています。 この手順の作成に使用するデモ データの会社は USMF です。 手順を開始するには、[人事管理] > [作業者] > [従業員] > [報酬] > [固定プラン] の順に移動します。

1. [新規] をクリックします。
2. [アクション] フィールドに、従業員の報酬の変更について説明する雇用/再雇用型の [固定報酬アクション] を選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [配置] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
    * 表示されているレベルは、職位におけるジョブの報酬レベルです。 報酬は、従業員に割り当てる前に、ジョブに設定する必要があります。  
6. [プラン] フィールドで、従業員の固定報酬プランを選択します。 [計画] ルックアップでは、従業員は適格性ルールに基づいて適格となるプランのみが表示されるようにフィルタ処理されます。
7. 一覧で、目的のレコードを見つけ、選択します。
    * 報酬の発効日と有効期限における既定値は、作業者職位の割り当て開始日および終了日から取得されます。 必要に応じて、これらの日付を調整できます。  
    * 固定報酬プランがステップ計画である場合、従業員に対する正しい支払いレートを含む手順を選択します。 固定報酬プランが段階的またはバンド プランである場合、従業員に対する正しい支払いレートを入力します。 支払レートは、計画の許容設定およびジョブの報酬レベルの最小または最大基準点に対して検証されます。  
8. [OK] をクリックします。


