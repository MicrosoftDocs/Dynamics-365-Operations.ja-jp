---
title: Finance and Operations バージョン 10.0.3 (2019 年 6 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.3 の新機能または変更された機能について説明します。 このバージョンは 6 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.3
ms.openlocfilehash: 3f498d697c19ace378d4730845ae4a89ee449f16
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693504"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1003-june-2019"></a>Finance and Operations バージョン 10.0.3 (2019 年 6 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 の新機能または変更された機能について説明します。 このバージョンは 6 月にリリースされ、ビルド番号は 10.0.107 です。 バージョン 10.0.3 の詳細については [追加リソース](whats-new-changed-10-0-3.md#additional-resources) を参照してください。

Retail の最新のリリースの新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.3 の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-3) を参照してください。

## <a name="feature-management"></a>機能管理

**機能管理** エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。

詳細については [機能管理](https://go.microsoft.com/fwlink/?linkid=2080380) を参照してください。

## <a name="enable-bank-foreign-currency-revaluation-without-a-parameter"></a>パラメーターなしで銀行の外貨再評価を有効にする
銀行の外貨再評価はバージョン 10.0.2 でリリースされ、それを有効にするために現金と銀行のパラメータを含めました。 機能管理を使用して利用可能なすべての法人に対して、銀行の外貨再評価を有効化できるようになりました。 

詳細については [銀行の外貨再評価](https://go.microsoft.com/fwlink/?linkid=2079802) を参照してください。

## <a name="expense-reports-re-imagined"></a>経費レポートの再設計
経費精算書エントリは、経費精算書の完成にかかる時間を節約し、単純化するために再設計されています。 機能管理でこの機能を有効にして、経費レポートを入力するため必要なデータ、オプションのデータ、有効になっていないデータを判断するための経費フィールドの表示を設定する、新しい設定フォームを追加できます。 新しい経費ワークスペースはこの機能で有効化され、以前の経費ワークスペースと置き換えられる、入力体験を向上させるランディング ページです。 

詳細は [経費レポートの再設計](https://go.microsoft.com/fwlink/?linkid=2087165) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

この Finance and Operations のリリースでは、拡張性をサポートするために多くの機能拡張が行われています。 たとえば、列挙体、メタデータ、メソッドに拡張性の機能拡張が行われています。 詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0.3 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10-3.md)を参照してください。

## <a name="tax-engine"></a>税エンジン

> [!NOTE]
> 税エンジン (GTE) は、現在のみインドのみで使用可能となっています。

### <a name="calculate-tax-in-accounting-currency-for-importexport-order"></a>受注をインポート/エクスポートし、会計通貨の税金の計算を行う

Finance and Operations の今回のリリースでは、**税設定パラメータ** ページに新しいパラメータが追加されました。これにより、インポート/エクスポートを行う注文に対して、税金を計算する通貨を選択できます。 既定では、 **トランザクション通貨** を使用して、インポート/エクスポートを行う注文に対し、計算する税金の通貨を選択できます。 既定では、 **トランザクション通貨** は元のシステム動作と同じです。 **会計通貨** を選択すると、システムが会計通貨の課税金額に基づいて税金を計算します。

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新についての詳細は、[ローカライズおよび規制機能 – 規制の更新](../../../finance/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations バージョン 10.0.3 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=320385&dbType=3&qc=d5539716f56ccea45e2187c269570772af20e1f10a78371811220da6315a3c34) を参照してください。

### <a name="platform-update-27"></a>プラットフォーム update 27
Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 には、プラットフォーム更新プログラム 27 が含まれています。 プラットフォーム更新プログラム 27 の詳細については、 [Dynamics 365 for Finance and Operationsプラットフォーム更新プログラム 27 (2019 年 6 月) の新機能または変更された機能について](whats-new-platform-update-27.md)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
