---
title: 製造オーダーの見積
description: USMF デモ データ会社または用意したデータ セットを使用して、この手順を実行できます。
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0450186382b6c306910fc6653f67ce313b7cfc2c69a134a9a806d1a232dc0fd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765421"
---
# <a name="estimate-a-production-order"></a>製造オーダーの見積

[!include [banner](../../includes/banner.md)]

USMF デモ データ会社または用意したデータ セットを使用して、この手順を実行できます。 どちらの場合も、ステータスが [作成済] である未処理の製造オーダーが必要です。 これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 2 番目です。


## <a name="estimate-a-production-order"></a>製造オーダーの見積
1. [生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。
2. グリッドでステータスが [作成済] の注文を選択します。
3. アクション ウィンドウで、[製造オーダー] をクリックします。
4. [見積] をクリックします。
    * このステップでは、1 つの製造オーダーの見積原価が計算されます。   
5. [OK] をクリックします。

## <a name="view-the-calculation-details"></a>計算の詳細の表示
1. [アクション] ペインで [原価の管理] をクリックします。
2. [計算の詳細の表示] をクリックします。
    * このページは、原価内訳を表示します。 たとえば、先頭行の完成品の単位あたりの原価価格合計を表示できます。 後続の行には、部品表、生産工順、および間接原価などの原価が含まれます。  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]