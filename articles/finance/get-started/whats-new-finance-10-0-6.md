---
title: Dynamics 365 Finance 10.0.6 (2019 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Finance 10.0.6 の新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 57b10735ce83e9a46756d262f312112a736ebf14
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070410"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-1006-november-2019"></a>Dynamics 365 Finance 10.0.6 (2019 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance 10.0.6 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.234 です。 一般提供開始日は 11 月ですが、新機能は 10 月の初期リリースで使用できます。 バージョン 10.0.6 の詳細については [追加リソース](whats-new-finance-10-0-6.md#additional-resources) を参照してください。

## <a name="feature-management-enhancements"></a>機能管理の拡張
機能管理を使用すると、既定ですべての新機能を有効にできます。それには機能を有効にするための確認と、まだ有効になっていないすべての機能を有効にすることが必要です。 

## <a name="select-consolidation-amount-from-control-on-the-consolidate-online-for-dual-currency-consolidation"></a>デュアル為替連結用オンラインでの連結の「連結金額の選択元」コントロール
この機能は、連結会社の取引通貨として使用される通貨 (会計またはレポート通貨) をコントロールするのに役立ち、通貨が同じ場合、ソースの会社から連結会社に金額を自動的にコピーすることができます。

## <a name="cancel-bank-reconciliation"></a>口座調整のキャンセル
ユーザーは、口座の調整を最新のものから始まる順序でキャンセルすることができます。 履歴が追跡され、調整が取り消された時期と担当者が表示されます。 これにより、ユーザーは、定期処理中に発生したエラーを修正するために仕訳帳を手動で調整する必要がなくなります。

## <a name="create-checks-with-a-blank-status-on-the-checks-page"></a>[小切手] ページで空白状態の小切手を作成する
**小切手** ページでは、新しい小切手番号の作成や小切手の削除など、小切手に関するメンテナンスタスクを実行できます。 支払プロセス中にこの機能が有効になっている場合、支払プロセス中に空白ステータスの小切手を作成することはできません。 この拡張機能により、不必要に小切手を無駄にすることがなくなります。

## <a name="reset-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>仕入先請求書のワークフロー ステータスを、修復不可能からドラフトにリセットする
ワークフローの履歴ページを使用して、ワークフロー状態をドラフトにリセットできます。 このページは、仕入先請求書 または 共通 > 照会 > ワークフロー へ移動することで開くことができます。 ワークフロー状態をドラフトにリセットするには、取り消し を選択します。 また、仕入先請求書 または 保留中の仕入先請求書 ページの 取り消し アクションを選択して、ワークフロー状態をドラフトにリセットすることもできます。 ワークフロー ステータスをドラフトにリセットした後、仕入れ先請求書 ページで編集できるようになります。

## <a name="revenue-recognition"></a>収益認識
収益認識管理は、会計および財務のプロフェッショナルが国際財務報告基準 (IFRS) 15 および会計基準成文化 (ASC) 606に準拠するために行うステップを自動化するのに役立ちます。

新しい機能には、次のような製品バンドルとキットのサポートが含まれます。

- ソフトウェアおよびメンテナンス
- ソフトウェアおよびサービス
- ソフトウェア
- ハードウェアおよびサービス

これらの処理能力により、次の機能が処理されます。

- 収益価格設定 
- 収益スケジュール
- バンドルの設定 
- 複数の販売注文の再配賦
- ワークスペースのナビゲーションおよびレポート

## <a name="revenue-pricing"></a>収益価格設定
ユーザーは、顧客に請求するのとは異なって認識される価格を入力することができます。

[![収益価格設定のスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)](../accounts-receivable/media/rev-rec-whats-new-1-revenue-pricing.png)

## <a name="revenue-schedules"></a>収益スケジュール
収益スケジュールによって、収益遅延の月数が決まります。 その月の実際の日付に基づいて、月に均等配分、または発生した回数に基づいてスケジュールを作成するオプションがあります。

[![収益スケジュールのスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)](../accounts-receivable/media/rev-rec-whats-new-2-revenue-schedules.png)

## <a name="multiple-sales-order-reallocation"></a>複数の販売注文の再配賦

[![複数の販売注文の再配賦のスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)](../accounts-receivable/media/rev-rec-whats-new-3-multiple-sales-order-reallocation.png)

## <a name="workspace"></a>ワークスペース 
新しいワークスペースは、繰延収益に対して作成された収益スケジュール レコードのステータスを確認するために使用されます。

[![収益認識ワークスペースのスクリーンショット](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)](../accounts-receivable/media/rev-rec-whats-new-4-revenue-recognition-workspace.png)

## <a name="project-contract-committed-detail"></a>プロジェクト契約の確定済詳細
プロジェクト契約の資金調達ソースで確定された金額の詳細にドリルダウンして、確定された金額を構成する活動をユーザーが簡単に確認できるようになりました。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
10.0.6 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) を参照してください。

### <a name="platform-update-30"></a>プラットフォーム update 30
Dynamics 365 Finance 10.0.6 には、プラットフォーム更新プログラム 30 が含まれています。 プラットフォーム更新プログラム 30 についての詳細は、[Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能と変更点](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md)を参照してください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックでは、Dynamics 365 forfin-ops-core/ Finance and Operations で削除または推奨されない機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
