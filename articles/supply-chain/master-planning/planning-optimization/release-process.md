---
title: 計画最適化リリース プロセスおよびリリース履歴
description: このトピックでは、計画最適化のリリース プロセスおよびリリース履歴に関する情報を提供します。
author: crytt
ms.date: 7/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 64c8cd3ed6ff522a9ef90831ae502c5d50fbc05816aaa764d2a8e122934fc2bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722394"
---
# <a name="planning-optimization-release-process-and-release-history"></a>計画最適化リリース プロセスおよびリリース履歴

[!include [banner](../../includes/banner.md)]

Microsoft は、計画最適化を月ごとに更新します。 ただし、業務要件に基づいて、スケジュール済みリリース間に追加の更新がリリースされる場合があります。

各リリースは、計画最適化が使用可能な個別の地域に公開されます。 このプロセスは通常、3 日かかります。

計画最適化の更新中に、マスター プランの実行が通常より少し遅くなる可能性があります。

計画最適化を使用する環境では、最新のリリースが自動的に提供されます。 ユーザー アクションは必要ありません: サービスが自動的に更新されます。 ただし、重要な変更機能が自動的に環境にプッシュされることはありません。 既定では、重要と見なされる変更はオフにされ、[機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して明示的に有効にする必要があります。 したがって、これらの変更は、有効にするまで環境に表示されません。

環境内で計画最適化が更新されると通知は表示されないので、次の表のリリース ノートを確認して、変更がいつリリースされたのか、またどの機能が導入されたのかを決定できます。 この表は、計画最適化のためにリリースされた変更、それらの変更が機能管理の機能に関連付けられているかどうか、およびリリース日を示しています。

| 変更 | 機能管理の詳細 | リリース日 |
|---|---|---|
| <p>無限能力のスケジューリングに必要なリソース タイプの要件</p><p>無限能力スケジューリングのためのリソース効率とカレンダー効率</p><p>詳細については、[無限能力を使用したスケジューリング](infinite-capacity-planning.md) を参照してください。 | <p>バージョン 10.0.20 の機能管理で使用できます。</p><p>機能名: *計画最適化の無限能力のスケジューリング*</p> | 2021 年 7 月 6 日 |
| 一般的な品質改善 | 機能管理は必要ありません。 | 2021 年 7 月 6 日 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]