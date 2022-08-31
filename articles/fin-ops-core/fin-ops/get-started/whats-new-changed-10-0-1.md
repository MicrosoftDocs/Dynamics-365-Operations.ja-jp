---
title: Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能
description: この記事では、Dynamics 365 財務と運用バージョン 10.0.1 の新機能または変更された機能について説明します。 このバージョンは 4 月にリリースされます。
author: sericks007
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.1
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b4aaf8dea774299ce87bffc11a10692c0d1aad8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267756"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1001-april-2019"></a>Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 財務と運用バージョン 10.0.1 の新機能または変更された機能について説明します。 このバージョンは 4 月にリリースされ、ビルド番号は 10.0.51 です。 バージョン 10.0.1 の詳細については [追加リソース](whats-new-changed-10-0-1.md#additional-resources) を参照してください。

Retail の最新のリリースの新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.1 の新機能と変更](../../../commerce/get-started/whats-new-10-0-1.md) を参照してください。


## <a name="enable-edit-for-externally-maintained-fields"></a>外部管理フィールドの編集を有効化

見込顧客リストの現金化への統合など、外部システムとの統合シナリオのため、グローバル アドレス帳および顧客レコードの特定のフィールドは、外部システムで管理されることを予想して外部管理とマークされています。 **外部管理フィールドの編集を有効化** オプションがグローバル アドレス帳パラメータ (**組織管理 > グローバル アドレス帳 > グローバル アドレス帳パラメータ**) に既定値の **いいえ** で追加されました。  ユーザー シナリオでこれらのフィールドを外部管理の場合も編集可能にする必要がある場合は、値を **はい** に設定できます。

## <a name="russian-features"></a>ロシア用の機能

### <a name="journal-of-alcohol-sales"></a>アルコール販売の仕訳帳
この機能は法定形式のアルコール小売販売の仕訳帳の印刷を含みます。

### <a name="electronic-format-of-accounting-reporting"></a>会計レポートの電子形式
電子申告コンフィギュレーションが利用可能です。 これを使用すると、電子形式で会計レポートを生成したり、構成された財務諸表に基づいて計算したデータを保持できます。 詳細については [電子形式の会計レポート (ロシア)](../../../finance/localizations/rus-accounting-reporting.md) を参照してください。

[財務諸表 (ロシア)](../../../finance/localizations/rus-financial-reports.md) で次の作業を行う方法に関する情報を見つけることができます:
- 財務諸表を設定します。
- 財務諸表の計算結果を使用するように電子申告を構成します。
- 財務諸表を生成し結果を保存するように電子メッセージを構成します。

Excel で財務諸表の印刷を構成する方法の詳細は [Excel での財務諸表のコンフィギュレーション (ロシア)](../../../finance/localizations/rus-excel-financial-report.md) を参照してください。

### <a name="assessed-tax-registers-and-electronic-format-of-declaration-version-505-2019"></a>評価税登録および申告バージョン 5.05 (2019) の電子形式
この機能を使用すると、2019 年の報告から適用可能な、不動産資産に関する技術情報および税務情報の保管、評価税登録の計算、および電子形式で評価税申告の生成が可能になります。 詳細については [評価税申告 (ロシア)](../../../finance/localizations/rus-assessed-tax-declaration.md) を参照してください。

### <a name="transport-tax-registers-and-electronic-format-of-declaration"></a>輸送税登録および申告の電子形式
この機能を使用して、車両の技術情報および税務情報を保持し、輸送税登録を計算し、電子形式で輸送税申告を生成することができます。

### <a name="land-tax-registers-and-electronic-format-of-declaration-version-506-2018"></a>土地税登録および申告バージョン 5.06 (2018) の電子形式
この機能を使用すると、2018 年の年次報告から適用可能な、土地面積に関する技術情報および税務情報の保管、土地税登録の計算、および電子形式で土地税申告の生成が可能になります。

### <a name="vat-declaration-in-electronic-format-version-506-2019"></a>電子形式の VAT 申告バージョン 5.06 (2019)
この機能によって 2019 年の報告から適用可能な XML 形式の VAT 明細書を生成できます。
詳細については [VAT 申告 (ロシア)](../../../finance/localizations/rus-VAT-declaration.md) を参照してください。

### <a name="sales-purchase-books-and-factures-journals-in-electronic-format-2019"></a>販売、購買帳簿、Facture 仕訳帳の電子形式 (2019)
この機能により、販売、購買帳簿、factures 仕訳帳を 2019 年から適用される電子形式で生成できます。 販売および購買帳簿の作業方法の詳細は [売上帳簿、購買帳簿、請求書 Facture 仕訳帳](../../../finance/localizations/rus-sales-books-purchase-books.md) を参照してください。

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[規制の更新](../../../finance/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

## <a name="extensibility-enhancements"></a>拡張性の強化

このFinance and Operations のリリースでは、拡張性をサポートするために多くの機能拡張が行われています。 たとえば、列挙体、メタデータ、メソッドに拡張性の機能拡張が行われています。 詳細については、[Dynamics 365 Financeバージョン 10.0.1 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-10-1.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0.1 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=299640&dbType=3&qc=2da6de70aab0f4c61b0f920b3242211f5043697189d50a6e1fb1ac3d27ee5f78)を参照してください。

### <a name="platform-update-25"></a>プラットフォーム update 25
プラットフォーム更新プログラム 25 を含む Microsoft Dynamics 365 財務と運用バージョン10.0.1。 プラットフォーム更新プロフラム 25 の詳細ついては [Dynamics 365 財務と運用プラットフォーム更新プログラム 25 の新機能や変更 (2019 年 4 月)](whats-new-platform-25.md) を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事では、Dynamics 365 Finance の削除済みまたは非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

