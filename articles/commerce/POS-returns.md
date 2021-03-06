---
title: POS での返品の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションで、現金払いトランザクションまたは顧客注文に対して返品を開始する方法について説明します。
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 496c4fe5230a599acf60fac39e51c43db372f92c
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129818"
---
# <a name="create-returns-in-pos"></a>POS での返品の作成

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリで、現金払いトランザクションまたは顧客注文に対して返品を開始する方法について説明します。

> [!NOTE]
> Commerce バージョン 10.0.20 リリース以降では、**POS での統合返品処理エクスペリエンス** という新しい機能が利用可能です。 この機能により、トランザクション タイプ (現金払いトランザクションまたは顧客注文) や注文が作成された元のチャネルに関係なく、POS でのより一貫した統合返品プロセスが提供されます。 すべての組織でこの新しい機能を有効にし、POS による返品処理の全体的な信頼性を向上することをお勧めします。
>
> 機能を有効にした後で無効にすることはできません。

## <a name="process-returns-by-using-the-return-transaction-operation"></a>返品トランザクション操作を使用した返品の処理

POS [画面レイアウト](pos-screen-layouts.md) に返品トランザクション操作を追加することをお勧めします。 Commerce バージョン 10.0.20 リリースより前のリリースでは、返品トランザクション操作は、現金払いトランザクションのみの返品処理を正しくサポートしています。 Commerce バージョン 10.0.20 リリース以降で **POS 用の統合返品処理エクスペリエンス** 機能をオンにすると、返品トランザクション操作は、顧客の注文 (既に請求済の "受け取り" や "自宅への配送" 注文など) から発生する返品処理もサポートします。

返品トランザクション操作から、ユーザーは、次の 4 つの検索基準のいずれかを入力して、返品の対象となる現金払いトランザクションまたは顧客注文を検索できます。 ユーザーは、デバイス キーボード、画面上のキーパッド、またはバーコード スキャナーを使用して、これらの基準を入力できます。

- 受領書 ID
- 注文番号
- チャネル参照 ID (注文確認 ID とも呼ばれる)
- 請求書 ID

検索基準に一致するトランザクションまたは注文が見つかった場合は、**返品可能な製品** ページが表示されます。 そこで、ユーザーは返品される品目を指定できます。 返品数量や理由コードを入力することもできます。

返品可能製品リストの各注文明細行について、POS は元の購買数量と、以前に処理された返品の数量に関する情報を表示します。 ユーザーが注文明細行に対して入力する返品数量は、**返品可能** フィールドの値以下である必要があります。

![返品可能な製品ページ](media/returnslist.png)

返品処理中に、ユーザーが物理的製品を持ち、その製品にバーコードがあれば、ユーザーは返品を登録するために、バーコードをスキャンできます。 バーコードをスキャンするごとに、返品数量が 1 品目増加します。 ただし、バーコード ラベルに数量が埋め込まれている場合は、その数量が **今すぐ返品** フィールドに入力されます。

ユーザーは、**返品可能な製品** ページで返品する品目を手動で選択し、右側の詳細ウィンドウを使用して **今すぐ返品** フィールドを更新することもできます。

トランザクションに最大使用可能な **今すぐ返品** の数量を指定している場合、ユーザーは POS アプリ バーの **すべて選択** 操作を選択して、すべての明細行に返品可能な最大数量を設定できます。

**今すぐ返品** 数量がある各明細行の場合、ユーザーは詳細パネルを使用して返品理由コードを選択する必要があります。 現金払いトランザクションの返品の場合、返品理由コードは、店舗の機能プロファイルの情報コードとして構成します。 顧客注文の返品の場合、返品理由コードは、Dynamics 365 Commerce Headquarters の **返品理由コード** ページで構成します。

返品する必要がある品目ごとに返品数量と理由コードを設定した後、ユーザーは POS アプリ バーの **返品** 操作を選択して処理を進めることができます。 POS トランザクション ページが表示され、前のページで選択した返品可能な品目がカートに追加されます。 品目の **今すぐ返品** 数量がトランザクションでマイナスの数量明細行として表示され、払戻の総額が計算されます。

ユーザーが返品トランザクションに明細行を追加できるのはユーザーは、交換注文を作成する場合です。 ユーザーは、追加されたプラス数量の選択した販売明細行に対して **返品** 操作を使用して、返品トランザクションにさらに特別な返品品目を追加することもできます。

> [!NOTE]
> POS での **返品** 操作では、元のトランザクションに対する検証は行わないので、製品を返品することができます。 そのため、許可されているユーザーのみがこの操作を実行できるようにするか、この操作を使用する場合は、マネージャーの上書きが必要になることをお勧めします。

精算時に払戻が必要な場合、組織は顧客への払戻に使用できる支払方法を制限する [払戻支払ポリシー](refund_policy_returns.md) を構成できます。 元の取引がクレジット カードを使用して支払われた場合は、支払プロセッサとシステム構成に応じて、ユーザーが [元のカードに対して払戻を発行](dev-itpro/linked-refunds.md) できる場合があります。 この場合、顧客が再びクレジット カードを機械に通すことなく、払戻を処理できます。 元の支払トークンを使用して、払戻が発行されます。

## <a name="other-return-options-in-pos"></a>POS でのその他の返品オプション

