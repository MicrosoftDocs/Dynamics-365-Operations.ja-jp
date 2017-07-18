---
title: "需要予測の設定"
description: "このトピックでは、需要予測の準備として実行する必要のある設定タスクについて説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 74d520199410711b80b750a12ee726633e09d01c
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="demand-forecasting-setup"></a>需要予測の設定

[!include[banner](../includes/banner.md)]


このトピックでは、需要予測の準備として実行する必要のある設定タスクについて説明します。  

これらの設定作業には、次のデータとパラメーターの設定が含まれています。

## <a name="item-allocation-key"></a>品目配賦キー
需要予測は、品目が品目配賦キーの一部である場合にのみ品目と分析コードで計算されます。 このルールは、大量の品目をグループ化するために適用され、需要予測を迅速に作成できるようにします。 品目配賦キーの割合は需要予測が生成されたときは無視されます。 予測は、履歴データのみに基づいて作成されます。 

品目配賦キーが予測の作成時に使用される場合、品目および分析コードは、一つの品目配賦キーのみの一部である必要があります。 

品目配賦キーに最小在庫管理単位 (SKU) を追加するには、[**マスター プラン**] &gt; [**設定**] &gt; [**需要予測**] &gt; [**品目配賦キー**] に移動します。 [**品目の割り当て**] ページを使用して、品目を配賦キーに割り当てます。

## <a name="intercompany-planning-groups"></a>会社間計画グループ
需要予測は会社間予測を生成します。 Microsoft Dynamics 365 for Finance and Operations では、まとめて計画された会社は 1 つの会社間計画グループにグループ化されます。 需要予測と見なされる品目配賦キーを会社ごとに指定するには、[**マスター プラン**] &gt; [**設定**] &gt; [**会社間計画グループ**] の順に移動して、品目配賦キーを会社間計画グループのメンバーに関連付けます。 

既定では、品目配賦キーが会社間計画グループのメンバーに割り当てられない場合、需要予測は、すべての Finance and Operations 会社からのすべての品目配賦キーに割り当てられたすべての品目について計算されます。 会社および品目配賦キーの追加のフィルタ処理オプションは、[**統計ベースライン予測の生成**] ページで使用できます。 

予測される品目の数を確認してください。 Microsoft Azure Machine Learning を使用する場合、不要な品目によって原価が上昇する可能性があります。

## <a name="demand-forecasting-parameters"></a>需要予測パラメーター
需要予測のパラメーターを設定するには、[**マスター プラン**] &gt; [**設定**] &gt; [**需要予測のパラメーター**] の順に移動します。 需要予測が会社間で実行されるため、設定はグローバルです。 つまり、設定はすべての会社に適用されます。 

需要予測は予測数量を生成します。 そのため、数量が表す測定単位は [**需要予測の単位**] フィールドで指定する必要があります。 集約およびパーセント配分が意味をなすものであることを保証するために、測定単位は一意である必要があります。 集計およびパーセント配分の詳細については、「[ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)」を参照してください。 需要予測に含まれる SKU で使用されるすべての測定単位については、測定単位および一般的な予測の測定単位の変換ルールがあることを確認します。 予測の生成が実行されると、測定単位換算がない品目の一覧が記録されるので、簡単に設定を修正できます。 

需要予測は、依存要求と独立要求の両方を予測する場合に使用できます。 たとえば、[**販売注文**] チェック ボックスがオンになっていて、需要予測の対象と見なされるすべての品目が販売される品目である場合にのみ、システムは独立した要求を計算します。 ただし、重要なサブコンポーネントは品目配賦キーに追加および需要予測に含めることができます。 この場合、[**生産明細**] チェック ボックスがオンであるなら、依存予測が計算されます。 

Finance and Operations で予測されるベースラインを作成するための 2 つの方法があります。 履歴データの先頭に予測モデルを使用または履歴データを予測にコピーできます。 [**予測生成戦略**] フィールドでは、これら 2 つの方法を選択することができます。 予測モデルを使用するには、[**Azure Machine Learning**] を選択します。 

**需要予測のパラメーター**ページの左ウィンドウにある [**予測分析コード**] をクリックして、需要予測を生成するときに使用する予測分析コードのセットを選択することもできます。 予測分析コードは、予測が定義される詳細レベルを示します。 会社、サイト、品目配賦キーは必須の予測分析コードですが、倉庫、在庫状態、顧客グループ、顧客 ID、国/地域、都道府県、およびすべての品目分析コードのレベルで予測を生成することもできます。 

予測の分析コードを、需要予測に使用される分析コードの一覧にいつでも追加できます。 予測分析コードを一覧から削除することもできます。 ただし、手動調整は、予測分析コードを追加、または削除すると失われます。 

需要予測の観点からみてすべての品目は同じ方法で動作しません。 同様の品目は、一つの品目配賦キーおよびトランザクション タイプなどのパラメーターにグループ化でき、予測方法の設定は品目配賦キーごとに設定できます。 [**需要予測パラメーター**] ページの左ウィンドウにある [**品目配賦キー**] をクリックします。 

予測を生成する場合、Finance and Operations では、Machine Learning Web サービスを使用します。 サービスに接続する場合、Microsoft Azure Machine Learning Studio にサインインしたら、Finance and Operations に次の情報を提供する必要があります:

-   Web サービス アプリケーション プログラミング インターフェイス (API) キー
-   Web サービス エンドポイント URL
-   Azure ストレージ アカウント名
-   Azure ストレージ アカウント キー

**注:** カスタム ストレージ アカウントを使用している場合にのみ、Azure ストレージ アカウントの名前とキーが必要です。 オンプレミス バージョンを展開する場合、Machine Learning サービスを履歴データにアクセスできるようにするため、Azure のカスタム ストレージ アカウントが必要です。 

要求予測を作成する場合、Machine Learning Studio または Finance and Operations の需要予測実験を使用して自分のサービスを配置できます。 Finance and Operations の需要予測実験を Web サービスとして展開するための手順は、Finance and Operations で入手可能です。 [**需要予測パラメーター**] ページで、[**Azure Machine Learning**] タブをクリックします。

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a>Finance and Operations の需要予測 Machine Learning サービスの設定
Finance and Operations の需要予測サービスでコンフィギュレーションできるパラメーターを表示するには、[**マスター プラン**] &gt; [**設定**] &gt; [**需要予測**] &gt; [**予測アルゴリズム パラメーター**] の順に移動します。 [**予測アルゴリズム パラメーター**] ページでは、パラメーターの既定値を示します。 これらのパラメーターを [**需要予測パラメーター**] ページで上書きできます。 [**一般**] タブを使用してパラメーターをグローバルに上書きするか、[**品目配賦キー**] タブを使用して品目配賦キーごとにパラメーターを上書きします。 品目配賦キーで上書きされるパラメーターの影響を受けるのは、その品目配賦キーによって関連付けられる品目の予測のみです。

<a name="see-also"></a>参照
--------

[需要予測の概要](introduction-demand-forecasting.md)

[統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)

[ベースライン予測の手動調整の実施](manual-adjustments-baseline-forecast.md)




