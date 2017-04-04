---
title: "予算作成用のホーム ページ"
description: "このトピックでは、の予算作成機能のコンポーネント、予算作成ツール、Microsoft Dynamics 365の機能の概要を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>予算作成用のホーム ページ

このトピックでは、の予算作成機能のコンポーネント、予算作成ツール、Microsoft Dynamics 365の機能の概要を提供します。

<a name="components-of-budgeting-functionality"></a>予算作成機能のコンポーネント
-------------------------------------

通常、会社のリソース予定サイクルは、計画、予算作成、予測活動で構成されます。
[![予算作成機能コンポーネント] (。/media/budgeting機能components.jpg) ] (。/media/budgeting機能components.jpg、予算の計画のドキュメントを介して、戦略的計画と年間予算の両方のプロセス サポートされます。 予算計画ドキュメントは、Microsoft Excel と密に統合されています。 ユーザーは、無制限な金額と定量的なシナリオを構成することができ、予算作成の組織階層も定義してトップダウンおよびボトムアップ予算作成方法の両方をサポートできます。 予算を [Microsoft Dynamics 365 for Operations] で設定し、承認した後、予算計画を予算登録エントリに変換します。 予算登録エントリは、予算を管理し、予算コード経由で追跡できる金額を維持するためのツールを提供します。 予算登録エントリでは、元の予算の変更、転送の実行、予算金額の前年度からの繰り越しができます。 決定した予算に基づいて、会社は予算管理を有効にすることができます。 管理レベルは、組織の文化と組織の成熟度レベルに依存します。 成熟度レベルの低い組織は、予算が目標を満たしていない場合、予算を "現状のまま" とし、プロアクティブよりリアクティブです。 他の組織は、予算財源が使用できない場合、ユーザーが購入することを妨げる予算管理ポリシーを有効にする可能性があります。 最後に、非常に、した組織が出張ではなく、従業員が組織ターゲットについて教育の付いたターゲットになど、「ポリシーによって継承するように考慮されますオンライン会議を」組織の-カルチャの設定、 Dynamics 365 for Operationsは、会社の管理を選択 ((使用できる超過予算を超過した警告されたり自分自身に、) に選択できるユーザーを続行する方法を予算に移動する転記されない厳しい) または支払/入金を有効にする予算管理フレームワークが含まれます。 最後に、ローリングの予測を使用できます。 ローリングの予測は現物に予算の定期的な比較、[のみに会社が予算に対して有効にする方法を定義するのに使用されます。 ローリング予測は、傾向を見つけるのにも使用されます。 Microsoft Dynamics 365 for Operations では、ローリング予測は、最初の計画活動として予算計画ドキュメント経由でサポートされます。 ローリング予測は、次回の予算サイクルの計画と並列して実行できます。

-   [基本予算作成: 概要およびコンフィギュレーション](basic-budgeting-overview-configuration.md)
-   [予算管理: 概要およびコンフィギュレーション](budget-control-overview-configuration.md)
-   [予算計画: 概要およびコンフィギュレーション](budget-planning-overview-configuration.md)
-   [予測職位](position-forecasting.md)
-   [予算の計画の根拠のドキュメント] (予算計画を行うdocs.md) 
-   [予算の計画のMicrosoft Excelテンプレート] (予算計画勝ってtemplates.md) 

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations の予算作成ツール
[![のツール] (。/media/budgeting-tools.jpg) ] (。/media/budgeting-tools.jpg)  

追加の計画機能および予算作成機能は、Dynamics 365 for Operations 全体で使用でき、元帳予算に統合されます。

-   **要員予算** – 従業員の予算作成は、職位、報酬グループなどの詳細な予算原価コンポーネント計画を含みます。
-   **固定資産予算** – 固定資産情報に基づいて、計画済み減価償却を計算し、固定資産に関連する他の計画済みトランザクションを記録できます。
-   **プロジェクト予算** プロジェクト モジュールで、詳細なプロジェクト予測を作成できます。 プロジェクトの予測には、予定時間、経費、および品目に関する詳細が含まれます。
-   **需要予測**トランザクション履歴データに基づいて、–将来の在庫要求の見積と、需要予測を作成できます。

予算計画に他のモジュールから計画データを移動する方法についての情報は、[他のモジュールとの予算計画の統合](budget-planning-integration-other-modules.md)を参照してください。

## <a name="user-interface-and-reporting-capabilities"></a>ユーザー インターフェイスとレポート機能
Dynamics 365 for Operations では、ユーザーは直接 Dynamics 365 for Operations クライアントで (コンフィギュレーション可能な予算計画ドキュメント ページを使用することにより)、または Excel を使用して、予算計画を作成できます。 Excel は、いくつかの追加機能を提供します。 たとえば、予算計画のソースとして外部データを使用し、カスタム計算を実行し、Microsoft PivotTable やグラフを使用できます。 予算計画プロセスの変数のほとんどは、コンフィギュレーションできます。 たとえば、予算作成者、予算作成する対象、プロセスの概要を定義できます。 予算計画には Excel を使用できますが、Dynamics 365 for Operations では、全くの単一のソースとして保持され、予算管理の問題を防ぐのに役立ちます。 定期処理プロセスは、予算作成の初期データを予算計画に移動するために使用できます。 レポートについては、Dynamics 365 for Operations は、予算作成データを表示および分析できる一連の標準的な照会ページを提供します。 予算計画データは、Management Reporter を使用してアクセスでき、別の予算計画シナリオは、Management Reporter レポートで列として表示できます。





