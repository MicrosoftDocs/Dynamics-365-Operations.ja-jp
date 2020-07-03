---
title: ネットワーク周辺機器のサポート
description: このトピックでは、店舗でサポートされているネットワーク周辺機器の概要について説明します。
author: rubendel
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e59700b1241caddced356b8f448547dc66813d37
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416595"
---
# <a name="support-for-network-peripherals"></a>ネットワーク周辺機器のサポート

[!include [banner](../includes/banner.md)]

このトピックでは、店舗におけるネットワーク周辺機器のサポートおよび設定について説明します。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| 登録 | 販売時点管理 (POS) レジスターのインスタンスを構成するために使用されるエンティティ。 |
| デバイス | POS レジスタの物理的なインスタンスとそれに割り当てられた最新の POS アプリケーションの表現。 |
| 専用ハードウェア ステーション | Windows 用 Modern POS および Android アプリケーション用 Modern POS に組み込まれているプロセス間通信 (IPC) ハードウェア ステーション。 |
| ドロワーのキック (d/k) ポート | キャッシュ ドロワーをレシート プリンターに接続するための従来の方法。 |
| ネットワーク周辺機器 | ネットワーク対応型の支払ターミナル、レシート プリンター、キャッシュ ドロワーの組み込みサポート。 |
| ESC/P | "Escape/P" とも呼ばれるプリンターの Epson 標準コードは、販売時点管理プリンターにコマンドを送信するために一般的に使用されている、Epsonで作成されたプリンター コントロール言語です。 |

## <a name="supported-pos-clients-and-devices"></a>サポートされている POS クライアントとデバイス

ネットワーク周辺機器用の機能は、Windows 用 Modern POS および Android POS クライアント用 Modern POS でサポートされています。

この機能は、ネットワーク対応型の支払ターミナルとレシート プリンターをサポートしています。 キャッシュ ドロワーのサポートを提供するには、d/k ポートを介して、キャッシュ ドロワーをネットワーク対応型のレシート プリンターに接続します。

この機能に対するすぐに使える、[Adyen 向け Microsoft Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3) によって提供されます。 ただし、その他の支払コネクタは、コマース ソフトウェア開発キット (SDK) を介してサポートされる可能性があります。 サポートされているレシート プリンターには、Star Micronics と Epson のネットワーク対応型レシート プリンターがあります。

すぐに使えるサポートは、Epson および Star Micronics レシート プリンターのネットワーク プロトコルに対して提供されます。 d/k ポートを介してこれらのプリンターに接続されたキャッシュ ドロワーは、ESC/P プロトコルを介してサポートされます。

## <a name="set-up-network-peripherals"></a>ネットワーク周辺機器のセットアップ

### <a name="adyen-payment-terminal"></a>Adyen 支払ターミナル

