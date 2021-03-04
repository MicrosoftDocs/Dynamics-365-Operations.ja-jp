---
title: 引き取りかんばんルールの作成
description: この手順は、リーン環境で材料を転送する引き取りかんばんルールを作成するために必要な設定を表示します。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 963a6dce8affc23f001dcb04219821ceff3a2d92
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431672"
---
# <a name="create-a-withdrawal-kanban-rule"></a>引き取りかんばんルールの作成

[!include [banner](../../includes/banner.md)]

この手順は、リーン環境で材料を転送する引き取りかんばんルールを作成するために必要な設定を表示します。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、新しい材料または変更された材料の補充を準備している、プロセス エンジニアまたはバリュー ストリーム マネージャーを対象としています。


## <a name="create-new-kanban-rule"></a>新しいかんばんルールの作成
1. [かんばんルール] に移動します。
2. [新規] をクリックします。
3. [タイプ] フィールドで、「引き取り」を選択します。
    * 引き取りタイプは、材料や商品を転送するためのかんばんルールに使用されます。  
4. [最初の計画活動] フィールドで、値を入力または選択します。
    * ReplenishSpeakerComponents を選択します。   この活動は倉庫 11、場所 11 から倉庫 12、および場所 12 へコンポーネントを移動するように設定されています。  
5. [製品] フィールドで、値を入力または選択します。
    * M0007 を選択します。  
6. [リード タイム] フィールドで、数値を入力します。
    * たとえば、60 です。  
7. [計量単位] フィールドで、値を入力または選択します。
    * たとえば、分単位です。  

## <a name="set-quantities-for-kanban"></a>かんばんの数量を設定します。
1. 既定の数量を「5」に設定します。
    * これは、かんばんごとに転送される数量です。  
2. [固定かんばん数量] フィールドで、「2」を入力します。
    * これは有効にするかんばんの量です。 この場合、2 つのかんばんが、それぞれ 5 つずつ転送します。  
3. [下限値に対する警告] フィールドで、「1」を入力します。
    * 出荷先にあるべきすべてのかんばんの最小数量を追跡するために使用されます。 たとえば、これはかんばんの数量の概要に使用されます。  
4. [上限値に対する警告] フィールドで、「2」を入力します。
    * 出荷先にあるべきすべてのかんばんの最大数量を追跡するために使用されます。 たとえば、これはかんばんの数量の概要に使用されます。  

## <a name="create-kanbans"></a>かんばんの作成
1. [保存] をクリックします。
    * かんばんルールは、かんばんを作成する前に保存する必要があります。  
2. [追加] をクリックします。
    * 提示された「新しいかんばんの数」が 2 であるために、有効なかんばんはないことに注意してください。これは「固定かんばん数量」と等しくなります。  
3. [作成] をクリックします。
    * これは、2 つのかんばんを作成します。  
    * この引き取りかんばんルールのために、それぞれ 5 つずつに対し 2 つのかんばんが作成されたことに注意してください。  これは、この手順の最後のステップです。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]