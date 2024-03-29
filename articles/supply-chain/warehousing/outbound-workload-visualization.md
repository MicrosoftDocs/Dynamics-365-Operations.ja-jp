---
title: 出庫ワークロードの視覚化
description: この記事は、ワークロードの視覚化に関する情報を提供します。 この機能により、倉庫管理者と監修者は、現在の作業の進捗状況と残っている金額を監視するために使用できるカスタム ワークロード グラフを作成できるようになります。 倉庫管理者は、複数のビューを作成し、必要に応じて自動更新を設定できます。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78d0d81095bb52a314936dd7590a5690d94ecb15
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334418"
---
# <a name="outbound-workload-visualization"></a>出庫ワークロードの視覚化

[!include [banner](../includes/banner.md)]

**出庫ワークロードの視覚化** ページからアクセスできる高度な設定機能により、倉庫管理者と監修者は、現在の作業の進捗状況と残っている金額を監視するためのカスタム ワークロード グラフを作成できます。 倉庫管理者は、複数のビューを作成し、必要に応じて自動更新を設定できます。 出庫ワークロードの視覚化は、倉庫のパフォーマンス ページでの表示に適しています。

この機能は、集荷作業の進行状況を追跡するために使用できます。 この機能は労働管理に統合されており、労務管理が設定されている場合は、表示されている集荷作業の残りの時間数を計算して表示することができます (フィルター処理)。

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>出庫ワークロードの視覚化機能をオンまたはオフにする

この機能を使用するには、システムでオンにする必要があります。 Supply Chain Management バージョン 10.0.25 では、この機能は既定で有効になっています。 Supply Chain Management バージョン 10.0.29 では、この機能は必須であり、オフにすることはできません。 10.0.29 より以前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *ワークロードの視覚化を発信する* 機能を検索して、この機能をオンまたはオフにすることができます。

## <a name="set-up-outbound-workload-visualizations"></a>出庫ワークロードの視覚化の設定

視覚化を設定するには、フィルター (ビュー) のコレクションを作成し、異なるタイプの分析を表示するように各フィルターを設計します。 フィルターを設計するには、**フィルターの構成** ページを使用します。

出庫ワークロードの視覚化を設定するには、次の手順を実行します。

1. **倉庫管理 \> 倉庫の監視レポート \> 出庫ワークロードの視覚化** の順に移動します。

    **出庫ワークロードの視覚化** ページが表示されます。 フィルターを作成すると、このページに視覚化が表示されます。 必要な数のフィルターを作成することができます。 作成したすべてのフィルターは、ユーザー アカウントに保存されるため、後で使用することができます。 つまり、各ユーザーは作成された独自のフィルターのセットを持つことになります。 これらのフィルターは、他のユーザーと共有されることはありません。

1. **出庫ワークロードの視覚化** ページのアクション ウィンドウの **フィルター** タブで、**フィルターの構成** を選択します。
1. **フィルターの構成** ページのアクション ウィンドウで、**新規** を選択してフィルターを追加し、次のフィールドを設定します。

    - **X 軸のグループ テーブル** – X 軸の値をグループ化するために使用するフィールドを含むテーブルを選択します。
    - **X 軸のグループ フィールド** – **X 軸グループ テーブル** フィールドで選択したテーブルのフィールドの中から、X 軸の値をグループ化するために使用するフィールドを選択します。
    - **X 軸値のテーブル** – グループをさらに分析するために使用する必要があるフィールドを含むテーブルを選択します。
    - **X 軸値のフィールド** – **X 軸グループ テーブル** フィールドで選択したテーブルのフィールドの中から、グループごとに分析する必要のある値を提供するフィールドを選択します。
    - **自動更新** – 視覚化を自動的に更新するかどうかを選択します。
    - **更新間隔 (分)** – 自動更新の間隔を分単位で入力します。
    - **表示レベル** – グラフでオープン行とオープン ヘッダー カウントのどちらを表示するかを選択します。
    - **ピッキング タイプ** – **表示レベル** フィールドを _明細行を開く_ に設定した場合は、グラフの内の開いている作業明細行の数に、初期ピック、段階的ピック、または初期ピックと段階的ピックの両方を含めるかどうかを選択します。
    - **サイト** – グラフを読み込むサイトを選択します。
    - **サイト** – グラフを読み込む倉庫を選択します。
    - **含める日数** – グラフを生成する過去の日数を入力します。
    - **作業指示書タイプ** – フィルター処理する出庫作業指示書タイプを選択します。

    ![フィルターの構成ページ。](media/work-viz-filters-1.png "フィルターの構成ページ")

