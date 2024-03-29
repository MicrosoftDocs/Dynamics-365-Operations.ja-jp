---
title: オムニ チャネルの高度な自動請求
description: この記事では、高度な自動請求機能を使用して Commerce チャネル注文の他の注文請求を管理するための機能について説明します。
author: hhainesms
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: d44bc4ef61341c394b627ddbe10768d2ddf98de0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292708"
---
# <a name="omni-channel-advanced-auto-charges"></a>オムニ チャネルの高度な自動請求

[!include [banner](includes/banner.md)]

この記事では、Dynamics 365 for Retail バージョン 10.0 で利用可能な高度な自動請求機能のコンフィギュレーションと配置について説明します。

高度な自動請求機能が有効になっていると、サポートされている任意の Commerce チャネル (販売時点管理 (POS)、コール センター、およびオンライン) で作成された注文は、ERP アプリケーションで定義された [自動請求](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) 設定を、ヘッダーおよび明細行レベルの両方に関連する請求に使用できます。

Retail バージョン 10.0 より前のリリースでは、[自動請求](/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) 設定は、E コマースおよびコール センター チャネルで作成された注文によってのみアクセス可能です。 バージョン 10.0 以降では、POS で作成された注文は、自動請求設定を使用できます。 これにより、追加の雑費は、販売トランザクションに体系的に追加することができます。

バージョン 10.0 より前のリリースを使用すると、POS ユーザーは、「すべて出荷」または「選択された出荷」 POS トランザクションの作成中に、配送料を手動で入力するように求められます。 アプリケーションの雑費機能は、請求金額が注文にどのように書き込まれるかに関して使用されますが、体系的な計算は提供されません。計算は、請求金額の値を決定するためのユーザーの入力に依存します。 請求金額は単一の「出荷」関連費用コードとしてのみ追加でき、作成後に POS で簡単に編集または変更することはできません。

手動のプロンプトを使用して出荷費用を追加することは、バージョン 10.0 以降でも使用可能です。 組織が **高度な自動請求** パラメーターを有効にしていない場合、手動で請求金額を入力するよう指示する POS は同じままです。

高度な自動請求機能を使用すると、POS ユーザーは自動請求設定テーブルに基づいて定義された雑費について、体系的に計算することができます。 さらに、ユーザーは、ヘッダーまたは明細行レベル (現金払いまたは顧客注文に対して) の POS 販売トランザクションに無制限の追加請求および手数料を、追加または編集することができます。

## <a name="enable-advanced-auto-charges"></a>高度な自動請求を有効にする

**Retail および Commerce\> Headquarters 設定 \> パラメーター \> Commerce パラメーター** ページで、**顧客注文** タブに移動します。**請求金額** クイック タブで、**高度な自動請求を使用する** を **はい** に設定します。

![高度な自動請求パラメーター。](media/advancedchargesparameter.png)

高度な自動請求を有効にすると、すべて出荷または選択された出荷の顧客注文を作成する時に、ユーザーは POS 端末で手動で出荷費用を入力するよう求められることはなくなります。 POS 注文諸費用は体系的に計算され、POS トランザクションに追加されます (作成する注文の条件に一致する自動請求テーブルが見つかる場合)。 ユーザーは、POS 画面レイアウトに追加できる新規に追加されたPOS操作を使用して、ヘッダーまたは明細行レベルの請求を手動で追加または維持することもできます。

高度な自動請求を有効にすると、**出荷費用コード** および **出荷費用の返金** の既存の **Commerce パラメーター** は、使用できなくなります。 これらのパラメーターは、**高度な自動請求を使用する** のパラメーターが **いいえ** に設定されている場合にのみ適用できます。

