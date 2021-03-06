---
title: 単一レベル構造を使用した BOM の計算 (2016 年 2 月)
description: この手順は、原価表に基づく単一レベル展開を使用して、完成品のコストを計算する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821396"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>単一レベル構造を使用した BOM の計算 (2016 年 2 月)

[!include [banner](../../includes/banner.md)]

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
    * 省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。    コストの構成は次のとおりです:  *    10 は ITEM_A から、 10 は ITEM_B から、 10 は BOM_2 から派生します。 この場合、BOM_2 は計算によってではなく、標準原価 10 として入力されたので、その詳細はありません。  *    7 は一定のコストである段取り時間から派生し、追加の 7 は実行時操作 (プロセス) から派生します。  *    間接原価に対応する他の金額もあります。  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]