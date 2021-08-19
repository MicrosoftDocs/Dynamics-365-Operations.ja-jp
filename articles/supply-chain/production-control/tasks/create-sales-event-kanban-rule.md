---
title: 販売イベントかんばんルールの作成
description: この手順は、販売注文の作成時に発生するかんばんルールを作成するのに必要な設定を対象としています。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ed9df21e37a963d3f7dd22f111270ac3069463ba2a0592b8133cef919567f78
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751844"
---
# <a name="create-a-sales-event-kanban-rule"></a>販売イベントかんばんルールの作成

[!include [banner](../../includes/banner.md)]

この手順は、販売注文の作成時に発生するかんばんルールを作成するのに必要な設定を対象としています。 かんばんルールのイベントは、販売注文明細行に基づいて必要量を補充します。 この手順の作成に使用するデモ データの会社は USMF です。 これは、新しい製品または変更された製品の生産を準備している、プロセス エンジニアまたはバリュー ストリームのマネージャーを対象としています。




## <a name="create-a-new-kanban-rule"></a>新しいかんばんルールの作成
1. [かんばんルール] に移動します。
2. [新規] をクリックします。
3. [補充方法] フィールドで、「イベント」を選択します。
    * [イベント] を選択すると、かんばんルールは、たとえば販売注文明細行の作成といったイベントによってトリガーされることになります。   これは、各かんばんが特定の需要を満たす必要がある領域に適用されます。  
4. [最初の計画活動] フィールドで、値を入力または選択します。
    * [最終アセンブリ] を選択します。  
5. [詳細] セクションを展開します。
6. [製品] フィールドで、値を入力または選択します。
    * [L0050] を選択します。  

## <a name="define-an-event"></a>イベントの定義
1. [イベント] セクションを展開します。
2. [販売イベント] フィールドで、「自動」を選択します。
    * 販売イベントの [自動] を選択すると、このかんばんルールは、販売明細行が製品および受入場所に一致すると自動的に発生します。 この手順では、倉庫 13 の製品 L0050 です。  
3. [最小イベント数量] を「50」に設定します。
    * 最小イベント数量が 50 の場合、かんばんルールは、イベントが 50 またはそれ以上の数量の場合にだけ発生します。  
4. [生産フロー] セクションを展開します。
    * 受入場所が倉庫 13 であることに注目してください。 これは、このかんばんルールがこの場所に対して発生されることを意味します。  
    * この例では、製品 L0050 の販売明細行、数量 50 以上、倉庫 13、によりこのかんばんルールが発生します。  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>イベントかんばんルールをトリガーする販売明細行の作成
1. [すべての販売注文] に移動します。
    * かんばんルールが保存されたときに警告が表示されます。これは販売注文作成中にリアルタイムでかんばんが作成されることを意味します。  
2. [新規] をクリックします。
3. [顧客口座] フィールドで値を入力または選択します。
    * たとえば、[US-003] を選択します。  
4. [OK] をクリックします。
5. [品目番号] フィールドに、'L0050' を入力します。
6. [サイト] フィールドで、「1」と入力します。
    * [倉庫 13] が [サイト 1] にあるために、[サイト 1] を選択します。  
7. [倉庫] フィールドで、値を入力または選択します。
    * [倉庫] を 13 に設定します。  
8. 数量を '75' に設定します。
    * 作成されたかんばんルールを発生させるために、50 以上の数量を入力します。  

## <a name="verify-that-kanban-is-created"></a>かんばんが作成されていることの確認
1. [製品と供給] をクリックします。
2. [ペギング ツリーの表示] をクリックします。
    * 販売明細行と同じ数量のかんばんが作成されることを確認します。 製品 L0050 を生産するのに必要な原材料の問題も確認できます。 これは、この手順の最後のステップです。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]