**POS での統合返品処理エクスペリエンス** 機能を有効にすると、ユーザーは POS で **仕訳帳の表示** 操作を使用して、現金払いトランザクションや顧客注文の返品を開始できます。 次に、仕訳帳でトランザクションを選択し、POS アプリ バーで **返品** 操作を選択できます。 この操作は、注文に返品可能な明細行がある場合にのみ使用できます。 **返品トランザクション** 操作と同じユーザー エクスペリエンスを開始します。

また、ユーザーは、POS で **注文の取り消し** 操作を使用して、顧客注文を検索して取り消すこともできます。 (この操作は、現金払いトランザクションには使用できません)。 この場合、顧客注文を選択した後に、POS アプリ バーの **返品** 操作を使用して顧客注文の返品を開始できます。 この操作は、注文に返品可能な明細行がある場合にのみ使用できます。 **返品トランザクション** または **仕訳帳の表示** 操作と同じユーザー エクスペリエンスを開始します。

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>返品注文が販売注文として Commerce Headquarters に転記される 

**POS での統合返品処理エクスペリエンス** 機能を有効にすると、POS で作成されたすべての返品は、マイナス明細行を持つ販売注文として Commerce Headquarters に書き込まれます。 Commerce バージョン 10.0.20 リリースより前のリリースでは、ユーザーは返品注文をマイナス明細行のある販売注文として転記するか、商品返品確認 (RMA) プロセスを通じて作成された返品注文にするか選択できます。 

**POS での統合返品処理エクスペリエンス** 機能では、RMA プロセスを使用して POS で返品を作成するオプションは非推奨になりました。 この機能を有効にすると、すべての返品がマイナス明細行を含む販売注文として作成されます。

## <a name="offline-return-processing-improvements"></a>オフライン返品処理の改善

多くの場合、POS で返品が処理されると、システムは、返品可能な現在の数量を確認するために Commerce Headquarters にリアルタイム サービス (RTS) 呼び出しを実行しようとします。 この検証により、顧客が複数の場所で同じ品目を返品しようとする不正なシナリオを防止できます。

ネットワークや接続の問題が原因で RTS 呼び出しを実行できない状況に対処するために、Commerce Headquarters からの返品数量データを店舗のチャネル データベースに定期的に同期するプロセスが導入されています。 このチャネル側の返品追跡により、POS に表示される **返品可能** 数量が、POS がオフラインの場合でも、適切に正確であることが保証されます。 また、POS がチャネル側の情報を引き続き検証して、不正な返品を防ぐこともできます。

オフラインの返品プロセスを適切な方法で使用するには、組織は Commerce Headquarters で **返品数量の更新** バッチ ジョブが頻繁に実行されるようにスケジュールする必要があります。 このジョブは、Commerce チャネルから Commerce Headquarters に新しいトランザクションを取り込む P ジョブと同じ頻度で実行することをお勧めします。

**返品数量の更新** ジョブでは、Commerce Headquarters で見つかったすべての販売注文について返品可能な数量を計算します。 次に、ジョブによって計算されたデータをチャネル データベースに送信して、店舗のチャネルを更新できるようにする必要があります。 この目的のために、**返品数量** (1200) の配送ジョブが使用されます。 返品可能数量に関するデータは Commerce Headquarters から同期されるため、返品が POS で処理され、RTS 呼び出しが実行できない場合、POS はチャネル側の返品情報を使用して、指定された販売明細行の **返品可能** 数量を検証できます。

RTS 呼び出しが実行できず、POS が返品検証にチャネル側のデータを使用している場合、ユーザーに "オフライン" 返品を作成していることを通知する警告メッセージが表示されます。 そのため、**返品数量の更新** ジョブが最後に処理され、チャネルに同期された時期によっては、POS に表示される **返品可能** 数量が最新ではなく、正確ではない可能性があることが認識されます。

例えば、顧客が最近、別のチャネルで注文明細行の返品を処理しましたが、そのデータは **返品数量の更新** ジョブを通じてチャネル データベースにまだ同期されていません。 その後、顧客は別の店舗に移動し、同じ品目を再び返品しようとします。 この場合、店舗がリアルタイムの返品データを取得するために RTS 呼び出しを Commerce Headquarters に行うことができない場合、POS は品目の再返品を許可します。 ただし、ユーザーは、返品の検証に使用されている情報が最新ではない可能性があることを警告されます。 ユーザーが受信するメッセージは、警告メッセージのみです。 ユーザーが返品の処理を続行することはできます。

チャネル側の情報が何らかの理由で最新ではなく、実際の **返品可能** 数量を超える数量についてオフラインの返品が処理されると、明細書の転記を実行して Commerce Headquarters でトランザクションを作成するときにエラーが生成される場合があります。

> [!NOTE]
> **POS での統合返品処理エクスペリエンス** 機能が有効になると、シリアル化された製品の返品検証をサポートする新しいオプション機能が使用可能になります。 詳細については、[販売時点管理 (POS) でシリアル番号管理された製品の返品](POS-serial-returns.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[販売時点管理 (POS) でシリアル番号管理された製品の返品](POS-serial-returns.md)

[以前に承認および確認済みのトランザクションのリンクされた払戻](dev-itpro/linked-refunds.md)

[チャネルの返品と払戻のポリシーの作成および更新](refund_policy_returns.md)

[POS ユーザー インターフェイスのビジュアル コンフィギュレーション](pos-screen-layouts.md)
