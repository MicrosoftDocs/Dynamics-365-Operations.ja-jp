--- 
title: "単一レベル構造を使用した BOM の計算 (2016 年 2 月のみ)"
description: "この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 36096c9a0c8dde1028728ec257dfa63e7fb669af
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>単一レベル構造を使用した BOM の計算 (2016 年 2 月のみ)

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。 これは、BOM 計算シリーズの 6 番目のタスクです。 このタスクの作成に使用するデモ データの会社は USMF です。

1. [リリースされた製品] に進みます。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 製品 BOM_1 を選択します。  
3. [アクション] ペインで [原価の管理] をクリックします。
4. 品目価格をクリックします。
5. [品目原価の計算] をクリックします。
    * 省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。  
6. [原価計算バージョン] フィールドで、ドロップ ダウン ボタンをクリックして、ルックアップを開きます。
    * このデモでは、「10」を選択します。 これは、原価価格をコンポーネントに追加する際に使用される、同じ原価バージョンです。  
7. [OK] をクリックします。
8. [計算の詳細の表示] をクリックします。
    * 省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。    以下に原価の構成を示します。 •    10 は ITEM_A から派生し、10 は ITEM_B から派生し、10 は BOM_2 から派生します。 この場合、BOM_2 は計算によってではなく、標準原価 10 として入力されたので、その詳細はありません。  •  7 は段取り時間から派生します。これは一定の原価であり、追加の 7 は実行時工程 (プロセス) から派生します。  •   また、間接原価に対応するその他の金額も存在します。  
9. @SysTaskRecorder:_RequestClose


