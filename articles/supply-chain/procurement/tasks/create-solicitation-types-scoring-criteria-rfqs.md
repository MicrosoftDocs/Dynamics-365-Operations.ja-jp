---
title: RFQ の入札タイプとスコア基準の作成
description: このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40625152a579bb269411d026d77d449902c8d4bc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016809"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>RFQ の入札タイプとスコア基準の作成

[!include [banner](../../includes/banner.md)]

このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。 さらに見積依頼 (RFQ) で入札タイプを使用し、既定のスコア方法を設定する方法も示します。 通常、これらのタスクを実施するのは、購買マネージャーです。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。 開始する前に、使用可能なスコア方法を設定する必要があります。


## <a name="create-a-solicitation-type"></a>入札タイプの作成
1. [調達] > [設定] > [見積依頼] > [入札タイプ] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [スコア方法] フィールドで、この入札タイプに使用するスコア方法を選択します。
6. [保存] をクリックします。
7. ページを閉じます。

## <a name="use-the-solicitation-type"></a>入札タイプの使用
1. [調達] > [見積依頼] > [すべての見積依頼] の順に移動します。
2. [新規] をクリックします。
3. [入札タイプ] フィールドで、作成した入札タイプを選択します。 
    *   
4. [OK] をクリックします。
5. [スコア基準] をクリックします。
    * 表示されるスコア基準は、入札タイプに関連付けたスコア方法からなる基準です。 このページで基準を追加、または削除することもできます。 他のスコア方法から新しい基準をコピーして追加することも可能です。  
6. [コピー基準] をクリックします。
7. [スコア基準] フィールドで値を入力または選択します。
8. [OK] をクリックします。
9. ページを閉じます。

