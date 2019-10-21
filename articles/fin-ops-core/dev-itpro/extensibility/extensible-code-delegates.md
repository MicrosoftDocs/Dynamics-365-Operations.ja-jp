---
title: 委任
description: このトピックでは、拡張可能コードとデリゲートを書き込む方法について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: a01001e8734da0b412fc39ac52425b970b2311da
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191636"
---
# <a name="delegates"></a>委任
[!include [banner](../includes/banner.md)]

既存のデリゲートをサブスクライブできますが、新しいデリゲートを作成しないでください。 コマンド チェーン (CoC) には、デリゲートを優先する豊富で堅牢で簡単な拡張メカニズムが用意されています。

新しい委任を作成する代わりに、[拡張可能メソッドを記述するためのガイドライン](extensible-methods.md)で説明されているように、適切な名前を持つ小さいメソッドでコードを構造化します。

デリゲートを使用する場合は、該当する場合は応答が 1 つだけになるようにすること検討してください。 詳細については、[要求または応答シナリオの EventHandlerResult クラス](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/event-handler-result-class)を参照してください。
