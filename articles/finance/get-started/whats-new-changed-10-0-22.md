---
title: Dynamics 365 Finance 10.0.22 (2021 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.22 プレビュー リリースの新機能または変更された機能について説明します。
author: kfend
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2021-09-023
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c759082a86f4bc04ecb1c1aa514ee6e15e7e3c4b
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675063"
---
# <a name="preview-features-in-dynamics-365-finance-10022-november-2021"></a>Dynamics 365 Finance 10.0.22 (2021 年 11 月) の機能のプレビュー

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.22 の新機能または変更された機能について説明します。 このバージョンには 10.0.995 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー**: 2021 年 9 月
- **リリースの一般提供 (手動更新)**: 2021 年 10 月
- **リリースの一般提供 (自動更新)**: 2021 年 11 月


## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。 これらの機能を使用または無効にする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| 機能領域 | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| 一般会計  | 消費税通貨での **コード別消費税支払** レポートの生成   | 10.0.22 より前は、この機能は既定で有効になっていませんでした。 この機能を使用するには、手動で有効化する必要がありました。 10.0.22 のリリースでは、この機能が既定で有効になりました。 この機能の詳細については、[支払コード別費税支払レポートを印刷する](../general-ledger/print-sales-tax-payment-by-code-report.md)を参照してください。   |




## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム
Dynamics 365 Finance 10.0.22 には、プラットフォーム更新プログラムが含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.22 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md) を参照してください。 

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) を参照してください。

### <a name="regulatory-updates"></a>規制の更新
Finance and Operations アプリの規制の更新については、[規制の更新](../localizations/regulatory-updates.md)を参照してください。 規制の更新を調べるもう 1 つの方法は、LCS にログインして、問題検索ツールを使用して予定されている規制更新を表示することです。 問題検索では、国、機能の種類、およびリリースを使用して検索を実行できます。 

### <a name="dynamics-365-2021-release-wave-plans"></a>Dynamics 365: 2021 リリース ウェーブ プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 Finance 2021 リリース ウェーブ 2](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance)をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際にそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Finance で削除または廃止された機能](removed-deprecated-features-finance.md) トピックでは、Dynamics 365 Finance で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Finance の削除済みまたは非推奨の機能](removed-deprecated-features-finance.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
