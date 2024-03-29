---
title: 発注書に対する入庫積荷の倉庫処理
description: この記事では、発注書に対する入庫積荷の倉庫処理プロセスについて説明します。
author: Mirzaab
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 38d5ba96690dd855556a7f69591ef5b9ee5f9d7b
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335678"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>発注書に対する入庫積荷の倉庫処理

[!include [banner](../includes/banner.md)]

この記事では、発注書に対する入庫積荷の倉庫処理プロセスについて説明します。

入庫積荷ごとに、システムには既に関連する販売注文が含まれている必要があり、関連する積荷の仕様や輸送計画、またはその両方が含まれている場合もあります。 入庫積荷の作成および管理方法の詳細については、[業務プロセス: 入庫積荷の配送計画](/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads) を参照してください。

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>概要: 入庫積荷の作成、登録、および受信方法

次の図は、倉庫に到着したときに発注書数量がある入庫積荷を処理するための一般的なフローを示しています。

![入庫積荷の処理プロセス。](media/inbound-process.png "入庫積荷の処理プロセス")

1. **仕入先が発注書を確定します。**

    プロセスは、発注書がシステムに入力されて、注文を確定する仕入先に配信されると開始されます。 発注書は、入庫積荷レコードを作成する前に存在している必要があります。 ただし、注文が確定されていない場合でも、入庫積荷を作成できます。 詳細については、[発注書の承認と確認](../procurement/purchase-order-approval-confirmation.md) を参照してください。

1. **着荷とその内容を計画するために、入庫積荷レコードが作成されます。**

    入庫積荷レコードは、1 つ以上の発注書の仕入先出荷を表します。 積荷は、1 つの物理的な輸送単位 (トラックなど) として倉庫に到着すると予想されます。 入庫積荷レコードは計画目的で使用され、物流コーディネーターは仕入先から積荷の進捗状況を追跡できます。 また、注文明細行の数量を登録したり、到着作業や棚入作業など倉庫業務の進捗を管理するためにも使用されます。 積荷は、自動または手動で作成でき、仕入先からの発注書または事前出荷通知 (ASN) のいずれかに基づいて作成できます。 詳細については、[入庫積荷を作成または変更する](/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load) を参照してください。

1. **仕入先は、積荷の発送を確認します。**

    仕入先が積荷を発送すると、受入倉庫の物流コーディネーターは、積荷の出荷を確認します。 受入会社が **輸送管理** モジュールを使用している場合、インバウンド出荷の確認により、入庫積荷に関連付けられたその他の積荷管理プロセスが開始されます。 詳細については、[出荷用の積荷を確認する](/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping) を参照してください。

