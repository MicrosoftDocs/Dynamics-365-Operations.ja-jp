---
title: ピース ピッキング確認
description: ピース ピッキングにより、モバイル デバイスでピッキング作業または棚卸作業を通して各在庫を確認することができます。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a925685b80c635cf036f19748e16d415953ed5fdda7b81498baeade35ccbfcab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766005"
---
# <a name="piece-picking-confirmation"></a>ピース ピッキング確認

[!include [banner](../includes/banner.md)]

ピース ピッキングにより、モバイル デバイスでピッキング作業または棚卸作業を通して各在庫を確認することができます。 ピッキングについては、ピッキングする作業に指定された数量まで、処理する作業量を確認することができます。 棚卸作業では、棚卸在庫をスキャンでき、合計金額を追跡できます。

ピース ピッキングを有効にすると、製品の確認書が自動的に選択されます。 作業の種類の選択については、最大個数を設定できます。 これにより、作業プロセス中に確定する必要がある在庫数数に最大値を設定できます。 最大数量は、処理されている現在の作業単位に基づいています。 棚卸作業の種類には、最大値を設定できません。

スキャンされたバーコードに関連付けられた数量と測定単位 (UOM) を使用することもできます。 これにより、複数のライセンス番号の入荷、購買注文の品目、移動オーダーの品目および負荷品目を含む着信フローでの受領が実行されます。 また、バーコードをスキャンすると、バーコード上の UOM と作業単位の間で変換された確認済みの在庫総数に数量が加算されます。 バーコードで UOM をカウントすると、その数量が順序グループでカウントできることが確認された場合、数量が合計カウントに加算されます。

## <a name="where-it-applies"></a>該当する場合

ピース ピッキングは、すべての棚卸作業と任意のタイプの作業における初期ピッキング作業に適しています。 品目がシリアル番号で管理されている場合、またはナンバー プレート (LP) の場所から製品またはかんばんをピッキングしアイテムがステージングに設定されている場合、ピース ピッキングは適用されません。

## <a name="set-up-piece-picking"></a>ピッキング ピッキングの設定

1.  モバイル デバイスのメニュー項目で、作業確認の設定フォームを開きます: [倉庫管理] > **倉庫管理** > **設定** > **モバイル デバイス** > **モバイル デバイスのメニュー項目** に進みます。 
2. モバイル デバイス メニュー品目から、[作業確認の設定] を開きます。

作業タイプが選択または集計の場合、以下のオプションが選択可能になります。


|           オプション           |                                                                            説明                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ピース ピッキング確認 | 選択と棚卸作業タイプに使用できます。 製品の確認書が自動的に選択されます。 モバイル デバイスから各在庫を確認できます。 |
|  ピースの最大数  |                   ピース ピッキングの確認が有効化された場合にピッキング作業に使用できます。 確認する必要がある在庫数の制限を設定します。                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]