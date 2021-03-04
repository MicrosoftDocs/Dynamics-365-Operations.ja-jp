---
title: プロセス ジョブのかんばんルールの変更
description: この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431693"
---
# <a name="change-kanban-rules-for-a-process-job"></a>プロセス ジョブのかんばんルールの変更

[!include [banner](../../includes/banner.md)]

この手順は、使用されているかんばんルールの指定されたかんばんへの変更を対象としています。 これは負荷リソースのレベルに、または故障の場合に便利です。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、リーン生産会社で働いていて、バリュー ストリームを担当するプランナーを対象としています。


## <a name="copy-kanban-rule"></a>かんばんルールのコピー
1. [かんばんルール] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * L0001 のイベントかんばんルール 000022 を選択します。  
3. [かんばんルールの複製] をクリックします。
4. [OK] をクリックします。

## <a name="change-kanban-rule"></a>かんばんルールの変更
1. ページを閉じます。
2. [かんばん作業のスケジューリング] に移動する。
3. 一覧で、選択された行をマークします。
    * かんばん 000177 の明細行を選択します。  
4. [代替かんばんルールの使用] をクリックします。
5. [次へ] をクリックします。
6. [かんばんルール] フィールドで、値を入力または選択します。
    * 先に作成されたかんばんルールを選択します。 これは、最大数のかんばんルールです。  
7. [完了] をクリックします。
    * ここでは、かんばん作業は別のかんばんルールを使用します。 これは負荷の作業セルのレベルに有用です。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]