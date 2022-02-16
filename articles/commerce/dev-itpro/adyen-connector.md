---
title: Adyen 向け Dynamics 365 Payment Connector の概要
description: このトピックでは、Adyen 向け Microsoft Dynamics 365 Payment Connector の概要について説明します。
author: rassadi
ms.date: 12/20/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 97377d5e154360fddba566451abb6eb4f83ae482
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984181"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Adyen 向け Dynamics 365 Payment Connector の概要

[!include [banner](../includes/banner.md)]

このトピックでは、Adyen 向けの Microsoft Dynamics 365 Payment Connector の概要と、サポートされる機能の包括的な一覧を示します。 関連トピックでは、Adyen のサインアップ、コネクタのコンフィギュレーション、よく寄せられる質問、一般的な問題に関するトラブルシューティングのガイダンスを提供します。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| 支払コネクタ | Microsoft Dynamics 365 Commerce (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。 このトピックで説明されているコネクタは、標準の支払ソフトウェア開発キット (SDK) を使用して実装されました。 |
| カードあり | Dynamics 365 販売時点管理への支払ターミナル コネクタで物理的なカードが提示および使用される支払トランザクションを参照します。 |
| カードなし | 電子商取引またはコール センター シナリオなど、現物カードが提示されない支払トランザクションを参照します。 これらのシナリオでは、支払に関連する情報は、電子商取引 Web サイト、コール センター フロー、または販売時点管理上または支払ターミナルで手動で入力されます。 |

## <a name="supported-features-functionality-versions-and-terminals"></a>サポートされているフィーチャ、機能、バージョン、およびターミナル

独創的な Adyen 向け Dynamics 365 Payment Connector は標準支払 SDK を使用します。 そのため、他の支払コネクタのために使用することができない特別な機能はありません。

### <a name="supported-versions"></a>サポートされているバージョン

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 のサポートされているバージョン
ファーストパーティーの独創的な Adyen 向け Dynamics 365 Payment Connector は Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.3 (2019 年 1 月) またはそれ以降、および Microsoft Dynamics 365 Retail バージョン 8.1.3 またはそれ以降でサポートされます。 ただし、サード パーティは Microsoft Dynamics 365 の初期バージョンのために他の Adyen 用支払コネクタを開発することができます。

#### <a name="supported-adyen-firmware-versions"></a>サポートされている Adyen ファームウェア バージョン
次の表は、Microsoft Dynamics 365 Retail POS の各バージョンでサポートされている最小および最大の Adyen ファームウェア バージョンを示しています。

---

# <a name="10019"></a>[10.0.19](#tab/10-0-19)
### <a name="dynamics-365-retail-pos-version-10019"></a>Dynamics 365 Retail POS バージョン 10.0.19
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_59p7 | adyen_v1_64p7 |
| | *注: ギフト カードのキャッシュ アウトに関する詳細については、以下を参照してください* |

# <a name="10020"></a>[10.0.20](#tab/10-0-20)
### <a name="dynamics-365-retail-pos-version-10020"></a>Dynamics 365 Retail POS バージョン 10.0.20
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_62p9 | adyen_v1_64p7 |
| | *注: ギフト カードのキャッシュ アウトに関する詳細については、以下を参照してください* |

# <a name="10021"></a>[10.0.21](#tab/10-0-21)
### <a name="dynamics-365-retail-pos-version-10021"></a>Dynamics 365 Retail POS バージョン 10.0.21
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_64p7 | adyen_v1_65p8 |
| | *注: ギフト カードのキャッシュ アウトに関する詳細については、以下を参照してください* |

# <a name="10022"></a>[10.0.22](#tab/10-0-22)
### <a name="dynamics-365-retail-pos-version-10022"></a>Dynamics 365 Retail POS バージョン 10.0.22
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_65p8 | adyen_v1_67p10 |

# <a name="10023"></a>[10.0.23](#tab/10-0-23)
### <a name="dynamics-365-retail-pos-version-10023"></a>Dynamics 365 Retail POS バージョン 10.0.23
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_69p5 | adyen_v1_71p10 |

# <a name="10024"></a>[10.0.24](#tab/10-0-24)
### <a name="dynamics-365-retail-pos-version-10024"></a>Dynamics 365 Retail POS バージョン 10.0.24
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_69p5 | adyen_v1_71p10 |

---

> [!NOTE]
> Adyen では、Microsoft がメジャー バージョンをテストした後にマイナー バージョンの更新をリリースする場合があります。 メジャー バージョンがサポートされている限り、同じメジャー バージョン内でマイナー バージョンの更新を行うことができます。 通常これらの更新プログラムは、特定の問題のみを修正するプログラムであり、同じメジャー ファームウェア バージョンが以前にテストされている場合においては、完全な再テスト基準に達するテストを行ってはいません。 更新が、ドキュメントに表示されている最大 Adyen ファームウェア バージョンを超える必要はありません。 
>
> バージョン 53より前の Adyen ファームウェア バージョンからバージョン 53に移行する場合は、POS KB **4577957** が Commerce、バージョン10.0.11 から 10.0.14 の更新をする必要があります。 これらのバージョンのいずれかが使用されていて、修正プログラムが含まれていない場合、アップグレード後の支払ターミナルは、NFC 経由での支払のみを許可します。 POS に修正プログラムを適用すると、この問題が解決されます。 POS バージョンがバージョン 10.0.11より古い場合、サポート要求を提出して、MPOS が利用できないため KB **4577957** の修正が必要であることを示します。
> 
> Adyen ファームウェアのバージョンが 59p7 ~ 62p9 の場合、**ギフト カード のキャッシュ アウト** 操作では、ギフト カードを手動で入力する場合に PIN の入力を 2 回要求します。 この問題は、ギフト カードを読み取る時点では再現されません。 Adyen は調査しています。 

### <a name="supported-payment-terminals"></a>サポートされる支払端末
Adyen 向け Dynamics 365 Payment Connector はデバイスに依存しない [Adyen 支払端末 API](https://www.adyen.com/blog/introducing-the-terminal-api) を活用します。 このアプリケーション プログラミング インターフェイス (API) がサポートするすべての支払端末をサポートします。 サポート対象の支払端末の完全な一覧については、[Adyen POS 端末](https://www.adyen.com/pos-payments/terminals)ページを参照してください。

### <a name="supported-payment-instruments"></a>サポートされる支払機器

#### <a name="supported-debit-and-credit-cards"></a>サポートされているデビット カードまたはクレジット カード

| ブランド | バリアント | カードあり | 電子商取引 | コール センター |
|---|---|:-:|:-:|:-:|
| MasterCard | クレジット | ✔ | ✔ | ✔ |
| MasterCard | デビット | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | クレジット | ✔ | ✔ | ✔ |
| VISA | デビット | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | クレジット | ✔ | ✔ | ✔ |
| AMEX | デビット | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| 検出 | 標準 | ✔ | ✔ | ✔ |
| 検出 | Android Pay | ✔ |  |  |
| 検出 | Apple Pay | ✔ |  |  |
| 検出 | Samsung Pay | ✔ |  |  |
| Diners | 標準 | ✔ | ✔ | ✔ |
| Dineromail | 標準 | ✔ | ✔ | ✔ |
| JCB | 標準 | ✔ | ✔ | ✔ |
| Union Pay \* | 標準 | ✔ |  |  |
| Interac Debit\* | 標準 | ✔ |  |  |

\* Interac と Union Pay の定型カード トークンは Adyen から提供されていないため、カードが存在しない取引では対応していません。

#### <a name="supported-gift-cards"></a>サポートされるギフト カード
| スキーム | カードあり | カードなし |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

Adyen 向け Dynamics 365 Payment Connector を介してこれらの外部ギフト カード スキーマをサポートするには、追加手順完了する必要があります。 詳細については、[外部ギフト カードのサポート](/dynamics365/unified-operations/retail/dev-itpro/gift-card)を参照してください。

#### <a name="supported-wallets"></a>サポートされる wallet

| スキーム | カードあり | カードなし |
|---|---|---|
| Alipay | 将来のリリースでサポートが追加されます。 | 無 |
| WeChat | 将来のリリースでサポートが追加されます。 | いいえ |

#### <a name="supported-card-present-input-methods"></a>サポートされているカード提示入力方法
| 入力方法 | サポート | 摘要 |
|---|:-:|---|
| ディップ | ✔ | |
| 読み取る | ✔ | |
| タップ | ✔ | |
| POS UI を通じて手動入力。 |  | 今回は、サポートされていません |
| 支払ターミナルを通じて手動入力。 | ✔ | クレジット、デビット、および暗証番号入力のギフト カードにおける手動入力をサポートします。 | 


#### <a name="supported-card-present-countries"></a>カード提示がサポートされている国

次の国には、Adyen のカード サポートと共に、使用可能なコマース コンポーネントがあります。 コマースの現在の国際的な利用可能性については、[国際的な利用可能性ページ](/dynamics365/get-started/availability) を参照してください。

| 国 | サポート |
| --- | :-: |
| オーストラリア | ✔ |
| オーストリア | ✔ |
| ベルギー | ✔ |
| カナダ | ✔ |
| チェコ共和国 | ✔ |
| デンマーク | ✔ |
| エストニア | ✔ |
| フィンランド | ✔ |
| フランス | ✔ |
| ドイツ | ✔ |
| 香港特別行政区 | ✔ |
| ハンガリー | ✔ |
| アイスランド | ✔ |
| アイルランド | ✔ |
| イタリア | ✔ |
| ラトビア | ✔ |
| リトアニア | ✔ |
| マレーシア | ✔ |
| オランダ | ✔ |
| ノルウェー | ✔ |
| ポーランド | ✔ |
| シンガポール | ✔ |
| スイス | ✔ |
| スペイン | ✔ |
| スウェーデン | ✔ |
| スイス | ✔ |
| 英国 | ✔ |
| 米国 | ✔ |
| ブラジル | 将来のリリース |

#### <a name="supported-card-not-present-countries"></a>カード不提示がサポートされている国

次の国では、Adyen はカードを使用しない取引をサポートします。 特定の国のサポートの詳細については、[Adyen 連絡先 ](https://www.adyen.com/contact/sales) に問い合わせください。 コマースの現在の国際的な利用可能性については、[国際的な利用可能性ページ](/dynamics365/get-started/availability) を参照してください。

| 国 | 
| --- |
| アルゼンチン |
| アルメニア |
| オーストラリア |
| オーストリア |
| バーレーン |
| ベルギー |
| ブラジル |
| ブルガリア |
| カナダ |
| チリ |
| 中国 |
| コロンビア |
| クロアチア |
| キプロス |
| チェコ共和国  |
| デンマーク |
| エジプト |
| エストニア |
| フィンランド |
| フランス |
| ジョージア |
| ドイツ |
| ジブラルタル |
| ギリシャ |
| ガーンジー |
| 香港特別行政区 |
| ハンガリー |
| アイスランド |
| インド |
| インドネシア |
| アイルランド |
| マン島 |
| イスラエル |
| イタリア |
| 日本 |
| ジャージー島 |
| 韓国 |
| クウェート |
| ラトビア |
| リトアニア |
| ルクセンブルク |
| マレーシア |
| マルタ |
| メキシコ |
| モロッコ |
| オランダ |
| ニュージーランド |
| ノルウェー |
| ペルー |
| ポーランド |
| ポルトガル |
| カタール |
| ルーマニア |
| サウジアラビア |
| セルビア |
| シンガポール |
| スロバキア |
| スロベニア |
| 南アフリカ |
| スペイン |
| スウェーデン |
| スイス |
| 台湾 |
| タンザニア |
| タイ |
| トルコ |
| アラブ首長国連邦 (UAE) |
| 英国 |
| プエルトリコを含むアメリカ合衆国  |

#### <a name="supported-dynamics-365-payment-features"></a>サポートされる Dynamics 365 支払フィーチャ

次の表は、Adyen 向け Dynamics 365 Payment Connector がサポートする一連のフィーチャを示します。 これらのフィーチャは、2018 年 12 月に支払 SDK および一部のコンポーネントで導入された拡張機能を使用します。 それらは Adyen 向け Dynamics 365 Payment Connector 専用ではありません。 異なる支払端末に対するこれらの拡張機能を取得する方法の詳細については、[支払端末のエンドツーエンド支払統合を作成する](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension)を参照してください。

| スキーム | カードあり | カードなし |
|---|:-:|:-:|
| [ギフト カードの残高を清算する](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [重複支払保護](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| オムニ チャネルのトークン化 | ✔ | ✔ |
| リンクされた払戻 | ✔<br>(10.0.1 以降) | ✔<br>(10.0.1 以降) |
| [オンライン支払の保存](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(10.0.2 以降) | 
| [コール センターおよび電子商取引の外部ギフト カード](./gift-card.md) | ✔<br>(10.0.10 以降) | 
| [SCA 支払リダイレクト](../adyen_redirect.md) | | ✔<br>(10.0.12 以降) |
| [専用の支払ターミナルおよびプリンターとキャッシュ ドロワーのプロンプト](../pos-multi-hws.md) | ✔<br>(10.0.12 以降) | |
| [Adyen コネクタによる SDK レベルのチップ サポート](tipping.md) | ✔<br>(10.0.14 以降) | |
| [注文請求の増分取得](incremental-capture.md) |  | ✔<br>(10.0.18 以降) |

## <a name="next-steps"></a>次のステップ

Adyen 向け Dynamics 365 Payment Connector のサインアップおよび構成方法についての詳細は、[Adyen 向け Dynamics 365 Payment Connector](adyen-connector-setup.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector の設定](adyen-connector-setup.md)

[Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問](adyen-connector-faq.md)

[Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
