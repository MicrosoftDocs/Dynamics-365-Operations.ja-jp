---
title: 作業ラインの詳細
description: この記事では、システムの個々の作業ラインの包括的、並べ替え可能、フィルター処理可能な一覧を表示する作業ラインの詳細ページに関する情報を提供します。
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1017527419acc2e4cb42b2bcb83131339d82b665
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218885"
---
# <a name="work-line-details"></a>作業ラインの詳細

[!include [banner](../includes/banner.md)]

**作業ラインの詳細** ページには、システムの個々の作業ラインの包括的、並べ替え可能、フィルター処理可能な一覧が表示されます。 これにより、倉庫で計画および実行されている作業の完全な概要が表示されます。 すべての作業ラインの表示とオープン作業ラインのみの表示を簡単に切り替えることができます。 各ラインに対して表示される詳細には、作業ステータス、品目番号、場所、作業数量、積荷 ID、および出荷 ID が含まれます。

## <a name="turn-on-the-work-line-details-feature"></a>作業ラインの詳細機能をオンにする

Supply Chain Management のバージョン 10.0.21 では、この機能は既定で有効になっています。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページで機能状態を確認し、必要に応じて有効化または無効化することができます。 この機能は次のように一覧表示されます。

- **モジュール:** *倉庫管理*
- **機能名:** *作業ラインの詳細*

## <a name="open-and-use-the-work-line-details-page"></a>作業ラインの詳細ページを開いて使用する

作業ラインの詳細の一覧を表示するには、**倉庫管理 \> 作業 \> 作業ラインの詳細** の順に移動します。 ここでは、実行できるアクションは次のとおりです。

- **フィルター** フィールドを使用して、使用可能なパラメーターに対して特定の値をとるラインを検索します。 (使用可能なパラメーターには、グリッドに列として表示されない多数のパラメーターが含まれています。)
- **クローズ済の表示** チェックボックスを使用して、閉じたラインを表示または非表示にできます。
- **分析コードの表示** を選択して、**分析コード表示** ダイアログ ボックスを開きます。ここでは、グリッド内のさまざまな分析コード列を表示または非表示にすることができます。
- 任意の列見出しを選択してメニューを開き、その列の値によって一覧の並べ替え、またはフィルター処理を選択できます。
- 作業ラインを選択し、**場所の変更** を選択して、その作業ラインの場所を変更できるダイアログ ボックスを開きます。 指定した場所は、場所のディレクティブの設定を上書きします。
- 作業ラインを選択し、**作業ラインのキャンセル** を選択して、その作業ラインの数量を部分的または完全に減らすことができるダイアログ ボックスを開きます。
- 数量を調整します。
- 任意の作業ラインの背後にあるトランザクションを表示します。

## <a name="try-out-the-feature"></a>機能を試す

このセクションでは、作業ラインの詳細を操作する方法を示す 3 つの部分からなるデモについて説明します。

### <a name="make-sample-data-available"></a>サンプル データを有効化する

ここで指定されたサンプル レコードと値を使用してこのデモを実行するには、標準の [デモ データ](../../fin-ops-core/fin-ops/get-started/demo-data.md) がインストールされているシステムを使用する必要があります。 また、開始する前に **USMF** 法人を選択する必要があります。

このデモは、実稼働システムで作業するときのガイダンスとして使用することもできます。 ただし、独自の値に置き換える必要があり、標準のデモ データが提供するいくつかのタイプの必要なレコードが不足している可能性があります。

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>シナリオの設定に十分な利用可能在庫があることの検証

**USMF** のデモ データを使用している場合は、まず、関連する各ピッキング場所に十分な在庫が利用できるようにシステムが設定されていることを確認する必要があります。 このデモでは、次の在庫があることが予想されます。

- **品目 M9200:** 45 個 (または以上)
- **品目 M9202:** 10 個 (または以上)

次の手順に従って、十分な在庫があることを確認し、必要な調整を行います。

1. **倉庫管理 \> 設定 \> 場所のディレクティブ** の順に移動し、倉庫 51 で販売注文のピッキングに使用されるピッキング場所を決定します。 (詳細については、[作業テンプレートと場所ディレクティブを使い倉庫作業の制御](control-warehouse-location-directives.md) を参照してください。)
1. 関連する場所で在庫レベルを確認します。
1. 必要に応じて在庫を調整します。 手動による移動を作成したり、補充を使用したり、またはその他のフローを適用して在庫を調整したりできます。

