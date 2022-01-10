---
title: 複数の注文の処理中に、システムが計画した注文を見つけられない
description: 複数の計画された注文に対して操作を行い、少なくとも 2 つの注文が同じアイテム ID に属している場合、「計画された注文が存在しません」というエラーが発生します。
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920807"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>複数の注文の処理中に、システムが計画した注文を見つけられない

エラーコード: SYS24774

## <a name="symptoms"></a>現象

複数の計画された注文のうち、少なくとも 2 つの注文が同じアイテム ID に属している場合に、同時に操作を行おうとすると、次のようなエラーメッセージが表示されます。 たとえば、注文が確定したときや、注文タイプが変更されたときなどにエラーが発生します。

> 計画オーダー %1 が存在しません。

## <a name="cause"></a>原因

システムが注文を確定したり、注文の種類を変更したりする際には、その品目に対する既存の計画注文を再検討し、計画供給が需要と既存の供給にマッチしているかどうかを確認する必要があります。 このプロセスの一環として、システムは品目の計画的な注文を再作成します。 そのため、システムが処理を期待している 2 つ目の計画された注文は存在しなくなります。

## <a name="workaround"></a>回避策

注文を処理する前に承認が必要になります。 この方法では、システムがその品目の最初の注文を処理する際に、注文が削除されることはありません。
