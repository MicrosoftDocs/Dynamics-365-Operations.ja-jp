---
title: 出荷がリリースされるとすぐにピッキング作業が生成されるようにする
description: 積荷がリリースされたときに作業をすぐに生成する必要がある場合は、それに応じてウェーブ テンプレートを構成する必要があります。 このページでは、手順を説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476894"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>出荷がリリースされても、ピッキング作業がすぐには生成されない

## <a name="symptoms"></a>現象

販売注文または移動注文を使用して作成し、出荷を倉庫にリリースします。 しかしながら、ピッキング作業はまだ生成されていないことに気づきます。

## <a name="resolution"></a>解決策

積荷がリリースされたときに作業をすぐに生成する必要がある場合は、それに応じてウェーブ テンプレートを構成する必要があります。 ウェーブ テンプレートでは、次のオプションを *はい* に設定します。

- ウェーブの作成を自動化
- 倉庫へのリリース時にウェーブを処理する
- ウェーブを自動的にリリースする