機能が有効化されると、出荷費用や他の請求金額を計算して POS 販売注文に追加する方法のビジネス プロセス フローが変更されるため、この機能を有効にする前に、従業員のテストとトレーニングを必ず行ってください。 プロセス フローが POS からのトランザクション作成に影響することを確認してください。 コール センターおよび E コマースの注文では、高度な自動請求を有効にした場合の影響は最小限になります。 コール センターおよび E コマース アプリケーションは、追加の注文手数料を計算するために、これまで自動請求テーブルに関連していたのと同じ動作を続けます。 コール センターのチャンネル ユーザーは、ヘッダーまたは明細行レベルでシステムが計算した自動請求を手動で編集することも、ヘッダーまたは明細行レベルで追加の雑費を手動で追加することもできます。

## <a name="add-pos-operations"></a>POS 操作の追加

POS アプリケーション環境で高度な自動請求が正しく機能するように、新しい POS 操作が追加されました。 これらの操作を [POS 画面レイアウト](/dynamics365/unified-operations/retail/pos-screen-layouts)に追加し、高度な自動請求を展開して POS デバイスに展開する必要があります。 このような操作が追加されていない場合、ユーザーは POS トランザクションの費用を管理または維持することができず、自動請求設定に基づいて体系的に計算される請求金額を調整または変更することができません。 少なくとも、**請求金額の管理** 操作を POS レイアウトに展開することをお勧めします。

新しい操作を次に示します。

- **142 - 請求金額の管理** – この操作を使用して、POS ユーザーが手動または自動請求計算によって体系的に追加された POS トランザクションの雑費を表示および編集できるようにします。
- **141 - ヘッダーの諸費用の追加** – この操作を使用して、ユーザーがヘッダーレベルの雑費を POS トランザクションに手動で追加 (および使用する費用コードを選択) できるようにします。
- **140 - 明細行の諸費用の追加** – この操作を使用して、ユーザーが明細行レベルの雑費を POS トランザクション明細行に手動で追加 (および使用する費用コードを選択) できるようにします。
- **143 - 請求金額の再計算** – この操作を使用して、販売トランザクションの請求金額の完全な再計算を実行します。 以前にユーザーが上書きした自動請求は、現在のカート設定に基づいて再計算されます。

すべての POS 操作と同様に、操作を実行するためにセキュリティ コンフィギュレーションでマネージャーの承認が必要になることがあります。

**高度な自動請求を使用する** のパラメーターが無効になっている場合でも、上の一覧に表示している POS 操作を POS レイアウトに追加することは可能であることに注意するのは重要です。 このシナリオにおいて、組織は手動で追加された変更の表示、および **諸費用の管理** 操作を使用した編集という追加された利益を得ることができます。 **高度な自動請求を使用する** のパラメーターが無効になっている場合でも、ユーザーは POS トランザクションに対して **ヘッダーの諸費用の追加** および **明細行の諸費用の追加** 操作を使用することもできます。 **高度な自動請求を使用する** が無効になっている時に **請求金額の再計算** 操作が使用される場合、あまり機能的ではありません。 このシナリオにおいて、再計算は行われず、トランザクションに手動で追加された諸費用すべてが $0.00 にリセットされるだけです。

## <a name="use-case-examples"></a>ユース ケース例

このセクションでは、チャネル注文の範囲内での自動請求とその他の請求の設定と使用方法を理解するのに役立つユース ケース例を紹介します。 これらの例は、**高度な自動請求を使用する** のパラメーターが有効になっているときのアプリケーションの動作を示しています。

### <a name="auto-charges-header-charges-example"></a>ヘッダー諸費用の自動請求の例

#### <a name="use-case-scenario"></a>ユース ケース シナリオ

小売業者は、任意の Commerce チャネルで製品の出荷が必要なトランザクションが作成されたときに、配送料を自動的に追加したいと考えています。 小売業者は、2 種類の配送方法を提供します: 陸送便および航空便です。 顧客が陸送便を選択し、注文金額が 100 ドルより小さい場合、小売業者は 10.00 ドルの配送料を顧客に請求します。 注文金額が 100 ドルを超え、顧客が陸送便を選択した場合、追加の配送料は請求されません。 顧客がすべての注文に対して航空便を選択した場合、合計金額に関係なく、20.00 ドルの配送料が請求されます。