Adyen 支払ターミナルの設定方法については、[Adyen の Dynamics 365 支払コネクタ](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3#pos-payment-terminal)の「POS 支払ターミナル」セクションを参照してください。

### <a name="epson-or-star-micronics-receipt-printer-and-a-cash-drawer"></a>Epson または Star Micronics レシート プリンターとキャッシュ ドロワー

#### <a name="epson-prerequisite"></a>Epson の前提条件

プリンターが Epson ePOS 印刷をサポートしている場合は、Epson 社の製品マニュアルを参照して、Epson プリンターの Web サイトにアクセスして ePOS 印刷を有効にする方法について参照してください。 ePOS 印刷が構成されている場合、プリンターは電源サイクル後に、IP アドレスを示す勘定書を印刷します。

#### <a name="star-micronics-prerequisite"></a>Star Micronics の前提条件

イーサネットをサポートするネットワーク対応 Star Micronics プリンターは、Star Micronics プリンター ユーティリティを使用してネットワーク プロトコルを使用するように構成できます。 ネットワーク印刷をサポートする Star Micronics デバイスの設定方法については、「Star Micronics」で提供されているドキュメントを参照してください。 デバイスが正しく構成されている場合は、プリンター ユーティリティのユーザー インターフェイス (UI) を通じて、プリンターの IP アドレスを取得できます。

#### <a name="set-up-a-hardware-profile"></a>ハードウェア プロファイルの設定

1. Dynamics 365 Commerce で、**ハードウェア プロファイル** を検索します。
2. **新規** を選択します。
3. ハードウェア プロファイル番号を割り当て、説明を入力します。
4. さまざまなデバイス タイプのクイック タブで、次のデバイス タイプを設定します。

    | デバイス | 種類 | デバイス名 | 追加の詳細 |
    |---|---|---|---|
    | プリンター | ネットワーク | **Epson** または **Star** | デバイス名は大文字と小文字が区別されます。 **レシート プロファイル ID** を割り当てます。 |
    | キャッシュ ドロワー | ネットワーク | **Epson** または **Star** | デバイス名は大文字と小文字が区別されます。 キャッシュ ドロワーが複数の POS デバイスによって共有される場合は、**共有シフトの使用** オプションを **はい** に設定します。 |

5. **保存** を選択します。

#### <a name="set-up-modern-pos-for-windows-or-modern-pos-for-android-clients-that-have-built-in-hardware-station-logic"></a>ビルトインのハードウェア ステーション ロジックを持つクライアントに対して、Windows 用 Modern POS または Android クライアント用 Modern POS を設定します。

1. Dynamics 365 Commerce で、**レジスター** を検索します。
2. レジスター番号を選択してレジスターを選択し、**編集** を選択します。
3. 作成したハードウェア プロファイルをレジスターに割り当てて、専用の支払ターミナルを使用するようにします。 このレジスターにマップされているデバイスには、Windows アプリケーション用のモダン POS か Android アプリケーション用のモダン POS のいずれかを使用する必要があります。
4. **保存** を選択します。
5. アクション ウィンドウの **レジスター** タブで、**IP アドレスの構成** を選択します。
6. **プリンター** のクイックタブで、プリンターの IP アドレスを入力します。 ポート番号のフィールドを空欄のままにします。
7. **キャッシュ ドロワー** のクイックタブで、プリンターの IP アドレスを入力します。 ポート番号のフィールドを空欄のままにします。
8. **保存** を選択します。
9. **すべての店舗** を検索します。
10. **小売チャンネル ID** 値を選択して店舗を選択し、**編集** を選択します。
11. **ハードウエア ステーション** クイック タブで、**追加**を選択します。
12. **ハードウェア ステーション タイプ** フィールドを **専用** に設定します。
13. 説明を入力しますが、ハードウェア プロファイルを設定したり、このハードウェア ステーションにその他の値は設定したりしないでください。
14. **保存** を選択します。
15. **配布スケジュール** を検索します。
16. 配分スケジュール **1090** を選択して、**今すぐ実行** を選択します。
17. 配分スケジュール **1070** を選択して、**今すぐ実行** を選択します。

iOS 用 Modern POS およびクラウド アプリケーション用 Modern POS には、組み込みのハードウェア ステーション ロジックはありません。 このいずれかのアプリケーションを使用している場合は、次の手順を実行します。

1. Dynamics 365 Commerce で、**すべての店舗** を検索します。
2. **小売チャンネル ID** 値を選択して店舗を選択し、**編集** を選択します。
3. **ハードウエア ステーション** クイック タブで、**追加**を選択します。
4. **ハードウェア ステーション タイプ** フィールドを **共有** に設定します。
5. 説明を入力します。 ハードウェア ステーションは、組み込みのハードウェア ステーション ロジックを持つ POS クライアントを含め、複数の POS クライアントで共有できます。
6. **ハードウェア プロファイル** フィールドで、ドロップダウン矢印を使用して、ネットワーク周辺機器のハードウェア プロファイルをこのハードウェア ステーションに割り当てます。
7. **保存** を選択します。
8. レシート プリンターとキャッシュ ドロワーのハードウェア ステーションが選択されている状態で、**IP アドレスの構成** を選択します。
9. プリンターのクイックタブで、プリンターの IP アドレスを入力します。 ポート番号のフィールドを空欄のままにします。
10. キャッシュ ドロワーのクイックタブで、プリンターの IP アドレスを入力します。 ポート番号のフィールドを空欄のままにします。

    > [!NOTE]
    > 共有ハードウェア ステーションを設定する方法の詳細については、[小売りハードウェア ステーションの設定とインストール](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation)を参照してください。

11. **保存** を選択します
12. **配布スケジュール** を検索します。
13. 配分スケジュール **1090** を選択して、**今すぐ実行** を選択します。
14. 配分スケジュール **1070** を選択して、**今すぐ実行** を選択します。

### <a name="sharing-network-peripherals"></a>ネットワーク周辺機器の共有

ネットワーク レシート プリンターとキャッシュ ドロワーは、複数の POS デバイスで共有できます。 これらを共有するには、共有ハードウェア ステーションを使用して、デバイスへの接続を仲介することができます。 または、Windows 用 Modern POS または Android 用 Modern POS を使用している場合は、レジスターのプロパティで同じデバイスを直接コンフィギュレーションできます。

支払ターミナルは、共有ハードウェア ステーションが支払ターミナルへの接続を仲介するために配置されている場合にのみ共有できます。 レジスター レベルで同じ支払ターミナルの IP アドレスを直接設定することによって、支払ターミナルを共有することはできません。 この方法を使用した場合、個々の POS クライアントがデバイスをロックして要求すると、問題が発生します。

## <a name="related-articles"></a>関連記事

- [Android と iOS での POS ハイブリッドアプリの設定](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Adyen 向け Dynamics 365 Payment Connector](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [専用の支払ターミナルおよびプリンターとキャッシュ ドロワーのプロンプト](https://go.microsoft.com/fwlink/?linkid=2129966)
