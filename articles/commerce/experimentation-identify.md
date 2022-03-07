---
title: 仮想を識別して実験のメトリックを決定する
description: このトピックでは、Dynamics 365 Commerce で E コマース Web サイトで実行する実験の仮想および成功メトリックを識別する方法について説明します。
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: a3f5d44e008e4092557d75c8f5d830d5ae36a091
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799053"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>仮想を識別して実験の成功メトリックを決定する
実験ライフサイクルの第 1 フェーズでは、実験の仮想を識別して、成功を評価するために追跡するメトリックを決定することが含まれます。 次の図は、Dynamics 365 Commerce の E コマース Web サイトでの[実験の設定と実行](experimentation-overview.md)に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。 

[ ![実験ユーザー体験 - 識別](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

仮想とは、実験の結果を予測する明細書です。 たとえば、ユーザーの行動および収集した Web サイトのデータに関する調査など、仮想の定義には多くの要因があります。 仮想により、実験で検証する前提および理論を定義します。 実験の仮想の例としては、「*皆、夏には軽量で明るい色のものを着たいので、夏の期間は、ホーム ページにある白い T シャツの写真は、ネイビーのセーターよりもクリック率が高くなる。*」 その場合は、白い T シャツとネイビーのセーターを含むバリエーションを作成し、両方を同時に公開します。

仮想を検証するには、実験の成功または失敗を Web サイトのユーザーがリンクやボタンをクリックするなどのユーザーのアクションに直接関連付ける必要があります。 これらのアクションは、実験を追跡するサード パーティ サービスに報告されるイベントに対応する必要があります。 時間の経過と共に、アクションを実行するユーザーの割合は、レポートを生成して分析を実施するために使用できるメトリックとして集計されます。 使用可能なすべてのイベントおよび属性を確認するには、[診断とトラブルシューティングの Commerce コンポーネント イベント](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)を参照してください。

## <a name="previous-step"></a>前のステップ
[Dynamics 365 Commerce での実験](experimentation-overview.md)


## <a name="next-step"></a>次のステップ
[実験の設定](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]