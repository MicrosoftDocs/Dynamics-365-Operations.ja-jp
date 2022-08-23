---
title: 電子メッセージ
description: この記事では、Microsoft Microsoft Dynamics 365 Finance の電子メッセージの概要および設定情報を提供します。
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3e2fe6a70d449adea07f5aa0db9e625f0378d8c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283457"
---
# <a name="electronic-messaging"></a>電子メッセージ

[!include [banner](../includes/banner.md)]

この記事では、**電子メッセージ** (EM) 機能の概要および設定情報を提供します。

最近では、世界中の様々な国や地域の政府および立法当局が、それらの国または地域に登録されている企業の報告要件を実施しています。 要件の目的は、それらの企業から電子フォーマットで、会計、保管、処理されたシステムから直接、データを取得できるようにするためです。

Microsoft Microsoft Dynamics 365 Finance の EM 機能は、Finance と、政府および立法当局が提供する公式情報の報告、送信および受信のために提供するシステムの間の様々な電子相互運用をサポートします。

EM 機能は、**電子申告** (ER) モジュールと統合されています。 電子メッセージの ER 形式を設定することができます。 詳細については、[電子申告 (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)を参照してください。

## <a name="basic-concepts-for-em-functionality"></a>EM 機能の基本概念

EM 機能は、次のエンティティに基づいています:

- **電子メッセージ** – 税務署に送信するレポートなど、内部でレポートおよび送信されるべきレポートまたは申告。
- **電子メッセージ項目** – レポートされるメッセージに含める必要があるレコード。
- **電子メッセージの処理** – 必要なデータを収集し、レポートを生成し、Azure BLOB ストレージにデータを格納し、システム外部にレポートを送信し、システム外部から応答を受信し、受信した情報に基づいてデータベースを更新する一連のアクション。 チェーンのアクションは、リンクまたはリンク解除できます。

次の図は、EM のフローを示します。

![電子メッセージのデータ フロー。](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM 機能でサポートされるシナリオ

EM 機能は、次のシナリオをサポートしています。

- 様々なタイプの関連するエクスポート ER 形式に基づいて、メッセージを手動で作成し、レポートを生成します。 これらのタイプには、Microsoft Excel、XML、JavaScript Object Notation (JAVA)、PDF、テキスト、および Microsoft Word が含まれます。
- 関連するインポート ER 形式を使用して機関から要求および受信されたメッセージを、自動的に作成し処理します。
- メッセージ項目として、データ ソースからの情報を収集し処理します。 データ ソースは、Finance テーブルです。
- 追加の情報を格納し、メッセージまたはメッセージ項目に関連して特別に定義された実行可能なクラスを呼び出すことによってさまざまな値を評価します。
- メッセージ項目に収集された情報を集計し、その情報をメッセージごとに分割し、関連するエクスポート ER 形式のレポートを生成します。
- Azure Key Vault に格納されているセキュリティ情報を使用して、生成されたレポートをWeb サービスに送信します。
- 必要に応じて、Web サービスからの応答の受信、応答の解釈、Finance のデータの更新を行います。
- 生成されたすべてのレポートを格納して確認します。
- メッセージまたはメッセージ項目に対して実行されるアクションに関連するすべてのログ情報を格納して確認します。
- さまざまなメッセージの状態およびメッセージ項目の状態を使用して、処理をコントロールします。

## <a name="security-privileges"></a>セキュリティ権限

電子メッセージに対して、次のセキュリティ権限が使用可能です。

| セキュリティ権限           | アクセス レベル | 関連 |
|------------------------------|--------------|-------------|
| 電子メッセージの管理 | この権限により、EM 機能への完全なアクセス権があります。 この権限がある場合、電子メッセージを設定し、すべての処理を実行することができます。 | この権限は、**売上税トランザクションの管理** セキュリティ職務権限に含まれています。 この職務権限は、**経理担当** セキュリティ ロールに含まれています。 |
| 電子メッセージの表示     | この権限により、EM 機能への読み取り専用アクセス権があります。 この特権がある場合、電子メッセージの設定とメッセージを表示することができます。 ただし、設定または実行を行うことはできません。 | この権限は、**売上税トランザクション状態の照会** セキュリティ職務権限に含まれています。 この職務権限は、次のセキュリティ ロールに含まれています。<ul><li>取立マネージャー</li><li>売掛金管理係</li><li>売掛金管理マネージャー</li><li>税経理担当</li><li>経理担当</li><li>会計マネージャー</li><li>会計監修者</li><li>販売マネージャー</li><li>買掛金勘定係</li></ul> |
| 電子メッセージの処理  | この権限により、**電子メッセージ** および **電子メッセージ項目** ページのみへのアクセス権があります。 この権限がある場合、それらのページから呼び出される処理すべてを実行することができます。 | この権限は、**電子メッセージの処理** セキュリティ職務権限に含まれています。 この職務権限は、**電子メッセージオペレーター** セキュリティ ロールに含まれています。 |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM 機能によってサポートされる国固有の規制機能

次の表では、EM 機能でサポートされている一部の国固有の規制機能に関する情報を提供します。

| 国     | 機能名 | 機能のデモ記録 |
|-------------|--------------|------------------------|
| スペイン       | [VAT に関する情報の即時提供 (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| ハンガリー     | [オンライン請求システム](../localizations/emea-hun-online-invoicing.md) | |
| イギリス | [税のデジタル化 (MTD) – VAT 明細書の提出の変更](../localizations/emea-gbr-mtd-vat-integration.md) | [財務と運用: 英国のデジタル税 ― Dynamics 365 における VAT 申告](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| リトアニア   | [i.SAF の報告](../localizations/emea-ltu-isaf.md) | |
| ポーランド      | [レジスターを使用した VAT 申告 (JPK_V7M、VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK VAT 監査レジスター](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| オランダ | [オランダの VAT 申告](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| チェコ共和国 | [VAT 申告](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| ブラジル      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| ロシア      | [VAT 申告](../localizations/rus-vat-declaration.md) | |
| ロシア      | [電子形式の会計レポート](../localizations/rus-accounting-reporting.md) | |
| ロシア      | [利益税申告](../localizations/rus-profit-tax-declaration.md) | |
| ロシア      | [評価税申告](../localizations/rus-assessed-tax-declaration.md) | |
| ロシア      | [輸送税申告](../localizations/rus-transport-tax-declaration.md) | |
| ロシア      | [土地税の申告](../localizations/rus-land-tax-declaration.md) | |
| ノルウェー      | [Altinn に直接送信される VAT 還付](../localizations/emea-nor-vat-return.md) | [Dynamics 365 Financeで Altinn に直接提出できる新しい VAT 還付](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| フランス      | [VAT 申告 (フランス)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| オーストリア     | [VAT 申告 (オーストリア)](../localizations/emea-aut-vat-declaration-austria.md) | |
| ドイツ     | [VAT 申告 (ドイツ)](../localizations/emea-deu-vat-declaration-germany.md) | |
| オランダ | [オランダの VAT 申告](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| スウェーデン      | [VAT 申告 (スウェーデン)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| スイス | [VAT 申告 (スイス)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


