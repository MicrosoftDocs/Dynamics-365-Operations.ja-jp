---
title: オムニチャネル Commerce 注文支払
description: このトピックでは、Microsoft  Dynamics 365 Commerce オムニ チャンネル コマースの注文決済機能について説明します。
author: rubendel
manager: annbe
ms.date: 07/28/2020
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
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e2151f71b302f691e3c01f5aee30edb843410d6a
ms.sourcegitcommit: 79c0c6f3ee7828c755e7d71eb0ebbef8998afbad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2020
ms.locfileid: "3713940"
---
# <a name="omni-channel-commerce-order-payments"></a>オムニチャネル Commerce 注文支払

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft  Dynamics 365 Commerce オムニ チャンネル コマースの注文決済機能について説明します。 この機能を使用すると、コマース本部から電子商取引や販売時点管理 (POS) と注文の決済を編集することができます。

## <a name="key-terms"></a>重要な用語

| 相談 | 説明 |
|---|---|
| コマースの決済 | 決済は、POS または電子商取引のストア フロントで生成された顧客注文に関連付けられています。 |
| 注文の完了 | 注文が送信される前に確実に決済いを回収するコールセンターのビジネス ロジックです。 コールセンター パラメータの**注文完了を有効にする** 設定は、このビジネス ロジックを有効化するために使用されます。 詳細については、[注文の完了を有効化する](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) を参照してください。 
| コール センターの注文 | コール センターのユーザーがコマース本部で作成する注文。 |
| 売掛金 (AR) 販売注文 | コール センターを使用していないユーザーが、マース本部の売掛金を通じて作成する注文です。 AR 販売注文の決済は、コール センター注文の完了後は編集できません。 |

## <a name="overview"></a>概要

Dynamics 365 Commerce は、POS、電子商取引、コール センターの3つの主要なチャンネルで構成されています。 Commerce バージョン 10.0.12 およびこれ以前のバージョンでは、各チャンネルで作成された注文の決済明細行の管理が統一されていません。 例えば、コールセンターで注文が作成、編集された場合、注文完了フローを利用することで、注文を処理する前にそれらの注文に対して決済が指定されるようになります。 ただし、POS 注文と電子商取引では、コール センターの注文の完了に対応していません。 統一性の欠落を確認するには、コマース本部の **顧客サービス** ページに移動し、**決済** ボタンを使用して、どの注文から**決済**ページにアクセスできるかを確認します。

次の図は、コール センターで作成された注文を示しています。 この注文の行が選択されている場合は、**決済** ボタンが使用できます。 

![決済ボタンが利用可能なコールセンターの注文](../dev-itpro/media/COP_CC_PAY.png)

次の図は、POS で作成された注文を示しています。 この注文の行が選択されている場合は、**決済** ボタンが使用できません。

![決済ボタンが利用できない POS の注文](../dev-itpro/media/COP_NONCC_PAY.png)

商取引バージョン 10.0.13 およびそれ以降では、電子商取引および POS で作成された注文の **決済** ページにアクセスできます。 また、[オムニチャネル コマース注文決済] 機能を有効にすると、コール センターの注文に対してのみ使用可能だった注文完了機能を利用して編集することができます。

この機能を有効にすると、**販売注文の集計** ダイアログを使用して、POS および電子商取引で発生した注文の決済を編集することができます。  

![この機能が有効になった際に作成された POS または電子商取引の注文で使用できる決済ボタン](../dev-itpro/media/COP_ORDERCOMPLETION.png)

## <a name="prerequisites"></a>必要条件

オムニチャネル コマース注文決済機能を有効にするには、まず他の機能をいくつか有効にし、他の構成を完了する必要があります。 これらの機能は、**オムニチャネル コマース注文決済** を有効にする要件である以外に、受注に関連する機能的なギャップに対応するため、ベストプラクティスとして有効にする必要があります。 

オムニチャネル コマース注文決済機能を有効にする際に、前提条件のいずれかが満たされていない場合は、前提条件の機能と構成が整うまでは続行できない旨のメッセージが表示されます。

![前提条件となる機能と構成についてのメッセージ](../dev-itpro/media/COP_PRE.png)

### <a name="prerequisite-features"></a>前提条件となる機能

オムニチャネル コマース注文決済を正しく実行するには、次の機能を使用する必要があります。

