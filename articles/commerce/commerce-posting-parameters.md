---
title: コマース転記パラメーター
description: このトピックでは、Microsoft Dynamics 365 Commerce での財務トランザクションおよび現物トランザクションの転記に固有のパラメータについて説明します。
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649204"
---
# <a name="commerce-posting-parameters"></a>コマース転記パラメーター

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce での財務トランザクションおよび現物トランザクションの転記に固有のパラメータについて説明します。 コマース転記パラメーターは、コマース本部の **小売とコマース \> 本社の設定 \> パラメーター \> コマース パラメーター \> 転記** にあります。

## <a name="periodic-discount-parameters"></a>期間割引パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有の期間割引パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| 期間割引を転記する | このオプションは、期間割引を勘定科目に転記するかどうかを制御します。 期間割引には、組み合わせ割引、数量割引、および割引サービスが含まれます。 このパラメータを有効にすると、**期間割引** セクションで追加のフィールドを設定できます。 |
| 勘定タイプ | <p>期間割引の転記に使用するアカウントのタイプを選択します。</p><ul><li>**標準** – システムはこのページの割引関連フィールドを使用しません。 代わりに、コマース本部の **転記** ページで定義されているアカウントを使用します (**在庫管理 \> 設定 \> 転記 \> 転記フォーム**)。</li><li>**定期処理** – システムは、このページの割引関連フィールドで指定されたコマース割引アカウントを使用します。 このオプションを選択した場合、次のサービスのタイプごとに一般会計 (GL) 勘定を指定する必要があります (割引、組み合わせ、数量、およびしきい値)。 各割引を設定するときに、勘定を定義できます。 割引勘定転記機能が割引設定ページで使用されると、コマース割引 GL 勘定から割引 GL 勘定に転記された割引を再分類するために追加の借方項目および貸方項目が作成されます。 詳細については、[小売割引](retail-discounts-overview.md) を参照してください。</li></ul> |
| 情報コード割引を転記する | このオプションは、標準のコマース ソリューションでは使用されなくなったため、廃止されます。 |
| 注文の期間割引の転記 | このオプションは、小売期間割引を顧客注文やコール センター注文の元帳に転記するかどうかを制御します。 |

## <a name="inventory-update-parameters"></a>在庫更新パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有の在庫更新パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| バッチ番号が見つからない場合は既定のバッチ ID を使用 | このオプションは、バッチ番号が見つからず、マイナス在庫が許可されている場合に、バッチが有効なアイテムに既定のバッチ ID を使用するかどうかを制御します。 |
| 既定のバッチ ID | 品目のバッチ番号が見つからない場合に使用するバッチ番号と、**バッチ番号が見つからない場合は既定のバッチ ID を使用する** パラメーターが有効になっています。 |

## <a name="aggregation-parameters"></a>集計パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有の集計パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| 金庫保管 | このパラメーターを有効にすると、明細転記中にすべてのトランザクションが集計され、各ドロップに個別の明細行を作成するのではなく、転記する仕訳帳に 1 行が作成されます。 |
| 銀行入金 | このパラメーターを有効にすると、明細転記中にすべてのトランザクションが集計され、各ドロップに個別の明細行を作成するのではなく、転記する仕訳帳に 1 行が作成されます。 |
| 販売取引 | このパラメーターを有効にして、取引明細書の転記プロセスの一部としてトランザクションを連結します。 このパラメーターを有効にすることをお勧めします。 以前は、**伝票トランザクション** という名前でした。 |
| 返品を集約できません。 | このオプションが選択されている場合、小売明細書が転記された際に各返品取引は個別の販売注文として転記されます。 |

## <a name="batch-processing-parameters"></a>バッチ処理パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有のバッチ処理パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| 同時明細書の最大数 | このフィールドは、複数の明細書を転記するために使用されるバッチ タスクの数を定義します。 |
| 明細書別注文処理の最大スレッド | このフィールドは、1 つの明細書の販売注文を作成して請求するために、明細書の転記バッチ ジョブで使用するスレッドの最大数を表します。 明細書の転記プロセスが使用するスレッドの総数は、このパラメーターの値に **同時に転記する明細書の最大数** パラメーターの値を掛けることによって計算されます。 このパラメーターの値が高すぎると、明細書転記プロセスのパフォーマンスに悪影響を与える可能性があります。 |
| 集計に含まれる最大トランザクション明細行 | このフィールドは、新しいトランザクションが作成される前に、1 つの集計トランザクションに含まれるトランザクション明細行の数を定義します。 集計トランザクションは、顧客、営業日、財務分析コードなどのさまざまな集計基準に基づいて作成されます。 1 つのトランザクションからの明細行が異なる集計トランザクションに分割されないことに注意してください。 したがって、集計トランザクションの行数が、特徴的製品の数などの要因に基づいて若干増減する可能性があります。 |
| 店舗トランザクションを検証するスレッドの最大数 | このフィールドは、トランザクションの検証に使用されるスレッドの最大数を定義します。 トランザクションの検証は、トランザクションが明細書に取り込まれる前に行われる必要がある必須ステップです。 また、組織がギフトカードを使用していない場合でも、**コマース パラメーター** ページの **転記** タブ上にある **ギフト カード** クイックタブでギフト カード商品を定義する必要があります。 |

次の表に、上記の表のパラメーターの推奨値について一覧表示しています。 これらの値は、配置の構成と使用可能なインフラストラクチャに合わせてテストし、カスタマイズする必要があります。 推奨値を超える値は、他のバッチ処理に悪影響を与える可能性があり、検証する必要があります。

