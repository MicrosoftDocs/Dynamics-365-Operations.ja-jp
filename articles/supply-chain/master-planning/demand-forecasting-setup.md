---
title: 需要予測の設定
description: このトピックでは、需要予測の準備として実行する必要のある設定タスクについて説明します。
author: ChristianRytt
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f53171361b655ab4ae05894d098203df0af8d60
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920776"
---
# <a name="demand-forecasting-setup"></a>需要予測の設定

[!include [banner](../includes/banner.md)]

このトピックでは、需要予測の設定方法について説明します。  

## <a name="item-allocation-keys"></a>品目配賦キー

品目配賦キーは、品目のグループを設定します。 需要予測は、品目が品目配賦キーの一部である場合にのみ品目と分析コードで計算されます。 このルールは、大量の品目をグループ化するために適用され、需要予測を迅速に作成できるようにします。 予測は、履歴データのみに基づいて作成されます。

品目配賦キーが予測の作成時に使用される場合、品目および分析コードは、一つの品目配賦キーのみの一部である必要があります。

品目配賦キーを作成して、それに在庫管理単位 (SKU) を追加するには、次の手順に従います。

1. **マスター プラン \> 設定 \> 需要予測 \> 品目の配賦キー** の順に移動します。
1. リスト ペインで品目配賦キーを選択するか、アクション ペインで **新規** を選択して新しいものを作成します。 新規または選択されたキーのヘッダーで、次のフィールドを設定します。

    - **品目配賦キー** - キーの固有の名前を入力します。
    - **名前** - キーに内容を示す名前を入力します。

1. 次のいずれかの手順に従って、選択した品目配賦キーに品目を追加するか、品目を削除します。

    - **品目配賦** クイック タブで、ツールバーの **新規** ボタンや **削除** ボタンを使用して、必要に応じて品目を追加または削除します。 各行に対して品目番号を選択し、必要に合って他の列の分析コード値を割り当てる必要があります。 ツールバーで **分析コードの表示** を選択して、グリッドに表示される分析コード列のセットを変更します。 (**パーセント** 列の値は、需要予測が生成されたときは無視されます。)
    - 多数の品目をキーに追加する場合は、[アクション ウィンドウ] で **品目の割り当て** を選択すると、選択したキーに複数の項目を見つけて割り当てるページが開 きます。

> [!IMPORTANT]
> 各品目配賦キーには該当する品目のみを含めるのに注意してください。 Microsoft Azure Machine Learning を使用する場合、不要な品目によって原価が上昇する可能性があります。

## <a name="intercompany-planning-groups"></a>会社間計画グループ

需要予測は会社間予測を生成できます。 Dynamics 365 Supply Chain Management では、まとめて計画された会社は同じ会社間計画グループにグループ化されます。 会社ごとに、どの品目配賦キーを需要予測と見なす必要がある場合に、品目配賦キーを会社間計画グループ メンバに関連付ける必要があります。

> [!IMPORTANT]
> 計画の最適化では、現在、会社間計画グループはサポートされていません。 計画の最適化を使用する会社間計画を実行するには、すべての関連会社のマスター プランを含むマスター プラン バッチ ジョブを設定します。

自分の会社間計画グループを設定するには、次の手順に従います。

1. **マスター プラン \> 設定\> 会社間計画グループ** の順に移動します。
1. リスト ウィンドウで計画グループを選択するか、アクション ウィンドウで **新規** を選択して新しいグループを作成します。 新規または選択されたグループのヘッダーで、次のフィールドを設定します。

    - **名前** – 計画グループの一意の名前を入力します。
    - **説明** – 計画グループの短い説明を入力します。

1. **会社間計画グループ メンバー** のクイック タブで、ツール バーのボタンを使用して、グループに含む必要がある会社 (法人) ごとに行を追加します。 各行で、次のフィールドを設定します:

    - **法人** - 選択したグループのメンバーである会社 (法人) の名前を選択します。
    - **スケジューリング シーケンス** - 他の会社との関連において会社を処理する順序を割り当てます。 低い値が最初に処理されます。 この注文は、ある会社の需要が他の会社に影響する場合に重要になる可能性があります。 このような場合、需要を供給する会社は最後に処理する必要があります。
    - **マスター プラン** - 現在の会社に対してトリガーするマスター プランを選択します。
    - **静的プランへの自動コピー** - 計画の結果を静的プランにコピーする場合は、このチェック ボックスをオンにします。
    - **動的プランへの自動コピー** - 計画の結果を動的プランにコピーする場合は、このチェック ボックスをオンにします。

