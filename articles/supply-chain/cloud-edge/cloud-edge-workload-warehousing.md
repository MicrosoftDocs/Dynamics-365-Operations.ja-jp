---
title: クラウドおよびエッジのスケール ユニットの倉庫管理ワークロード
description: このトピックでは、スケール ユニットを有効化して、倉庫管理ワークロードから選択したプロセスを実行できるようにする機能について説明します。
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516822"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>クラウドおよびエッジのスケール ユニットの倉庫管理ワークロード

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> ワークロードのスケール ユニットが使用されている場合は、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。 このトピックでは、サポート対象として明示的に説明したプロセスのみを使用してください。

## <a name="warehouse-execution-on-scale-units"></a>スケール ユニットでの倉庫の実行

この機能により、スケール ユニットで、倉庫管理機能から選択したプロセスを実行できるようになります。 クラウドのスケール ユニットでは、選択した Microsoft Azure リージョンで専用の処理能力を使用して、クラウド内の負荷を実行します。 エッジのスケール ユニットでは、スケール ユニットが一時的にクラウドから切断されている場合でも、いくつかのワークロードを個別に実行できます。

このトピックでは、スケール単位として定義されている倉庫での倉庫管理の実行は、*倉庫実行システム* (*WES*) と呼ばれます。

## <a name="prerequisites"></a>必要条件

倉庫管理ワークロードと共に配置された Dynamics 365 Supply Chain Management ハブとスケール ユニットが必要です。 アーキテクチャと配置プロセスの詳細については、[製造と倉庫の管理ワークロードのためのクラウドとエッジのスケール ユニット](cloud-edge-landing-page.md) を参照してください。

## <a name="how-the-wes-workload-works-on-scale-units"></a>スケール ユニット上で WES ワークロードが動作する方法

倉庫管理ワークロードのプロセスについては、ハブとスケール ユニットの間でデータが同期されます。

スケール ユニットは、所有するデータのみを保持できます。 スケールユニットのデータ所有権の概念は、マルチマスタの競合の防止に役立ちます。 したがって、ハブによって所有されているプロセスと、そのスケール ユニットによって所有されているプロセスを理解することが重要です。

スケール ユニットは、次のデータを所有します。

- **ウェーブ処理データ** - 選択されたウェーブ プロセス メソッドは、このスケール ユニットのウェーブ処理の一部として処理されます。
- **作業処理データ** - 次の作業指示書処理のタイプがサポートされています。

    - 在庫移動 (手動移動とテンプレート作業による移動)
    - 発注書 (倉庫オーダーを介したプットアウェイ作業)
    - 販売注文 (簡単なピッキングと積荷作業)

- **倉庫オーダー入庫データ** - このデータは、倉庫に手動でリリースされた発注書に対してのみ使用されます。
- **ライセンス プレート データ** - ライセンス プレートはハブとスケール ユニットで作成できます。 専用の競合処理が指定されています。 このデータは倉庫固有ではないことに注意してください。

## <a name="outbound-process-flow"></a>出荷プロセス フロー

ハブは、次のデータを所有しています。

- 販売注文や移動オーダーなどのすべての元伝票
- オーダーの割り当てと発送積荷の処理
- 倉庫へのリリース、出荷の作成、ウェーブの作成プロセス

スケール ユニットは、ウェーブのリリース後の実際のウェーブ処理 (作業の割り当て、補充作業、需要作業の作成など) を所有します。 したがって、倉庫の作業者は、スケール ユニットに接続された倉庫アプリを使用して出荷作業を処理できます。

![ウェーブ処理フロー](./media/wes_wave_processing_flow.png "ウェーブ処理フロー")

## <a name="inbound-process-flow"></a>入庫プロセス フロー

ハブは、次のデータを所有しています。

- 発注書や販売返品注文などのすべての元伝票
- 入庫積荷処理

> [!NOTE]
> 入庫発注書フローは、概念的には出庫フローとは異なり、処理を実行するスケール ユニットは、このオーダーが倉庫にリリースされたかどうかによって異なります。

