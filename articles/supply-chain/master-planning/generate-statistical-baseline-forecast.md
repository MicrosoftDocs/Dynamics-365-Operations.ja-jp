---
title: "統計ベースライン予測の生成"
description: "この記事は、需要予測の計算に使用されるパラメータおよびフィルタについて説明しています。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 93646e37ee511d433097bb284fccc73c230aee32
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>統計ベースライン予測の生成

[!include[banner](../includes/banner.md)]


この記事は、需要予測の計算に使用されるパラメータおよびフィルタについて説明しています。 

ベースライン予測を作成するとき、計算に使用されるパラメーターとフィルターを最初に指定する必要があります。 たとえば、特定の会社について、翌月について、また選択した品目グループについて、過去 1 年のトランザクション データに基づいて、需要を見積もるベースライン予測を作成できます。 

需要予測の生成へは、**[マスター プラン] &gt; [予測] &gt; [需要予測] &gt; [統計ベースライン予測の生成]** の順に移動します。 

予測バケットは予測生成時に選択できます。 利用可能な値は、"日、週" および "月" です。 

予測されている生成するバケットの数は、[**予測期間**] フィールドに設定されています。 

予測方法が [**履歴需要の上書き**] に設定されている場合、履歴期間の終了は無視されます。 システムでは需要予測に、[**履歴期間**] にある [**開始日**] フィールドにセットされた日付から、[**予測期間**] フィールドに指定されたバケットの数をコピー します。 特定の日付以前から履歴需要をコピーして、生産のスケジューリング者は二つの方法で来四半期の計画を行うことができます:

-   昨年の同じ四半期の需要をコピーすることで。
-   前の四半期の需要をコピーすることで。

生産計画の混乱を回避するために、一定数の予測バケットは凍結できます。 この番号は、[**凍結タイム フェンス**] フィールドに設定されます。 [**調整された需要予測**] ページで、その値が変更されないよう視覚的表示があり、凍結するバケットのセルは無効になります。 

ベースライン需要予測の開始日は、現在の日付または将来の日付である必要はありません。 別の開始日を設定するには、[**ベースライン予測開始日 - 開始日**] フィールドを使用します。 たとえば、6 月に、翌年の予測を生成できます。 履歴需要およびベースラインの開始時の予測バケットが存在しないため、予測は正確ではない場合があります。 Microsoft Dynamics 365 for Finance and Operations の需要予測サービスを使用している場合、欠落したギャップを埋める 4 つの方法があります。 [**需要予測パラメーター**] ページで、MISSING\_VALUE\_SUBSTITUTION のパラメーターを設定して使用する方法を選択できます。 

[**ベースラインの予測の開始日**] - [**開始日**] フィールドは、予測バケットの先頭に設定する必要があります。たとえば、米国で予測バケットが週の場合、日曜日。 システムは、[**ベースライン予測の開始日**] - [**開始日**] フィールドを、予測バケットの先頭に合わせて自動的に調整します。 

[**ベースライン予測開始日** - [**開始日**] フィールドは、過去の日付に設定できます。 つまり、過去の需要予測を生成できます。 これはユーザーが予測サービス パラメータを微調整でき、過去に生成した統計予測を実際の履歴需要と一致できるため便利です。 ユーザーは、将来の統計ベースライン予測を生成する場合に、これらのパラメータの設定を使用できます。 

[**手動調整を需要予測に転送**] のチェック ボックスがオンの場合、新しい ベースライン予測に以前の需要予測繰り返しの手動調整を自動的に適用できます。 チェック ボックスがオフの場合、手動調整がベースライン予測に追加されませんが、削除もされません。 予測の手動調整は、予測のインポート時に [**ベースライン需要予測に対して行われた手動調整の保存**] のチェックボックスを オフにした場合にのみ、削除することができます。 手動調整は認証時に保存されます。 ユーザーが予測の手動調整を行い、Finance and Operations で予測を承認しない場合は変更が失われます。 手動調整に関する詳細、および動作については、「[調整された予測の承認](authorize-adjusted-forecast.md)」を参照してください。 

需要予測の生成には、ユーザーが生成された予測を識別できるように、名前とコメントをつけられます。 これらの値は、[**統計ベースライン予測の生成履歴**] ページの予測生成の履歴に表示されます。 

会社間計画グループ、品目配賦キーおよびその他のフィルタは予測生成時に適用できます。 これらはパフォーマンスの改善、または管理しやすいチャンクにデータを分割するのに使用できます。 ただし品目配賦キーをクエリで選択した場合でも、会社間計画グループに関連付けられない品目配賦キーのメンバーに対して需要予測は生成されない事に、注意してください。 

**ヒント**: 場合によっては、需要予測の生成中、または予測の生成がセッションログなしで完了時に、エラーが発生する場合があります。 これは、予測の生成に以前に使用されたクエリのデータが残っている場合に発生することがあります。 この問題を修正するには、[**選択**] をクリックして [**クエリ**] ページを開き、[**リセット**] をクリックし、ベースライン予測を再生成します。 

たとえば 1 つの品目または 1 つの品目配賦キーを一度に生成する場合など、大きい 1 つの品目の予測が生成されない場合や、パフォーマンスを向上させるために、[**マスタ プラン - 設定 - 需要予測**] - [**需要予測のパラメーター - Azure Machine Learning**] のタブで [**要求応答モードの使用**] のチェック ボックスを選択できます。

<a name="see-also"></a>参照
--------

[需要予測の設定](demand-forecasting-setup.md)

[ベースライン予測の手動調整の実施](manual-adjustments-baseline-forecast.md)

[調整された予測の承認](authorize-adjusted-forecast.md)