1. 既定では、品目配賦キーが会社間計画グループのメンバーに割り当てられない場合、需要予測は、すべての会社からのすべての品目配賦キーに割り当てられたすべての品目について計算されます。 **統計ベースライン予測の生成** ダイアログ ボックス (**マスター プラン \> 予測 \> 需要予測 \> 統計ベースライン予測の生成**) で、会社および品目配賦キーに対する追加のフィルタ オプションを使用できます。 選択した会社間計画グループ内の会社に品目配賦キーを割り当てるには、会社を選択し、**会社間計画グループ メンバー** のクイック タブで、ツール バーの **品目配賦キー** を選択します。

> [!IMPORTANT]
> 各会社間計画グループには該当する品目配賦キーのみを含めることに注意してください。 Azure Machine Learning を使用する場合、不要な品目によって原価が上昇する可能性があります。

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>需要予測のパラメーターの設定

**需要予測パラメータ** ページを使用して、システムでの需要予測の機能を制御する複数のオプションを設定します。

### <a name="open-the-demand-forecasting-parameters-page"></a>需要予測のパラメーター ページを開く

需要予測のパラメーターを設定するには、**マスター プラン \> 設定 \> 需要予測 \> 需要予測のパラメーター** の順に移動します。 需要予測が会社間で実行されるため、設定はグローバルです。 つまり、設定はすべての法人 (会社) に適用されます。

### <a name="general-settings"></a>一般設定

需要予測の一般設定を定義するには、**需要予測パラメータ** ページの **一般** タブを使用します。

#### <a name="demand-forecast-unit"></a>需要予測単位

需要予測は予測数量を生成します。 そのため、数量が表す測定単位は **需要予測の単位** フィールドで指定する必要があります。 このフィールドは、製品ごとに通常の在庫単位に関係なく、すべての需要予測で使用される単位を定義します。 一貫した予測ユニットを使用することで、集約およびパーセント配分が意味をなすものであることを確認します。 集計およびパーセント配分の詳細については、「[ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)」を参照してください。

需要予測に含まれる SKU で使用されるすべての測定単位については、ここで選択した測定単位および一般的な予測の測定単位の変換ルールがあることを確認します。 予測の生成を実行すると、測定単位換算がない品目の一覧が記録されます。 そのため、設定を簡単に修正できます。 測定単位とこれらを変換する方法の詳細については、[測定単位の管理](../pim/tasks/manage-unit-measure.md) を参照してください。

#### <a name="transaction-types"></a>トランザクション タイプ

**トランザクション タイプ** クイック タブのフィールドを使用して、統計ベースライン予測の生成時に使用するトランザクション タイプを選択します。

需要予測は、依存受容と独立要求の両方を予測する場合に使用できます。 たとえば、**販売注文** オプションが *はい* になっていて、需要予測の対象と見なされるすべての品目が販売される品目である場合にのみ、システムは独立した要求を計算します。 ただし、重要なサブコンポーネントは品目配賦キーに追加および需要予測に含めることができます。 この場合、**生産明細** オプションが *はい* であるなら、依存予測が計算されます。

**品目配賦キー** タブを使用して、1 つ以上の特定の品目配賦キーの トランザクション タイプを上書き できます。このタブには同様のフィールドが表示されます。

#### <a name="choose-how-to-create-the-baseline-forecast"></a>ベースライン予測の作成方法の選択

**予測生成戦略** フィールドでは、ベースライン予測の作成に使用する方法を選択できます。 3 つのメソッドを使用できます。

- *履歴需要のコピー* - 履歴データをコピーするだけで予測を作成します。
- *Azure Machine Learning Service* -  : Azure Machine Learningサービスを使用する予測モデルを使用します。 Azure Machine Learning サービスは、Azure の最新の機械学習ソリューションです。 したがって、予測モデルを使用する場合に使用することをお勧めします。
- *Azure Machine Learning* - Azure Machine Learning スタジオ (クラシック) を使用する予測モデルを使用します。 Azure Machine Learning スタジオ (クラシック) は廃止され、間もなく Azure から削除されます。 そのため、需要予測を初めて設定する場合は *Azure Machine Learning Service* を選択することをお勧めします。 現在、Azure Machine Learning スタジオ (クラシック) を使用している場合は、できるだけ早く Azure Machine Learning Service に切り替える必要があります。