| 機能名 | 説明 |
|---|---|---|
| コマースの統一支払転記仕訳帳の既定値 | この機能は、コールセンター、POS、または電子商取引チャネルを介して作成された注文に対して、ビジネス ロジックが顧客支払仕訳帳と顧客返金仕訳帳を作成する方法を変更します。 |
| オムニ チャネル支払 | この機能を使用すると、「オンラインで購入し、店で受け取る」 などのオムニチャネルの決済シナリオを有効化できます。 詳細については、[オムニチャネル決済の概要](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments) を参照してください。 |  
| 請求に対する支払保護の重複 | この機能は、請求書発行のシナリオで重複した決済の保護を可能にします。 コマースの決済機能は、請求書発行シナリオのカスタマイズに影響する可能性があります。 組織に請求書発行のカスタマイズがある場合は、本番環境でコマースの決済機能を有効にする前に、それらがリファクターされていることを確認してください。 | 
| 複数のキャプチャの払戻を有効にする | この機能を使用すると、注文に対して複数のリンクされた払戻を実行する機能が改善されます。 |
| 認証の有効期限が切れたクレジットカードの決済明細行を手動で無効化する | この機能により、決済明細行の期限が切れた場合に手動で削除することができ、承認を更新しません。 |

### <a name="configure-prerequisites"></a>必要条件の構成

#### <a name="map-payment-methods-to-operations"></a>決済方法をオペレーションにマッピングする

コマース本部で注文に対する決済の管理がサポートされるように、すべてのチャネルの支払い方法に対応するオペレーションにマッピングする必要があます。 オムニチャネル コマースの注文決済機能をオンにする前に、決済方法をマッピングすることで、同等のオペレーションのマッピングが存在しない各決済方法で警告が表示されないようにすることができます。

次の図は、コールセンターのオペレーションに対する決済方法のマッピングを示しています。

![コールセンターのオペレーションにマッピングされた決済方法](../dev-itpro/media/COP_OPERATION.png)

#### <a name="configure-a-call-center"></a>コール センターの構成

