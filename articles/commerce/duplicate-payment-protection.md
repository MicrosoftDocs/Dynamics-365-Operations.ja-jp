---
title: 重複支払の防止
description: この記事では、Modern POS で Dynamics 365 Commerce が支払いの重複を防ぐ方法について説明します。
author: BrianShook
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2018-11-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a24f8eab99d122d56697852dec5a52122a72afb5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865955"
---
# <a name="duplicate-payments-prevention"></a>重複支払の防止

[!include [banner](includes/banner.md)]

この記事は、Dynamics 365 Commerce Modern POS の重複支払防止機能の概要を提供します。

## <a name="overview"></a>概要

この記事では、販売時点管理 (POS) が支払ターミナルの通信を喪失し、POS とターミナルの同期がされない状況から回復する時のユーザー エクスペリエンスを説明します。

重複支払保護機能により、Modern POS は、通信が失われても、顧客が支払ターミナルを使用して別に支払処理をし、結果として重複して支払ってしまうようなことなくシームレスに回復できます。

> [!NOTE]
> 重複支払保護機能は、支払ターミナルを使用して行われた支払に対してのみサポートされています。

この記事では、重複支払保護機能の次の側面について説明します。

- [前提条件](#prerequisites) – Modern POS でこの機能を使用するため、一連の前提条件を設定します。
- [シナリオの詳細](#scenario-details) – 重複支払保護機能の対象となるシナリオの詳細な説明。
- [トラブルシューティング](#troubleshooting) – 重複支払保護機能で問題が発生したときに実行する手順です。
- [追加リソース](#additional-resources) – 重複支払保護機能を使用する場合に役に立つ関連記事の一覧。

## <a name="prerequisites"></a>必要条件

- 支払コネクタおよび対応する支払ゲートウェイまたはプロセッサは、この機能をサポートする必要があります。 *支払コネクタ* は、コマース (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。 この記事で説明されているコネクタは、標準支払 SDK を使用して実装されています。
- コネクタが対応する重複支払保護インターフェイスを実装する場合、 その機能は Modern POS で自動的に有効になります。 それ以外の場合、自動的に無効になっています。

<!---
The [Implement Duplicate Payment Protection](TODO) article describes in detail how to implement support for the duplicate payment protection feature for a given payment connector.
The [Dynamics 365 Payment Connector for Adyen](TODO) has built in support for the duplicate payment protection feature.
-->

## <a name="scenario-details"></a>シナリオの詳細

重複支払保護機能は、支払が開始され、支払ターミナルで完了するどのようなシナリオにも適用可能ですが、Modern POS に対応する応答を受信することはできません。 その結果、顧客のカード (クレジット_カード) などに請求されますが、支払明細行は POS に追加されません。 ほとんどの場合、レジ担当者は支払ターミナルで後続支払をトリガーし、結果として顧客の重複支払が発生します。

### <a name="how-duplicate-payments-scenarios-are-triggered"></a>重複する支払のシナリオが発生する方法

1. **レジ担当者が支払を開始します。**

    レジ担当者が、**カードで支払う** をクリックし、**支払** ページに移り、**支払/入金** をクリックして、カード支払を開始します。

2. **顧客は支払ターミナルを操作します。**

    支払が開始された後、支払ターミナルは、顧客に支払を求めます。 顧客は、支払ターミナルで支払プロセスを開始します。 

3. **Modern POS が支払ターミナルへの接続を失います**

    - 顧客が支払ターミナルで支払を実行中に、Modern POS は、クラッシュ、ネットワーク接続の喪失、終了、もしくはターミナルの再起動のいずれかにより、支払ターミナルへの接続を失います。
    - レジ担当者は Modern POS を再起動し、いかなる接続の問題も報告します。

4. **顧客は支払ターミナルでの支払を完了**

    Modern POS をリセットし、顧客が支払ターミナルで支払を完了すると、請求されます。

5. **Modern POS を起動します**

    レジ担当者が Modern POS のリセット/起動を完了しますが、支払が買い物カゴに追加されません。

### <a name="payment-recovery-scenarios"></a>支払の回収シナリオ

POS またはネットワーク通信が回復した後は、レジ担当者が前の支払を使用するように要求されるいくつかのシナリオがあります。 支払の回収をトリガーできるいくつかのシナリオを次に示します。

回復されない支払があり、レジ担当者が次のアクションのいずれかを実行する場合、支払が既にされていることを示すダイアログ ボックスがレジ担当者に表示されます。

- カード支払を使用して金額に対して別の支払を起動します。
- カード支払を使用して支払額に対して別の支払を起動します。
- 買い物カゴの明細行を無効化しようとします。
- 取引を無効化しようとします。
- 取引を停止しますか?

![支払を回復します。](media/Payments/Duplicate-Payment-Protection/Recover-Payment.png)

レジ担当者が **OK** をクリックすると、支払が復旧し、支払明細行として買い物カゴに追加されます。

重複支払保護機能の主な機能は、元の支払が正常に処理され、対応する支払明細行が買い物カゴに追加されたのと同じ、あるべき状態に Modern POS を戻すことです。

### <a name="how-to-skip-payment-recovery"></a>支払の回復をスキップする方法

場合によっては、レジ担当者は明示的に重複支払保護をスキップし、前の支払を復元しないように選択できます。 その場合、レジ担当者は、支払を復元しないで取引を無効化するための次の手順を使用できます。

1. **Modern POS の再起動**

    Modern POS の支払ターミナルへの接続が失われた後、POS を再起動します。

2. **取引を無効にします**

    買い物カゴページに移動し、**トランザクションの無効化** をクリックします。

3. **回復した支払を無視します。**

    回復した支払が使用可能であることを示す新しいダイアログ ボックスが表示されます。 **無視** をクリックして復元した支払をスキップします。

![支払の回復をスキップします。](media/Payments/Duplicate-Payment-Protection/Void-Transaction.png)

### <a name="what-to-do-if-the-customer-leaves-the-store"></a>顧客が店舗を出てしまった場合にすること

場合によっては、レジ担当者が取引を確定する前に顧客が店舗から出て行ってしまうことがあります。 そのような場合は、[支払の回復をスキップする方法](#how-to-skip-payment-recovery)セクションで説明されている手順に従い、取引を無効にして、支払ゲートウェイ/プロセッサのポータルで支払を手動で無効にします。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="general-issues"></a>一般的な問題

すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。 ログは、Windows イベント ログの以下のノードにあります。

- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS
- アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station

### <a name="validate-that-the-customer-is-not-double-charged"></a>顧客が重複して請求されていないか検証します。

重複支払保護機能が有効になっている場合でも、販売者が、二重請求が発生していないことを検証することをお勧めします。 これを行うには、対応する支払ゲートウェイ/プロセッサ ポータル上のすべての取引を確認します。

### <a name="payment-recovery-fails"></a>支払の回復が失敗する時

Modern POS で、前の支払の復元中にエラーが発生する可能性があります。 このエラーは、支払コネクタまたは支払ゲートウェイ/プロセッサが前の支払の復元を許可しないという問題がある時に発生します。 この問題を解決するには、前の支払を復元できないために起きているので、レジ担当者は [支払の回復をスキップする方法](#how-to-skip-payment-recovery) セクションで説明されているように、回復をスキップしなければなりません。

## <a name="additional-resources"></a>追加リソース

- [支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
