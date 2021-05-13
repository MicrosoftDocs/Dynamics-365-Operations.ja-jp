---
title: 委任
description: このトピックでは、拡張可能コードとデリゲートを書き込む方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: dce859e4b0ce471917c22155dbad5a98481ad97a
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923407"
---
# <a name="delegates"></a>委任
[!include [banner](../includes/banner.md)]

既存のデリゲートをサブスクライブできますが、新しいデリゲートを作成しないでください。 コマンド チェーン (CoC) には、デリゲートを優先する豊富で堅牢で簡単な拡張メカニズムが用意されています。

新しい委任を作成する代わりに、[拡張可能メソッドを記述するためのガイドライン](extensible-methods.md)で説明されているように、適切な名前を持つ小さいメソッドでコードを構造化します。

デリゲートを使用する場合は、該当する場合は応答が 1 つだけになるようにすること検討してください。 詳細については、[要求または応答シナリオの EventHandlerResult クラス](../dev-tools/event-handler-result-class.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