#### <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

このシナリオでは、2 つの自動請求テーブルの構成が必要です。

**売掛金 \> 諸費用の設定 \> 自動請求** に移動します。

2 つの異なるヘッダー レベルの自動請求をコンフィギュレーションします。 配送方法を、1 つは「陸送便モード」、1 つは「航空便モード」に設定します。 このシナリオでは、「すべての顧客」を使用するように構成します。

陸送便の料金については、**自動請求** ページの明細行セクションで、.01 ドル と 100 ドルの間の注文に対して適用されるであろう料金を 10.00 ドルとして定義してください。 100.01 ドル以上の注文には費用がかからないことを示すために別の請求金額の明細行を作成します。

![自動請求テーブルの 2 つの例。](media/headerchargesexample.png)

航空便の料金については、自動請求フォームの明細行セクションで、すべての注文 (0.01 ドルから 9,999,999 ドルの間) に適用される 20.00 ドルの費用を定義します。

**1040 配送スケジュール** ジョブを実行して、POS がそれらを利用できるように Commerce Scale Unit/Channel DB に変更を送信します。

#### <a name="sales-processing-for-this-scenario"></a>このシナリオの販売処理

上記の設定手順が完了し、変更がチャネル データベースに適用された後、陸送便または航空便の配送方法をヘッダー レベルに設定した POS 、コール センター、または E コマース チャネルで作成された顧客注文または販売トランザクションは、これらの費用を利用して自動的に販売に適用します。

現時点では、自動請求設定が特定の販売チャネルにのみ適用されることを指定する機能がないため、これらの配送モードを利用する法人内で作成されたすべての販売トランザクションに請求が適用されます。

POS および E コマースのシナリオでは、これらの注文に明確に定義された「ヘッダー」がないため、トランザクションのすべての販売明細行がまったく同じ配送モードで出荷するように設定されている場合のみヘッダー レベルの料金が適用されます。 POS または E コマースによって作成されたトランザクションに「混合モード」のフルフィルメントがある場合、明細行レベルの自動請求のみが考慮され適用されます。

コール センターのシナリオでは、ユーザーが注文ヘッダーで出荷方法の設定を制御できるため、一部の販売明細行が別の出荷方法を使用するように構成されている場合でも、ヘッダーレベルの料金がこれらの注文に適用されます。 コール センターの注文に対するヘッダー レベルの料金は、常に販売注文の注文ヘッダー レベルで定義されている出荷方法に基づきます。

### <a name="auto-charges-line-charges-example"></a>明細行諸費用の自動請求の例

#### <a name="use-case-scenario"></a>ユース ケース シナリオ 

小売業者は、顧客が特定のモデルのコンピューターを購入した際にかかる設定料金を、顧客に追加請求したいと考えています。 このコンピューターは、小売業者が顧客のために行う追加設定が必須です。 小売業者は、この設定に追加料金がかかることを顧客に通知しました。 小売業者は、財務報告の目的で、この料金を製品販売価格とは別に管理することを希望しています。 この特定のコンピューターを任意のチャネルで購入すると、19.99 ドルの設定料金が顧客に請求されます。

#### <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

このシナリオでは、1 つの明細行自動請求テーブルのコンフィギュレーションが必要です。

**買掛金 \> 諸費用の設定 \> 自動請求** に移動します。

**レベル** ドロップダウン メニューを **明細行** に設定し、すべての顧客および設定料金が請求される特定の製品または製品グループに対して、新しい自動請求レコードを作成します。

![1 つの明細行レベルの自動請求テーブルの例。](media/linechargesexample.png)

**1040 配送スケジュール** ジョブを実行して、POS がそれらを利用できるように Commerce Scale Unit/Channel DB に請求金額を送信します。

#### <a name="sales-processing-for-this-scenario"></a>このシナリオの販売処理

