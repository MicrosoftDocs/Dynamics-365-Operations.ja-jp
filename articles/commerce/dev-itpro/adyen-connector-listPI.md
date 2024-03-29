---
title: オンライン支払手段を Adyen コネクタで保存
description: この記事では、電子商取引の Adyen コネクタを使用して支払手段を保存する方法を説明します。
author: BrianShook
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.industry: Retail
ms.openlocfilehash: 8962421d9a31b775193fd7ba57fa03d03891175a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279141"
---
# <a name="saving-online-payment-instruments-with-the-adyen-connector"></a>オンライン支払手段を Adyen コネクタで保存


[!include [banner](../includes/banner.md)]

この記事では、Dynamics 電子商取引プラットフォームで Adyen の "カードが存在しない" 支払コネクタを使用しているときの支払い方法の保存に関連する設定と機能について説明します。 

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| トークン | 支払プロセッサが参照として提供する一連のデータ。 トークンは、支払カード番号、支払認証、前回の支払キャプチャを表すことができます。 トークンは、販売時点管理 (POS) システムの外で機密データを保持するのに役立つため重要です。 |
| カードのトークン | POS システムのストレージに対して支払プロセッサが提供するトークン。 カードのトークン (またはカードの参照) は、それを受け取る販売者のみが使用できます。 |
| 承認 (認証) トークン | POS システムが支払プロセッサに承認要求をした後、支払プロセッサはその要求に対する応答の一部として POS システムに固有の ID を提供します。 承認を取り消したり無効にしたりするなどのアクションを実行するためにプロセッサが呼び出されたときに、この承認トークンや承認参照を後で使用できます ただし、承認トークンは、注文が履行されたとき、またはトランザクションが確定したときに、資金を取得するために最もよく使用されます。 |
| リスト PI | この記事で説明されている機能に対して頻繁に使用される一般名。 リスト PI は、同じ電子商取引 Web サイトを通じて行われる将来のチェックアウト中に、支払手段を保存し、以前に使用された支払手段を一覧にする機能を意味します。 |
| 名前付きユーザー | チェックアウト時にオンライン ストアフロントにログインしている電子商取引の顧客。 名前付きユーザーは一意の顧客 ID を持ち、オンライン ストアフロントにログインするたびにそのオンライン購入が常に同じ顧客 ID にマップされます。 |

## <a name="overview"></a>概要

電子商取引の注文を作成する場合、小売企業は将来のトランザクションで使用できるように顧客の支払カード情報を保存するよう促すことがよくあります。 この記事では、この機能 ("リストPI") が Adyen の Microsoft Dynamics 365 支払コネクタを通じて配送される方法を説明します。 Adyen 支払コネクタはこの機能をそのままではサポートしておらず、サード パーティの支払コネクタについてはカスタマイズが必要です。 また、すべての支払プロセッサが同じ方法で支払カード情報の保存をサポートしているとは限りません。 

リスト PI 機能の初期状態の実装では、支払プロセッサを使用して、その支払コネクタで既に処理された支払手段に対して、オンライン顧客の一意な ID のマッピングを保持する必要があります。 名前付きユーザーとして Web サイトにログインしている顧客のみに、支払カード情報を次回のオンライン訪問のために保存するオプションがあります。 "ゲスト チェックアウト" オプションを使用してオンライン注文を作成する顧客は、将来のトランザクションに対して支払カードの情報を保存できません。 

## <a name="prerequisites"></a>必要条件

リスト PI 機能には次の要素が必要です:

- 電子商取引と Microsoft Dynamics 365 Commerce の統合
- リスト PI 機能と互換性のある支払コネクタ
- 顧客がその支払プロセッサに保存させたい支払手段に一意の顧客 ID をマッピングする支払プロセッサ

一般的な支払コネクタとソフトウェア開発キット (SDK) の実装方法の詳細については、[IT プロおよび開発者向けのコマース ホームページ](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors) にアクセスしてください。

## <a name="setup"></a>セットアップ

リスト PI 機能には次のコンポーネントと設定手順が必要です:

