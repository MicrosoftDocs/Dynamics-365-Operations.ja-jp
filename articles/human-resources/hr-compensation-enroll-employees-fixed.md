---
title: 固定報酬プランへの従業員の登録
description: 報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc8373a4a39a1a212ab445b2b300fbddfe0e4a39
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113271"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>固定報酬プランへの従業員の登録

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

