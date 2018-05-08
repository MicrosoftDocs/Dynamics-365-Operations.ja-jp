---
title: "バーコード タイプの管理"
description: "この手順は、ピッキング リスト レポートの一部として使用される、新しいバーコードの定義を設定する方法を示します。"
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bar-code-types"></a>バーコード タイプの管理

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、ピッキング リスト レポートの一部として使用される、新しいバーコードの定義を設定する方法を示します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 USMF を使用すると、表示される例の値を使用できます。 通常、これらのタスクを実施するのは、倉庫マネージャーです。

1. [バーコード] に移動します。
2. [新規] をクリックします。
3. [バーコード設定] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [バーコード タイプ] フィールドでオプションを選択します。
    * USMF を使用している場合、「Code 39」を選択できます。  
6. [サイズ] フィールドに数値を入力します。
7. [最大の長さ] フィールドに数値を入力します。
8. [保存] をクリックします。
9. ページを閉じます。
10. [在庫および倉庫管理パラメーター] に移動します。
11. [バーコード設定] フィールドで値を入力または選択します。
    * 以前に作成したバーコード設定を選択します。しかしバーコード形式は、プロセスで使用されているレコード タイプに対する固有識別子の形式と一致している必要があることに注意してください。 たとえば、ピッキング ルートに対するバーコード形式は、通常番号順序であるピッキング ルート参照の形式と一致する必要があります。  
12. [保存] をクリックします。
13. ページを閉じます。

