---
title: 倉庫の在庫レベルの調整 (基本倉庫)
description: この手順では、倉庫にある製品の在庫レベルを調整するために、在庫調整仕訳帳を作成して転記するプロセスを説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 450e95d8a4d5a216b84a3c944c6c63b4a8ad10c5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838826"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>倉庫の在庫レベルの調整 (基本倉庫)

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、倉庫にある製品の在庫レベルを調整するために、在庫調整仕訳帳を作成して転記するプロセスを説明します。 これを開始する前に、在庫調整用の在庫仕訳帳名を設定してある必要があります。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 通常、これらのタスクを実施するのは、倉庫の従業員です。


## <a name="create-an-inventory-adjustment-journal"></a>在庫調整仕訳帳の作成
1. [在庫管理] > [仕訳入力] > [品目] > [在庫調整] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、使用する在庫調整仕訳帳の名前をクリックします。
    * 他の一部のフィールドは、選択した在庫調整仕訳帳の名前の設定に基づいて設定されます。  
5. [OK] をクリックします。

## <a name="create-journal-lines"></a>仕訳帳明細行の作成
1. [新規] をクリックします。
2. 一覧で、品目番号フィールドをマークします。
3. [品目番号] フィールドで、品目を選択します。 デモ データの会社 USMF を使用する場合は、「D0001」を入力します。
4. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧でサイトを選択します。
6. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で倉庫を選択します。
    * 必須分析コードとして場所を持つ品目を選択した場合は、ここで場所を指定する必要があります。  
8. [数量] フィールドに数値を入力します。
    * 原価価格のフィールドには、在庫入庫用に単位あたりの原価を指定します。 品目番号に対して原価が指定されていない場合、または原価を手動で変更する場合は、ここでそれを行います。  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>在庫調整仕訳帳の検証および転記
1. [検証] をクリックします。
2. [OK] をクリックします。
3. [転記] をクリックします。
    * この種の仕訳帳を転記すると、在庫入庫または在庫出庫が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。  
4. [OK] をクリックします。
5. フォームを閉じます。
6. ページを閉じます。

