---
title: "Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.1.2 の新機能または変更された機能について説明します。 このバージョンは 2018 年 12 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: b364a31d-52de-45c5-b698-64c5262c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Release 8.1.2
ms.translationtype: HT
ms.sourcegitcommit: 9290114388b210dfdfd980e293df2e21d0aa50ea
ms.openlocfilehash: 2a16ab6d2d240205a02c0c5a34f144e1bdb76a04
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-812-december-2018"></a>Dynamics 365 for Finance and Operations バージョン 8.1.2 (2018 年 12 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.2 の新機能または変更された機能について説明します。 このバージョンは 2018 年 12 月にリリースされ、ビルド番号は 8.1.195 です。

Microsoft Dynamics 365 for Retail の最新リリースの新機能と変更については、[Dynamics 365 for Retail の新機能と変更点](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new)を参照してください。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

## <a name="bug-fixes"></a>バグ修正

プラットフォーム更新 22 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2037783)を参照してください。

## <a name="platform-update-22"></a>プラットフォーム update 22

プラットフォーム更新プログラム 22 を含む Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.2。 プラットフォーム更新プログラム 21 に関する詳細については、[Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能](whats-new-platform-update-22.md) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳しくは、[Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-812.md)をご覧ください。

## <a name="derived-dimension-values"></a>派生分析コード値

今回のリリースには、派生した分析コード値の変更を防止し、派生した分析コード値で既存の分析コード値を上書きできるようにする機能が含まれています。 詳細については、「[財務分析コード](../../financials/general-ledger/financial-dimensions.md)」を参照してください。

## <a name="intrastat-format-changes-for-belgium"></a>ベルギーのイントラスタット形式の変更
今回のリリースには、2019 年の報告に適用されるベルギーの XML イントラスタット形式への変更が含まれています。 新しい形式を適用するには、LCS 共有資産ライブラリから ER コンフィギュレーションの次のバージョン (またはそれ以降のバージョン) をインポートする必要があります: Intrastat (BE).version.2.6.xml。 コンフィギュレーションをインポートする方法の詳細については、[Lifecycle Services からコンフィギュレーションをインポートする](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md)を参照してください。 

## <a name="russian-specific-features"></a>ロシア固有の機能
今回のリリースには、ロシアの固有の次の機能が含まれています。

### <a name="third-party-miscellaneous-charges-for-russia"></a>ロシアのサード パーティの雑費
- 購入済商品の原価に含める (他の仕入先からの請求書の明細行に配賦)。 
- 第三者に再振出。 
- その他の経費勘定の再割り当て。

### <a name="bailment-for-russia"></a>ロシアの寄託

**受託者側の会計**
 - 法律によって必要とされる、委託の場合の在庫受領書の会計および基本フォーム MX-1 の生成。 
 - 委託された在庫入庫の会計、基本フォーム MX-3 の委託と生成。 
 - 受託者側の委託原価計算。
 
 **所有者側の会計**
 - 寄託への在庫移動、および寄託サービス契約に基づく商品の所有者側での寄託から在庫への返品の会計。

### <a name="goods-in-transit-for-russia"></a>ロシアの輸送中の商品

**プロパティの受け渡しが延期された顧客への販売**
 - 延期されたプロパティの移動を含む販売後の請求書。 つまり、顧客債務が転記されず、すべての支払税が転記され、品目は流通倉庫に転送されます。 
 - 負債が転記されたプロパティの受け渡し、および流通倉庫からの品目の販売を登録します。

**仕入先からの輸送中の商品**
 - 品目タイプが "輸送の間の購買済品目" の特別な転記プロファイルによる仕入先からの輸送中の商品の登録。 
 - 輸送中の在の保有法の作成 (INV-6)。

### <a name="optional-posting-of-transfer-orders-to-general-ledger"></a>オプションの一般会計への移動オーダーの転記
移動オーダーを転記する場合に、総勘定元帳に転記する、または転記しないというオプション。

### <a name="profit-tax-registers-for-assets"></a>資産の利益税登録
次の税登録を使用できます。
 - **商品原価計算**
 - **FA オブジェクト情報** 
 - **IA オブジェクト情報** 
 - **FA 減価償却** 
 - **IA 減価償却** 
 - **FA/IA 販売**
 - **減価償却特別復旧**

### <a name="sales-purchase-books-additional-sheets-invoice-factures-journal-in-electronic-format"></a>販売、購買帳簿、追加シート、電子形式の請求書 Facture 仕訳帳
今回のリリースでは、販売の電子形式、購買帳簿、他のシート、電子申告で構成されている Facture の仕訳帳。 

新しい形式を適用するには、LCS 共有資産ライブラリから ER コンフィギュレーションの次のバージョンまたはそれ以上のバージョンをインポートする必要があります。  
 - VAT 申告モデル (RU).version.46
 - VAT 申告モデル マッピング (RU).version.46.70
 - 仕入帳形式.version.46.13
 - 売上帳簿形式.version.46.13
 - 購買帳簿追加シート形式.version.46.9
 - 売上帳簿追加シート形式.version.46.9
 - Facture 仕訳帳format.version.46.4
 
詳細については、[Lifecycle Services からのコンフィギュレーションのインポート](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md) を参照してください。 

これらのコンフィギュレーション バージョンは、パブリック プレビューとしてリリースされ、受け取ったフィードバックに基づいて更新されます。 これらを使用して、販売の電子形式、購買帳簿、他のシート、Facture の仕訳帳がどのように電子申告で構成されているかを参照してください。 実際の環境で派生したカスタム コンフィギュレーションの基本コンフィギュレーションとしてこれらのコンフィギュレーションを使用しないでください。

詳細については、[売上帳簿、購買帳簿、および請求書 Facture 仕訳帳](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/rus-sales-books-purchase-books)を参照してください。


