---
title: Finance and Operations でのワークフロー サブシステムの更新
description: この記事では、財務と運用のワークフロー システムについて説明します。
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 13511
ms.assetid: 0e3aa2cd-2327-45ba-bf38-0ef543fa8f67
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9327dba6d347fabc0dc116085eb1a61220cbbea5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868744"
---
# <a name="workflow-subsystem-updates-in-finance-and-operations"></a>Finance and Operations でのワークフロー サブシステムの更新

[!include [banner](../includes/banner.md)]

この記事では、財務と運用のワークフロー システムについて説明します。 Microsoft Dynamics AX 2012 以降に実装された変更について説明し、ワークフロー システムに関する詳細へのリンクも示します。 

Dynamics AX 2012 を使用していれば、Finance and Operations のワークフロー システムはおなじみのものです。 Dynamics AX 2012 のワークフロー サブシステムの詳細については、次のトピックを参照してください。

| このテーマについて学ぶには | この記事を参照してください                                             |
|-----------------------------|------------------------------------------------------------|
| ワークフロー システム         | <https://technet.microsoft.com/library/dd309672.aspx> |
| モジュールごとのワークフロー タイプ    | <https://technet.microsoft.com/library/dd362043.aspx> |
| ワークフロー要素           | <https://technet.microsoft.com/library/dd309626.aspx> |
| ワークフロー アクション            | <https://technet.microsoft.com/library/dd362144.aspx> |
| ワークフローの参加者       | <https://technet.microsoft.com/library/dd309598.aspx> |
| ワークフローの例           | <https://technet.microsoft.com/library/dd309636.aspx> |
| ワークフローの開発       | <https://msdn.microsoft.com/library/cc967389.aspx>    |
| ワークフローの実装     | <https://msdn.microsoft.com/library/cc585061.aspx>    |

## <a name="primary-changes-to-the-workflow-system"></a>ワークフロー システムの主な変更
Finance and Operations で実装された基本変更を次に示します。

-   新しいアプリケーション状態機械機能との統合により、ワークフロー イベントを基になるエンティティの状態機械での状態遷移に関連付けできます。 このバインディングにより、ビジネス ロジックをステート マシン内で集中化することが可能になり、また、ワークフロー システムをそのステート マシンの宣言コンシューマーにすることが可能になります。 ワークフロー メタデータは、特定のワークフロー イベントが発生したときに実行される状態遷移を参照できます。 したがって、追加のコードを記述することなく、ワークフロー内で状態遷移を行うことができます。
-   ワークフロー エディターは、1 回クリックしてダウンロードするプログラムになりました。 このエディターは、サービスを使用して Finance and Operations と通信します。つまり Dynamics AX 2012 からの豊富でグラフィカルなワークフロー設計操作を引き継ぐことができます。
-   ワークフロー開発ウィザードは Microsoft Visual Studio にポート済みです。


## <a name="additional-resources"></a>追加リソース

[開発者向け技術概念ガイド](../dev-tools/developer-home-page.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]