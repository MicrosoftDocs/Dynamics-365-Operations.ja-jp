---
title: "製造オーダーから出荷ドックへのクロスドッキング"
description: "このトピックでは、生産ラインから出荷輸送ドックまでの完了レポートがされているクロスドッキング材料のプロセスを管理する方法について説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b424be5396df9434cd799ca7e7e9342a7c476e29
ms.openlocfilehash: 231808260eeab73120bab43558ab5745f9fdbe46
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>製造オーダーから出荷ドックへのクロスドッキング

このトピックでは、生産ラインから出荷輸送ドックまでの完了レポートがされているクロスドッキング材料のプロセスを管理する方法について説明します。

<a name="introduction"></a>はじめに
------------

生産から出荷場所へのクロスドッキングは、大量生産しており、生産ラインから完了レポートされ次第完成品を出荷することを理想とするメーカーに適しています。 製造サイトで在庫を増やすのではなく、物理的に顧客需要の近くに位置した物流センターに製品を出荷することを目的としています。

製品に対する当座の需要がない場合、製造サイトの倉庫場所に保管する必要があります。 このプロセスは *便乗クロスドッキング* とも呼ばれますが、それは製品出荷の需要があった場合には、内部保管用にその製品をしまい込むのではなく、その機会に便乗するべきだということを示しています。

次の例では、生産ライン (2) の最後に開始するフローの 3 つのバリエーションを示します。

製品が生産出荷場所 (3) に完了レポートされると、フォーク リフト ドライバーは、この場所 (3) でパレットをピックアップします。

-   製品を生産 (1) から物流センター (7) へ移す計画活動 (6) がある場合、トラック ドライバーはシステムによりパレットをベイ ドア場所 (4) のそばに置くよう指示されます。
-   既にトレーラーがそのベイ ドアに割り当てられている場合、トラック ドライバーはそのトレーラに直接製品を積み込むよう指示されます。
-   製品を移す計画活動がない場合、フォーク リフト ドライバは製品を内部倉庫 (5) 内の場所に保管するよう指示されます。