*倉庫へリリース* プロセスを使用している場合は、倉庫オーダーが作成され、関連する入荷フローの所有権がスケール ユニットに割り当てられます。 ハブでは、入荷受信を登録することはできません。

作業者は、スケール ユニットに接続された倉庫アプリを使用して入荷プロセスを実行できます。 その後、データはスケール ユニットで記録され、入庫倉庫オーダーとして報告されます。 それ以降のプットアウェイの作成や処理も、スケール ユニットで処理されます。

*倉庫へのリリース* プロセスを使用していないため、*倉庫オーダー* を使用していない場合は、倉庫 の入荷と作業の処理をスケール ユニットから独立して処理できます。

![入庫プロセス フロー](./media/wes_Inbound_flow.png "入庫プロセス フロー")

## <a name="supported-processes-and-roles"></a>サポートされているプロセスとロール

すべての倉庫管理プロセスが、スケール ユニットの WES ワークロードでサポートされているわけではありません。 したがって、各ユーザーが使用できる機能に合った役割を割り当てることをお勧めします。

このプロセスを容易にするために、**システム管理 \> セキュリティ \> セキュリティの構成** でのデモデータには、*ワークロード上の倉庫管理* という名前のロールが含まれています。 このロールの目的は、倉庫マネージャがスケール ユニットの WES にアクセスできるようにすることです。 このロールは、スケール ユニットでホストされているワークロードのコンテキストに関連するページへのアクセスを許可します。

スケール ユニットのユーザー ロールは、ハブからスケール ユニットへの初期データ同期の一部として割り当てられます。

ユーザーに割り当てられているロールを変更するには、スケール ユニットで **システム管理 \> セキュリティ \> ユーザーをロールに割り当て** に移動します。 スケール ユニットでのみ倉庫マネージャとして行動するユーザーには、*ワークロードの倉庫マネージャー* ロールのみを割り当てる必要があり ます。 このアプローチを使用すると、これらのユーザーは、サポートされている機能にのみアクセスできるようになります。 これらのユーザーに割り当てられているその他のロールをすべて削除します。

ハブとスケール ユニットの両方で倉庫マネージャとして行動するユーザーには、既存の *ワークロードの作業者* ロールのみを割り当てる必要があり ます。 このロールでは、倉庫作業者がユーザー インターフェイス (UI) に表示される機能 (移動オーダー処理など) にアクセスすることが許可されますが、現在スケール ユニットではサポートされていないことに注意してください。

## <a name="supported-wes-processes"></a>サポートされている WES プロセス

次の倉庫実行プロセスは、スケール ユニットで WES ワークロードに対して有効にすることができます。

- 販売注文と需要補充に対して選択されたウェーブ メソッド
- 倉庫アプリを使用した販売注文と需要補充からの作業指示書の実行
- 倉庫アプリを使用した手持在庫の照会
- 倉庫アプリを使用した在庫移動の作成と実行
- 倉庫アプリを使用した発注書の登録と、プットアウェイの処理

次の作業指示書タイプは、スケール ユニット展開でのワークロードの WES で現在サポートされています。

- 販売注文
- 補充
- 在庫移動
- 倉庫オーダーにリンクされている発注書

現在、スケール ユニットでは、ソース ドキュメントの他の処理はサポートされていません。 たとえば、スケール ユニットの WES ワークロードの場合、次のアクションを実行することはできません。

- 移動オーダーをリリースします。
- 出庫倉庫のピッキングと出荷操作を処理します。

> [!IMPORTANT]
> スケール ユニットでワークロードを使用している場合、ハブで特定の倉庫に対してサポートされていないプロセスを実行することはできません。

次の倉庫管理機能は、現在スケール ユニットではサポートされていません。

- 有効な追跡用分析コードがある品目 (バッチ番号やシリアル番号の分析コードなど) の入庫および出庫処理
- 在庫ステータス変更の処理
- ブロッキングステータス値を持つ在庫の処理
- 品質管理との統合
- 製造との統合
- CW 品目の処理
- 超過配送と過少配送の処理
- 負の手持在庫の処理

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>出庫 (販売注文と需要補充に対してのみサポートされている)

