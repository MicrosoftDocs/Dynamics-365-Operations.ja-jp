---
title: 交換するかんばんルールの作成
description: この手順では、既存のかんばんルールを特定日付の新しいかんばんルールに置き換えることを対象としています。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae589f81811c1586e0e24de94eaf5f467f19debb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210873"
---
# <a name="create-a-replacement-kanban-rule"></a>交換するかんばんルールの作成

[!include [banner](../../includes/banner.md)]

この手順では、既存のかんばんルールを特定日付の新しいかんばんルールに置き換えることを対象としています。 これは、生産フローの変更または補充ルールを調整およびスケジューリングする必要がある場合に役立ちます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、変更された生産フローまたは新しい補充ルールに対する生産を準備しているプロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。 このタスクは、新しいルールでかんばんルール 000022 を交換し、新しいルールについて最大数量を 48 から 100 に増加させます。


## <a name="select-a-kanban-rule-to-replace"></a>置換するかんばんルールを選択します。
1. [かんばんルール] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * かんばんルール 000022 を選択します。  

## <a name="create-a-replacement-kanban-rule"></a>交換するかんばんルールの作成
1. かんばんルールの置換をクリックします。
2. [有効日] フィールドに日時を入力します。
    * 今から 1 週間など、将来の日付を選択します。 これは、新しいかんばんルールが有効になり、古いかんばんルールを置き換える日付と時刻です。  
    * かんばんルールが生産フローのパスを変更する場合は、別の活動を選択できます。  この手順では、活動をそのままの状態にします。  
3. [OK] をクリックします。
    * 新しいかんばんルールを作成すると、かんばんルール 000022 が置換されることに注意してください。  
    * 有効日は、選択した日付に従ってかんばんルールを置き換える場合に設定されます。  
4. 一覧で、目的のレコードを見つけ、選択します。
    * 置換されたかんばんルール 000022 を選択します。  
    * 置換されたかんばんルールが有効期限と同じ日付をもつと、これが切れる日付であることに注意してください。  
5. 一覧で行 1 を選択します。
    * リストの先頭にある新しいかんばんルールを選択します。 これは、最大かんばん番号のかんばんルールです。  
6. 一覧で、選択された行のリンクをクリックします。
    * かんばんルールを開くには、かんばんルール番号をクリックします。  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>交換するかんばんルールの最大数量の変更
1. 最大数量を「100」に設定します。
    * Quantities FastTab を展開して、Maximum quantity field を確認します。 100 に最大数量を変更すると、100 のかんばんが処理されるようになります。    これは、このタスクの最後のステップです。  