1. **フィルターの構成** ページを閉じて、**出庫ワークロードの視覚化** ページに戻ります。

    新しいフィルター設定に基づいて、**出庫ワークロードの視覚化** ページにデータが表示されるようになりました。 これで、新しいフィルターが使用可能になり、**フィルター** フィールドで選択されます。 グラフの最上部には、次のフィールドがあります:

    - **フィルター**: このフィールドには、これまでに作成したすべてのフィルターが含まれます。 データをグラフに表示するには、フィルターを選択します。
    - **最終更新日時** – このフィールドは、グラフの情報が最後に更新された日時を表示します。
    - **見積済/実際の時間** – 労働基準がシステムで設定されている場合、このオプションを *はい* に設定すると、計算された集荷時間の累計がグラフの各列の上部に表示されます。 労働基準を使用していない場合、このオプションは使用できません。

    ![視覚化の例。](media/work-viz-chart.png "視覚化の例")

1. グラフ内の任意のバーを選択して、関連する作業明細行の詳細を表示します。

    ![作業ラインの詳細。](media/work-viz-work-details.png "作業ラインの詳細")

## <a name="example-outbound-workload-visualization-for-zones"></a>例: ゾーンの出庫ワークロードの視覚化

この例では、各ゾーンの作業明細行を表示する視覚化と、各作業項目のステータス (_未処理_、_終了_、または _キャンセル_) を設定します。 この場合は、次の設定を含むフィルターを設定できます。

- **フィルター名** – このフィルターの名前 (_ゾーンと作業ステータス_ など) を入力します。
- **説明** – このフィルターの簡単な説明 (_ゾーンと作業ステータス_ など) を入力します。
- **X 軸のグループ テーブル** – _場所_ を選択します。
- **X 軸グループ** – _ゾーン ID_ を選択します。
- **X 軸の値テーブル** – ゾーンごとの作業を表示するので、_作業_ を選択します。
- **X 軸の値フィールド** – 作業の状態を表示するので、_作業状態_ を選択します。
- **自動更新** – 視覚化を自動的に更新するかどうかを選択します。
- **ピッキング タイプ** – ステージング場所からの最初のピックとピックの両方を含めるために、_初期ピックとステージピック_ を選択します。 つまり、基本的には、作成したすべてのピック作業行を含める必要があります。
- **表示レベル** – 作業ヘッダーごとではなく明細行ごとの情報を表示するために、_未処理の明細行_ を選択します。

以下の図は、結果としてのグラフの一例を表しています。

![ゾーンと作業状態の視覚化。](media/work-viz-chart.png "ゾーンと作業状態の視覚化")

このグラフには、**FLOOR** および **BULK** という名前の 2 つのゾーンと **空白** のゾーンが示されています。 **空白** のゾーンは、ゾーンのメンバーではないすべての作業明細行を表します。 グラフには、関係のないすべてのフィルター処理されたデータが常に **空白** として表示され、できるだけ視覚化できるようになっています。 **FLOOR** ゾーンでは、グラフに 3 つの終了した明細行と 4 つの未処理の明細行が表示されています。 **BULK** ゾーンでは、グラフに 4 つの終了した明細行と 1 つの未処理の明細行、24 のキャンセルされた明細行が表示されています。 最後に、ゾーンに含まれていない 8 つの終了した明細行がグラフに表示されるため、**空白** として一覧されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]