上記の設定手順が完了し、変更がチャネル データベースに適用された後、この品目が注文に含まれている POS 、コール センター、または E コマース チャネルで作成された顧客注文または販売トランザクションは、明細行レベルの料金が注文合計に体系的に追加されるようにトリガーします。

現時点では、特定の販売チャネルにのみ適用されるように明細行レベルの自動請求を設定する機能がないため、法人内の明細行レベルの自動請求設定と一致するすべての販売明細行に請求が適用されます。

### <a name="manual-header-charges-example"></a>手動ヘッダー諸費用の例

#### <a name="use-case-scenario-description"></a>ユース ケース シナリオの説明

小売業者は、店舗で製品を注文する顧客に特別な宅配方法の提供を提案することによって、標準的なプロセスに例外を設けています。 小売業者と顧客は、顧客がこのサービスに対して 25 ドルの追加手数料を支払うことに同意しました。 受注者はこの追加料金をトランザクションに追加する必要があります。 手数料は一律であり、注文のどの製品にも関連していないため、ヘッダー諸費用が使用されます。

#### <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

**売掛金\>諸費用の設定\>請求金額** に移動して、このシナリオで使用される請求コードが正しく設定されていることを確認してください。

![請求の例。](media/chargesexample.png)

配送関係の割引やプロモーションの目的で、請求金額を「配送」関係のものとみなす場合は、請求コードの **出荷費用** を **はい** に設定します。 この請求金額が POS アプリケーションでの返品トランザクションの処理中に体系的に払い戻されることも許可されている場合は、**払戻可能** を **はい** に設定します。 **払戻可能** フラグは、**高度な自動請求を使用する** のパラメーターが **はい** に設定されている場合にのみ適用されます。

**1040 配送スケジュール** ジョブを実行して、POS がそれらを利用できるように Commerce Scale Unit/Channel DB に請求金額を送信します。

POS からユーザーがアクセスできるボタンがこの操作を呼び出すことができるように、**ヘッダー諸費用の追加** 操作を[POS 画面レイアウト](/dynamics365/unified-operations/retail/pos-screen-layouts)に設定する必要があります (操作 141)。 画面レイアウトの変更は、配送スケジュール機能を介してチャネルにも配信する必要があります。

#### <a name="sales-processing-of-manual-header-charges"></a>手動ヘッダー諸費用の販売処理

POS アプリケーションでシナリオを実行するために、POS ユーザーは通常通りに販売トランザクションを作成し、製品およびその他の構成を販売に追加します。 支払を回収する前に、ユーザーは **ヘッダー諸費用を追加** の操作を実行する必要があります。これはユーザーに費用コードを選択して料金値を入力するように促します。 ユーザーがプロセスを完了すると、料金はヘッダー レベルの請求金額として販売注文に追加されます。

このプロセスは、ツールバーの **販売** タブにある既存の **請求金額** 機能を使用してコール センターに適用できます。 **諸費用の管理** ページで、ユーザーは新しい注文ヘッダーに請求金額の明細行を追加できます。

### <a name="manual-line-charges-example"></a>手動雑費明細行の例

#### <a name="use-case-scenario"></a>ユース ケース シナリオ

顧客が、5 品目の販売注文のうち 2 品目を贈答用に包装するように要求しました。 小売業者は、品目ごとに 2.00 ドルの手数料でこのオプションのサービスを提供します。 受注者は、贈答用包装が必要な特定の品目にこれらの手数料を追加する必要があります。

#### <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

**売掛金\>諸費用の設定\>請求金額** に移動して、このシナリオで使用される請求コードが正しく設定されていることを確認してください。

出荷関係の割引やプロモーションの目的で、請求金額を「出荷」関係のものとみなす場合は、請求コードの **出荷費用** を **はい** に設定します。 請求金額が POS アプリケーションでの返品トランザクションの処理中に体系的に払い戻されることも許可されている場合は、**払戻可能** を **はい** に設定します。 **払戻可能** フラグは、**高度な自動請求を使用する** のパラメーターが **はい** に設定されている場合にのみ適用されます。