| パラメーター | 推奨値 | 詳細 |
|-----------|-------------------|---------|
| 同時に転記する明細書の最大数 | <p>**明細書** ジョブを実行しているバッチ グループに使用できるバッチ タスクの数にこのパラメータを設定します。</p><p>**一般ルール :** Application Object Server (AOS) 仮想サーバーの数に、AOS 仮想サーバーごとに使用できるバッチ タスクの数を乗算します。</p> | **小売明細書 - チケット フィード** 機能が有効な場合、このパラメータは適用されません。 |
| 明細書別注文処理の最大スレッド | テスト値を **4** で開始します。 通常、この値は **8** を超えてはなりません。 | このパラメーターは、販売注文の作成と転記に使用されるスレッドの数を定義します。 これは、明細書ごとの転記に使用できるスレッドの数を表します。 |
| 集計に含まれる最大トランザクション明細行 | テスト値を **1000** で開始します。 コマース本社構成によっては、注文の数が少ない方がパフォーマンスに役立つ場合があります。 | このパラメータは、明細書の転記時に各販売注文に含める明細行の数を定義します。 この数に達すると、明細行は新しい注文に分割されます。 分割は販売注文レベルで発生するため、販売明細行の数は指定した数と正確には等しくなりません。 しかし、この数は設定された数に近くなります。 このパラメーターを使用して、顧客の名前が付いた小売トランザクションの販売注文を生成します。 |
| 店舗トランザクションを検証するスレッドの最大数 | このパラメータは **4** に設定し、許容できるパフォーマンスを達成できない場合にのみ増加することをお勧めします。 このプロセスで使用するスレッドの数が、バッチ サーバーで使用できるプロセッサの数を超えられません。 スレッド数が多すぎると、他のバッチ処理が影響を受ける可能性があります。 | このパラメーターは、特定の店舗で同時に検証できるトランザクションの数を制御します。 |

> [!NOTE]
> 明細書転記に関連する、さらに小売店舗および **コマース パラメーター** ページで定義されるすべての設定およびパラメーターが、改良された明細書転記機能に適用されます。

## <a name="invoice-parameters"></a>請求書パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有の請求書パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| 仕訳帳名 | 販売注文の支払用の顧客支払仕訳帳を作成するときに使用される支払仕訳帳の名前。 この設定は、販売時点管理 (POS)、コール センター、およびeコマース チャネルの注文に対して転記されるすべての注文支払に適用されます。 |
| アカウント名 | 支払アカウントの名前。 |
| 支払方法からの分析コードを優先する | このフラグを有効にすると、支払仕訳帳は、店舗からの分析ではなく、支払方法の分析を優先します。 |
| 税額計算動作 | このパラメータは、明細書の転記中に作成された販売注文が請求されるときの動作を指定します。<ul><li>**再計算** – 税金を再計算します。</li><li> **再計算しない** – POS で計算された税額を使用します。</li></ul> |
| 仕訳帳名 | 払戻のための顧客支払仕訳帳が作成される際に使用される仕訳名。 この設定は、POS、コール センター、およびeコマース チャネルの注文に対して転記されるすべての注文支払に適用されます。 |

## <a name="statement-parameters"></a>ステートメント パラメーター

次の表に、財務トランザクションおよび現物トランザクションの転記に固有のステートメント パラメーターを示します。

| パラメーター | Description |
|-----------|-------------|
| 計算時に在庫を引き当てる | このパラメーターを有効にすると、明細書の計算は、明細書が転記されるまで在庫を一時的に予約します。 このパラメータは、明細書計算のパフォーマンスを向上させるために既定で無効になっています。 更新された在庫情報は、**在庫の転記** バッチ ジョブを使用して計算されます。 [トリクル フィードベース](trickle-feed.md) ベースの小売店舗トランザクションの注文作成が有効になっている場合、**転記** 在庫バッチ ジョブは使用されなくなることに注意してください。 |
| 棚卸を無効化する必要がある | このフラグを設定した場合、コマース本社での転記時に棚卸が無効化されます。 |
| エラーの財務分析コードの再計算 | このパラメーターを有効すると、明細書の転記に失敗した場合、後続の明細書転記で財務分析コードを再評価できます。 |
| 返品店舗の財務分析コードを使用します | このパラメーターを有効にすると、元のトランザクションの財務分析コードではなく、店舗の財務分析コードを使用するリンクされた返品販売注文を作成できます。 |
| 返品のリンク解除 | このパラメータを有効にすると、明細書は未転記の販売の返品をブラインド返品として作成できます。 このパラメータは既定で無効になっているので、無効のままにすることをお勧めします。 |
| 丸め差額の転記を無効にする | このパラメータは、支払処理中のトランザクション支払と総額の丸め差額の転記を無効にします。 |
| 顧客預金の自動決済 | このパラメーターを有効にすると、小売明細書の転記中に転記された顧客預金は、顧客未処理トランザクションに対して決済されます。 |
| POS からの現金管理調整を有効にして使用する | このパラメーターを有効にすると、POS で現金管理の調整が行われ、その値が小売財務諸表の転記に渡され、明細行が作成されます。 |
| 元帳伝票の詳細レベル | このパラメーターは、POS から発生する選択されたトランザクションの元帳伝票に含まれる詳細レベルを定義します。 トランザクション タイプには、収入、経費、および割引が含まれます。 割引の場合、このパラメーターは、定期割引の勘定番号と通常割引の勘定番号番号が異なる場合にのみ考慮されます。 詳細が必要な場合を除き、**集計** がこれらの転記の推奨値です。 集計レベルの転記が定義されている場合、**TransactionDiscountTrans.RecID** は入力されません。 Commerce 10.0.27 バージョン リリースでは、このフラグの名前が変更され、移動されました。 以前は **詳細レベル** という名前で、**在庫更新** セクションにありました。 |