1. **積荷が倉庫に到着し、作業者が数量を登録します。**

    トラックが倉庫の入庫ドックに到着すると、倉庫作業者が積荷の数量を登録します。 **倉庫管理** モジュールを使用する場合、作業者はモバイル デバイスを使用して登録を行います。 詳細については、[発注書に対する製品受領書 - 登録](../procurement/product-receipt-against-purchase-orders.md#registration) および [入荷時に到着する品目数量の登録](#register-item-quantities-arriving) セクションを参照してください。

1. **登録済積荷数量は、発注書に転記されます。**

    積荷数量が着荷済として登録された後、これらの数量は製品受領書である必要があります - つまり、現物の在庫増加を記録するために、会社の在庫元帳に転記されます。 詳細については、[発注書に対する製品受領書 - 製品受領書](../procurement/product-receipt-against-purchase-orders.md#product-receipt) と [登録済製品数量を発注書に転記する](#post-registered-quantities) を参照してください。

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>入荷時に到着する品目数量の登録

Microsoft Dynamics 365 Supply Chain Management は、注文済製品の到着を記録するためのいくつかの運用方法をサポートします。 したがって、特定の業務要件に合わせてシステムをコンフィギュレーションができます。 このセクションでは、システムで倉庫管理プロセス (WMS) が有効になっている場合に、モバイル デバイスを使用して、入荷品目数量を登録する方法について説明します。 ただし、モバイル デバイスの代わりに着荷仕訳帳を使用することに基づく代替フローがあります。 そのフローの詳細については、[品目の着荷仕訳帳を使用した倉庫管理プロセスに対応した品目の登録](tasks/register-items-advanced-warehousing.md)を参照してください。

最初に、倉庫に入庫積荷が到着したとき、倉庫作業者は、出荷に含まれる品目の数量を登録する必要があります。 通常は、ハンドヘルド スキャナーを使用します。 このワークフローは、システムに次の品目が存在する場合にのみ使用できます:

- **出荷で予定されている品目の数量を説明する入庫積荷レコード**

    通常、仕入先は、出荷が倉庫に到着する前に入庫積荷レコードを確認します。 したがって、積荷は _出荷済_ 状態になります。 ただし、倉庫作業者は、状態が _未処理_ または _受入済_ である積荷についても品目数量を登録することができます。

- **積荷入庫をサポートするようにコンフィギュレーションされたモバイル デバイス メニュー**

    モバイル デバイス用の[倉庫管理モバイル アプリ](../warehousing/install-configure-warehouse-management-app.md) は、次の作業作成プロセスをサポートします :

    - 積荷品目入庫
    - 積荷品目入庫とプット アウェイ
    - 混合ライセンス プレートの受取では、モバイル デバイス メニュー項目の **元伝票明細行 ID メソッド** フィールドが _積荷品目入庫_ に設定されます。 詳細については、[混合ライセンス プレートの受取](mixed-license-plate-receiving.md) を参照してください。
    - 混合ライセンス プレートの受取とプット アウェイでは、モバイル デバイス メニュー項目の **元伝票明細行 ID メソッド** フィールドが _積荷品目入庫_ に設定されます。 詳細については、[混合ライセンス プレートの受取](mixed-license-plate-receiving.md) を参照してください。

    > [!NOTE]
    > プロセスに関係なく、入荷場所に登録されている数量を取得し、それらを通常の保管場所に保管する作業がシステムによって生成されます。 _積荷品目入庫とプット アウェイ_ または _混合ライセンス プレートの受取とプット アウェイ_ プロセスを使用すると、積荷数量を登録した作業者に対しても、登録タスクの一環として、デバイスからプット アウェイ作業を行うよう指示が出されます。 対照的に、_積荷品目入庫_ と _混合ライセンス プレートの受取_ プロセスの場合、プット アウェイ作業は登録タスクから切り離して行われることが前提です。

- **入庫積荷のピッキングとプット作業を定義する作業テンプレート**

    この品目は、前の品目に関連付けられています。 _発注書_ の作業指示書タイプには少なくとも 1 つの作業テンプレートが必要であり、ピック/プット作業タイプのセットが含まれている必要があります。

モバイル デバイスは、積荷数量登録のフローで倉庫の入庫係をガイドします。 少なくとも、このフローには、各積荷 ID について次の手順が含まれます:

1. 積荷 ID を入力します。
2. 入庫済品目の品目番号を入力します。
3. 受け取った品目番号の数量を入力します。
4. この番号を自動的に生成するようにシステムが設定されていない場合は、品目の最初の場所のライセンス プレート番号を入力します。
5. **OK** をタップします。

作業者がこれらの手順を完了すると、購買注文明細行の数量が 1 つの積荷で到達し、すべての積荷数量が登録されている場合、システムは適切なエンティティに対して次の更新を行います:

| エンティティ | 更新 | 注記 |
|---|---|---|
| 積載 | 積荷明細行の **作業作成数量** フィールドが更新され、登録済数量が表示されます。 | 積荷の出荷確認が実行されていない場合、**積荷の状態** 値は、_出荷済_ または _未処理_ のままになります。 少なくとも 1 行のプット アウェイ作業が開始されている場合は、_処理中_ に変更されます。 |
| 関連する積荷数量がに登録されている発注書の在庫トランザクション |<p>次のフィールドが更新されます:</p><ul><li><b>受領</b> フィールドは <i>登録済</i> に設定されます。</li><li><b>場所</b> フィールドが、入庫ドックの場所コードで更新されます。 (このコードは、各倉庫の <b>既定の受入場所</b> フィールドで指定されます。)</li><li><b>ライセンス プレート</b> フィールドは、登録時に入力または生成されたライセンス プレート番号で更新されます。</li><li><b>積荷 ID</b> フィールドは、数量が登録された積荷の数で更新されます。 (注記を参照。)</li></ul> | 発注書の在庫トランザクションと積荷に対して登録された数量を関連付ける機能は、_発注書の在庫トランザクションを積荷と関連付ける_ という名前のオプション機能としてバージョン 10.0.9 で導入されました。 この機能は、購入済商品の単一注文が複数の積荷として出荷される運用フロー、または積荷に複数の発注書数量が含まれる場合に特に役立ちます。 |
| 倉庫のプット アウェイ | 作業は作業テンプレートに基づいて作成され、登録済数量を入荷場所から通常の保管場所に移動するように作業者に指示します。 | 保管場所の選択は、プット 場所のディレクティブによって制御されます。 場所のディレクティブが定義されていない場合、作業のプット アウェイの場所は空になります。 |

倉庫作業者は、_積荷品目入庫_ プロセスを使用せずに、1 つ以上の関連付けられた積荷とともに、発注書の受入を登録できます。 次の方法を選択できます。

- **モバイル デバイスで:** _発注書明細行受取_ および _発注書明細行受取とプット アウェイ_ プロセスを使用します。 (購買注文明細行の数量に対して複数の積荷が存在する場合、作業者は _発注書明細行受取_ プロセスを使用できません。 代わりに、作業者は、_積荷品目入庫_ プロセスに関連付けられているデバイス アクションを使用するように指示されます。)
- **クライアント側:** 着荷仕訳帳を使用します。
- **クライアント側:** 購買注文明細行からアクセスできる **登録** アクションを使用します。

> [!NOTE]
> 上記のいずれかの方法を使用して発注書受入が登録されている場合、_注書の在庫トランザクションを積荷と関連付ける_ 機能がオンになっていても、発注書の在庫トランザクションと積荷の間にリンクは作成されません。 このルールの例外の 1 つとして、**発注書明細行受取** オプションを使用し、注文明細行に対して _受入済_ 以外の状態をもつ積荷が 1 つのみの場合です。

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>入庫積荷数量の登録時に不一致を処理する

倉庫作業者は、部分的な積荷数量の入庫登録を行うことができます。 次に、各部分な積荷数量の入庫により、登録済数量の受入状態が _登録済_ の個別の在庫トランザクションが作成され、ロット ID は元の購買注文明細行を参照します。

#### <a name="load-under-receiving"></a>積荷の入荷不足

積荷が到達したときに、品目の数量が、積荷レコードに示されている数量よりも少ない場合、倉庫の入庫担当は、到着して登録された実際の数量と一致するように、クライアントで直接作業して、積荷明細行の数量を減らすことでこの不一致を確認できます。

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>積荷の入庫超過

超過入荷は、積荷が到達し、品目の数量が予定される積荷明細行の数量を超過した場合に発生します。 入庫登録時に、超過入庫を許可するかどうか、またどの程度許可するかを制御できます。

倉庫作業者が超過配送を登録しようとしたときに発生する処理を制御するには、関連するモバイル デバイス メニュー項目の **受入超過積荷** フィールドを使用します。 このフィールドは、次のタイプの作業作成プロセスを使用するモバイル デバイス メニュー項目で使用できます:

- 積荷品目入庫
- 積荷品目入庫とプット アウェイ
- 混合ライセンス プレートの受取 (**元伝票明細行 ID メソッド** フィールドが _積荷品目入庫_ に設定されている場合)
- 混合ライセンス プレートの受取とプット アウェイ (**元伝票明細行 ID メソッド** フィールドが _積荷品目入庫_ に設定されている場合)

次の表では、**受入超過積荷** フィールドで使用できるオプションについて説明します。

| 先頭値 | 説明 |
|---|---|
| 許可 | 従業員は、選択した積荷の残りの未登録数量を超える数量の受入を登録できますが、登録数量の合計が、積荷に関連付けられている購買注文明細行の数量 (超過配送率の調整後) を超えていない場合に限ります。 |
| ブロック | <p>作業者は、選択した積荷の残りの未登録数量を超える数量 (超過配送率の調整後) の受入を登録できません。 受入を登録しようとする作業者にエラーが表示され、未登録の残りの積荷数量と同じかそれ以下の数量を登録するまで続行できません。</p><p>既定では、積荷明細行の超過配送率の値は、関連付けられている購買注文明細行からコピーされます。 <b>受入超過積荷</b> フィールドが <i>ブロック</i> に設定されている場合、システムは超過配送率の値を使用して、積荷明細行に登録できる合計数量を計算します。 ただし、その値は、必要に応じて個々の積荷に対して上書きできます。 この動作は、注文明細行の超過配送率を表す超過数量の一部またはすべてが複数の積荷に不均等に配分される受入フローで重要になります。 以下はシナリオの例です:</p><ul><li>1 つの購買注文明細行に対して複数の積荷があります。</li><li>購買注文明細行に 0 (ゼロ) を超える超過配送率があります。</li><li>数量は、超過配送率を考慮せずに 1 つ以上の積荷に対して既に登録されています。</li><li>超過配送数量が最終積荷で到着します。</li></ul><p>このシナリオでは、倉庫監督者が関連する積荷明細行の超過配送率を既定値から最終積荷に全超過配送を登録できるように十分な大きさの値に増加させた場合のみ、モバイル デバイスを使用して超過数量を登録することができます。</p> |
| 終了した積荷のみをブロック | 作業者は、オープンな積荷に対して積荷明細行の数量を超過入庫できますが、状態が _受入済_ である積荷に対してはできません。 |

> [!NOTE]
> **受入超過積荷** フィールドの既定値は、_許可_ です。 この値を使用すると、動作はバージョン 10.0.11 で _積荷数量の受入超過_ 機能が導入される前に使用可能であった標準動作と一致します。

### <a name="put-away-the-registered-quantities"></a>登録済数量のプット アウェイ

モバイル デバイスでの登録が完了すると、_数量の入庫登録_ アクションによって在庫と倉庫レコードが更新され、数量が入庫ドックの場所にあり、予約可能であることが示されます。 ただし、通常、会社の倉庫業務では、数量を入庫ドックから通常の倉庫保管場所に移動して、後続のピッキング プロセスを実行できるようにする必要があります。 プット アウェイの指示は、入庫積荷が受入済として登録された場合に、自動的に生成されるプット アウェイ作業でキャプチャされます。

倉庫作業者がプット アウェイ作業を完了すると、次のテーブルに示すように、更新によっていくつかのエンティティが更新され、結果を記録および追跡します。

| エンティティ | 更新 | 注記 |
|---|---|---|
| 積載 | <p>次のフィールドが更新されます:</p><ul><li><b>積荷の状態</b> 値が <i>処理中</i> に変更されます。</li><li><b>作業状態</b> 値が <i>作業の完了 100.00%</i> に変更されます。</li></ul> | 作業者が少なくとも 1 行のプット アウェイ作業に対してプット アウェイ タスクを開始すると、**積荷の状態** 値が、_処理中_ に変更されます。 |
| 関連する数量がプット アウェイされている作業の在庫トランザクション | **入庫** と **場所** フィールド、およびその他の関連フィールドは、入荷場所から保管場所への移動を反映するように更新されます。 | 発注書の在庫トランザクションの **入庫状態** 値は、_登録済_ のままです。 |
| 倉庫のプット アウェイ | **作業状態** 値が _クローズ済_ に変更されます。 | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>登録済製品数量を発注書に転記する

入庫製品の数量がシステムに登録されると、販売およびその他の出庫および内部業務に関連して予約できるようになります。 ただし、システムは在庫 (中間) 勘定をまだ更新しません。 この更新は、業務チームが登録済製品受領書を転記した場合にのみ発生します。

製品受領書を転記できるページを開くには、業務チームのメンバーは、次の手順の _いずれか_ に従います。

- 関連する積荷レコードを開き、**製品受領書** アクションを選択します。
- **倉庫管理 \> 定期処理のタスク \> 製品受領書の更新** に移動し、**積荷 ID** フィールドで、転記する積荷を指定します。
- 関連する発注書を開き、**製品受領書** アクションを選択します。
- **調達 \> 発注書 \> 製品の入荷 \> 製品受領書ジョブの転記** に移動します。

**積荷** ページ (および更新ジョブの同等ページである **製品受領書の更新** ページ) で使用可能な **製品受領書** アクションは、状態が _登録済_ の発注書の数量についてのみ、製品受領書の数量を更新します。 ただし、**発注書** ページで使用可能な **製品受領書** アクションには、両方の処理状態 (_注文済_ と _登録済_) で数量を含めることができます。 また、_入庫数量_ や _登録済数量とサービス_ などの追加パラメータを使用して、製品受領書の転記の範囲を制御することもできます。

状態が _確定済_ の注文のみが、製品受領書になります、つまり転記できます。 未確認の発注書の場合、**製品受領書** アクションは利用不可と表示されます。

### <a name="post-registered-quantities-from-the-load-page"></a>積荷ページから登録数量を転記する

製品の入庫を行い、**積荷** ページから登録済数量を転記するには、次の前提条件が整っている必要があります。

- 積荷には、状態が _登録済_ である数量単位が少なくとも 1 つ必要です。
- 積荷状態は _出荷済_ である必要があります。
- 積荷に関連付けられている発注書は、状態が _確認済_ である必要があります。

> [!NOTE]
> 積荷状態が _出荷済_ に設定されていない場合、システムは、製品受領書の更新を実行する前に、自動的に積荷を確認します。 (積荷状態は、ユーザーが積荷のインバウンド出荷を登録したときに、_出荷済_ に設定されます。)

製品の入庫を行い、選択済積荷に関連付けられている着荷登録を転記するには、作業者は **積荷** ページで **製品受領書** アクションを選択します。 開かれたページには、次の主要な詳細があります:

- **設定** タブの **パラメータ** セクションの **数量** フィールドには、_登録済数量_ が表示されます。 ここではその他のオプションは使用できません。
- **概要** クイック タブのグリッドには、選択済積荷に含まれるすべての発注書が一覧表示されます。
- **明細行** クイック タブのグリッドには、登録済数量を含むすべての注文明細行が表示されます。

> [!NOTE]
> **明細行** タブに表示される注文明細行の数量は、Supply Chain Management のバージョンで _積荷ごとに複数の製品受領書を許可する_ 機能が使用可能使用であり、有効になっているかどうかによって、異なる計算が実行されます。
>
> | バージョン | 計算 |
> |---|---|
> | バージョン 10.0.10 より前のバージョン、および _積荷ごとに複数の製品受領書を許可する_ 機能が有効になっていない新しいバージョン | 明細行の数量は、モバイル デバイスまたはクライアントから積荷とは無関係に複数の積荷に対して登録が行われたかどうかに関係なく、_その購買注文明細行_ のすべての登録済数量の合計です。 |
> | バージョン 10.0.10 以降では、_積荷ごとに複数の製品受領書を許可する_ 機能が有効になっています | 明細行の数量は、**製品受領書の転記** アクションが開始された、_積荷レコード_ のすべての登録済数量の合計です。 |

ユーザーが **OK** を選択して、製品受領書の転記を確認すると、システムは適切なエンティティに対して次のキー更新を行います。

| エンティティ | 更新 |
|---|---|
| 明細行の数量が転記の範囲に含まれている発注書の在庫トランザクション | <p>次のフィールドが更新されます (ただし、他にも複数の更新があることに注意してください):</p><ul><li><b>受領</b> フィールドは <i>登録済</i> に設定されます。</li><li><b>現物日付</b> フィールドは、転記の日付で更新されます。</li></ul> |
| ユーザーが製品受領書を転記した積荷 | 積荷の更新は、使用されているバージョンと、**積荷ごとに複数の製品受領書を許可する** フィールドの設定によって異なります。 ルールについては、このセクションの後半のテーブルで説明します。 |

**積荷ごとに複数の製品受領書を許可する** フィールドでは、会社が積荷入庫の受取ポリシーを選択できます。 会社は、運用フローに応じて、同じ積荷に対して複数の製品受領書の転記を許可または禁止することを選択できます。 物流マネージャーは、**積荷ごとに複数の製品受領書を許可する** フィールドを次のいずれかの値に設定することをお勧めします。

- **いいえ** – 倉庫の入庫係が、指定した時間枠内に各積荷とともに到着するすべての注文数量を常に登録する場合は、この値を選択します。 積荷数量が登録されていない場合、システムは、到着していないか、積荷にないとみなし、積荷の一部とは見なしません。 積荷から実行される製品受領書の転記は、同じ前提を使用します。 製品受領書に加えて、すべての登録済数量 (その主な機能) を更新し、積荷が完了し、追加処理のためにクローズされたことを宣言します。 この場合、すべての積荷明細行の数量が登録数量に対して自動的に更新され、登録数量が登録されていない積荷明細行は削除され、積荷状態は _受入済_ に変更されます。
- **はい** – 倉庫の入庫係が、到着した積荷のすべての数量を登録するの時間がかかる場合は、この値を選択しますが、その間に、製品の入庫を行い、既に登録済の数量を転記する必要があります。 この場合、物流マネージャーは、製品受領書の転記ジョブが実行された後も積荷をオープンにしておき、残りの積荷数量を登録し、製品受領書を継続的に元帳に更新できるようにします。
- **プロンプト** – 積荷入庫方針が混在しており、製品受領書の転記を実行するたびに決定が必要な場合は、この値を選択します。

次の表に、**積荷ごとに複数の製品受領書を許可する** 設定の効果をまとめます。

| 積荷ごとに複数の製品受領書を許可する | 積荷数量 | 貨物の状態 | 注記 |
|---|---|---|---|
| このフィールドが使用できない場合 (10.0.10 より前のバージョン) | <p>積荷数量は、登録済数量と等しくなるように設定されます。</p><p>積荷数量が 0 (ゼロ) に更新された場合、つまり登録が行われていない場合、積荷明細行が削除されます。</p><p>積荷に積荷明細行がない場合、積荷が削除されます。</p> | _受入済_ | 注文明細行の登録済数量に複数の積荷が存在する場合、受領書が転記された積荷の状態のみが _受入済_ に更新されます。 |
| 無 | <p>積荷数量は、積荷 ID に関連付けられた登録済数量と等しくなるように設定されます。</p><p>在庫トランザクションの積荷 ID が記録されていない場合、10.0.10 より前のバージョンの動作と一致します。</p> | _受入済_ | |
| 有 | 更新なし | _受入済_、登録済積荷数量の合計が積荷数量以上である場合 | |
| 有 | 更新なし | _出荷済_ または _処理中_、登録済積荷数量の合計が積荷数量より少ない場合 | |

**積荷状態** フィールドを _受入済_ に設定すると、その積荷に対してこれ以上製品受領書の転記を行うことはできません。 ただし、次の条件下では、作業者は受入済積荷に対して残りの注文数量を登録できます。 (詳細については、この記事の前半の [積荷の入荷超過](#load-over-receiving) セクションを参照してください。)

- Supply Chain Management のバージョンは 10.0.11 よりも古いバージョンです。
- _積荷数量の受入超過_ 機能がオンになり、積荷品目入庫アクションのモバイル デバイス メニュー項目の **受入超過積荷明細行の数量** フィールドが _許可_ に設定されます。

製品の入庫を行い、状態が _受入済_ の積荷に対して追加の登録済積荷数量を転記するには、関連する発注書から転記アクションを実行する必要があります。

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>発注書ページから登録済数量を転記する

製品の入庫を行い、**発注書** ページから登録済数量を転記するには、**製品受領書** アクションを選択する前に、次の作業を完了します:

- **設定** タブの **パラメータ** セクションで **数量** フィールドを _登録済数量_ に設定します。
- **製品受領書** フィールドに、転記に含まれる発注書の番号を入力します。

> [!NOTE]
> 転記範囲に含まれる明細行の数量は、モバイル デバイスまたはクライアントからの積荷とは無関係に、複数の積荷に対して数量登録が行われたかどうかに関係なく、注文明細行のすべての登録済数量の合計です。 **積荷ごとに複数の製品受領書を許可する** フィールドが使用できない、または有効になっていない場所で実行された場合、製品受領書の転記が積荷から実行される場合も同じルールが適用されます。

ユーザーが **OK** を選択して、製品受領書の転記を確認すると、システムは適切なエンティティに対して次のキー更新を行います。

| エンティティ | 更新 |
|---|---|
| 明細行の数量が転記の範囲に含まれている発注書の在庫トランザクション | <p>次のフィールドが更新されます (ただし、他にも複数の更新があることに注意してください):</p><ul><li><b>受領</b> フィールドは <i>登録済</i> に設定されます。</li><li><b>現物日付</b> フィールドは、製品受領書の転記アクションの日付で更新されます。</li></ul> |
| 積載 | 積荷の更新は、**積荷ごとに複数の製品受領書を許可する** フィールドが使用可能であり、有効になっているかどうかによって異なります。 ルールについては、次のテーブルで説明します。 |

次の表に、**積荷ごとに複数の製品受領書を許可する** 設定の効果をまとめます。

| 積荷ごとに複数の製品受領書を許可 | 積荷数量 | 貨物の状態 | 注記 |
|---|---|---|---|
| このフィールドが無効または使用不可の場合 (10.0.10 より前のバージョン) | 更新なし | 更新は行われません。 (状態は、_未処理_、_出荷済_、または _処理中_ のままです。) | 製品受領書の転記は発注書から開始されるため、更新ロジックには、その範囲内の登録済数量と登録が記録された積荷との間の関連付けに関する情報はありません。 したがって、状態更新の積荷を選択することはできません。 |
| 有効な機能 | 更新なし | <p>次のいずれかのアクションが発生します:</p><ul><li>発注書の在庫トランザクションの入庫済数量と購買済数量の合計が関連付けられている積荷の数量以上の場合、状態は<i>入庫済</i> に変更されます。</li><li>積荷のすべての明細行が前の条件を満たさない場合、状態は <i>未処理</i>、<i>出荷済</i>、<i>処理中</i> のままになります。</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>物流工程に適切な製品受領書の転記オプションを選択する

前に説明したように、システムには 2 つの製品受領書転記オプションが用意されています。 オプションには、次の場所からアクセスできます:

- **積荷** ページ、または **倉庫管理 \> 定期処理のタスク** メニューから更新ジョブとして
- **発注書** ページ、または **調達 \> 発注書 \> 製品の入荷** メニューから更新ジョブとして

積荷を使用して、入庫指示の輸送と倉庫処理を計画および管理する会社は、積荷を処理するように設計された次の機能を使用することをお勧めします:

- 製品数量の到着を積荷に対して登録するための、倉庫モバイル デバイス での **積荷品目入庫** アクション
- 在庫元帳を更新するために、積荷から開始された **製品受領書の転記** アクション

> [!NOTE]
> その他の数量登録および製品受領書転記機能を使用して、対応する入庫業務プロセスをサポートできます。 ただし、専用の積荷に特化した機能と、またはその代わりに使用する場合、積荷レコードのデータ精度と積荷管理フローのシームレスさが損なわれる可能性があります。

## <a name="example-scenarios"></a>シナリオ例

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>サンプル シナリオを実行するためにシステムを準備する

このセクションで説明するサンプル シナリオを実行するには、まず、必要な機能がすべてシステムで有効になっていることを確認する必要があります。 必要なデモデータも、システムで使用できる必要があります。

#### <a name="turn-on-the-required-features"></a>必要な機能を有効にする

これらのシナリオでは、_積荷ごとに複数の製品受領書を転記する_ 機能とその前提条件となる機能が必要です。 管理者は、次の手順に従って、これらの機能を有効にできます。

1. **機能管理** ワークスペースを開きます。 (このワークスペースを検索して使用する方法の詳細については、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。)

1. _発注書の在庫トランザクションと負荷を関連付ける_ 機能がオンになっていることを確認します。 Supply Chain Management のバージョン 10.0.21 の時点では、この機能は必須です。この機能は既定で有効になっていて、再度オフにできない状態です。 ただし、この機能は引き続き次のように[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)にリストされています。

    - **モジュール:** _倉庫管理_
    - **機能名:** _発注書の在庫トランザクションと負荷を関連付ける_

1. 次のように表示される _積荷ごとに複数の製品受領書を転記する_ 機能をオンにします:

    - **モジュール:** _倉庫管理_
    - **機能名:** _積荷ごとに複数の製品受領書を転記する_

#### <a name="enable-sample-data"></a>サンプルデータの有効化

指定されたサンプル レコードと値を使用してこれらのシナリオを実行するには、標準の [デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md) がインストールされているシステムを使用する必要があります。 開始する前に、**USMF** 法人も選択する必要があります。

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>モバイル デバイスの使用時に積荷品目を入庫するメニュー項目を追加する

倉庫の入庫係がモバイル デバイスを使用して、積荷にリンクされている入庫在庫を登録する前に、その目的でモバイル デバイス メニュー項目を作成する必要があります。

このセクションでは、モバイル デバイスのメニュー項目を作成し、既存のメニューに追加します。 倉庫作業者は、メニュー項目を倉庫管理モバイル アプリで選択できるようになります。

1. **倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー項目** に移動し、モバイル デバイス メニューに次の設定のメニュー項目が含まれていることを確認します:

    - **モード:** _作業_
    - **作業作成プロセス:** _積荷品目入庫_
    - **ライセンスプレートの生成:** _はい_

    その他のすべての設定は、既定値のままにすることができます。

    ![モバイル デバイス メニュー項目の設定。](media/inbound-mobile-menu-items.png "モバイル デバイス メニュー項目の設定")

    モバイル デバイス メニュー項目の設定方法の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。

2. メニュー項目の設定が完了したら、**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイス メニュ** に移動し、モバイル デバイスのメニュー構造に追加します。

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>シナリオ例 1: 一部の品目が欠落している積荷を登録する

このシナリオでは、すべての予定数量が存在しない入庫積荷の数量を登録する方法を示します。 次に、発注書用の製品受領書を転記する方法を示します。

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>積荷を作成して、発注書の受入を計画する

この手順では、発注書と関連する積荷を手動で作成します。 次に、積荷を更新して、仕入先から出荷されたことをシミュレートします (積荷の状態を更新する)。 その後、倉庫プランナーは **積荷の状態** で積荷をフィルタし、予定の入庫積荷を検索できます。

1. **調達 \> 発注書 \> すべての発注書** に移動します。
1. **新規** を選択します。
1. **発注書の作成** ダイアログ ボックスで、**仕入先** フィールドを _1001_ に設定します。
1. **OK** を選択し、ダイアログ ボックスを閉じて、発注書を作成します。
1. 新しい発注書には、**購買注文明細行** の下に明細行が既に含まれています。 この明細行に次の値を設定します:

    - **品目番号:** _A0001_
    - **倉庫:** _24_
    - **数量:** _10_

1. アクション ウィンドウの **購買** タブで、**アクション \> 確認** を選択します。 注文の状態が _確認済_ になりました。
1. アクション ウィンドウの **倉庫** タブで、**アクション \> 積荷計画ワークベンチ** を選択します。
1. **積荷計画ワークベンチ** ページの アクション ウィンドウの **供給と需要** タブで、**追加 \> 新しい積荷へ** を選択します。
1. **積荷テンプレートの割り当て** ダイアログ ボックスで、**積荷テンプレート ID** フィールドを _20_ に設定します。
1. **OK** を選択し、ダイアログ ボックスを閉じて、ワークベンチに戻ります。
1. **積荷** セクションで、**積荷 ID** を選択して、新しく作成された積荷を開きます。
1. 積荷ヘッダーと明細行の詳細 を確認して、次の点に注意してください:

    - **積荷** クイックタブでは、**積荷の状態** フィールドが _未処理_ に設定されます。
    - **積荷明細行** セクションには、**数量** フィールドが _10_ に設定され、**作業作成数量** フィールドが _0_ (ゼロ) に設定されている単一明細行があります。

    ![貨物の詳細。](media/inbound-load-details.png "貨物の詳細")

1. アクション ウィンドウの **出荷と入荷** タブで、**確定 \> インバウンド出荷** を選択します。 **積荷の状態** が _出荷済_ に変更されていることに注意してください。
1. 次の手順で使用できるように、**積荷 ID** の値をメモしておきます。

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>積荷で到着した数量の受入を登録する

積荷が倉庫の入庫ドックに到着すると、入庫係は、モバイル デバイスで積荷数量を登録します。

1. モバイル デバイスを使用して、倉庫 24 にサインインします。 (標準デモ データでは、ユーザー IDとして _24_、パスワードとして _1_ を使用してサインインします。)
1. このシナリオ用に作成した _積荷品目入庫_ メニュー項目を選択します。
1. 画面のデータ入力指示に従って、次の値を入力します。 (順序は、使用しているモバイル デバイスやエミュレーターによって異なる場合があります。)

    - **積荷** – 前の手順で作成した積荷 ID を入力します。
    - **品目** – この積荷に必要な品目である _A0001を_ を入力します。
    - **数量** – 積荷に存在する実際の数量として _9_ を入力します。 この数量は予定数量を下回っていることに注意してください。

1. 作業が完了したことがデバイスから通知されるまで、他のすべてのフィールドを空白のままにするか、既定値に設定したまま、ワークフローを続行します。

以上で、積荷入庫タスクが完了し、入庫担当者は次のタスクに進むことができます。 ただし、倉庫の入庫担当は最終的に積荷レコードを確認し、入庫済数量が予定数量を下回っていること確認できるます。 次に、Web クライアントを使用して次の手順を実行します。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 一覧で、入庫した積荷を見つけます。 (積荷の状態が _出荷済_ である入庫積荷を含めるには、**クローズ済の表示** チェック ボックスをオンにする必要がある場合があります。) 次に、**積荷 ID** 列でリンクを選択して積荷を開きます。
1. 積荷レコードで、**積荷の状態** 値は、_出荷済_ のままですが、積荷明細行の **作業作成数量** 値が _9_ に変更されていることに注意してください。
1. **調達 \> 発注書 \> すべての発注書** に移動します。
1. 一覧で、入庫したばかりの購買を検索し、**発注書** 列でリンクを選択して、注文を開きます。
\
1. **購買注文明細行** クイックタブで、**在庫 \> ビュート \> ランザクション** を選択します。
1. 2 つの発注書トランザクションの詳細を確認します。 (**在庫トランザクション** ページをカスタマイズして、グリッドに **積荷 ID** フィールドを表示する必要がある場合があります。) 次の 2 つのトランザクションが表示されます。

    - _登録済_ 状態の受入があるトランザクションは、モバイル デバイスを使用して特定の積荷に対して実行された _9_ の登録数量を表します。 **積荷 ID** は、当該トランザクションに関連付けられています。
    - _注文済_ 状態の受入があるトランザクションは、残りの未登録の注文明細行数量 _1_ を表します。

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>製品の入庫を行い、発注書に登録済積荷数量を転記する

この手順では、製品の入庫を行い、積荷用に登録した在庫を転記します。 その結果、入庫した在庫とそれに関連する原価が、会社の総勘定元帳に追加されます。

1. **倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 一覧で、入庫した積荷を検索します。 (積荷の状態が _出荷済_ である入庫積荷を含めるには、**クローズ済の表示** チェック ボックスをオンにする必要がある場合があります。) 次に、**積荷 ID** 列でリンクを選択して積荷を開きます。
1. アクション ウィンドウの **出荷と入荷** タブで、**入庫 \> 製品受領書** を選択します。 アクションの確認を求められたら、**はい** を選択します。
1. **製品受領書の転記** ダイアログ ボックスの **明細行** クイック タブで、グリッドを調べます。 選択済積荷に対して数量が登録されている購買注文明細行を確認する必要があります。

    > [!NOTE]
    > _積荷ごとに複数の製品受領書を転記する_ 機能が使用できないか、有効になっていないバージョンでは、**積荷明細行** グリッドに表示される既定の数量は、購買注文明細行に関連付けられているすべての積荷で登録された合計数量になります。

1. **概要** クイック タブで、グリッドの **製品受領書** フィールドを調べます。 選択済積荷の ID を含む番号に設定されていることに注意してください。
1. **OK** を選択して製品受領書を転記し、**製品受領書の転記** ダイアログ ボックスを閉じます。
1. 積荷の詳細に戻ります。 次の点に注意してください:

    - **積荷の状態** フィールドが _入庫済_ に設定されます。
    - 積荷明細行では、積荷の **数量** 値が _10_ から _9_ 個に変更され、登録済数量と一致しますが、**作業作成数量** 値は _9_ のままです。

購買チームは、仕入先からの残りの注文数量 1 の配送を想定していない場合は、明細行の配送残量を _0_ に更新することで注文を閉じることができます。 ただし、不足している部品が元の積荷に到達したことがすぐに判明した場合、倉庫の担当者は次のいずれかのアクションを実行できます:

- 数量を同じ積荷に対して登録します。 この場合、**積荷の状態** フィールドは _出荷済_ にリセットされ、**作業作成数量** 値は _10_ に更新されます。 この選択は、次の状況でのみ使用できます:

    - _積荷数量の受入超過_ 機能が使用できないか、または有効になっていません。
    - _積荷数量の受入超過_ 機能が使用可能で有効になっていて、**受入超過積荷明細行の数量** フィールドが _許可_ に設定されています。

- 新規または既存の積荷に数量を加算し、通常の方法で処理します。
- 積荷処理を伴わない方法で数量を登録または入庫します。

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>シナリオ例 2: 一部の品目が不足している複数の入庫積荷に到着する数量を登録する

このシナリオでは、単一の購買注文明細行に関連するインバウンド出荷は 2 つの積荷に分割されます。 たとえば、重量またはボリューム、あるいはその両方に対する物理的な積荷の制約により、1 つの購買注文明細行が複数の積荷に分割される場合があります。

このシナリオでは、同じ積荷に対して複数の製品受領書の転記を処理する方法も示します。 複数の入庫積荷で到着する数量を登録しますが、数量が予定される数量と一致しません。 製品受領書の転記を通じて発生する原価の更新は、同じ積荷に対して複数回行われます。

#### <a name="set-up-load-receiving-policies"></a>積荷入庫ポリシーの設定

この手順では、同じ積荷から複数の製品受領書の転記を有効にします。

1. **倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。
1. **積荷** タブで、**積荷ごとに複数の製品受領書を許可する** フィールドを _はい_ に設定します。

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>2 つの積荷を作成して、発注書の受入を計画する

この手順では、発注書と 2 つの積荷を作成します。 次に、各積荷を手動で更新して、仕入先から出荷されたことをシミュレートします (積荷の状態を更新します)。 その後、倉庫プランナーは **積荷の状態** で積荷をフィルタし、予定の入庫積荷を検索できます。

また、明細行に指定された数量より 20% 多い数量を受け取ることができるように、購買注文明細行を設定する方法についても説明します。

1. **調達 \> 発注書 \> すべての発注書** に移動します。
1. **新規** を選択します。
1. **仕入先** クイックタブで、**仕入先** フィールドを _1001_ に設定して、**OK** を選択します。
1. 新しい発注書が開き、**購買注文明細行** のグリッドに空白行が表示されます。 この注文明細行に次の値を設定します:

    - **品目番号:** _A0001_
    - **倉庫:** _24_
    - **数量:** _10_

1. **明細行の詳細** クイック タブ の **配送** タブで、**超過配送** フィールド を _20_ に設定します。
1. アクション ウィンドウの **購買** タブで、**アクション \> 確認** を選択します。 注文の状態が _確認済_ になりました。
1. アクション ウィンドウの **倉庫** タブで、**アクション \> 積荷計画ワークベンチ** を選択します。
1. **積荷計画ワークベンチ** ページの アクション ウィンドウの **供給と需要** タブで、**追加 \> 新しい積荷へ** を選択します。
1. **積荷テンプレートの割り当て** ダイアログ ボックスで、**積荷テンプレート ID** フィールドを _20_ に設定します。 **詳細** タブで、**数量** 値を _10_ から _5_ に変更して、購買注文明細行の数量を部分的に追加します。
1. **OK** を選択して設定を適用し、ダイアログ ボックスを閉じます。
1. 手順 8 から 10 を繰り返して、2 番目の積荷を作成します。 今回は、**数量** フィールドがすでに _5_ に設定されているはずです。
1. **積荷計画ワークベンチ** ページの **積荷** グリッド で、作成した最初の積荷の **積荷 ID** 値を選択します。 **積荷の詳細** ページが表示され、選択済積荷が表示されます。 以下の手順を実行します。

    1. アクション ウィンドウの **出荷と入荷** タブで、**確定 \> インバウンド出荷** を選択します。
    1. **積荷の状態** 値が _出荷済_ に変更されていることに注意してください。
    1. 閉じるボタンを選択して、**積荷計画ワークベンチ** ページに戻ります。

1. 作成した 2 番目の積荷に対して、前の手順を繰り返します。
1. **積荷** グリッドに表示される 2 つの **積荷 ID** 値をメモします。

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>最初の積荷に到着した数量の部分的な入庫を登録し、登録済積荷数量を転記する

積荷が倉庫の入庫ドックに到着すると、入庫係は、モバイル デバイスに積荷数量を登録します。 積荷にリンクされた登録済在庫は、積荷に基づいて発注書の製品受領書を転記することで、会社の総勘定元帳で原価更新されます。

この手順では、入庫係がモバイル デバイスに積荷数量を登録する方法を示します。

1. モバイル デバイスを使用して、倉庫 24 にサインインします。 (標準デモ データでは、ユーザー IDとして _24_、パスワードとして _1_ を使用してサインインします。)
1. このシナリオ用に作成した _積荷品目入庫_ メニュー項目を選択します。
1. 画面のデータ入力指示に従って、次の値を入力します。 (順序は、使用しているモバイル デバイスやエミュレーターによって異なる場合があります。)

    - **積荷** – 前の手順で作成した最初の積荷 ID を入力します。
    - **品目** – この積荷に必要な品目である _A0001を_ を入力します。
    - **数量** – _3_ を入力します。 この数量は予定数量を下回っていることに注意してください。 このシナリオでは、入庫係として、この積荷のすべての数量を登録する時間がないと仮定します。 この手順の後半で、この手順を繰り返して、**数量** フィールドを _2_ に設定し、残りの数量を登録します。

1. 作業が完了したことがデバイスから通知されるまで、他のすべてのフィールドを空白のままにするか、既定値に設定したまま、ワークフローを続行します。
1. Web クライアントで、**倉庫管理 \> 積荷 \> すべての積荷** に移動します。
1. 一覧で、入庫したばかりの積荷を検索し、**積荷 ID** 値を選択して積荷を開きます。 **積荷の状態** 値は、_出荷済_ のままですが、積荷明細行の **作業作成数量** 値が _3_ に変更されていることに注意してください。
1. アクション ウィンドウの **出荷と入荷** タブで、**入庫 \> 製品受領書** を選択します。 アクションの確認を求められたら、**はい** を選択します。
1. **製品受領書の転記** ダイアログ ボックスで、表示されている値を確認して変更せずに、**OK** を選択します。
1. 選択済積荷の **積荷の詳細** ページに戻ります。 次の点に注意してください:

    - **積荷の状態** フィールドは _出荷済_ のままです。
    - 積荷明細行では、積荷の **数量** 値は、元の積荷数量である _5_ 個のままで、**作業作成数量** 値は _3_ のままです。

1. この手順を繰り返して、この積荷の残りの数量の登録を完了します。 ただし、手順 3では、**数量** フィールドを _2_ に設定します。

これで、最初の積荷入庫タスクが完了しました。 実行した 2 つの製品受領書更新ごとに 1 つずつ、2 つ の製品受領仕訳帳が作成されています。

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>2 番目の積荷に到着した数量の入庫を登録し、超過配送数量を計上する

このシナリオでは、入庫係は積荷にある数量を超える数量を入庫登録します。 システムが超過配送を許可するように設定されているため、超過配送が許可されます。

1. モバイル デバイスを使用して、倉庫 24 にサインインします。 (標準デモ データでは、ユーザー IDとして _24_、パスワードとして _1_ を使用してサインインします。)
1. このシナリオ用に作成した _積荷品目入庫_ メニュー項目を選択します。
1. 画面のデータ入力指示に従って、次の値を入力します。 (順序は、使用しているモバイル デバイスやエミュレーターによって異なる場合があります。)

    - **積荷** – 前に作成した 2 番目の積荷 ID を入力します。
    - **品目** – この積荷に必要な品目である _A0001を_ を入力します。
    - **数量** – _7_ を入力します。これは、仕入先が発注書の合計数量 12 (10 は元の注文数量、2 は 20% の許容超過配送数量です) の一部として配送することを許可されている残りの数量です。 最初の積荷に対して、5 個が既に登録されていることに注意してください。

2 番目の積荷は、数量 7 で更新され、この数量に基づいて製品の入庫を行い、更新できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]