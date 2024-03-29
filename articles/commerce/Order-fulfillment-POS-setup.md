---
title: 店舗における注文のフルフィルメントの設定
description: この記事では、店舗注文のフルフィルメントの設定方法における概要を説明します。
author: BrianShook
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c60de59f1007256b67a56a5ede0b83857b73bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855033"
---
# <a name="set-up-order-fulfillment-for-stores"></a>店舗における注文のフルフィルメントの設定

[!include [banner](includes/banner.md)]

多くの小売業者は、注文する店舗を有効化することで、注文のフルフィルメントを最適化したいと考えています。 店舗レベルでの注文のフルフィルメントは、特定の店舗の過剰在庫のシナリオを軽減するために役立ちます。また、店舗が余分な能力を持っているか、店舗が顧客とのより近い輸送距離内に位置する場合に、物流の視点から必要とされる場合があります。 これに対処するために、販売時点管理で統一された注文のフィルフィルメントの操作が利用できます。

特定の店舗でのフィルフィルメントの注文は、ヘッダーまたは注文の明細行で指示された店舗の倉庫が割り当てられています。

販売時点管理での注文フルフィルメントの操作によって、注文を処理するための販売時点管理に、1 つの作業領域が提供されます。 これには、注文の受付、出荷済にマーキング、または店舗での受け取り開始のすべてが含まれます。

## <a name="set-up-the-order-fulfillment-operation"></a>注文のフルフィルメント操作を設定

注文のフルフィルメント、[操作 ID 928](pos-operations.md)、は販売時点管理の、店舗の注文フルフィルメント作業領域へのアクセスに利用できます。

手順に従って、[ボタン グリッドに工程を追加](pos-screen-layouts.md) から、販売時点管理での注文のフルフィルメントを呼び出す際に使用するパラメーターを指定します。 既定では、注文のフルフィルメント工程を指定した後、**すべての注文** が選択されます。 このパラメーターで構成される場合に、工程が現在の店舗にてフルフィルメントの全注文明細行を一覧表示します。 また、ユーザーが店舗から出荷する注文を見たい時だけボタンに割り当てられ使用可能とされるのは、**出荷する注文** です。 最後に、**集荷の注文** です。 販売時点管理で呼び出されると、店舗で集荷される注文のみをリストします。 別のパラメーターは、フルフィルメントの注文を表示するさまざまな方法をユーザーに付与し異なるボタンへ割り当てることができます。

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>販売時点管理で注文のフルフィルメントへのアクセスを有効にします。

注文のフルフィルメント操作は、そのまま使用できる独自のアクセス許可を持っていませんが、将来的に、ユーザーは **注文の取得を許可** のアクセス許可に、販売時点管理から操作の呼び出しを要求する可能性があります。

店舗レベルの構成設定では、販売時点管理の範囲内から注文明細行を手動で受け入れる必要があるかどうかを決定することができます。 構成オプションが設定されていない場合は、注文明細行は既定で承諾されます。 構成オプションが有効とされている場合、販売時点管理のユーザーは **注文の受け入れを許可** のアクセス許可を取得し、販売時点管理の範囲内で注文を受け入れるようにする必要があります。

### <a name="enable-manual-order-acceptance"></a>手動受注の有効

既定により、店舗に割り当てられる注文明細行は、**受入済** としてマークされます。 つまり、割り当てられた店舗から充当され、それ以上の割り当てを受けることはないと仮定されます。 場合によっては、小売業者が達成できる前に手動で受注希望の可能性があります。 たとえば、店舗が短期で配置され注文を達成することができない場合、店長は特定の日に適切に処理が可能だと思うほど多くの注文を受理します。 注文を受理するまで、さまざまな店舗にバック オフィスで再割り当てされる場合があります。 この方法により、注文受付は注文が店舗で認められ、達成されることを示す方法を提供します。

店舗集配の注文明細行は、**"保留中"** とマークされ、受理の対象にはなりません。