### <a name="part-1-create-picking-work"></a>パート 1: ピッキング作業の作成

作業の作成を開始する前に、予定した方法で作業要求に対応するように倉庫が設定されていることを確認してください。

これらの手順に従って、ピッキング作業を作成します。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
1. **新規** を選択して、**販売注文の作成** ダイアログ ボックスを開きます。
1. **販売注文の作成** ダイアログ ボックスでは、次の値を設定します。

    - **顧客** クイック タブで、**顧客 ID** フィールドを _US-001_ に設定します。
    - **一般** クイック タブの **倉庫** フィールドを _51_ に設定します。

1. **OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。
1. 新しい販売注文が開かれます。 **販売注文行** グリッドに新しい空の行が含まれます。 この注文明細行に次の値を設定します。

    - **品目番号:** _M9200_
    - **数量:** _20_
    - **単位:** _個_

1. 新しい注文明細行を選択し、**在庫** メニューで、**引当** を選択して **引当** ページを開きます。
1. **引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当します。
1. **引当** ページを閉じて、販売注文に戻ります。
1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。 システムは出荷を作成し、それを新しい積荷に追加して、必要な作業を作成します。
1. 最初の注文で使用したのと同じ顧客 ID と倉庫に対して 2 番目の販売注文を作成します。 この注文に次の 2 つの注文明細行を追加します。

    - **行 1:** **品目番号** フィールドを _M9200_ に、**数量** フィールドを _25_ に、**単位** を _個_ に設定します。
    - **行 2:** **品目番号** フィールドを _M9202_ に、**数量** フィールドを _10_ に、**単位** を _個_ に設定します。

1. 手順 6 ～ 8 を繰り返して、各注文明細行の在庫の引当を行い (一度に 1 つずつ)、手順 9 を繰り返して、注文を倉庫にリリースします。

### <a name="part-2-change-the-location-for-a-work-line"></a>手順 2: 作業ラインの場所を変更する

1. **倉庫管理 \> 作業 \> 作業ラインの詳細** の順に移動します。
1. このデモ用に作成した作業ラインの 1 つを検索して選択します。
1. **場所の変更** を選択して、**新しい場所の選択** ダイアログ ボックスを開きます。
1. **新しい場所の選択** ダイアログ ボックスの **場所** フィールドで、作業ラインの新しい場所を選択します。
1. **OK** を選択して変更を適用し、ダイアログ ボックスを閉じます。

> [!IMPORTANT]
> 新しい保管場所に使用可能な十分の在庫がある場合 (ピッキングの場合)、または場所タイプの検証に合格した場合 (プットの場合) にのみ、場所の変更を送信できます。

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>手順 3: 作業ラインの数量の変更または作業ラインのキャンセル

1. **倉庫管理 \> 作業 \> 作業ラインの詳細** の順に移動します。
1. このデモ用に作成した作業ラインの 1 つを検索して選択します。 作業タイプが _ピッキング_ である作業ラインについてのみ、数量をキャンセルまたは変更できることに注意してください。
1. **作業ラインのキャンセル** を選択して、**キャンセルする数量** ダイアログ ボックスを開きます。
1. **キャンセルする数量** ダイアログ ボックスで、**数量** フィールドの値を変更して、ラインに現在指定されている数量 *から減算* される数量を指定します。 既定では、**数量** フィールドには全数量が表示されます。

    - 全数量をキャンセルすると、**作業ステータス** 値が _キャンセル済_ に変更されますが、**作業数量** フィールドには、元の値が引き続き表示されます。
    - 数量の一部のみをキャンセルした場合、**作業数量** フィールドは更新されて新しい値が表示されますが、**作業ステータス** 値は変更されません。

1. **OK** を選択して変更を適用し、ダイアログ ボックスを閉じます。

> [!IMPORTANT]
> 作業ラインの数量の一部のみをキャンセルする場合は、積荷明細行から古い数量を削除する必要もあります。 それ以外の場合は、過少配送が正しく設定されていないと、積荷明細行は出荷確認できません。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]