[![](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>クロスドッキングのコンフィギュレーション
**作業ポリシー** でクロスドッキング プロセスをコンフィギュレーションします。 作業ポリシーには、ワーク オーダー タイプ、場所、および製品が含まれます。 次の例では、クロスドッキングは製品 X と場所 Y 用にコンフィギュレーションされています。

#### <a name="work-order-types"></a>ワーク オーダー タイプ

-   ワーク オーダー タイプ: 完成品のプット アウェイ
-   作業作成方法: クロスドッキング
-   クロスドッキング ポリシー名: 移動オーダー

#### <a name="inventory-locations"></a>在庫場所

-   倉庫: 51
-   場所: Y

#### <a name="products"></a>製品

-   品目番号: X

現在、クロスドッキングは 2 つのワーク オーダー タイプでのみコンフィギュレーションすることができます。

-   完成品のプット アウェイ
-   連産物と副産物のプット アウェイ

**クロスドッキング ポリシー** では、どのドキュメント タイプがクロスドッキングに適用可能かを定義します。 現在、サポートされている唯一のドキュメント タイプは **移動オーダー** です。 次の例では、クロスドッキング ポリシーのコンフィギュレーションを示します。

### <a name="cross-docking-policy-name-transfer-order"></a>クロスドッキング ポリシー名: 移動オーダー

-   順序番号: 10
-   ワーク オーダー タイプ: 移動の出庫
-   クロスドッキング需要には場所が必要です: いいえ
-   クロスドッキング戦略: 日時

### <a name="sequence-number"></a>一連番号

**順序番号** はドキュメント タイプの優先順位を示します。 現在、**移動の出庫** がサポートされている唯一のタイプです。 したがって、複数のワーク オーダー タイプがサポートされている場合にのみ、順序番号が意味を持つことになります。

### <a name="cross-docking-policy"></a>クロスドッキング ポリシー

クロスドッキング ポリシーでは、移動オーダーの需要の優先順位付けのポリシーも設定します。 たとえば、同じ製品に対して複数の移動オーダーがある場合、積荷に設定され移動オーダーに関連付けられた予定の日時がオーダー間の優先順位を決定します。 予定の日付と時刻は直接積荷に設定するか、積荷に関連付けられている **予定のスケジュール** で設定できます。 優先順位は、クロスドッキング戦略によって決定されます。 現在、**日時** という 1 つの戦略しかありません。

### <a name="cross-docking-demand-requires-location"></a>クロスドッキング需要には場所が必要です

クロスドッキング ポリシーでは、移動オーダーがクロスドッキング用に適格となるため割り当てられた場所を持つよう、条件を設定することができます。 この条件は [**クロスドッキング需要には場所が必要です**] フィールドで設定されます。 積荷に関連付けられている予定のスケジュール上の場所は、クロスドッキングされている商品の最終場所として使用されます。 クロスドッキングされている商品の最終場所は **プット** ワーク オーダー タイプの **移動の出庫** の場所ディレクティブによって決定されます。 トレーラーがベイ ドアに割り当てられた場合にのみ完成品をクロスドッキングするというシナリオでは、[**クロスドッキング需要には場所が必要です**] フィールドを設定すると役立つかもしれません。 このシナリオでは、商品は直接生産ラインからトレーラーに移されます。 ベイ ドアにトレーラーが割り当てられると、ユーザーは場所を予定のスケジュールに割り当て、結果その場所をクロスドッキングに適用可能にします。 次のセクションでは 2 つの例を説明します。

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>シナリオ 1 – 製造から移動オーダーへのクロスドッキング

製品は生産ラインで完了レポートされた後、トラックに積み込むベイ ドア場所に移され、物流センターへ移されます。 会社の USMF を使用します。

1.  クロスドッキング用に新しい順序番号を有効にします。 [**番号順序**] ページに移動し、[**生成**] ボタンを選択します。 ウィザードでプロセスを説明します。
2.  クロスドッキング ポリシーを作成します。 [**クロスドッキング ポリシー**] ページに移動し、「**移動オーダーへのクロスドッキング**」という新しいポリシーを作成します。 なお、選択できる唯一のワーク オーダー タイプは **移動の出庫** で、使用可能な唯一のクロスドッキング戦略は **日時** です。
3.  作業ポリシーを作成します。 [**作業ポリシー**] ページに移動し、「**クロスドッキング L0101**」という名前の新しい作業ポリシーを作成します。
4.  自動的に移動オーダーに作成されるように、積荷を設定します。 倉庫パラメーターでは、移動オーダーの作成時に自動的に作成されるよう積荷を設定します。 積荷は移動オーダーをクロスドッキングの対象とするための前提条件です。
5.  品目と積荷のマッピングを設定します。 [**品目と積荷のマッピング**] ページに移動し、**CarAudio** 品目グループに標準の積荷テンプレートを設定します。 このマッピングは、移動オーダーが作成される際に自動的に積荷テンプレートを積荷に挿入します。
6.  移動オーダーを作成します。 品目番号 L0101 の移動オーダーを作成します。 数量 = 20。
7.  積荷計画ワークベンチから移動オーダーをリリースします。 [**出荷**] タブで積荷計画ワークベンチのメニュー項目を選択して、積荷明細行の [**リリース**] メニューで [**倉庫にリリース**] を選択します。 移動オーダーに **移動の出庫** タイプのオープン ウェーブ明細行ができました。
8.  製造オーダーを作成します。 [**製造オーダー**] リスト ページに移動し、製品 L0101 の製造オーダーを作成します。 数量 = 20。 製造オーダーを見積もりして開始します。 なお、[**ピッキング リスト転記**] フィールドは [**いいえ**] に設定されたままです。
9.  モバイル デバイスから完了レポートをします。 モバイル デバイス ポータルに移動し、メニュー項目 [**完了レポートとプット アウェイ**] を選択します。 次はハンドヘルド デバイスから L0101 の完了レポートをします。 なお、プット場所は **ベイ ドア** です。 この場所は **プット** ワーク オーダー タイプの **移動の出庫** 場所のディレクティブから検出されます。 なお、タイプ **移動の出庫** の作業が作成され完了していることにも注意してください。 移動オーダー作業の詳細に移動して作業を確認します。
10. 次は製造オーダーでさらに 20 個を開始し、ハンドヘルド デバイスを使用して 20 個の完了レポートをしてみます。 今回は、場所 **LP 001** がプット場所として提示されます。 この場所は **完成品のプット アウェイ** の場所のディレクティブから検出されます。 クロスドッキングの営業案件が存在しないため、この場所のディレクティブが使用されています。 LP-001 の移動オーダーは最初のクロスドッキング活動によって完全に処理されました。

タイプ **完成品のプット アウェイ** の作業が作成され処理されました。

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>シナリオ 2 - 予定のスケジュールを用いた生産から移動オーダーへのクロスドッキング

製品は、生産ラインで完了レポートされた後、ベイ ドア場所の予定のスケジュールによって識別されるベイ ドア場所に移されます。 会社の USMF を使用します。

1.  クロスドッキング ポリシーを変更します。 [**クロスドッキング需要には場所が必要です**] チェック ボックスを選択して、シナリオ 1 で作成したクロスドッキングのポリシーを変更します。
2.  新しい移動オーダーを作成します。
3.  **積荷計画ワークベンチ** を開きます。
4.  積荷計画ワークベンチから [**積荷**] セクションに移動し、[**輸送**] メニューの [**予定のスケジュール**] を選択して新しい予定のスケジュールを作成します。 なお、予定のスケジュールは [**注文番号**] フィールドの移動オーダーを参照しています。 [**場所での計画された開始日時**] フィールドで、予定の日時を設定できます。 この日時は、クロスドッキング需要がクロスドッキング プロセス中に優先されているときに使用されます。 このフィールドで設定した日時は、対応する積荷の [**出荷予定日時**] フィールドを更新します。 [**出荷詳細**] クイック タブ上の場所が、移動オーダーの出荷場所を決定します。
5.  **積荷計画ワークベンチ** 上で倉庫へリリースします。
6.  品目番号 **L0101** の製造オーダーを作成し、数量 20 で状態を **開始済** に設定します。
7.  モバイル デバイスから完了レポートをします。
8.  モバイル デバイス ポータルに移動し、[**完了レポートとプット アウェイ**] メニュー項目を選択します。
9.  ハンドヘルド デバイスから品目番号 **L0101** の完了レポートをします。 なお、今回のプット場所は **ベイ ドア 2** です。 この場所は、**移動入庫** 場所のディレクティブではなく、予定のスケジュールから検出されます。

### <a name="additional-information"></a>追加情報

-   クロスドッキング シナリオは、バッチおよびシリアル番号分析コードが引当階層の場所の上と下の両方で定義されている、バッチおよびシリアル制御された品目でサポートされています。


