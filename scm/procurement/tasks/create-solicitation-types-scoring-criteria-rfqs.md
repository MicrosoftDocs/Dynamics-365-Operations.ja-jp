--- 
title: "RFQ の入札タイプとスコア基準の作成"
description: "このガイドでは、入札タイプの作成、および入札タイプにスコア方法を関連付ける方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04f8cb1a6375be9371bca2af7e4044392ce7322b
ms.openlocfilehash: c77173c5dd9f0513de5d794f7453715ceff550da
ms.contentlocale: ja-jp
ms.lasthandoff: 08/02/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>RFQ の入札タイプとスコア基準の作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

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
4. [OK] をクリックします。
5. [スコア基準] をクリックします。
    * 表示されるスコア基準は、入札タイプに関連付けたスコア方法からなる基準です。 このページで基準を追加、または削除することもできます。 他のスコア方法から新しい基準をコピーして追加することも可能です。  
6. [コピー基準] をクリックします。
7. [スコア基準] フィールドで値を入力または選択します。
8. [OK] をクリックします。
9. ページを閉じます。