**1040 配送スケジュール** ジョブを実行して、POS がそれらを利用できるように Commerce Scale Unit/Channel DB に請求金額を送信します。

POS からユーザーがアクセスできるボタンがこの操作を呼び出すことができるように、**雑費明細行の追加** 操作を [POS 画面レイアウト](/dynamics365/unified-operations/retail/pos-screen-layouts)に設定する必要があります (操作 140)。 画面レイアウトの変更は、配送スケジュール機能を介してチャネルにも配信する必要があります。

#### <a name="sales-processing-of-the-manual-line-charge"></a>手動雑費明細行の販売処理

POS アプリケーションでシナリオを実行するために、POS ユーザーは通常通りに販売トランザクションを作成し、製品およびその他の構成を販売に追加します。 支払を回収する前に、ユーザーは POS 品目リスト表示から請求が適用される特定の明細行を選択し、**雑費明細行を追加** の操作を実行する必要があります。 ユーザーは、費用コードを選択して、請求金額を入力するように要求されます。 ユーザーがプロセスを完了すると、料金は明細行にリンクされ、明細行レベルの請求金額として注文合計に追加されます。 必要に応じて、ユーザーはこの処理を繰り返して、トランザクションの他の品目明細行に他の明細行の諸費用を追加できます。

**販売注文** ページの **販売注文明細行** セクションの **財務** ドロップダウン メニューの下にある「諸費用の管理」機能を使用することによって、同じ処理をコール センターに適用することができます。 このオプションを選択すると、**諸費用の管理** ページが開き、ユーザーは新しい明細行の特定の費用をトランザクションに追加できます。

## <a name="additional-features"></a>追加機能

### <a name="editing-charges-on-a-pos-sales-transaction"></a>POS 販売トランザクションでの請求金額の編集

**諸費用の管理** 操作 (142) を [POS 画面レイアウト](/dynamics365/unified-operations/retail/pos-screen-layouts) に追加して、ユーザーがシステム計算または手動で作成されたヘッダーまたは明細行レベルの諸費用を表示および編集または上書きできるようにします。 工程が追加されていない場合、ユーザーはPOSトランザクションの請求金額を調整することも、請求に関連付けられている費用コードのタイプなどの詳細を表示することもできません。

POS の **諸費用の管理** ページで、ユーザーはヘッダーおよび明細行レベルの請求金額の詳細を表示できます。 ユーザーはこのページで利用可能な **編集** 機能を使用して、特定の請求金額の明細行に請求される金額を変更することができます。 請求金額の明細行が手動で上書きされると、ユーザーが **請求金額の再計算** 操作をしない限り、体系的に再計算されることはありません。

**請求金額の上書き理由コード** が **Commerce パラメーター** 設定ページで設定されている場合、POS アプリケーションで請求料金が変更されたときに、ユーザーは理由コードを入力するように求められます。

上書きされた請求金額についての理由コードがキャプチャされている場合は、これらの上書きを確認および監査するための新しいレポートも利用可能です。 レポートは **Retail および Commerce\>照会およびレポート\>請求金額の上書き履歴** にあります。

### <a name="refunding-charges-on-a-pos-return-transaction"></a>POS 返品トランザクションの請求金額の返金

**高度な自動請求を使用する** のパラメーターが **はい** に設定されている場合、**出荷費用の返金** の既存の Commerce パラメーターは適用されなくなります。 高度な自動請求を使用する場合にどの請求金額を体系的に顧客に返金する必要があるかを示すには、関連する費用コードが **諸費用コード** 設定ページで **払戻可能** に設定されていることを確認します。 配送スケジュール処理によって、設定が Commerce チャネル データベースと同期されていることを確認してください。

