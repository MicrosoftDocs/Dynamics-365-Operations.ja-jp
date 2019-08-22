---
title: Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.1 の新機能または変更された機能について説明します。 このバージョンは 2018 年 10 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 11/06/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: b264a51c-52d1-45c5-b698-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Release 8.1
ms.openlocfilehash: 47383d413dc56a0478659d3e02df9f57e3b398f6
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863479"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-81-october-2018"></a>Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) の新機能または変更された機能について説明します。 このバージョンは 2018 年 10 月にリリースされ、ビルド番号は 8.1.136 です。

Microsoft Dynamics 365 for Retail の新機能と変更についての最新のリリースでについては、[Dynamics 365 for Retail の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new) を参照してください。

### <a name="announcing-the-dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノートの発表

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

## <a name="use-shared-number-sequences-to-copy-customers-or-vendors"></a>共有番号順序を使用して、顧客または仕入先をコピーする

共有番号順序を使用して、顧客 ID または仕入先 ID を割り当てることができます。 また、共有番号順序を使用して、同じ顧客 ID または仕入先 ID を維持したまま、法人間で顧客をコピーすることもできます。

追加の詳細については、[共有番号順序を使用して顧客をコピー](../../financials/accounts-receivable/copy-customer.md)および[共有番号順序を使用して仕入先をコピー](../../financials/accounts-payable/vendor-copy.md)を参照してください。

## <a name="customer-transactions-list-page"></a>顧客トランザクション リスト ページ

アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。 同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。

**グローバル トランザクション**ボタンが顧客ページに追加されました。 このボタンを使用して、すべての法人間で顧客のすべてのトランザクションを表示できます。 **顧客トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。

オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。

オープン顧客トランザクションの期日および割引日を更新することもでき、**顧客トランザクション**リスト ページに期日を追加できます。

詳細については、[顧客トランザクション リスト ページ](../../financials/accounts-receivable/customer-transactions-list-page.md)を参照してください。

## <a name="vendor-transaction-list-page"></a>仕入先トランザクション リスト ページ

アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。 同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。

**グローバル トランザクション**ボタンが仕入先ページに追加されました。 このボタンを使用して、すべての法人間で仕入先のすべてのトランザクションを表示できます。 **仕入先トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。

オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。 通貨換算のトランザクションを非表示にすることができる **通貨の再評価を非表示にする** フィルターが追加されました。

未処理の顧客トランザクションのために、期日および割引の日付を更新することもできます。 リリース 8.1 では、**仕入先トランザクション** リスト ページに期日を追加できるようにエクスペリエンスが改善されました。

詳細については、[仕入先トランザクション リスト ページ](../../financials/accounts-payable/vendor-transaction-list-page.md)を参照してください。

## <a name="financial-dimensions"></a>財務分析コード

顧客および仕入先などのマスター レコードの値は、新しい分析コードの既定値として使用できます。 新しい分析コードが作成されると、マスター レコード ID は、マスター レコードの分析コード値で入力されます。 たとえば、新しい顧客を作成するときに、顧客 ID は顧客分析コードで入力されます。 販売注文、請求書、または顧客 ID が必要なその他のドキュメントを作成するときは、既存の既定ルールが使用され、顧客 ID がドキュメントに追加されます。

ドキュメントにその分析コードを入力すると、他の分析コードの情報が自動的に入力されるように分析コードをコンフィギュレーションすることができます。 たとえば、コスト センター 10 を入力した場合、値 **20** が部門分析コードに自動的に入力されます。

エンティティを使用して、派生分析コードのセグメントと値を設定することができます。

詳細については、「[財務分析コード](../../financials/general-ledger/financial-dimensions.md)」を参照してください。

## <a name="dual-currency"></a>二重通貨

レポート通貨は、2 つ目の会計通貨として転用できるようになりました。 この機能は、二重通貨と呼ばれます。 二重通貨の変更を、コンフィギュレーション キーまたはパラメーターを通じて無効にはできません。 レポート通貨が 2 つ目の会計通貨として使用され、転記論理でのレポート通貨の計算方法が変更されたためです。

詳細については、[二重通貨](../../financials/general-ledger/dual-currency.md)を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、コマンド チェーン、委任、またはメンバーへのアクセスを提供することにより拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 さらに、列挙、メタデータ、および SQL 操作に拡張が加えられました。 詳細については、[Dynamics 365 for Finance and Operations バージョン 8.1 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-81.md)を参照してください。

## <a name="phantom-items"></a>ファントム品目

ファントム明細行タイプは、部品表 (BOM) および複数レベルの BOM 構造の明細行に対して使用できます。 ファントム BOM は、工順ネットワークのある BOM にも使用できます。

詳細については、[ファントム品目](../../supply-chain/production-control/phantom-items.md)を参照してください。

## <a name="russian-localization"></a>ロシア語のローカライズ

Dynamics 365 for Finance and Operations では、ロシアの必須規制要件がサポートされるようになりました (オンプレミス展開のみ)。 ロシア語ローカライズのこのリリースは、以下の機能領域が対象となっています: 買掛金勘定、売掛金勘定、前貸しホルダー、銀行および現金、クライアント銀行インターフェイスのエクスポート部分、固定資産、総勘定元帳と G/L 報告、財務報告書の電子報告、在庫、アドレス/FIAS、現金の移動、商品の移動、経費の評価、遅延経費、為替差異、仕掛品分野における VAT および利益税登録。

詳細については、[ロシア](../../financials/localizations/russia.md)を参照してください。

## <a name="vat-reporting-for-the-united-arab-emirates"></a>アラブ首長国連邦の VAT レポート

Finance and Operations の標準売上税機能は、アラブ首長国連邦の VAT 法の法律要件の大部分を満たすようになりました。 次の国固有の機能は、アラブ首長国連邦に固有です。

- VAT 報告で必要な追加のフィールドで、法人コンフィギュレーションが拡張されました。
- GCC 領土内の課税対象の国内工程を正しく記録するため、アラブ首長国連邦 (ARE 国コンテキスト) で VAT 逆請求機能が有効になりました。
- 追加の列および VAT 集計情報によって、追加の販売、請求書、および貸方票の印刷レイアウトが追加されました。
- アラブ首長国連邦の販売の請求書および貸方票は、ユーザー インターフェイスの新しい ar-AE アラビア語を含む 2 つの言語で印刷されるようになりました。
- VAT 還付申告レポートは、e-TAX FTA ポータルへのアップロードに対応する電子ファイル形式で印刷されます。
- 標準監査ファイル機能がアラブ首長国連邦のローカル機能と共有されました。 これは、bht 連邦税所轄官庁 FTA VAT 監査ファイル - (FAF) に必要であり、コンマ区切りファイル形式にエクスポートできます。
