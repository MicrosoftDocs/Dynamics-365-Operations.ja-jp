---
title: 予算作成用のホーム ページ
description: このトピックでは、Microsoft Dynamics 365 Finance の予算作成機能コンポーネント、予算作成ツール、およびレポート機能の概要を示します。
author: panolte
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2597dda47e3441d2c41497081849a2213974e55
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187919"
---
# <a name="budgeting-home-page"></a>予算作成用のホーム ページ

[!include [banner](../includes/banner.md)]

このトピックでは、予算作成機能コンポーネント、予算作成ツール、およびレポート機能の概要を示します。 

## <a name="components-of-budgeting-functionality"></a>予算作成機能のコンポーネント

通常、会社のリソース予定サイクルは、計画、予算作成、予測活動で構成されます。

[![予算作成機能コンポーネント](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

長期戦略的計画と年間予算計画の両方のプロセスは、予算計画ドキュメント経由でサポートされます。 予算計画ドキュメントは、Microsoft Excel と密に統合されています。 ユーザーは、無制限な金額と定量的なシナリオを構成することができ、予算作成の組織階層も定義してトップダウンとボトムアップの両方の予算作成方法をサポートできます。 予算をアプリケーションで設定し、承認した後、予算計画を予算登録エントリに変換します。 予算登録エントリは、予算を管理し、予算コード経由で追跡できる金額を維持するためのツールを提供します。 予算登録エントリでは、元の予算の変更、転送の実行、予算金額の前年度からの繰り越しができます。 決定した予算に基づいて、会社は予算管理を有効にすることができます。 管理レベルは、組織の文化と組織の成熟度レベルに依存します。 成熟度レベルの低い組織は、予算が目標を満たしていない場合、予算を "現状のまま" とし、プロアクティブよりリアクティブです。 組織によっては、予算財源が使用できない場合に、ユーザーが購入することを妨げる予算管理ポリシーを有効にすることもあります。

最後に、非常に成熟した組織は、従業員が組織の目標について教育されている組織文化を確立し、「出張の代わりにオンライン ミーティングを検討する」ようなポリシーを通じてこれらの目標に従う可能性があります。 アプリケーションには、会社の管理がハード コントロール (予算を超過する転記ができません) またはソフト コントロール (ユーザーが利用可能な予算資源を超えると警告されますが、続行方法を決めることができます) のいずれかを選択できる予算管理フレームワークが含まれます。 最後に、ローリング予測を使用できます。 ローリング予測は、予算対実績の定期的な比較であり、会社が予算との比較においてどの程度効果的に運営されているかを定義するために使用します。 ローリング予測はトレンドの特定にも使用されます。 Finance and Operations では、ローリング予測は、最初の計画活動として予算計画ドキュメント経由でサポートされます。 ローリング予測は、次回の予算サイクルの計画と並列して実行できます。

-   [予算作成の概要](basic-budgeting-overview-configuration.md)
-   [予算管理の概要](budget-control-overview-configuration.md)
-   [予算計画の概要](budget-planning-overview-configuration.md)
-   [職位予測](position-forecasting.md)
-   [予算計画妥当性ドキュメント](budget-planning-justification-docs.md)
-   [Excel の予算計画テンプレート](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>予算作成ツール
[![予算作成ツール](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

追加の計画機能および予算作成機能は使用可能で、元帳予算に統合されます。

-   **要員予算** – 従業員の予算作成は、職位、報酬グループなどの詳細な予算原価コンポーネント計画を含みます。
-   **固定資産予算** – 固定資産情報に基づいて、計画済み減価償却を計算し、固定資産に関連する他の計画済みトランザクションを記録できます。
-   **プロジェクト予算** プロジェクト モジュールで、詳細なプロジェクト予測を作成できます。 プロジェクトの予測には、予定時間、経費、および品目に関する詳細が含まれます。
-   **需要予測** – トランザクション履歴データに基づき、将来の在庫需要の見積、需要予測の作成ができます。

予算計画に他のモジュールから計画データを移動する方法についての情報は、[他のモジュールとの予算計画の統合](budget-planning-integration-other-modules.md)を参照してください。

## <a name="user-interface-and-reporting-capabilities"></a>ユーザー インターフェイスとレポート機能
ユーザーは直接クライアントで (コンフィギュレーション可能な予算計画ドキュメント ページを使用することにより)、または Excel を使用して、予算計画を作成できます。 Excel は、いくつかの追加機能を提供します。 たとえば、予算計画のソースとして外部データを使用し、カスタム計算を実行し、Microsoft PivotTable やグラフを使用できます。 予算計画プロセスの変数のほとんどは、コンフィギュレーションできます。 

たとえば、予算作成者、予算作成する対象、プロセスの概要を定義できます。 予算計画には Excel を使用できますが、アプリケーションでは、まったくの単一のソースとして保持され、予算管理の問題を防ぐのに役立ちます。 定期処理プロセスは、予算作成の初期データを予算計画に移動するために使用できます。 アプリケーションでは、予算作成データを表示および分析できる一連の標準的なレポートの照会ページを提供します。 予算計画データは、[Financial Reporting](../general-ledger/financial-reporting-getting-started.md) を使用してアクセスでき、別の予算計画シナリオは、財務諸表で列として表示できます。








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