コマース本部を使用して POS の注文決済を管理するには、コールセンター チャネルを少なくとも1つ構成する必要があります。 コール センター チャネル作成方法の詳細については、[コール センター チャネルの設定](https://docs.microsoft.com/dynamics365/commerce/channel-setup-callcenter#overview)を参照してください。

#### <a name="set-up-users-as-call-center-users"></a>ユーザーをコール センターのユーザーとして設定する

コマース本部で、コマースの決済を編集するユーザーは、コール センター チャネルのユーザーとして設定されている必要があります。 コール センター のユーザー設定方法の詳細については、[コール センター チャネルのユーザーを設定する](https://docs.microsoft.com/dynamics365/commerce/channel-setup-callcenter#set-up-channel-users)を参照してください。

#### <a name="turn-on-order-completion-for-call-centers"></a>コールセンターの注文完了を有効化する

コール センターで、注文完了機能をオンにする必要があります。 注文の完了機能では、注文の処理中に確実に決済が完了するビジネス ロジックが実施されます。 注文完了についての詳細については、[注文完了を有効化する](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) を参照してください。

#### <a name="remove-the-pay-later-option-from-the-pos"></a>POS から [後払い] オプションを削除する

POS で顧客の注文が作成されると、店舗はフルフィルメントのためにカード決済を収集するか、または**後払い**を選択してカード情報の収集をスキップすることができます。 オムニチャネル コマースの注文決済が有効になっている場合は、POS から**後払い**オプションを削除する必要があります。 これを削除するには、**機能プロファイル**を検索して、**機能プロファイル** ページを開きます。 関連する機能を選択し、**編集** をクリックします。 機能プロファイルの **全般** クイックタブで、**フルフィルメントの決済を要求する** フィールドの値を **必要** に変更します。 この変更は、POS で有効となる前にチャネル データベースに同期する必要があります。

## <a name="turn-on-the-omni-channel-commerce-order-payments-feature"></a>オムニチャネル コマース注文決済機能を有効化する

前述セクションで説明した前提条件が設定されていれば、オムニチャネル コマース注文決済機能を有効にすることができます。

1. **機能管理**ワークスペースで、**すべて** タブを選択してすべての機能の一覧を表示します。その後、**オムニチャネル コマース注文決済**を検索します。

    ![機能管理ワークスペースのオムニチャネル コマース注文決済機能](../dev-itpro/media/COP_ENABLE.png)

2. 機能を選択し、**直ちに有効化** を選択します。

> [!IMPORTANT]
> オムニチャネル コマース注文決済機能には、決済と注文管理のワークフローに対する多くの変更が含まれています。 この機能は、運用環境で有効にする前に網羅的なテストを行う必要があります。

オムニチャネル コマースの注文決済機能がオンになっている時に作成されたチャネルの注文を他の注文と区別する方法としては、この機能がオンになっている場合は、注文のヘッダーに**決済タイプ** フィールドが表示されます。 POS 注文および電子商取引の注文では、このフィールドは **コマース** に設定されます。

![決済タイプ フィールドがコマースに設定されている注文](../dev-itpro/media/COP_HEADERCOM.png)

コール センター注文の場合は、**決済タイプ** フィールドが **コールセンター** に設定されます。 売掛金勘定で作成された販売注文の場合は、このフィールドは表示されません。

## <a name="fulfill-orders-after-the-omni-channel-commerce-order-payments-feature-is-turned-off"></a>オムニチャンネル コマース注文決済の機能がオフになっている場合に注文を処理する

オムニチャネル コマース注文決済機能がオンになっている間に作成された POS 注文や電子商取引注文は、機能がオンになっている間に処理しなければなりません。 後でこの機能をオフにされた場合は、この機能を再度オンにするまで、注文の処理が行われません。

## <a name="manage-orders-that-were-created-before-the-omni-channel-commerce-order-payments-feature-is-turned-on"></a>オムニチャネル コマース注文決済機能がオンになる前に、作成された注文を管理する

オムニチャネル コマース注文決済機能がオンになる前に作成された注文は、機能がオンになった後も処理できます。 この機能が有効になっていても、注文の編集エクスペリエンスは変更されません。また、注文もオムニチャネルのコマース注文決済ワークフローに対応するように変更されません。 コール センター以外のユーザーが売掛金で作成した売上注文は、この機能をオンにする前と同じように動作します。

## <a name="key-scenarios"></a>重要なシナリオ

オムニチャネル コマースの注文決済機能をオンにすると、電子商取引や POS 注文のクレジットカード決済を注文の完了まで管理できるようになります。 たとえば、顧客がオンライン注文を行い、コールセンターに電話して注文の変更を依頼したとします。 この場合、注文完了機能を使用すると、その注文に対する支払いを調整して、新たな繰越高に対応させることができます。

支払を取り込む前に、注文明細行の次のプロパティを編集できます :

- カード タイプ
- カード番号
- 支払額
- パーセント金額

### <a name="edit-order-payments"></a>注文の決済の編集

コールセンター注文の完了における以下のシナリオは、POS または電子商取引の店舗で作成された注文支払に適用されます。

#### <a name="uncaptured-card-payments"></a>取り込みされていないカード決済

まだ部分的に請求書が発行されていない注文のカード決済の明細行については、支払いの取り込み前に以下のプロパティを編集することができます :

- カード タイプ
- カード番号
- 支払額
- パーセント金額

支払を編集した後は、注文送信プロセスでは、支払明細行の編集に必要な変更がすべて修正されます。

| シナリオ | 説明 | サポート |
|---|---|---|
| 編集をして、より大きな金額を指定します。 | 承認されているがまだ取り込みされていないカード決済の場合は、支払金額を増やすことができます。 支払明細行の金額が増加すると、新しい金額に対して新しい認証が作成され、以前の認証が無効になります。 | 有 |
| 編集をして、より小さな金額を指定します。 | 承認されているがまだ取り込みされていないカード決済の場合は、支払金額を減額することができます。 支払明細行の金額が減額されると、新しい金額に対して新しい認証が作成され、以前の認証が無効になります。 | 有 |
| 古いカードを削除し、新しいカードを追加します。 | 取り込みがされていないカードの支払承認は、注文から削除され、別のカードでの支払いに置き換えることができます。 最初のカードの認証がキャンセルされ、注文の送信時に新しいカードの認証が取得されます。 | 有 |

#### <a name="partially-and-fully-captured-card-payments"></a>一部または完全に取り込みがされたカードの決済

| シナリオ | 説明 | サポート |
|---|---|---|
| 請求書の発行に使用された注文の決済を編集します。 | オムニチャネルコマースの支払いがある注文の一部が請求された場合、コールセンターが注文を完了することにより、既存カードのカード支払い金額を、取り込み済の金額まで編集することができます。 その後、新しいカードを適用して、注文の繰越高を補充することができます。 | 有 |
| 完全にキャプチャされたカード支払明細行を編集して、より大きな金額を指定します。 | カード決済が完全に取り込まれている場合であっても、このカード決済の金額がコールセンターの注文完了によって増額された場合は、注文が送信されたときに、増額された金額に対してカードの新しい認証が作成されます。 | 有 |

### <a name="remove-order-payments"></a>注文決済の削除

| シナリオ | 説明 | サポート |
|---|---|---|
| 支払の承認 | オムニチャネルコマースの注文カード決済は、注文完了によって注文から削除することができますが、これは一部しか取り込まれていない場合に限ります。 | 有 |
| 前払 | 事前決済は注文完了後には削除できません。 事前決済は、適用後には注文から削除できません。 支払伝票は既に関連付けられています。 | 第        条 |
| 部分的に取り込まれた決済 | 決済が **支払済**であっても、完全には取り込みされていない場合は削除できません。 ただし、支払額はすでに計上されていた金額まで減額することができます。 これが発生すると、承認金額が新たな支払額と等しくなるよう、支払プロバイダーに要求が送信されます。 | 第        条 |
| 完全に取り込みがされたクレジット カードの事前決済 | 完全に取り込みがされたクレジットカード決済と事前決済は注文から削除できません。 | 第        条 |

### <a name="cancel-order-and-sales-lines"></a>注文のキャンセルと販売明細行

| シナリオ | 説明 | サポート |
|---|---|---|
| 取り込みがされていないクレジット カード決済のキャンセル | 注文がキャンセルされると、まだ取り込みがされていないカードの支払承認がキャンセルされます。 | 有 |
| 取り込みがされているが、請求書が発行されていないクレジット カード決済のキャンセル | POS で注文が作成され、カード決済を使用して予約金を取り込んだた場合、注文は請求がされる前にキャンセルされます。 カード決済は、注文の取消の一環として自動的に払戻されます。 | 有 |
| 部分出荷と請求書が発行された注文のキャンセル | 部分的に出荷や請求がされた注文をキャンセルすると、未請求の明細行の 実行がキャンセルされます。 注文の残高に対する未処理のクレジットカードの認証は自動的にキャンセルされません。 | 手動による払戻が必要となります。 |
| 請求書が発行済みで、未出荷となっている注文のキャンセル | 注文の請求書が発行されていても、品目のすべてが出荷されていない場合は、注文を取り消すことができます。 ただし、その注文に対して取り込みがされた支払は、自動的に払戻されません。 未請求の品目の未処理承認はキャンセルされませんが、そのカードを発行した銀行の承認期限ポリシーに従って期限切れになります。 | 手動による払戻が必要となります。 |
| 未実行または未請求の品目明細行のキャンセル | 未実行または請求済の注文明細行がキャンセルされた場合、注文完了のプロセスでは、新しい注文の合計と等しくなるように支払を減額する必要があります。 |

### <a name="refunds"></a>払戻

| シナリオ | 説明 | サポート |
|---|---|---|
| POS 注文と電子商取引注文のリンク済みの払戻額 | POS や電子商取引のチャネルから発生した注文に由来する返品注文は、請求時に請求されたカードに対してリンクされた払戻を発行することができます。 | 有 |
| AR 販売注文のリンクされた払い戻し | 注文完了による支払いの編集はできませんが、AR 販売注文で発行された返品は、請求時に請求された元のカードに連動して返金される場合があります。 | 
| リンクされていない払戻 | マーチャントの返品ポリシーと支払プロセッサがこの方法を許可している場合は、注文が最初に現金で支払われた場合や、支払いに使用された元のカードが有効でなくなった場合などに、リンクされていない払戻を返品注文に指定することができます。 | 有 |
| カード以外の事前決済への払戻 | 現金やクレジット メモなどのカード以外の事前決済で処理されていた返品注文は、リンクされた払戻の対象にはなりません。 払戻の処理には、**小切手**などの適切な支払い方法を指定する必要があります。 リンクされていない払い戻しを許可している組織は、決済プロセッサがこの方法を許可している場合、以前に注文に使用されていなかったクレジットカードに、カード以外の事前決済を返金することができます。 | 有 |

### <a name="edit-and-remove-orders-that-have-prepayments"></a>事前決済された注文の編集と削除

| シナリオ | 説明 | サポート |
|---|---|---|
| 事前決済の支払/入金明細行を編集します。 | 支払伝票は、事前決済の支払/入金明細行に関連付けることができます。 したがって、事前決済の支払/入金明細行を編集、削除することはできません。 | 第        条 |

## <a name="related-changes"></a>関連する変更点

オムニチャンネルのコマース注文決済に対応するにあたって、コマース バージョン 10.0.13 では既存の機能に変更が導入されています。

### <a name="consistent-selection-of-payment-journals-when-sales-orders-and-refund-payments-are-posted"></a>販売注文と払戻の支払が転記される際の支払仕訳帳の一貫した選択

コマース バージョン 10.0.12 までは、支払仕訳帳の割り当てがチャネル間で一貫していません。 コマース バージョン 10.0.13 およびそれ以降では、オムニチャンネルのコマース注文決済機能を有効にすると、すべてのチャンネルで **コマース パラメータ**ページの **転記** タブに指定されている支払伝票が使用されます。

![コマース パラメータ ページにおける支払伝票の割り当て](../dev-itpro/media/COP_VOUCH.png)

### <a name="check-payment-method"></a>小切手の支払方法

POS で作成された注文には、コマース本部で作成された小切手の番号は含まれません。 オムニチャンネルのコマース注文決済機能がオンになっている場合は、POS で作成され小切手で支払われる注文の小切手番号に **9999** が入力されます。

また、返金方法に**小切手**が指定されている場合は、小切手番号は不要です。