注文明細行の手動受け入れを有効にするには、**Retail および Commerce** \> **チャネル** \> **店舗** \> **すべての店舗** の順に移動します。 店舗を選択し、店舗の詳細を表示する店舗 ID をクリックします。 **編集** をクリックします。 **一般** クイック タブで、**注文のフルフィルメント** サブ ヘッダーを選び、**いいえ** から **はい** に **手動受理** を変更します。

### <a name="enable-reject-order-line-capability"></a>注文明細行の機能の拒否を有効

注文明細行は、販売時点管理からも拒否することができます。 注文明細行の拒否すると、その店舗では実行されず、注文明細行が別の店舗または倉庫に再割り当てされます。 注文明細行の否認アクセス許可は、作業者に関連付けられる POS アクセス許可グループの **否認注文の許可** のアクセス許可を通して付与されます。 明細行を否認する間、小売業者は作業者に拒否の理由を提供することができます。 これは、**情報コード活動** タイプの **注文のフルフィルメント** 情報コードを使用し、チャンネルに関連付けられている機能プロファイルの **注文明細行の否認** に情報コードを割り当てることで実現できます。

> [!NOTE]
> **情報コード活動** タイプの **注文のフルフィルメント** 情報コードのみ、**"注文明細行の否認** アクションに割り当てることができます。

### <a name="synchronize-changes-to-the-channel-database"></a>チャンネル データベースへの変更の同期

ボタン グリッドに工程が割り当てられた後、適切なアクセス許可が割り当てられ、そしてチャンネルがコンフィギュレーションされると、その変更はチャンネルのデータベースに同期させる必要があります。 そうするには、**Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール** の順に移動します。 スケジュール「1090 - レジスター」を選択し、ボタン グリッドの変更を同期した後、**今すぐ実行** をクリックします。 次に、「1060 - スタッフ」を選択することで、アクセス許可の変更を同期し、**今すぐ実行** をクリックします。 次に、「1070 - チャンネル コンフィギュレーション」を選択することで、チャンネルの変更を同期し、**今すぐ実行** をクリックします。 最後に、「1110 - グローバル コンフィギュレーション」を選択することで、新たに作成された否認理由の情報コードを同期し、**今すぐ実行** をクリックします。

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>販売時点管理での注文のフルフィルメントを使用

販売時管理を開き、注文のフルフィルメント操作を選択します。 構成方法によっては、すべての明細行、集荷の注文明細行または注文明細行の出荷が表示されます。

### <a name="order-fulfillment-view"></a>注文のフルフィルメントの表示

注文のフルフィルメントの表示は、店舗でフルフィルメントの注文明細行をリストし、次の列を含みます。

- 注文番号
- 製品番号
- 説明
- 注文済数量
- 配送指定日
- 顧客名
- フルフィルメントの状態

特定の注文明細行の追加情報は、注文明細行を選択して、ログインした販売時点管理ヘッダーに表示されるユーザー / シフト情報のすぐ下にあるポップ アップ メニューを開けることで、表示可能になります。 このメニューには、明細行の詳細用と注文詳細用の 2 つのタブがあります。 明細行の詳細タブには、次の情報が含まれています。

- 注文済数量
- 出荷 / 集配されある残りの数量
- ピッキング済数量
- 梱包済数量
- 請求済数量 (既に集配または出荷済)
- 荷渡方法
- 配送先住所

ポップ アップ メニューの詳細は、以下のような複数の注文レベルの詳細を提供するタブもあります。

- 顧客名
- 顧客 ID
- 注文番号
- 注文合計
- 注文残高

注文フルフィルメント表示の下部は、アクション ペインです。 注文の明細行に対して実行できる全てのアクションが含まれます。 明細行の状態に基づいてアクションが利用できない場合、、そのアクションは使用できません。

既定では、注文は **受入済** の状態になります。 注文の状態は、注文明細行の一覧に列として表示することができます。 チャンネル レベルで **手動受け入れ** がコンフィギュレーションされている場合、出荷済の全ての明細行では **"保留中"** と表示され、達成可能になる前に、受理される必要があります。 既定では、店舗集配の注文は **"保留中"** となり、受理する必要はありません。