次の表に、倉庫管理ワークロードがクラウドとエッジのスケール ユニットで使用されている場合に、サポートされる送信機能と、サポートされる場所を示します。

> [!WARNING]
> 販売注文の処理だけがサポートされているため、出庫倉庫管理処理を移動オーダーに対して使用することはできません。
>
> 一部の倉庫機能は、スケール ユニット単位で倉庫管理ワークロードを実行している倉庫では使用できません。

| 処理                                                      | ハブ | スケール ユニットの WES ワークロード |
|--------------------------------------------------------------|-----|------------------------------|
| 元伝票の処理                                   | あり | なし |
| 積荷および輸送管理の処理                | あり | なし |
| 倉庫にリリース                                         | あり | なし |
| 出荷の連結                                       | なし  | なし |
| クロスドッキング (ピッキング作業)                                 | なし  | なし |
| 出荷ウェーブ処理                                     | いいえ、ウェーブ状態の完了はハブで処理されます |<p>はい、しかし次の機能はサポートされていません。</p><ul><li>並列作業の作成</li><li>建物と並べ替えの読み込み</li><li>コンテナー化</li><li>サイクル ラベル印刷</li></li></ul><p><b>注記:</b> ハブにアクセスするには、ウェーブ処理の一部としてウェーブステータスを確定する必要があります。</p> |
| 倉庫作業の処理 (ライセンス プレートを含む)     | なし  | <p>はい、ただし、次の機能に対してのみ使用できます。</p><ul><li>販売ピッキング (有効な追跡分析コードを使用しない)</li><li>販売の読込み (有効な追跡分析コードを使用しない)</li></ul> |
| クラスター ピッキング                                              | なし  | なし |
| パッキング処理                                           | なし  | なし |
| 出庫の並べ替え処理                                  | なし  | なし |
| 積荷に関連するドキュメントの印刷                           | あり | なし |
| 船荷証券と ASN 生成                            | あり | なし |
| 出荷確認と梱包明細処理                | あり | なし |
| ショート ピッキング (販売注文)                                 | なし  | なし |
| 作業のキャンセル                                            | なし  | なし |
| 作業場所の変更 (販売注文)                      | なし  | なし |
| 作業の完了 (販売注文)                                 | なし  | なし |
| ブロックとブロック解除の作業                                       | なし  | なし |
| ユーザーの変更                                                  | なし  | なし |
| 作業レポートの印刷                                            | なし  | なし |
| ウェーブ ラベル                                                   | なし  | なし |
| 作業を取消                                                 | なし  | なし |

### <a name="inbound"></a>着信

次のテーブルに、倉庫管理ワークロードがクラウドとエッジのスケール ユニットで使用されている場合に、サポートされる入庫機能と、サポートされる場所を示します。

| 処理                                                          | ハブ | スケール ユニットの WES ワークロード |
|------------------------------------------------------------------|-----|------------------------------|
| ソース&nbsp;ドキュメント&nbsp;処理                                       | あり | なし |
| 積荷および輸送管理の処理                    | あり | なし |
| 出荷の確認                                            | あり | なし |
| 倉庫への発注書リリース (倉庫オーダー処理) | あり | なし |
| 発注書品目受取とプット アウェイ                        | <p>はい、&nbsp;&nbsp;&nbsp;倉庫オーダーがない場合</p><p>いいえ、倉庫オーダーがある場合</p> | <p>はい、倉庫オーダーがある場合、および発注書が <i>負荷</i> の一部に含まれていない場合。 ただし、2 つのモバイル デバイスのメニューアイテムを使う必要があります。ひとつは入荷用 (<i>発注書品目の受信</i>)、もうひとつは <b>既存の作業を使用</b> オプションを有効にした状態でそのプットアウェイを処理する必要があります。</p><p>いいえ、倉庫オーダーがない場合。</p> |
| 発注書明細行受取とプット アウェイ                        | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | なし |
| 返品注文入庫およびプット アウェイ                               | あり | なし |
| 混合ライセンス プレートの受取とプット アウェイ                        | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | なし |
| 積荷品目入庫                                              | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | なし |
| ライセンス プレートの受け取りおよびプット アウェイ                              | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | なし |
| 移動オーダー品目入庫とプット アウェイ                        | あり | なし |
| 注文明細行の受取とプット アウェイの移動                        | あり | なし |
| 作業のキャンセル                                                | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | <p>はい、しかし (<b>倉庫管理パラメータ</b> ページ上の) <b>キャンセル作業時に受信を登録解除する</b> オプションはサポートされていません。</p> |
| 発注書製品受領処理                        | あり | なし |
| 入荷の一部としてのクロス ドッキング作業の作成                 | <p>はい、倉庫オーダーがある場合</p><p>いいえ、倉庫オーダーがある場合</p> | なし |