> [!TIP]
> 明細行レベルの返金可能な請求金額が、返品数量に基づいて計算されることを確認するためのガイダンスは、[返金可能な請求金額は、返品数量に基づいて計算されません](/troubleshoot/Refund-charges-miscalculated-for-partial-quantity-returned.md) を参照してください。

### <a name="refunding-charges-on-a-return-order-transaction"></a>注文トランザクションの請求金額の返金

請求金額は、Commerce で作成された **返品注文** に体系的に返金されません。 **返品注文** を作成するときに、**諸費用のコピー** オプションを選択する必要があります。 **諸費用のコピー** が選択されていない場合、元の販売トランザクションからの請求金額は自動的に返金されません。 **諸費用のコピー** が選択されている場合、すべての請求金額が返品注文にコピーされ、ユーザーは返金したくない請求金額を編集または削除できます。 コール センターの返品注文プロセスでは、現在 **諸費用コード** 設定の **払戻可能** フラグを認識しません。

### <a name="configuring-pos-receipts-to-show-charges"></a>請求金額を表示する POS レシートのコンフィギュレーション

高度な自動請求機能をサポートするために、次のレシート要素がレシート明細行とフッターに追加されました。

- **明細行出荷費用** – この明細行レベルの要素は、販売明細行に適用されている特定の費用コードを再計算するために使用されます。 **諸費用コード** ページで **出荷** 費用とフラグ設定されている費用コードのみがここに表示されます。
- **明細行その他の請求金額** – この明細行レベルの要素は、販売明細行に適用されている出荷以外の特定の費用コードを再計算するために使用されます。 **明細行その他の請求金額** は、**諸費用コード** ページの **出荷** フラグ設定が有効になっていない費用コードです。
- **注文出荷費用の詳細** – このフッター レベルの要素は、**諸費用コード** で **出荷** 費用とフラグ設定されている注文に適用される費用コードの説明を表示します。
- **注文出荷費用** – このフッター レベル要素は、出荷関係の費用のドル価値を示します。
- **注文の諸掛の詳細** – このフッターレベルの要素は、出荷関係の費用としてフラグ設定されていない注文に適用される費用コードの説明を表示します。
- **注文の諸掛** – このフッター レベルの要素は、出荷関連ではない他の費用のドル価値を表示します。

請求金額を再計算する範囲を定義するために、組織が領収書フッターに自由書式のフィールドを追加することをお勧めします。

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>POS 注文が完了するまでに請求が計算されないようにする

一部の組織では、ユーザーがすべての販売明細行を POS トランザクションに追加し終えるまで、請求金額の計算を待つ場合があります。 品目が POS トランザクションに追加されるときに請求金額が計算されないようにするには、店舗で使用される **機能プロファイル** の **手動による請求金額の計算** のパラメーターをオンにします。 このパラメーターを有効にすると、POS ユーザーは製品の POS トランザクションへの追加が完了したときに **合計を計算する** 操作を行う必要があります。 **合計を計算する** 操作は、必要に応じて注文ヘッダーまたは明細行の自動請求の計算をトリガーします。

### <a name="charges-override-reports"></a>請求金額の上書きレポート

ユーザーが、計算済みの請求金額を手動でオーバーライドするか、または手動の請求金額をトランザクションに追加した場合、監査のためにデータは **請求金額のオーバーライド履歴** レポートで使用可能になります。 レポートは **Retail および Commerce\>照会およびレポート\>請求金額の上書き履歴** からアクセスできます。 このレポートに必要なデータはチャネル データベースから "P" 配信スケジュール ジョブを使用して HQ にインポートされることに注意するのは重要です。 したがって、POS で実行された直後のオーバーライドに関する情報は、このジョブが HQ に店舗のトランザクション データをアップロードするまで、すぐにはレポートで使用可能になりません。

## <a name="additional-resources"></a>追加リソース

[チャンルごとの自動請求の有効化とコンフィギュレーション](auto-charges-by-channel.md)

[ヘッダー請求金額を一致する販売明細行に比例配分する](pro-rate-charges-matching-lines.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
