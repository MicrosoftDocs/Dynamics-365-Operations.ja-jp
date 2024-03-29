---
title: 作業の分割
description: この記事では、作業分割機能に関する情報を提供します。 この機能を使用すると、複数の作業オーダーをいくつかの小さな作業オーダーに分割し、その後で複数の倉庫作業者に割り当てることができます。 これにより、複数の倉庫作業者が同じ作業を同時に選択できるようになります。
author: Mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 83333f4d8c755bc0ca4b2d141a5591ef43501b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857028"
---
# <a name="work-split"></a>作業の分割

[!include [banner](../includes/banner.md)]

作業分割機能を使用すると、複数の作業 ID (複数の行を含む作業順序) をいくつかの小さな作業 ID に分割し、それを複数の倉庫作業者に割り当てることができます。 このように、複数の倉庫作業者が同じ作業作成番号を同時にピッキングすることができます。

> [!IMPORTANT]
> ステータスが *未処理* または *処理中* の作業指示書のみを分割できます。

## <a name="turn-on-the-work-split-functionality"></a>作業分割機能を有効にする

作業分割機能を使用するには、システムで機能および前提となる機能を有効にする必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。

最初に、前提条件となる *組織全体の作業ブロック* 機能が有効になっていない場合は、オンにします。 Supply Chain Management のバージョン 10.0.21 の時点では、この機能は必須です。この機能は既定で有効になっていて、再度オフにできない状態です。 ただし、この機能は引き続き次のように[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)にリストされています。

- **モジュール:** *倉庫管理*
- **機能名:** *組織全体の作業のブロック*

> [!NOTE]
> この機能が有効になっている場合は、すべての法人で機能をオンにすると、データ アップグレードが自動的に適用されます。

次に、次の手順に従って、*作業分割* 機能を有効にします。

- **モジュール:** *倉庫管理*
- **機能名:** *作業分割*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>[作業の詳細] ページと [すべての作業] ページの拡張

*作業分割* 機能によって、**作業の詳細** ページと **すべての作業** ページのアクション ウィンドウの **作業** タブに、次の 2 つのボタンが追加されます。

- **作業分割**: 現在の作業 ID を別々の作業員が処理できる複数の小さい作業 ID に分割します。
- **作業分割セッションのキャンセル**: 作業分割セッションをキャンセルし、作業を処理できるようにします。

![作業分割と作業分割セッションのキャンセル ボタン。](media/Work_split_buttons.png "作業分割と作業分割セッションのキャンセル ボタン")

> [!IMPORTANT]
> **作業分割** ボタンは、次のいずれかの条件が満たされている場合には使用できません。
>
> - 作業ステータスが *未処理* または *処理中* 以外になっている。
> - 作業 ID にコンテナー ID が関連付けられている。 (コンテナーは、物理的なアクションを必要とするため体系的に分割することはできません)。
> - 作業は、クラスターに関連付けられています。
> - 作業指示書タイプが次のいずれかのタイプ以外になっている。
>
>    - 販売注文
>    - 原材料のピッキング
>    - 移動の出庫
>
> - 作業が現在別のユーザーによって分割されている。 別のユーザーによって既に分割されている作業の分割ページを開こうとすると、エラー メッセージ "ID \#\#\#\# の作業は現在分割中です。 数分後に再試行してください。 このメッセージが引き続き表示される場合は、スーパーバイザーに連絡してください" が表示されます。

新しい作業ブロックの理由 *分割作業* は、作業 ID が分割処理中であることを示します。 ユーザーが作業を実行しようとした場合、**分割作業** ページと倉庫管理モバイル アプリの両方に表示されます。 ブロックの理由を使用する場合、作業 ID の **ブロックされたウェーブ** フィールドの名前が **ブロック** に変わります。

## <a name="initiate-a-work-split"></a>作業分割の開始

この機能により、作業 ID から作業明細行を分割するための新しい **分割作業** ページが追加されます。 ページが最初に開かれたときに、作業ステータスが *未処理* で分割可能な明細行が表示されます。 アクション ウィンドウで、**作業分割** を選択して、選択した作業を処理します。

作業を分割するには、次の手順を実行します。

1. 次の作業ページのいずれかを開きます。

    - **作業の詳細** (**倉庫管理 \> 作業 \> 作業の詳細**)
    - **すべての作業** (**倉庫管理 \> 作業 \> すべての作業**)

1. グリッドで、分割する作業 ID を選択します。 **作業指示書タイプ** フィールドには、次のいずれかの値を設定する必要があります。

    - 販売注文
    - 原材料のピッキング
    - 移動の出庫