**品目配賦キー** タブを使用して、1 つ以上の特定の品目配賦キーの予測生成メソッドを上書きできます。このタブには同様のフィールドが表示されます。

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>既定の予測アルゴリズム パラメータのグローバルな上書き

既定の予測アルゴリズムのパラメータと値は、**需要予測パラメータ** ページ (**マスター プラン \> 設定 \> 需要予測 \> 需要予測パラメータ**) に割り当てられます。 ただし、**需要予測パラメータ** ページの **一般** タブにある **予測アルゴリズム パラメータ** クイック タブを使用して、グローバルに上書きできます。  **需要予測パラメータ** ページの **品目配賦キー** タブを使用して、これらのキーを特定の配賦キーに対して上書きすることもできます。

ツール バーの **追加** ボタンと **削除** ボタンを使用して、必要なパラメーター上書きのコレクションを確立します。 リストの各パラメータについて、**名前** フィールドの値で次のいずれかの値を選択し、**値** フィールドに適切な値を入力します。 ここで説明していないすべてのパラメータは、**需要予測パラメータ** ページの設定 から値を受け取 ります。 標準パラメータ セットの使用方法およびパラメータの値の選択方法の詳細については、[需要予測モデルの既定のパラメータと値](#model-parameters) を参照してください。

### <a name="set-forecast-dimensions"></a>予測分析コードの設定

予測分析コードは、予測が定義される詳細レベルを示します。 会社、サイト、品目配賦キーは、必要な予測分析コードです。 会社、サイト、品目配賦キーは必要な予測分析コードですが、倉庫、在庫状態、顧客グループ、顧客 ID、国/地域、都道府県、および/または品目レベル、そしてすべての品目分析コードのレベルで予測を生成することもできます。 **需要予測のパラメーター** ページの **予測分析コード** を使用して、需要予測を生成するときに使用する予測分析コードのセットを選択することもできます。

予測の分析コードを、需要予測に使用される分析コードの一覧にいつでも追加できます。 予測分析コードを一覧から削除することもできます。 ただし、手動調整は、予測分析コードを追加、または削除すると失われます。

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>特定の品目配賦キーに対する上書きの設定

需要予測の観点からみてすべての品目が同じ方法で動作するわけではありません。 したがって、**一般** タブで定義した設定のほとんどについて、配賦キー固有の上書きを設定できます。例外は需要予測単位です。 特定の品目配賦キーの上書きを設定するには、次の手順に従います。

1. **需要予測パラメータ** ページの **品目配賦キー** タブで、ツール バー ボタンを使用して、左側のグリッドに品目配賦キーを追加するか、必要に応じて削除 します。 次に、上書きを設定する配賦キーを選択します。
1. **トランザクション タイプ** クイック タブで、選択した配賦キーに属する製品の統計ベースライン予測の生成に使用するトランザクションのタイプを有効します。 この設定は、**一般** タブでの作業と同様に機能しますが、選択した品目配賦キー にのみ適用されます。 ここでのすべての設定 (*はい* 値と *いいえ* の値の両方) は、**一般** タブのすべての **トランザクション タイプ** 設定を上書きします。
1. **予測アルゴリズム パラメータ** クイック タブで、選択した配賦キーに属する製品に対する予測生成戦略および予測アルゴリズム パラメータの上書 きを選択します。 これらの設定は、**一般** タブでの作業と同様に機能しますが、選択した品目配賦キーにのみ適用されます。 ツール バーの **追加** ボタンと **削除** ボタンを使用して、必要なパラメーター上書きのコレクションを定義します。 リストの各パラメータについて、**名前** フィールドの値で次のいずれかの値を選択し、**値** フィールドに適切な値を入力します。 標準パラメータ セットの使用方法およびパラメータの値の選択方法の詳細については、[需要予測モデルの既定のパラメータと値](#model-parameters) を参照してください。

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Azure Machine Learning Service への接続の設定

**Azure Machine Learning Service** タブ を使用して、Azure Machine Learning Service への接続を設定します。 このソリューションは、ベースライン予測を作成するためのオプションの 1 つです。 このタブのこれらの設定は、**予測生成戦略** フィールドが *Azure Machine Learning Service* に設定されている場合にのみ有効になります。

Azure Machine Learning Service を設定し、この設定を使用して接続する方法の詳細については、[Azure Machine Learning Service の設定](#setup-amls) を参照してください。

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Azure Machine Learning スタジオ (クラシック) への接続の設定

> [!IMPORTANT]
> Azure Machine Learning スタジオ (クラシック) は廃止されました。 したがって、このワークスペース用の新しいワークスペースは、Azure で作成できなくなりました。 このサービスは、類似した機能など、さまざまな機能を提供する Azure Machine Learning Service によって置き換えられたのです。 Azure Machine Learning をまだ使用していない場合は、Azure Machine Learning Service の使用を開始する必要があります。 既に Azure Machine Learning スタジオ (クラシック) 用に作成されたワークスペースがある場合は、この機能が Azure から完全に削除されるまで、引き続きそのワークスペースを使用できます。 ただし、できるだけ早く Azure Machine Learning Service に更新することをお勧めします。 アプリケーションは引き続き、Azure Machine Learning スタジオ (クラシック) が廃止されたという警告を表示しますが、予測結果には影響されません。 Azure Machine Learning Service を設定し、この設定を使用して接続する方法の詳細については、[Azure Machine Learning Service の設定](#setup-amls) を参照してください。
>
> Supply Chain Management を使用する新しいコンピュータ 学習ソリューションと古い学習ソリューションを使用する場合は、古い Azure Machine Learning スタジオ (クラシック) ワークスペースを使用できる限り、その間は自由に切り替えることができます。

既に使用できる Azure Machine Learning スタジオ (クラシック) ワークスペースがある場合は、それを使用して Supply Chain Management に接続することで予測を生成できます。 この接続を設定するには、**需要予測パラメータ** ページの **Azure Machine Learning** タブを使用 します。 (このタブの設定は、次の場合にのみ有効になります。**予測生成戦略** フィールドは *Azure Machine Learning* に設定されています。) Azure Machine Learning スタジオ (クラシック) ワークスペースに次の詳細を入力します。

- Web サービス アプリケーション プログラミング インターフェイス (API) キー
- Web サービス エンドポイント URL
- Azure ストレージ アカウント名
- Azure ストレージ アカウント キー

> [!NOTE]
> カスタム ストレージ アカウントを使用している場合にのみ、Azure ストレージ アカウントの名前とキーが必要です。 オンプレミス バージョンを展開する場合、Machine Learning を履歴データにアクセスできるようにするためには、Azure でカスタム ストレージ アカウントが必要です。

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>需要予測モデルの既定のパラメータと値

機械学習を使用して予測計画モデルを生成する場合は、*アルゴリズム パラメータを予測* するための値を設定して機械学習オプションを制御します。 これらの値は、Supply Chain Management から Azure Machine Learning に送信されます。 **予測アルゴリズムのパラメータ** ページでは、提供する値のタイプと各値を制御します。

既定のパラメータや需要予測サービスで使用される値を設定するには、**マスター プラン \> 設定 \> 需要予測 \> 予測アルゴリズム パラメーター** の順に移動します。 標準的なパラメータ セットが用意されています。 各パートナーにじゃ次のフィールドがあります。

- **名前** - Azure で使用されるパラメータの名前。 通常、この名前は、Azure Machine Learning のテストをカスタマイズしていない限り変更しないのが一般的です。
- **説明** - パラメータの一般的な名前。 この名前は、システムの他の場所 (**需要予測パラメータ** ページなど) でパラメータを識別するために使用されます。
- **値** - パラメータの規定値を選択します。 入力する値は、編集するパラメータによって異なります。 
- **説明** - パラメータの簡単な説明、およびパラメータの使用方法。 通常、この説明には、**値** フィールドの有効な値に関する情報が含 まれます。

既定では、次のパラメータが提供されます。 (この標準リストに戻す必要が生じ場合は、アクション ウィンドウで **復元** を選択します。)

- **信頼レベルのパーセンテージ** – 信頼区間は、需要予測の商品見積として機能する値の範囲で構成されます。 95% の信頼レベルのパーセンテージは、未来の需要が信頼区間の範囲外になるリスクが 5% あることを示します。
- **季節性の強制** – 特定のタイプの季節性を使用するようにモデルに強制するかどうかを指定します。 このパラメーターは ARIMA と ETS のみ適用されます。 オプション: *AUTO (既定)*、*NONE*、*ADDITIVE*、*MULTIPLICATIVE*。
- **予測モデル** - 使用する予測モデルを指定します。 オプション: *ARIMA*、*ETS*、*STL*、*ETS+ARIMA*、*ETS+STL*、*ALL*。 最も適合するモデルを選択するには、*ALL* を使用してください。
- **最大予測値** – 予測に使用する最大値を指定します。 形式: +1E [n] または数値定数。
- **最小予測値** – 予測に使用する最小値を指定します。 形式: -1E [n] または数値定数。
- **欠落値の代入** – 履歴データのギャップを埋める方法を指定します。 オプション: *(数値)*、*MEAN*、*PREVIOUS*、*INTERPOLATE LINEAR*、*INTERPOLATE POLYNOMIAL*。
- **欠落値の代入スコープ** – 値の代入を個々の粒度属性の日付範囲に適用するか、データセット全体に適用するかを指定します。 履歴データのギャップを埋めるときにシステムが使用する日付範囲を確立するには、次のオプションを使用できます。

    - *GLOBAL* – システムは、すべての精度属性の日付の全範囲を使用します。
    - *HISTORY_DATE_RANGE* – システムは、**統計ベースライン予測の生成** ダイアログ ボックスの **履歴期間** セクションの **開始日** フィールドと **終了日** フィールドで定義された特定の日付範囲を使用します。
    - *GRANULARITY_ATTRIBUTE* – システムは、現在処理されている精度属性の日付範囲を使用します。

    > [!NOTE]
    > 精度属性は、予測が行われる予測分析コードの組み合わせです。 **需要予測パラメーター** ページで予測分析コードを定義できます。

- **季節性のヒント** – 季節データについては、予測の精度を高めるために予測モデルに対するヒントを指定してください。 形式: 需要パターンが繰り返し現れるバケット数を表す整数。 たとえば、6 か月ごとに繰り返されるデータの場合は *6* を入力します。
- **テスト セット サイズの割合** – 予測精度計算のテスト セットとして使用する履歴データの割合。

これらのパラメータの値は、**マスター プラン \> 設定 \> 需要予測 \> 需要予測パラメータ** に移動して上書きできます。 **需要予測パラメーター** ページで、このパラメーターを次の方法で上書きできます。

- **一般** タブを使用すると、パラメーターをグローバルに上書きできます。
- **品目配賦キー** タブを使用すると、特定の品目配賦キーに対してパラメータを上書きできます。 品目配賦キーで上書きされるパラメーターの影響を受けるのは、その特定品目配賦キーによって関連付けられる品目の予測のみです。

> [!NOTE]
> **予測アルゴリズムパラメータ** ページで、アクション ウィンドウのボタンを使用して一覧にパラメータを追加するか、一覧からパラメータを削除することができます。 しかしながら、通常、Azure Machine Learning のテストをカスタマイズしていない限りこのアプローチは使用すべきではありません。

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Azure Machine Learning Service の設定

Supply Chain Management では、独自の Azure サブスクリプションを設定して実行する必要がある Azure Machine Learning Service を使用して、需要予測を計算します。 このセクションでは、AzureのAzure Machine Learningサービスを設定し、それを Supply Chain Management 環境に接続する方法について説明します。

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>機能管理における Azure Machine Learning Service の有効化

需要予測に Azure Machine Learning Service を使用するには、Supply Chain Management の機能を有効にして統合を有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *マスター プラン*
- **機能名:** *需要予測向け Azure Machine Learning Service*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Azure での機械学習設定

Azure で機械学習を使用して予測を処理するには、その目的に合った Azure Machine Learning ワークスペースを設定する必要があります。 2 つのオプションがあります。

- Microsoft が提供しているスクリプトを実行してワークスペースを設定するには、[オプション 1: スクリプトを実行して自動的に機械学習ワークスペースを設定する](#ml-workspace-script) セクションを設定し、[Supply Chain Management での Azure Machine Learning Service 接続パラメータの設定](#demand-forecast-parameters) セクションに進みます。
- ワークスペースを手動で設定するには、[オプション 2: スクリプトを実行して手動で Machine Learning ワークスペース を設定する](#ml-workspace-manual) セクションを設定し、[Supply Chain Management での Azure Machine Learning Service 接続パラメータの設定](#demand-forecast-parameters) セクションに進みます。 このオプションを使用すると時間は長されますが、より詳細に制御できます。

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>オプション1 : Machine Learning ワークスペースを自動的に設定するスクリプトの実行

このセクションでは、Microsoft によって提供される自動スクリプトを使用して、Machine Learning ワークスペースを設定する方法について説明します。 必要に応じて、[オプション2: Machine Learning ワークスペースを手動で設定する](#ml-workspace-manual) の手順に従って、すべてのリソースを手動 で設定 できます。 両方のオプションを完了させる必要はありません。

1. GitHub で、[Azure Machine Learning を使った Dynamics 365 Supply Chain Management 需要予測のテンプレート](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) リポジトリ (repo) を開き、次のファイルをダウンロードします。

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. PowerShell ウィンドウを開き、前の手順でダウンロードした **quick_setup.ps1** スクリプトを実行します。 画面に表示される指示に従ってください。 このスクリプトは、必要なワークスペース、記憶域、既定のデータストア、および計算リソースを設定します。 ただし、この手順の残りの手順に従って、必要なパイプラインを作成する必要があります。 (パイプラインを使用すると、Supply Chain Management から予測スクリプトを開始できます。)
1. Azure Machine Learning スタジオで、手順 1 でダウンロードした **sampleInzip.csv** ファイルを、*demplan-azureml* という名前のコンテナーにアップロードします。 (quick_setup.ps1 スクリプトでこのコンテナーを作成しました)。このファイルは、パイプラインを公開し、テスト予測を生成するために必要です。 手順については、[block blob をアップロードする](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) を参照してください。
1. Azure Machine Learning スタジオで、ナビゲーターの **ノートブック** を選択します。
1. **ファイル** 構造: **Users/\[現在のユーザー\]/src** で次の場所を検索します。
1. 手順1. でダウンロードした残りの 4 ファイルを、前の手順で見つかった場所にアップロードします。
1. アップロードした **api_trigger.py** ファイルを選択して実行します。 API を介してトリガできるパイプラインが作成されます。
1. ワークスペースが設定されました。 [Supply Chain Management での Azure Machine Learning Service 接続パラメータの設定](#demand-forecast-parameters) セクションに進みます。

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>オプション2: Machine Learning ワークスペースを手動で設定する

ここでは、Machine Learning ワークスペースを手動で設定する方法について説明します。 このセクションの手順は、自動セットアップ スクリプトを実行しない場合にのみ実行する必要があります。詳細については、[オプション1 : スクリプトを実行して機械学習ワークスペースを設定する](#ml-workspace-script) を参照してください。

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>手順 1: 新しいワークスペースを作成する

新しいMachine Learning ワークスペースを作成するには、次の手順に従います。

1. Azure ポータルにサインインします。
1. **Machine Learning** サービスを開きます。
1. ツールバーで **作成** を選択して、**作成** ウィザードを開きます。
1. 画面に表示される指示に従ってウィザードを完了します。 作業時には、次の点に注意してください。

    - この一覧の他のポイントが別の設定を推奨しない限り、既定の設定を使用します。
    - Supply Chain Management のインスタンスが配置されている地域に一致する地域を選択してください。 それ以外の場合は、一部のデータが地域の境界を通過する場合があります。 詳細については、このトピックの後にある [プライバシー通知](#privacy) を参照してください。
    - リソース グループ、記憶域アカウント、コンテナー レジストリ、Azure キー コンテナー、ネットワーク リソースなどの専用リソースを使用します。
    - ウィザードの **Azure Machine Learning Service 接続パラメータの設定** ページで、記憶域アカウント名を指定する必要があります。 需要予測専用のアカウントを使用します。 需要予測の入力データおよび出力データはこのストレージ アカウントに格納されます。

詳細については、[ワークスペースの作成](/azure/machine-learning/quickstart-create-resources#create-the-workspace) を参照してください。

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>手順 2: ストレージの構成

自分のストレージを設定するには、次の手順を使います。

1. GitHub で、[Azure Machine Learning を使った Dynamics 365 Supply Chain Management 需要予測のテンプレート](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo を開き、**sampleInput.csv** ファイルをダウンロードします。
1. [手順1: 新しいワークスペースの作成](#create-workspace) で作成した記憶域アカウントを開 きます。
1. [コンテナーの作成](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) の手順に従って、*demplan-azureml* という名前のコンテナーを作成します。
1. 手順 1 でダウンロードした **sampleInput.csv** ファイルを今作成したコンテナーにアップロードします。 このファイルは、パイプラインを公開し、テスト予測を生成するために必要です。 手順については、[block blob をアップロードする](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob) を参照してください。

##### <a name="step-3-configure-a-default-datastore"></a>手順3: 既定のデータストアを構成する

既定のデータストアを設定するには、次の手順を使います。

1. Azure Machine Learning スタジオで、ナビゲーターの **データストア** を選択します。
1. [手順2: 記憶域の構成](#config-storage) セクションで作成した *demplan-azureml* Blob Storage コンテナーをポイントする、*Azure Blob Storage* タイプの新しいデータストアを作成します。 (新しいデータストアの認証タイプが *アカウント キー*。作成した記憶域アカウントのアカウント キーを指定します。 手順については、[ストレージ アカウントのアクセス キーの作成](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal) を参照してください。)
1. 詳細を開き、**既定のデータストアとして設定** を選択して、新しいデータストアを既定のデータストア化します。

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>手順4: 計算リソースを構成する

予測生成スクリプトを実行するように Azure Machine Learning スタジオで計算リソースを設定するには、次の手順に従います。

1. [手順1: 新しいワークスペースの作成](#create-workspace) セクションで作成した Machine Learning ワークスペースの詳細ページを開 きます。 **Studio のウェブ URL** の値を 検索し、リンクを選択して開きます。
1. ナビゲーション ウィンドウで、**計算する** を選択します。
1. **コンピューティング インスタンス** タブで、**新規** を選択して、新規コンピューティング インスタンスの作成に役立つウィザードを開きます。 画面に表示される指示に従ってください。 このコンピューティング インスタンスは、需要予測パイプラインの作成に使用されます (パイプラインの公開後に削除できます)。既定の設定を使用します。
1. **コンピューティング クラスター** タブで、**新規** を選択して、新規コンピューティング クラスターの作成に役立つウィザードを開きます。 画面に表示される指示に従ってください。 コンピューティング クラスタは、需要予測を生成するために使用されます。 この設定によって、パフォーマンスと実行の最大並列レベルが影響を受ける場合があります。 次のフィールドを設定しますが、他のすべてのフィールドについては既定の設定を使用します。

    - **名前** - *e2ecpucluster* と入力します。
    - **仮想機械のサイズ** - 需要予測の入力として使用すると予想されるデータの量に応じてこの設定を調整します。 需要予測の生成をトリガするために 1 つのノードが必要であり、予測の生成に使用できるノードの最大数は 10 なので、ノード カウントは 11 を超えてはいけません。 (ノード カウントは、[手順5: パイプラインの作成](#create-pipelines) セクションの parameters.py ファイルでも設定します。) 各ノードで、予測スクリプトを並列して実行する複数のワーカー プロセスが用意されています。 ジョブのワーカー プロセスの総数は、*ノードが持っているコア数* × *ノード数* になります。 たとえば、コンピューティング クラスターが *標準\_D4* (8 コア) で最大 11 ノードであるある場合、そして `nodes_count` の値が parameters.py ファイルで *10* の場合、並列処理の有効レベルは 80 になります。

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>手順 5: パイプラインを作成する

パイプラインは、Supply Chain Management から予測スクリプトを開始するための方法を提供します。 次の手順を使用して、必要なパイプラインを作成します。

1. GitHub で、[Azure Machine Learning を使った Dynamics 365 Supply Chain Management 需要予測のテンプレート](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) repo を開き、次のファイルをダウンロードします。

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Azure Machine Learning スタジオで、ナビゲーターの **ノートブック** を選択します。
1. **ファイル** 構造: **Users/\[現在のユーザー\]/src** で次の場所を検索します。
1. 手順1. でダウンロードした 4 ファイルを、前の手順で見つかった場所にアップロードします。
1. Azureで、アップロードした **parameters.py** ファイルを開いて確認します。 `nodes_count` の値が、[手順4: 計算リソースの構成](#config-compute-resources) セクションのコンピューティング クラスターに対して構成した値より 1 つ少ないことを確認 します。 `nodes_count` 値がコンピューティング クラスター内のノードの数以上の場合は、パイプラインを開始できる場合があります。 ただし、必要なリソースが待機している間は応答を停止します。 ノード カウントの詳細については、[手順4: 計算リソースの構成](#config-compute-resources) セクションを参照してください。
1. アップロードした **api_trigger.py** ファイルを選択して実行します。 API を介してトリガできるパイプラインが作成されます。

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>新しい Active Directory アプリケーションを設定する

Active Directory アプリケーションは、サービス元金を使用した需要予測専用のリソースで認証を行う必要があります。 したがって、予測を生成するために必要な最小レベルの権限がアプリケーションに必要となります。

1. Azure ポータルにサインインします。
1. テナントの Azure Active Directory (Azure AD) で新規アプリケーションを登録します。 手順については、[ポータルを使用して、リソースにアクセスできる Azure AD アプリケーションとサービス プリンシパルを作成する](/azure/active-directory/develop/howto-create-service-principal-portal) を参照してください。
1. ウィザード完了に伴い画面に表示される指示に従います。 既定の設定を使用します。
1. 新しい Active Directory アプリケーションに、[Azureの機械学習の設定](#ml-workspace) セクションで作成した次のリソースへの アクセス許可を与えます。 手順については、[Azureポータルを使用した Azure ロールの割り当て](/azure/role-based-access-control/role-assignments-portal?tabs=current) を参照してください。 この手順により、システムによって予測データのインポートとエクスポートが可能になります。また、Supply Chain Management から機械学習パイプラインの実行がトリガーされます。

    - Machine Learning ワークスペースの要因の役割
    - 専用の記憶域アカウントに対する貢献者のロール
    - 専用のストレージ アカウントに対するストレージ BLOB データの共同作成者

1. 作成したアプリケーションの **証明書と証書** セクションで、申請用のプログラム を作成します。 手順については、[クライアント シークレットを追加する](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) を参照してください。
1. アプリケーション ID とそのシークレットをメモします。 Supply Chain Management の **需要予測パラメーター** ページを設定する際には、後でこのアプリケーションの詳細が必要になります。

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Supply Chain Management での Azure Machine Learning Service 接続パラメータの設定

次の手順を使って、Supply Chain Management 環境を Azure で今設定した Machine Learning service に接続します。

1. Supply Chain Management にサインインします。
1. **マスター プラン \> 設定 \> 需要予測 \> 需要予測のパラメーター** の順に移動します。
1. **一般** タブで、**予測生成戦略** フィールドが *Azure Machine Learning Service* に設定されている必要があります。
1. **品目配賦キー** タブで、需要予測に Azure Machine Learning Service を使用する配賦キーごとに、**予測生成戦略** フィールドが *Azure Machine Learning Service* に設定されている必要があります。
1. **Azure Machine Learning Service** タブで、次のフィールドを設定します。

    - **テナント ID** – 自分の Azure テナント に ID を入力します。 Supply Chain Management は、この ID を使用して Azure Machine Learning Service で認証を行います。 自分のテナント ID は、Azure ポータルの Azure AD の **概要** ページにあります。
    - **サービス プリンシパル アプリケーション ID** - [Active Directory アプリケーション](#aad-app) セクションで作成したアプリケーションのアプリケーション ID を入力します。 この値は、Azure Machine Learning Service に対する API 要求を承認するために使用されます。
    - **サービス プリンシパル シークレット** - [Active Directory アプリケーション](#aad-app) セクションで作成したアプリケーションのサービス プリンシパル アプリケーション シークレットを入力します。 この値は、Azure StorageおよびAzure Machine Languageワークスペースに対して許可された操作を実行するために作成したセキュリティ キーのアクセス トークンを取得するために使用されます。
    - **ストレージ アカウント名** - Azure ワークスペースでセットアップ ウィザードを実行するときに指定した Azure ストレージ アカウント名を入力します。 (詳細については、[Azure で機械学習を設定する](#ml-workspace) を参照してください。)
    - **パイプライン エンドポイント アドレス** - Azure Machine Learning Service のパイプライン REST エンドポイントの URL を入力します。 このパイプラインは、[Azure で機械学習を設定する](#ml-workspace) 際の最後の手順として作成しました。 パイプライン URL を取得するには、ナビゲーションで **パイプライン** を選択して、Azure ポータル にログインします。 **パイプライン** タブで **TriggerDemandForecastGeneration** という名前のパイプライン エンドポイントを選択します。 その後、表示される REST エンドポイントをコピーします。

    ![需要予測パラメーターページの Azure Machine Learning Service タブ上のパラメータ。](media/azure-ml-service-parameters.png "需要予測パラメーターページの Azure Machine Learning Service タブ上のパラメータ")

## <a name="privacy-notice"></a><a name="privacy"></a>プライバシー通知

予測の生成戦略として *Azure Machine Learning Service* を選択すると、Supply Chain Management は、集計された数量、製品名とその製品分析コード、出荷場所と入荷場所、顧客 ID、予測パラメータなどの履歴の需要に対する顧客データを、コンピュータ 学習ワークスペースおよびリンクされたストレージ アカウントがある地域に、将来の需要を予測する目的のために自動的に送信します。 Azure Machine Learning Service は、 Supply Chain Management が配置されている地域とは異なる地域である場合があります。 一部のユーザーは、**需要予測パラメータ** ページで予測生成戦略を選択することで、この機能を有効 にするかどうかを制御 できます。

## <a name="additional-resources"></a>追加リソース

- [需要予測の概要](introduction-demand-forecasting.md)
- [統計ベースライン予測を生成する](generate-statistical-baseline-forecast.md)
- [ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