### <a name="order-fulfillment-line-actions"></a>注文フルフィルメントの明細行アクション

- **編集** – 注文状態が保留中の場合、販売時点管理では編集が可能です。 既に部分的にピッキング、梱包、または請求済の注文は、注文のフルフィルメント表示からは編集できません。
- **受け入れ** – チャネル レベルで **手動受け入れ** がコンフィギュレーションされる場合、明細行は注文フルフィルメントのプロセスを通過する前に、受理される必要があります。
- **ピッキング** – ピッキング オプションは、いくつかのアクションをサポートします。 最初に、**ピッキング** が注文明細行のステータスを更新し、店舗の他のユーザーが同じ明細行をピッキングしないようにします。 次に、**ピッキング リストの印刷** で選択した明細行または明細行のピッキング リストを印刷し、その状態を **ピッキング** に更新します。 ピッキング リストの形式は、レシートの形式の一部として制御されます。 レシート形式の設定方法の詳細については、[レシート テンプレートと印刷](receipt-templates-printing.md) を参照してください。 最後に、**ピッキング済としてマーク** は明細行がピッキングされていることを示します。 **ピッキング済としてマーク** は、バック オフィスでの在庫トランザクションの対応を開始します。 同時にすべての荷渡方法や注文間での複数の注文明細行のアクションに対して、ピッキング アクションを実行できます。
- **否認** – 明細行または部分明細行を否認することができます。 これにより、バックオフィスから別の店舗または倉庫に再割り当てが行われます。 明細行は、まだピッキングまたは梱包がされていない場合にのみ否認することができます。 既にピッキングの梱包済みの明細行を否認するには、バック オフィスからその明細行のピッキングまたは梱包を解除する必要があります。
- **梱包** – 梱包オプションは、選択した明細行の梱包明細を印刷する **梱包明細の印刷** アクションと、梱包済みとして明細行をマークし、バック オフィスで出荷済みとしてマークする **梱包済みとしてマーク** アクションの 2 つのアクションをサポートします。 同じ注文に属し、同じ荷渡方法である唯一の注文明細行は、同時に梱包することができます。 梱包明細の形式は、レシートの形式の一部として制御します。 レシート形式の設定方法の詳細については、[レシート テンプレートと印刷](receipt-templates-printing.md) を参照してください。
- **出荷** – 出荷アクションでは、バック オフィスで **出荷済** として選択された明細行にマークします。 明細行が完全に出荷された後は、もはや注文のフルフィルメント表示に出ません。
- **集配** – 集配アクションでは、集配のトランザクション表示に明細行が追加されます。 現在集配されない注文の他の明細行がある場合、数量ゼロのトランザクション表示に追加されます。 明細行が完全に集配された後、もはや注文のフルフィルメント表示に出ません。

### <a name="order-fulfillment-filtering"></a>注文のフルフィルメント フィルター

販売時点管理の注文のフルフィルメントは、フィルター処理が含まれており、必要なものをユーザーが検索しやすくなるようになります。 フィルターは、**販売時点管理** 画面の下部にあるアクション ペイン上で変更できます。 既定では、工程の設定に基づいて、**配送タイプ** フィルターが適用されます。 工程が、パラメーター **すべての注文** で設定されている場合、注文のフルフィルメントにアクセスすると、そのフィルターは適用されます。 同じことが **店舗集配** および **ストアから出荷** パラメータに適用されます。 注文のフルフィルメントの表示に適用可能なその他のフィルターが含まれます:

- 顧客番号
- 顧客名
- 顧客の電子メール
- 注文番号
- 荷渡方法
- 受領番号
- チャネル参照 ID
- 元の店舗番号
- 行ステータス
- 作成日
- 出荷日
- 入荷日


[!INCLUDE[footer-include](../includes/footer-banner.md)]
