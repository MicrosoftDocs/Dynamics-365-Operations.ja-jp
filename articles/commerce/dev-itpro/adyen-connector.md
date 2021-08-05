---
title: Adyen 向け Dynamics 365 Payment Connector
description: このトピックでは、Adyen 向け Microsoft Dynamics 365 Payment Connector の概要について説明します。
author: rassadi
ms.date: 07/07/2021
ms.topic: article
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
ms.openlocfilehash: da33ee2ecaffcfe464985d617f45dc4d7683a6a3
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433682"
---
# <a name="dynamics-365-payment-connector-for-adyen"></a>Adyen 向け Dynamics 365 Payment Connector

[!include [banner](../includes/banner.md)]

このトピックでは、Adyen 向け Microsoft Dynamics 365 Payment Connector の概要について説明します。 これには、サポートされているフィーチャおよび機能、コネクタの設定および構成のガイド、トラブルシューティング情報、および一般的な一部の問題に関する説明の包括的な一覧が含まれます。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| 支払コネクタ | Microsoft Dynamics 365 Commerce (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。 このトピックで説明されているコネクタは、標準の支払ソフトウェア開発キット (SDK) を使用して実装されました。 |
| カードあり | Dynamics 365 販売時点管理への支払ターミナル コネクタで物理的なカードが提示および使用される支払トランザクションを参照します。 |
| カードなし | 電子商取引またはコール センター シナリオなど、現物カードが提示されない支払トランザクションを参照します。 これらのシナリオでは、支払に関連する情報は、電子商取引 Web サイト、コール センター フロー、または販売時点管理上または支払ターミナルで手動で入力されます。 |

## <a name="overview"></a>概要

このトピックには、Adyen 向け Dynamics 365 Payment Connector の評価およびセットアップを支援するための以下のメイン セクションが含まれています。

- サポートされている仕様、機能、バージョン、およびターミナル – このセクションでは、Adyen 向け Dynamics 365 Payment Connector がサポートする一連の仕様および機能について説明します。
- Adyen でサイン アップ – このセクションでは Adyen でマーチャント口座にサイン アップする方法について説明します。
- 設定およびコンフィギュレーション – このセクションでは、販売時点管理 (POS)、コール センター、および電子商取引チャネルで Adyen 向け Dynamics 365 Payment Connector を設定およびコンフィギュレーションする方法について詳細に説明します。

## <a name="supported-features-functionality-versions-and-terminals"></a>サポートされているフィーチャ、機能、バージョン、およびターミナル

独創的な Adyen 向け Dynamics 365 Payment Connector は標準支払 SDK を使用します。 そのため、他の支払コネクタのために使用することができない特別な機能はありません。

### <a name="supported-versions"></a>サポートされているバージョン

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 のサポートされているバージョン
ファーストパーティーの独創的な Adyen 向け Dynamics 365 Payment Connector は Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.3 (2019 年 1 月) またはそれ以降、および Microsoft Dynamics 365 Retail バージョン 8.1.3 またはそれ以降でサポートされます。 ただし、サード パーティは Microsoft Dynamics 365 の初期バージョンのために他の Adyen 用支払コネクタを開発することができます。

#### <a name="supported-adyen-firmware-versions"></a>サポートされている Adyen ファームウェア バージョン
次の表は、Microsoft Dynamics 365 Retail POS の各バージョンでサポートされている最小および最大の Adyen ファームウェア バージョンを示しています。

---

# <a name="1009"></a>[10.0.9](#tab/10-0-9)
### <a name="dynamics-365-retail-pos-version-1009"></a>Dynamics 365 Retail POS バージョン 10.0.9
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_45p9 | adyen_v1_48p6 |

# <a name="10010"></a>[10.0.10](#tab/10-0-10)
### <a name="dynamics-365-retail-pos-version-10010"></a>Dynamics 365 Retail POS バージョン 10.0.10
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_45p9 | adyen_v1_51p7 |

# <a name="10011"></a>[10.0.11](#tab/10-0-11)
### <a name="dynamics-365-retail-pos-version-10011"></a>Dynamics 365 Retail POS バージョン 10.0.11
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_45p9 | adyen_v1_56p5 |

# <a name="10012"></a>[10.0.12](#tab/10-0-12)
### <a name="dynamics-365-retail-pos-version-10012"></a>Dynamics 365 Retail POS バージョン 10.0.12
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_48p7 | adyen_v1_56p5 |

# <a name="10013"></a>[10.0.13](#tab/10-0-13)
### <a name="dynamics-365-retail-pos-version-10013"></a>Dynamics 365 Retail POS バージョン 10.0.13
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_51p7 | adyen_v1_56p5 |

# <a name="10014"></a>[10.0.14](#tab/10-0-14)
### <a name="dynamics-365-retail-pos-version-10014"></a>Dynamics 365 Retail POS バージョン 10.0.14
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_56p5 | adyen_v1_56p9 |

# <a name="10015"></a>[10.0.15](#tab/10-0-15)
### <a name="dynamics-365-retail-pos-version-10015"></a>Dynamics 365 Retail POS バージョン 10.0.15
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_56p9 | adyen_v1_56p9 |

# <a name="10016"></a>[10.0.16](#tab/10-0-16)
### <a name="dynamics-365-retail-pos-version-10016"></a>Dynamics 365 Retail POS バージョン 10.0.16
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_56p9 | adyen_v1_56p9 |

# <a name="10017"></a>[10.0.17](#tab/10-0-17)
### <a name="dynamics-365-retail-pos-version-10017"></a>Dynamics 365 Retail POS バージョン 10.0.17
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_59p7 | adyen_v1_59p7 |
| | *注: ギフト カードのキャッシュ アウトに関する詳細については、以下を参照してください。* |

# <a name="10018"></a>[10.0.18](#tab/10-0-18)
### <a name="dynamics-365-retail-pos-version-10018"></a>Dynamics 365 Retail POS バージョン 10.0.18
| 最小 Adyen ファームウェア バージョン | 最大 Adyen ファームウェア バージョン |
| --- | --- |
| adyen_v1_59p7 | adyen_v1_64p7 |
| | *注: ギフト カードのキャッシュ アウトに関する詳細については、以下を参照してください* |

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

---

> [!NOTE]
> Adyen では、Microsoft がメジャー バージョンをテストした後にマイナー バージョンの更新をリリースする場合があります。 メジャー バージョンがサポートされている限り、同じメジャー バージョン内でマイナー バージョンの更新を行うことができます。 通常これらの更新プログラムは、非常にターゲットを定めた修正プログラムであり、同じメジャー ファームウェア バージョンが以前にテストされている場合に限り、完全な再テストの基準を満たしません。 更新が、ドキュメントに表示されている最大 Adyen ファームウェア バージョンを超える必要はありません。 
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

次の国では、カードが存在しない取引の場合は Adyen がサポートします。 特定の国のサポートの詳細については、[Adyen 連絡先 ](https://www.adyen.com/contact/sales) に問い合わせください。 コマースの現在の国際的な利用可能性については、[国際的な利用可能性ページ](/dynamics365/get-started/availability) を参照してください。

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


## <a name="sign-up-with-adyen"></a>Adyen でサインアップ

Adyen 向け Dynamics 365 Payment Connector を使用するには、Adyen を使用する別の契約を保有している必要があります。 Adyen のサービスの詳細について、またはテスト商業アカウントを作成するには、[Adyen Web サイト](https://www.adyen.com/signup)を参照してください。

## <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

> [!NOTE]
> これらの手順は、既に Adyen で商業口座にサインアップ済みで、Adyen 商業ダッシュ ボードへのアクセス権を保有していることを仮定しています。

### <a name="prerequisites"></a>必要条件

すべてのチャネルで支払を構成するには、次の前提条件を完了する必要があります。

#### <a name="set-up-a-processor-for-new-credit-cards"></a>新しいクレジット カードのプロセッサの設定

POS 端末、コール センター、または電子商取引で支払を処理するには、新しいクレジット カードに対して新しい既定の支払プロセッサを構成する必要があります。 次の手順に従って、既定の支払プロセッサを構成します。

1. バックオフィスにサインインして、**売掛\> 支払設定\> 支払サービス** の順に移動します。
2. アクション ウィンドウで、**新規** を選択してから、**設定** タブに、以下の情報を入力します。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | 支払サービス | 構成する支払サービスの名前を入力します。 | Adyen Payment Service |
    | 支払コネクタ | 新しいクレジット カードの支払に使用する支払コネクタを選択します。 | Adyen 向け Dynamics 365 Payment Connector |
    | テスト モード | Adyen コネクタに関しては、実稼働環境とテスト環境でこのフィールドを **false** に設定する必要があります。 | false |
    | クレジット カードの既定のプロセッサ | この支払プロセッサが新しいクレジット カードで使用される既定のプロセッサであるかを指定します。 | 有 |
    | ゼロ トランザクションの支払プロセッサをバイパスする | この支払プロセッサが 0 (ゼロ) の量の取引でスキップする必要があるかを指定します。 | 有 |

3. **支払サービス アカウント** タブで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | はい | はい | *Guid* |
    | バージョン | 使用する Adyen 向け Dynamics 365 Payment Connector のバージョンを入力します。 「V002」は、支払を提示しないカード用の新しい Adyen API を活用し、[SCA サポート](../adyen_redirect.md) に必要とされているため、すべての新しい実装に使用されるべきです。  | あり | あり | "V001"/"V002" |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | 有 | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 これは、**[ランダム]-[会社名]** の形式にて、実稼働環境の一意識別子です。 これは Adyen Customer Area ポータル上の、使用している会社の実稼働口座の **口座 > API URLs** の下で、API URL 内の接頭語として存在します。 詳細については、[ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。 | ライブのみ | 無 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | MerchantIdenfier |
    | ターミナル アーキテクチャ | このフィールドは、`Payment service account` 用 **クラウド** にセットする必要があります。 | 有 | 有 | クラウド |
    | ローカル パスワード フレーズ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー識別子 | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー バージョン | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 有 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 | 有 | 有 | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | なし | なし | 「svs」 または 「givex」 |
    | ターミナル ギフト カード エントリ | *POS のみ* 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | はい | はい | True/False |
    | E コマースでの支払情報の保存を許可します | *電子商取引のみ* サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | 有 | 有 | True/False |
    | 承認失効期間 (日数) | *POS のみ* 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | あり | あり | "7" |
    | 元のキー | バージョンに 「V002」 が指定されている場合は必須です。 このキーは Adyen Web サイトの [発生元キーを取得する方法](https://docs.adyen.com/user-management/how-to-get-an-origin-key) ページの指示に従い取得することができます。 |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

4. **カードの検証値** タブで、**カードの検証値を行う** はそのままで、**カードの検証値を空白とする** を **いいえ** に設定します。 


### <a name="pos-payment-terminal"></a>POS 支払端末

#### <a name="onboard-and-configure-an-adyen-payment-terminal"></a>Adyen 支払端末のオンボードおよび構成

> [!NOTE]
> 次の手順では、Adyen 支払端末へのアクセス権を保持していると仮定します。

Adyen Web サイトの[販売時点管理](https://docs.adyen.com/developers/point-of-sale)ページに移動して、指示に従って Adyen 支払端末をオンボードします。 Adyen 固有のアプリのダウンロードを指示するステップをスキップします。 オンボード プロセス中、各支払端末のための以下の情報を書き留めてください。 この情報は、このトピックの後半の[支払端末の IP アドレスおよび EFT POS 登録番号の構成](#configure-the-payment-terminal-ip-address-and-eft-pos-register-number)セクションで必要です。

- 支払端末の IP アドレス
- POIID (POIID はデバイスのシリアル番号およびモデル番号で構成されます。 これはデバイスを一意に識別するために使用されます。)

支払端末のオンボード後、[Adyen の顧客領域](https://ca-test.adyen.com/ca/ca/login.shtml)にサインインして、構成対称の端末に移動し、各支払端末のための以下の情報を書き留めてください。 この情報は、トピックの後半の[ローカル ネットワーク通信の EFT サービス](#eft-service-for-local-network-communication) セクションで必要になります。

- キー識別子
- キー パスフレーズ
- キー バージョン

#### <a name="set-up-a-dynamics-365-pos-hardware-profile"></a>Dynamics 365 POS ハードウェア プロファイルの設定

1. バックオフィスにサインインして、**小売とコマース \>チャネル設定\> POS 設定\> POS プロファイル\>ハードウェア プロファイル** の順に移動します。
2. Adyen 向け Dynamics 365 Payment Connector を追加するためのハードウェア プロファイルを選択します。
3. [EFT サービス](#eft-service)、および続く [PIN パッド](#pin-pad) セクションの手順に従います。

#### <a name="eft-service"></a>EFT サービス

Adyen 支払コネクタは、ローカル ネットワーク経由または Adyen のバックエンドのクラウドを介して、デバイスと通信するように構成できます。 インターネット サービスが依存しない環境またはオフライン モードが必要な環境では、**ローカル** 設定を使用する必要があります。 インターネット接続が強い環境や支払ターミナルに静的 IP アドレスを割り当てできない場合は、**クラウド** アーキテクチャが最適です。

##### <a name="eft-service-for-local-network-communication"></a>ローカル ネットワーク通信用の EFT サービス

1. **EFT サービス** クイックタブの、**EFT サービス** フィールドで、**支払コネクタ** を選択します。
2. **コネクタ** タブで、**新規** を選択してから、**コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。 **順序番号** フィールドで内の値が他のコネクタの値より小さいことを確認してください。
3. **コネクタ プロパティ** セクションで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | あり | あり | *Guid* |
    | バージョン | ハードウェア プロファイルの EFT 設定を、**V001** に設定します。 **V002** は、コール センターとストアフロントにのみ必要です。  | あり | あり | 「V001」 |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | 有 | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 これは、**[ランダム]-[会社名]** の形式にて、実稼働環境の一意識別子です。 これは Adyen Customer Area ポータル上の、使用している会社の実稼働口座の **口座 > API URLs** の下で、API URL 内の接頭語として存在します。 詳細については、[ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。| ライブのみ | 無 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | MerchantIdenfier |
    | ターミナル アーキテクチャ | ローカル通信端末の場合は、**ローカル** に設定する必要があります。 別のターミナル API アーキテクチャの詳細については、Adyen Web サイトの[ターミナル API の導入](https://www.adyen.com/blog/introducing-the-terminal-api)ページを参照してください。 | 有 | 有 | ローカル |
    | ローカル パスワード フレーズ | 支払端末の Adyen キー パスフレーズを入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | keypassphrase123 |
    | ローカル キー識別子 | 支払端末の Adyen キー識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | mykey |
    | ローカル キー バージョン | 支払端末の Adyen キー バージョンを入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | 0 |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 有 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 これらの値は、大文字と小文字を区別します。 | あり | あり | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | なし | なし | 「svs」 または 「givex」 |    
    | ターミナル ギフト カード エントリ | *POS のみ* 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | はい | はい | True/False |
    | E コマースでの支払情報の保存を許可します | *電子商取引のみ* サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | 有 | 有 | True/False |
    | 承認失効期間 (日数) | *POS のみ* 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | あり | あり | "7" |
    | 元のキー | *カードは存在しません*  |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

4. アクション ウィンドウで、**保存** を選択します。


##### <a name="eft-service-for-cloud-communication"></a>クラウド通信用 EFT サービス

1. **EFT サービス** クイックタブの、**EFT サービス** フィールドで、**支払コネクタ** を選択します。
2. **コネクタ** タブで、**新規** を選択してから、**コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。 **順序番号** フィールドで内の値が他のコネクタの値より小さいことを確認してください。
3. **コネクタ プロパティ** セクションで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | あり | あり | *Guid* |
    | バージョン | ハードウェア プロファイルの EFT 設定を、**V001** に設定します。 **V002** は、コール センターとストアフロントにのみ必要です。  | あり | あり | 「V001」 |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | あり | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 これは、**[ランダム]-[会社名]** の形式にて、実稼働環境の一意識別子です。 これは Adyen Customer Area ポータル上の、使用している会社の実稼働口座の **口座 > API URLs** の下で、API URL 内の接頭語として存在します。 詳細については、[ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。| ライブのみ | 無 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | MerchantIdenfier |
    | ターミナル アーキテクチャ | これは、支払ターミナルとのクラウド通信用に、**クラウド** に設定する必要があります。 別のターミナル API アーキテクチャの詳細については、Adyen Web サイトの[ターミナル API の導入](https://www.adyen.com/blog/introducing-the-terminal-api) ページを参照してください。 | あり | あり | クラウド |
    | ローカル パスワード フレーズ | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル キー識別子 | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル キー バージョン | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル Cryptor バージョン | この設定は、ローカル支払ターミナル通信にのみ使用されます。 既定値は、**1** のままにできます。 | あり | あり | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 これらの値は、大文字と小文字を区別します。 | あり | あり | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | なし | なし | 「svs」 または 「givex」 |    
    | ターミナル ギフト カード エントリ | *POS のみ* 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | はい | はい | True/False |
    | E コマースでの支払情報の保存を許可します | *電子商取引のみ* サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | 有 | 有 | True/False |
    | 承認失効期間 (日数) | *POS のみ* 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | あり | あり | "7" |
    | 元のキー | *カードは存在しません* |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

4. アクション ウィンドウで、**保存** を選択します。


##### <a name="pin-pad"></a>PIN パッド

1. **PIN パッド** クイックタブの、**PIN パッド** フィールドで、**ネットワーク** を選択します。
2. **デバイス名** フィールドに、**MicrosoftAdyenDeviceV001** と入力します。

#### <a name="set-up-a-dynamics-365-register"></a><a id="set-up-a-dynamics-365-register"></a>Dynamics 365 レジスターの設定

> [!NOTE]
> 次の手順では、POS レジスターと Adyen 支払端末の間の専用マッピングがあることを前提としています。 Microsoft インターネット インフォメーション サービス (IIS) に基づくハードウェア ステーションの場合、**小売とコマース\>チャネル\>店舗\>すべての小売店舗** に移動して、設定対象の店舗を選択します。 次に、その店舗のページの、**ハードウェア ステーション** クイック タブで、同じ手順を実行します。

複数のハードウェア ステーションで支払端末を使用することはできません。 支払端末を複数の POS デバイスで共有する必要がある場合は、支払端末との通信を管理するために、IIS ハードウェア ステーションを配置する必要があります。 

##### <a name="configure-the-payment-terminal-ip-address-and-eft-pos-register-number"></a>支払端末の IP アドレスおよび EFT POS レジスター番号の構成

1. バックオフィスにサインインして、**小売とコマース\>チャネル設定\> POS 設定\>レジスター** の順に移動します。
2. Adyen 支払端末にリンクするレジスターを選択します。
3. **POS レジスター** ページの、**一般** クイックタブの、**EFT** セクションの、**EFT POS レジスター番号** フィールドに、一意の番号を入力します。 
4. **プロファイル** セクションの **ハードウェア プロファイル** フィールドでは、以前構成したハードウェア プロファイルを選択します。
5. 変更を保存します。
6. アクション ウィンドウで、**レジスター** タブの、**ハードウェア** グループで、**IP アドレスのコンフィギュレーション** を選択します。
7a. **"ローカル" アーキテクチャを使用する場合:** **IP アドレス** フィールドの **PIN パッド** クイックタブの **IP アドレスのコンフィグレーション** ページで、次のフォーマットにあるターミナルの IP アドレスを入力します: `https://<IP address>:8443/nexo/<POIID>`。 ここでは、**\<IP address\>**  および **\<POIID\>** は、Adyen 支払端末をオンボードした際に記録した値です。 次に例を示します: `https://192.168.1.3:8443/nexo/MX925-123456789`。 この URL の値は、大文字と小文字を区別します。
7b. **"クラウド" アーキテクチャを使用している場合:** **IP アドレス** フィールドの **PIN パッド** クイックタブの **IP アドレス コンフィグレーション** ページで、Adyen 支払端末にオンボードした際にメモした **POIID** 値を入力します。 次に例を示します: `MX925-123456789`。 このフィールドの値は、大文字と小文字を区別します。
8. 支払ターミナルにオンボード プリンターが用意され、そのプリンターを使用してプロセッサからのレシートを印刷する場合は、**PIN パッド** クイックタブの **IP アドレス** フィルダーとは別の **ポート** フィルダーに、**123** と入力します。


#### <a name="update-the-modern-pos-or-iis-hardware-station-configuration"></a><a id="update-the-modern-pos-or-iis-hardware-station-configuration"></a>Modern POS または IIS ハードウェア ステーションのコンフィギュレーションの更新

Retail SDK を使用して Modern POS バージョンをパッキングする場合、インストーラーがパッケージ化される前に、SDK コードで 1 回のみこれらの手順を実行する必要があります。 それ以外の場合、標準 Modern POS または IIS ハードウェア ステーションがインストールされた後にこれらの手順を実行する必要があります。

1. **dllhost.exe.config** ファイル (Modern POS の場合) または **web.config** ファイル (IIS ハードウェア ステーションの場合) を開きます。
2. 個々に示すように、**PreloadedComposition** セクションを更新して、旧式の支払デバイス アダプターから標準支払デバイス アダプターに切替えます。

    ``` xml
    <PreloadedComposition>
        <composition>
            <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.PaymentDeviceAdapter" />
            <!-- Switch from legacy to standard Payment Device Adapter.
            <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.Legacy.PaymentDeviceAdapter" />
            -->
        </composition>
    </PreloadedComposition>
    ```
3. **appSettings** 変数の **"PrintReceiptsOnCardDeclineOrVoid"** 値を **True** に更新して、プロセッサからの応答を印刷拒否または印刷無効にします。 

### <a name="call-center"></a>コール センター

コール センターの支払のために Adyen 向け Dynamics 365 Payment Connector を構成するには、このトピックの前半の[新しいクレジット カードのプロセッサの設定](#set-up-a-processor-for-new-credit-cards)セクションの指示に従います。

### <a name="e-commerce"></a>E コマース

1. バックオフィスにサインインして、**小売とコマース\>チャネル\>オンライン店舗** の順に移動します。
2. Adyen 向け Dynamics 365 Payment Connector を追加するオンライン店舗を選択します。
3. **オンライン店舗** ページの、**支払口座** クイック タブで、**追加** を選択します。
4. **コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。
5. 以下の追加情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | はい | はい | *Guid* |
    | バージョン | 使用する Adyen 向け Dynamics 365 Payment Connector のバージョンを入力します。 「V002」は、支払を提示しないカード用の新しい Adyen API を活用し、[SCA サポート](../adyen_redirect.md) に必要とされているため、すべての新しい実装に使用されるべきです。  | あり | あり | "V001"/"V002" |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 | 有 | 有 | ライブ |
    | オプション ドメイン | 支払要求が Adyen に実行されるときに使用するドメインを入力します。 これは、**[ランダム]-[会社名]** の形式にて、実稼働環境の一意識別子です。 これは Adyen Customer Area ポータル上の、使用している会社の実稼働口座の **口座 > API URLs** の下で、API URL 内の接頭語として存在します。 詳細については、[ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。 | ライブのみ | 無 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | MerchantIdenfier |
    | ターミナル アーキテクチャ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル パスワード フレーズ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー識別子 | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー バージョン | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 無 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | *完全なクラウド API キー* |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 | 有 | 有 | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 可能な値は **SVS** および **GIVEX** です。 | いいえ | いいえ | SVS |
    | ターミナル ギフト カード エントリ | *POS のみ* 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | はい | はい | True/False |
    | E コマースでの支払情報の保存を許可します | *電子商取引のみ* サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | 有 | 有 | True/False |
    | 承認失効期間 (日数) | *POS のみ* 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | 有 | 有 | "7" |
    | 発生元キー | *電子商取引のみ* バージョンに "V002" が指定されている場合にのみ必要です。 このキーは Adyen Web サイトの [発生元キーを取得する方法](https://docs.adyen.com/user-management/how-to-get-an-origin-key) ページの指示に従い取得することができます。 |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

6. アクション ウィンドウで、**保存** を選択します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="can-i-share-a-payment-terminal-with-multiple-hardware-stations"></a>複数のハードウェア ステーションを使用して支払端末を共有することはできますか。

一連番号 支払端末は、単一のハードウェア ステーションまたは POS 端末でのみ使用できます。 複数のハードウェア ステーションを単一の支払端末に接続しようとすると、ロックの問題が発生します。 支払端末を複数の POS デバイスで共有する必要がある場合は、支払端末を管理するために、IIS ハードウェア ステーションを配置する必要があります。 

### <a name="can-i-reuse-my-existing-payment-terminal-with-the-adyen-connector"></a>Adyen コネクタで既存の支払端末を再使用することはできますか。

一連番号 Adyen 支払端末は Adyen ソフトウェアと共に投入されます。 そのため、Adyen を使用して構成されていない既存の支払端末は、Adyen 向け Dynamics 365 Payment Connector で再使用することはできません。

### <a name="do-i-need-a-static-ip-address-for-the-adyen-payment-terminal"></a>Adyen 支払端末に対して静的 IP アドレスは必要ですか。

はい。 Modern POS では、Adyen 支払端末と通信するための既知の IP アドレスが必要です。 Adyen 支払端末の IP アドレスはクライアントで変更することができますが、IP アドレスの変更を続けると顕著なオーバーヘッドが生じ、業務の中断の原因となります。

### <a name="can-i-use-my-merchant-bank"></a>自分の商業銀行を使用することはできますか。

はい。 Adyen は任意の商社銀行で作業することができます。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="pos-payment-terminals"></a>POS 支払端末

#### <a name="general-issues"></a>一般的な問題

すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。 以下のログは、Microsoft Windows イベント ログの以下のノードにあります。

- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS
- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station

#### <a name="failing-payment-transactions"></a>失敗する支払トランザクション

支払取引が Adyen 支払端末を介して適切に処理されないとき、Dynamics 365 POS 内の対応するエラー メッセージには PSP 参照番号 が含まれます (PSP は各取引を一意に識別するために使用される、Adyen が提供する参照 ID です)。 特定の取引について Adyen サポートに連絡するとき、この参照番号を提供します。

## <a name="common-issues"></a>一般的な問題

### <a name="pos-payment-terminals"></a>POS 支払端末

#### <a name="the-eft-terminal-id-isnt-set"></a>EFT ターミナル ID が設定されていません。

<table>
<tbody>
<tr>
<td><strong>タイトル</strong></td>
<td>EFT ターミナル ID が設定されていません。</td>
</tr>
<tr>
<td><strong>現象</strong></td>
<td>支払承認呼び出しが失敗し、ハードウェア エラーが発生します。 イベント ログ内のエラー メッセージは、<strong>EFT ターミナル ID</strong> 値が設定されていないことを示しています。</td>
</tr>
<tr>
<td><strong>根本原因</strong></td>
<td>この問題は、<strong>EFT POS 登録番号</strong>フィールドが レジスターまたは IIS ハードウェア ステーション上で設定されていないときに発生する場合があります。 また、値が設定されていても、POS 端末に正しく同期されていない場合に発生する場合があります。 さらに、値がキャッシュされるときに発生する場合があります。</td>
</tr>
<td><strong>修正</strong></td>
<td>このトピックの前半の <a href="#set-up-a-dynamics-365-register">Dynamics 365 レジスターの設定</a>のし手順に従います。 次に、<strong>1070</strong> および <strong>1090</strong> 配送スケジュールを実行します。 問題が解決されない場合は、<strong>EFT POS 登録番号</strong>フィールドがキャッシュされてリセットする必要がある可能性があるため、Modern POS の再アクティブ化を考慮します。</td>
</tr>
</tbody>
</table>

#### <a name="the-modern-pos-or-iis-hardware-station-configuration-isnt-updated"></a>Modern POS または IIS ハードウェア ステーションのコンフィギュレーションが更新されない

<table>
<tbody>
<tr>
<td><strong>タイトル</strong></td>
<td>Config が更新されない</td>
</tr>
<tr>
<td><strong>現象</strong></td>
<td>Modern POS エラー: 「サインイン エラー。 初期化データを読み込むことができませんでした。」</td>
</tr>
<tr>
<td><strong>根本原因</strong></td>
<td>POS が再配置されていても、dllhost.config ファイルが更新されていない場合に、この問題が発生する場合があります。</td>
</tr>
<td><strong>修正</strong></td>
<td>このトピックの前半の <a href="#update-the-modern-pos-or-iis-hardware-station-configuration">Modern POS または IIS ハードウェア ステーションのコンフィギュレーションの更新</a>セクションの手順に従います。 次に、タスク マネージャーの<strong>詳細</strong>タブで dllhost.exe タスクを終了して、Modern POS を再度開きます。 IIS ハードウェア ステーションを使用している場合は、IIS をリセットします。</td>
</tr>
</tbody>
</table>

#### <a name="invoicing-sales-orders-failed-due-to-stale-authorization"></a>古い承認のため、販売注文の請求に失敗

| 肩書き | 古い認証のため、キャプチャに失敗 |
|---|---|
| 現象 | 以下の理由で販売注文の請求に失敗しました。「呼び出しのターゲットによって例外がスローされました。 System.ArgumentException: 値を NULL にすることはできません。」 ログの基になるエラーは次の通りです。「キャプチャ呼び出しの間に次のエラーが発生しました - Adyen 用 Dynamics 365 Payment Connector: 古い認証のため、エラー コードの拒否メッセージのキャプチャに失敗しました。」 |
| 根本原因 | このエラーは、**認証の対象期間 (日数)** よりも古い認証を支払コネクタに送信してキャプチャするときに発生します。 |
| 固定 | **売掛金パラメータ、クレジット カード** の **期限切れから日数** の値が、すべてのチャンネルの販売プロパティで設定されている値よりも **1 日少ない日数** に設定され、請求を再試行することを確認します。 **認証の対象期間 (日数)** の推奨値は、Adyen の販売プロパティで 14、売掛金管理パラメータで 13 になります。 |

## <a name="additional-resources"></a>追加リソース

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
