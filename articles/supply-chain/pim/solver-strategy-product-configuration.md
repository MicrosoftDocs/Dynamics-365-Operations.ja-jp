---
title: 製品コンフィギュレーションのソルバー戦略
description: このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。
author: cvocph
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38755cc224ee2ae642d3caf7ad8ffea61f987206efc3ecd2ef81ecaf21cd6f4e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765981"
---
# <a name="solver-strategy-for-product-configuration"></a>製品コンフィギュレーションのソルバー戦略

[!include [banner](../includes/banner.md)]

このトピックでは、製品のコンフィギュレーションのパフォーマンスを向上させるためにソルバー戦略を使用する方法について説明します。

ソルバー戦略の概念は最初に Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) に導入されました。 そして、Microsoft Dynamics AX 2012 R3 と Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 の累積更新プログラム 8 (CU8) に拡張されました。

現在、ソルバー戦略概念は次の方法で構成されています。

- 既定
- 最小ドメインを先頭にする
- トップダウン
- Z3

## <a name="solver-strategy"></a>ソルバー戦略 

製品コンフィギュレーション モデルは、[制約充足問題 (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) として作成できます。 Microsoft Solver Foundation (MSF) では、製品コンフィギュレーション モデルから使用できる CSPs を解決するために、ソルバー戦略の 2 つのタイプを提供します。 これらのソルバー戦略は、[ヒューリスティック](https://techterms.com/definition/heuristic) に依存しています。これらは、問題が解決されたときに CSPs の変数が考慮される順序を決定するために使用されます。 ヒューリスティックは、問題または問題のクラスが解決されているときに、パフォーマンスに大きな影響を与える可能性があります。

製品コンフィギュレーション モデルのソルバー戦略は、どのソルバーがヒューリスティックで使用されているかを決定します。 **既定の**、**最小ドメインを先頭にする**、および **トップダウン** の戦略は MSF から 2 つのソルバーを使用します。一方、**Z3** 戦略は Z3 ソルバーを使用します。 

実際の顧客実装調査によると、製品コンフィギュレーション モデルのソルバー戦略の変更が、応答時間を数分から数ミリ秒に短縮することが可能だと示しています。 したがって、製品コンフィギュレーション モデルの最も効率的な戦略を見つけるため、さまざまなソルバー戦略に挑戦する価値はあります。

## <a name="change-the-settings-for-the-solver-strategy"></a>ソルバー戦略の設定を変更

ソルバー戦略を変更するには、アクション ペイン上の **製品コンフィギュレーション モデル** ページで、**モデルのプロパティ** を選びます。 そして、**モデルの詳細の編集** ダイアログ ボックスで、ソルバー戦略を選択します。

[![ソルバー戦略を変更。](./media/solver-strategy.png)](./media/solver-strategy.png)

現時点では、どのソルバー戦略が制約ベースの製品コンフィギュレーションの最も効率的な戦略になるかを自動的に検出するロジックはありません。 そのため、1 つずつソルバー戦略を試みる必要があります。

次の表では、さまざまなシナリオで使用するソルバー戦略に関する推奨事項を提供します。

| ソルバー戦略      | このシナリオの戦略を使用 |
|----------------------|-----------------------------------|
| 既定              | **既定の** 戦略は、テーブル制約に依存するモデルを解決するために最適化されています。 顧客実装調査によると、この戦略はテーブル制約が広く使用されているシナリオで最も効率的な戦略だと示しています。 |
| 最小ドメインを先頭にする | **最小限ドメインを先頭にする** および **トップダウン** 戦略は、密接な関係です。 顧客実装調査は、**トップダウン** 戦略が、**最小ドメインを先頭にする** 戦略より優れていることを示しています。 ただし、**最小ドメインを先頭にする** 戦略は下位互換性の製品に保管されています。 これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。 ただし、場合により、**既定** 戦略はこれら 2 つの戦略より優れています。 そのため、それぞれの戦略を試してください。 |
| トップダウン             | **最小限ドメインを先頭にする** および **トップダウン** 戦略は、密接な関係です。 顧客実装調査は、**トップダウン** 戦略が、**最小ドメインを先頭にする** 戦略より優れていることを示しています。 ただし、**最小ドメインを先頭にする** 戦略は下位互換性の製品に保管されています。 これら両方のソルバー戦略は、テーブル制約が使用されないくつかの算術式を含むモデルを解くことでより効率的であることが示されています。 ただし、場合により、**既定** 戦略はこれら 2 つの戦略より優れています。 そのため、それぞれの戦略を試してください。 |
| Z3                   | 既定のソルバー戦略として、**Z3** 戦略の使用をお勧めします。 パフォーマンスとスケーラビリティがについて考慮する場合は、その他の戦略を評価することができます。 |

## <a name="additional-resources"></a>追加リソース

[製品コンフィギュレーションの概要](build-product-configuration-model.md)

[ヒューリスティック](https://techterms.com/definition/heuristic)

[制約充足問題](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]