### <a name="warehouse-operations-and-exception-handing"></a>倉庫操作と例外処理

次のテーブルには、倉庫管理ワークロードがクラウドとエッジのスケール ユニットで使用されている場合に、サポートされる倉庫業務と例外処理の機能と、サポートされる場所を示します。

| 処理                                            | ハブ | スケール ユニットの WES ワークロード |
|----------------------------------------------------|-----|------------------------------|
| ライセンス プレートの照会                              | あり | あり                          |
| 品目の照会                                       | あり | あり                          |
| 場所の照会                                   | あり | あり                          |
| 倉庫の変更                                   | あり | あり                          |
| 振替                                           | なし  | あり                          |
| テンプレートによる移動                               | なし  | あり                          |
| 調整 (入/出)                                | あり | なし                           |
| 循環棚卸と不一致計算の処理 | あり | なし                           |
| ラベルの再印刷 (ライセンス プレート印刷)             | あり | なし                           |
| ライセンス プレートの構築                                | あり | なし                           |
| ライセンス プレートの分割                                | あり | なし                           |
| 配送担当者のチェックイン                                    | あり | なし                           |
| 配送担当者のチェックアウト                                   | あり | なし                           |
| バッチ廃棄コードを変更する                      | あり | なし                           |
| オープン作業一覧の表示                             | あり | なし                           |
| ライセンス プレートの連結                         | なし  | なし                           |
| グループからコンテナーを削除                        | なし  | なし                           |
| 作業のキャンセル                                        | なし  | なし                           |
| 最小/最大の補充処理                   | なし  | なし                           |
| 補充処理のスロッティング                  | なし  | なし                           |

### <a name="production"></a>実稼働

生産シナリオでの倉庫管理の統合は、次のテーブルに示すように現在はサポートされていません。

| 処理 | ハブ | スケール ユニットの WES ワークロード |
|---------|-----|------------------------------|
| <p>生産に関連するすべての倉庫管理プロセス。 次にいくつか例を挙げます。</p><li>倉庫にリリース</li><li>生産ウェーブプロセス</li><li>原材料のピッキング</li><li>完成品のプット アウェイ</li><li>連産物と副産物のプット アウェイ</li><li>かんばんのプット アウェイ</li><li>かんばんのピッキング</li><li>製造オーダーの開始</li><li>生産仕損</li><li>最後の生産パレット</li><li>材料消費の登録</li><li>空のかんばん</li></ul> | なし | なし |

## <a name="maintaining-scale-units-for-wes"></a>WES のスケール ユニットの管理

ハブとスケール ユニットの両方で実行される複数のバッチジョブが実行されます。

ハブのデプロイでは、バッチジョブを手動で管理できます。 次の 3 つのジョブは、 **倉庫管理 \> 定期タスク \> バックオフィス ワークロード管理** で管理できます。

- 作業状態更新イベントの処理
- サイクル実行制御転送イベントの処理
- 元の注文入庫登録

スケール ユニットのワークロードでは、次の 2 つのジョブは、 **倉庫管理 \> 定期タスク \> ワークロード管理** で管理できます。

- ウェーブ テーブル レコードを処理する
- サイクル実行制御転送イベントの処理