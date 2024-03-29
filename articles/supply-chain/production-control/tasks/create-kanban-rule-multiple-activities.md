---
title: 複数の活動のかんばんルールの作成
description: この手順では、生産フローの複数の活動を含むかんばんルールを作成する方法を示します。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f55034f4f0557023ce0c659c1e8258214cf8bfa3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569242"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>複数の活動のかんばんルールの作成

[!include [banner](../../includes/banner.md)]

この手順では、生産フローの複数の活動を含むかんばんルールを作成する方法を示します。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、リーン環境で新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。


## <a name="create-a-new-kanban-rule"></a>新しいかんばんルールの作成
1. [製品情報管理] > [リーン生産] > [かんばんルール] の順に移動します。
2. [新規] をクリックします。
3. [補充方法] フィールドで、「スケジュール済」を選択します。
4. [最初の計画活動] フィールドで、値を入力または選択します。
    * SpeakerAssemblyAndPolish を選択します。  
5. [複数の活動] チェック ボックスをオンにします。
    * 目的はかんばんルールに複数の活動を含むことです。 最後の計画の活動を選択すると、生産フローのパスを選択します。  
6. [最後の計画活動] フィールドで、値を入力または選択します。
    * 「SpeakerTestAndPackaging」を選択します。 値を選択した後、ページが自動的に開きます。 かんばんフローの SpeakerAssemblyAndPolish > SpeakerTestAndPackaging を選択します。 [OK] をクリックします。  
7. [詳細] セクションを展開します。
8. [製品] フィールドで、値を入力または選択します。
    * 品目 L0006 を選択します。  

## <a name="create-kanban-and-view-jobs"></a>かんばんの作成およびジョブの表示
1. [かんばん] セクションを展開します。
2. [追加] をクリックします。
3. [新しいかんばんの数] フィールドに「1」を入力します。
    * これで 1 つのかんばんが作成されます。  
4. 製品数量を「3」と設定します。
    * かんばんは 3 つの製品を処理します。  
5. [期限日時] フィールドに日時を入力します。
    * [今日] を入力できます。  
6. [作成] をクリックします。
7. [詳細] をクリックします。
    * かんばんには生産フローの 2 つのプロセス ジョブが含まれています。 1 番目は SpeakerAssemblyAndPolish で、2 番目は SpeakerTestAndPackaging です。  
    * これは最後のステップです!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]