- **電子商取引の統合** – オンライン ストアフロントとコマースの統合が必要です。 電子商取引 SDK の詳細は [電子商取引プラットフォーム ソフトウェア開発キット (SDK)](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk) を参照してください。
- **オンライン支払コンフィギュレーション** – Adyen の Dynamics 365 支払コネクタは、そのままでリスト PI をサポートします。 オンライン ストアの支払いを構成する方法については [Adyen の Dynamics 365 支払コネクタ](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) を参照してください。 

    この記事で説明されている電子商取引の設定手順を完了することに加えて、**オンライン ストア** フォームの支払口座クイック タブの **電子商取引で支払情報の保存を許可する** オプションを **はい** に設定する必要があります。 

- **オムニ チャネルの支払コンフィギュレーション** – バック オフィスで **小売とコマース \>本社の設定 \>パラメーター \>コマース共有パラメーター** に移動します。 次に **オムニ チャネルの支払** タブで **オムニ チャネルの支払を使用する** オプションを **はい** に設定します。 

## <a name="functional-experience"></a>機能のエクスペリエンス

### <a name="guest-checkout"></a>ゲスト チェックアウト

電子商取引の訪問者がゲストとしてチェックアウトを選択した場合、チェックアウト時に顧客レコードが作成されず、顧客は次の訪問時に支払手段を保存できません。 

### <a name="named-user-checkout"></a>名前付きユーザー チェックアウト

名前付きユーザー (サインインした顧客) が、チェックアウト プロセスの支払手順に進むとリスト PI 機能を経験します。 名前付きユーザーが初めてチェックアウトしたとき、クレジットカード情報が入力されるセクションに **次回の支払のために保存する** チェック ボックスが表示されます。 

![次回の支払のために保存するオプション。](../media/Payments/Save_PI.png)

このチェックボックスが選択された場合、支払のために新しいクレジットカードを送信すると、名前付きユーザーの一意の顧客 ID が支払プロセッサに送信され、クレジットカードが安全に保存されてその一意の顧客 ID にマップされます。 

同じ顧客が将来ストアフロントを訪れる際にサインインした場合、チェックアウト時の支払いに同じクレジットカードを選択ができます。 

![以前に保存された支払手段。](../media/Payments/Saved_PI.jpg)

### <a name="order-fulfillment-and-processing"></a>注文のフルフィルメントと処理

顧客がリスト PI 機能を使用して支払/入金明細行を適用した電子商取引の注文は、保存されたカード支払を使用せずに作成された注文と同じように機能します。 注文処理およびフルフィルメントの観点から 2 種類の支払を区別できません。 

## <a name="details-of-ecommerce-payment-card-tokenization"></a>電子商取引の支払カード トークン化の詳細

### <a name="standard-flow"></a>標準フロー

電子商取引の統合で、支払カードはチェックアウト プロセスの一部として通常は入力され、完了前の注文と共に保存されます。 カードの詳細は、支払プロセッサが提供する支払承認ページに直接入力されます。 カードの詳細を入力し、チェックアウト プロセスの次のステップに進むと、プロセッサが注文作成プロセスで使用するトークンを作成します。 

顧客がオンライン注文を終了すると、承認要求の一部として支払カード トークンが支払プロセッサに送信されます。 支払承認要求が成功した場合、支払プロセッサは承認トークンを送信して返信します。 この承認トークンは顧客の注文と共に保存され、その注文がバック オフィスから履行されるときに参照されます。 

### <a name="list-pi-flow"></a>リスト PI のフロー

標準フローとリスト PI フローの主な違いは、顧客がクレジットカード番号を完全に入力する必要がないことです。 代わりに顧客は以前に保存したクレジット カードを選択し、カード検証値 (CVV 番号) を提供するだけです。 顧客が正しい CVV 番号を提供し、チェックアウト プロセスの次の手順に進むと、支払プロセッサが承認要求を含む支払カード トークンを提供します。 

## <a name="related-articles"></a>関連記事

- [支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
