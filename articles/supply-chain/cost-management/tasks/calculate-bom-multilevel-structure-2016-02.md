---
title: 複数レベル構造を使用した BOM の計算 (2016 年 2 月)
description: この手順は、原価表に基づく複数レベル展開を使用して、完成品のコストを計算する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f0ec28a20d32fc38cd6e77a76a02fc9544db3ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432042"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>複数レベル構造を使用した BOM の計算 (2016 年 2 月)

[!include [banner](../../includes/banner.md)]

この手順は、原価表に基づく複数レベル展開を使用して、完成品のコストを計算する方法を示します。 これは、BOM 計算シリーズの 7 番目のタスクです。 このタスクの作成に使用するデモ データの会社は USMF です。

1. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 製品 BOM_1 を選択します。  
3. [アクション] ペインで [原価の管理] をクリックします。
4. 品目価格をクリックします。
5. [品目原価の計算] をクリックします。
    * 省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。  
6. [原価計算バージョン] フィールドで値を入力または選択します。
    * 原価計算バージョン 20 を選択します。その理由は、これが予定原価タイプであり、展開モードが複数レベルのためです。   複数レベル展開モードは、予定原価およびシミュレーション用です。 これは、標準原価には使用されません。  
7. [OK] をクリックします。
8. [計算の詳細の表示] をクリックします。
    * 省略記号 (...) をクリックして、トップ メニューにこのオプションを表示する必要があります。  この場合、このシリーズの最初のタスク ガイドで有効化された標準原価 10 ではなく、原材料、プロセス、および合計 29,40 の間接費を考慮して BOM_2 がどのように計算されたかに注目してください。  
9. [原価計算表] タブをクリックします。
    * [原価計算表] タブに移動したとき、原価グループごとの合計が以前のタスク ガイド内で行った計算と比較して異なります。  
10. [レベル] フィールドで、「複数」を選択します。
    * [複数] を選択すると、原価は BOM_2 の構成に従って分類されます。すなわち、10 は M1 原価グループ (ITEM_C) から派生し、15,60 は原価グループが L2 の製造から派生します。 また、間接原価も変化します。  
11. ページを閉じます。
12. ページを閉じます。