1. アクション ウィンドウの **作業** タブの、**作業** グループで、**作業分割** を選択します。

    **作業分割** ページが表示され、分割できる作業明細行が表示されます。 既定では、使用可能な作業行のみが表示されます。 作業 ID のすべての明細行 (たとえば作業タイプが *プット* である明細行) を表示するには、グリッドの上部にある **すべての行の表示** チェック ボックスをオンにします。

    "このページを分割して終了するまで、ユーザーはこの作業を処理できません" というメッセージが表示されます。

    現在の作業の **作業ブロック理由** フィールドが *作業分割* に設定され、その作業がブロックされます。

    ![ブロックの理由。](media/Blocking_reason.png "ブロックの理由")

1. 現在の作業 ID から削除する明細行を選択し、新しい作業 ID に追加します。 以下のイベントが発生します :

    - 作業を分割すると、元の作業 ID の選択した明細行がキャンセルされ、新しい作業 ID にコピーされます。
    - 既存の作業テンプレート構造と、プット (および将来のピック/プット) の場所も保持されます。 次の作業 ID フィールドの値は、元の作業から新しい作業にコピーされます。

        - 貨物 ID
        - 出荷 ID
        - 作業指示書タイプ
        - 注文番号
        - サイト
        - 倉庫
        - 作業の優先順位
        - 作業プール ID
        - ウェーブ ID
        - 作業作成数

    - 次のフィールドは、新しい作業 ID にコピーされません。

        - **作業 ID**: 適切な番号順序から新しい作業 ID が生成されます。
        - **作業ステータス**: このフィールドは、*未処理* に設定されます。
        - **ロック元**: このフィールドは、最初は空白に設定されます。
        - **ターゲット ライセンス プレート ID**: このフィールドは空白のままになります。
        - **作成日時**: このフィールドは、現在の日付と時刻に設定されます。
        - **ブロックされたウェーブ/固定**: このフィールドは、元の作業 ID と新しい作業 ID に対して再計算されます。

1. アクション ウィンドウで、**作業分割** を選択します。

作業が分割されている間、"処理中です - 作業分割" というメッセージが表示されます。 このメッセージが表示されている間は、メッセージ ボックスで **キャンセル** を選択することにより、操作を取り消すことができます。

**すべての明細行を表示** チェック ボックスをオフにすると、分割およびキャンセルされた行はグリッドに表示されなくなります。 このチェック ボックスがオンになっている場合は、その明細行の **作業ステータス** フィールドの値が *キャンセル済* に変更されていることを確認する必要があります。

次の通知は、新しい作業 ID が作成されたことを示します: "元の作業 \#\#\#\# からの分割によって作業 \#\#\#\# が作成されました"。

元の作業 ID (*プット* 明細行など) の他の作業明細行は、キャンセルされた作業明細行を反映するために、必要に応じて調整されます。 たとえば、*プット* 明細行の数量が 15 であって、*ピック* 明細行の合計数量が 10 である元の作業 ID がキャンセルされた場合、元の作業 ID の新しい *プット* 数量は 5 になります。

新しい作業をすぐにユーザーに割り当てることはできません。 ただし、必要に応じて **作業の詳細** ページの標準機能を使用することにより、ユーザーにそれを割り当てることができます。

> [!IMPORTANT]
> 2 つ以上の使用可能な作業明細行を含む作業 ID のみを分割できます。 作業明細行が 1 つしかない場合に **作業分割** を選択すると、"最初の作業では少なくとも 1 つの作業明細行を保持する必要があります" というエラー メッセージが表示されます。 この場合、分割は行われません。

## <a name="finish-a-work-split"></a>作業分割の完了

作業分割を完了するには、*作業分割* ブロックの理由を削除する必要があります。 この手順を実行するには、次の 2 つの方法があります。

- 作業を分割しているユーザーは、右上隅の **閉じる** ボタン (**X**) を選択することによって **作業分割** ページを閉じます。 ページを閉じると、*作業分割* ブロックの理由が削除されます。 この作業の *ブロック* 状態が再計算され、この作業に対してブロックの理由が残っていない場合、その作業はブロック解除されます。
- ユーザーは作業 ID を開いて、アクション ウィンドウの **作業分割セッションのキャンセル** ボタンを選択します。 *作業分割* ブロックの理由が削除され、**作業分割** ページが閉じられた場合と同様に、この作業の *ブロック* 状態が再計算されます。

*作業分割* ブロック理由が削除されると、モバイル デバイスで作業を実行できるようになります。ただし、**ブロック** 状態が作業 ID で *いいえ* に設定されている場合に限ります。

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a>倉庫管理モバイル アプリでのユーザー ブロック

分割された作業 ID に対して、倉庫管理モバイル アプリを使用してピッキング作業を実行しようとすると、"ID \#\#\#\# の作業は現在分割されています" というエラー メッセージが表示されます。 このメッセージが表示された場合は、**キャンセル** を選択します。 その後、他の作業の処理を続行できます。

## <a name="other-blocked-operations"></a>他のブロックされた操作

分割されている作業に関連する作業明細行、作業在庫トランザクション、または補充リンクを変更する工程が失敗し、"ID \#\#\#\# の作業は現在分割されています" というエラー メッセージが表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]