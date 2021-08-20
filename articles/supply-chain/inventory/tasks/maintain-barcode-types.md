---
title: バーコード タイプの管理
description: この手順は、ピッキング リスト レポートの一部として使用される、新しいバーコードの定義を設定する方法を示します。
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60fa8051ebe71c2606a5d6d3d1e22ec852023dd47301a008c98e9f4d7deaad29
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755357"
---
# <a name="maintain-barcode-types"></a>バーコード タイプの管理

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]