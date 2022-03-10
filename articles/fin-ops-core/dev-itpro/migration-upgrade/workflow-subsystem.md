---
title: Finance and Operations のワークフロー サブシステムのアップデート
description: このトピックでは、Finance and Operations のワークフロー システムを確認します。
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
ms.openlocfilehash: 0aea02b5a966e0eaf94694031b47b4bee0610d153798485af3429be95f704505
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751469"
---
# <a name="workflow-subsystem-updates-in-finance-and-operations"></a>Finance and Operations のワークフロー サブシステムのアップデート

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations のワークフロー システムを確認します。 Microsoft Dynamics AX 2012 以降に実装された変更について説明し、ワークフロー システムに関する詳細へのリンクも示します。 

Dynamics AX 2012 を使用したことがあれば、Finance and Operations のワークフロー システムはおなじみのものです。 Dynamics AX 2012 のワークフロー サブシステムの詳細については、次のトピックを参照してください。

| このテーマについて学ぶには | このトピックを参照                                             |
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
以下は、Finance and Operations に実装された主な変更点です。

-   新しいアプリケーション状態機械機能との統合により、ワークフロー イベントを基になるエンティティの状態機械での状態遷移に関連付けできます。 このバインディングにより、ビジネス ロジックをステート マシン内で集中化することが可能になり、また、ワークフロー システムをそのステート マシンの宣言コンシューマーにすることが可能になります。 ワークフロー メタデータは、特定のワークフロー イベントが発生したときに実行される状態遷移を参照できます。 したがって、追加のコードを記述することなく、ワークフロー内で状態遷移を行うことができます。
-   ワークフロー エディターは、1 回クリックしてダウンロードするプログラムになりました。 このエディターは、サービスを使用して Finance and Operations と通信します。つまり、Dynamics AX 2012 からの豊富でグラフィカルなワークフロー 設計操作を引き継ぐことができます。
-   ワークフロー開発ウィザードは Microsoft Visual Studio にポート済みです。


## <a name="additional-resources"></a>追加リソース

[開発者向け技術概念ガイド](../dev-tools/developer-home-page.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]