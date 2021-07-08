---
title: 品目に BOM または数式を含めることはできない
description: 注文を確定しようとする際、品目の検証中にエラー メッセージが表示されます。 品目に部品表 (BOM) または数式を含めることはできないことを示しています。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294119"
---
# <a name="item-cant-have-a-bom-or-formula"></a>品目に BOM または数式を含めることはできない

エラーコード: PRO2614

## <a name="symptoms"></a>現象

注文を確定しようとする際、品目の検証中に次のエラー メッセージが表示されます:

> 品目に BOM または数式を含めることができない

## <a name="resolution"></a>解決策

部品表 (BOM) または数式を含む品目は、タイプが *計画品目*、*BOM*、または *数式* である必要があります。 品目タイプを変更するには、次の手順に従います。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 関連する製品を開きます。
1. **エンジニア** クイックタブにおいて、**生産タイプ** フィールドを *計画品目*、*BOM*、または *数式* に設定します。
