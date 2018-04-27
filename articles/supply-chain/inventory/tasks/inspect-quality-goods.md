---
title: "商品の品質の調査"
description: "この手順では、品質指示を処理する方法を説明します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeed7eab750c606ea0009fa7c51baf96e2f9de51
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="inspect-the-quality-of-goods"></a>商品の品質の調査

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

この手順では、品質指示を処理する方法を説明します。 デモ データの会社 USMF でこのガイドを実行できます。 このサンプル手順を開始する前に、発注書「000016」を確認し、製品受領書を転記する必要があります。 これにより、品質指示が自動的に作成されます。 品質検査は、通常、品質検査の担当者により実行されます。


## <a name="select-a-quality-order"></a>品質指示の選択
1. [在庫管理] > [定期処理タスク] > [品質管理] > [品質指示] に移動します。
2. 一覧で、選択された行をマークします。
    * この手順を開始する前に作成された品質指示を選択します。  

## <a name="record-test-results"></a>テスト結果の記録
1. [結果] をクリックします。
2. [編集] をクリックします。
3. [結果量] フィールドに数値を入力します。
4. 一覧で、選択された行をマークします。
5. [結果] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、結果は定義済の結果に基づいています。 通常、サイズまたは他の分析コードなどより詳細なテスト結果を記録します。  
7. 一覧で、選択された行のリンクをクリックします。
8. [保存] をクリックします。
9. ページを閉じます。

## <a name="validate-the-quality-order"></a>品質指示を検証する
1. [検証] をクリックします。
2. [検証者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 検査を実行するユーザーを選択します。  
3. 一覧で、選択された行のリンクをクリックします。
4. [選択] をクリックします。
5. [OK] をクリックします。
6. ページを閉じます。

