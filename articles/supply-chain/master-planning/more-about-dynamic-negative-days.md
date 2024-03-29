---
title: マイナス在庫日数および動的マイナス在庫日数
description: この記事では、マイナス在庫日数および動的マイナス在庫日数に関する情報、およびこれらを使用してビジネスを支援する方法について説明します。
author: t-benebo
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcaaf46a0ddd84cded721c5d02d4a45cd4745114
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740360"
---
<!-- KFM: Split this up. non-dynamic for deprecated MP, and "dynamic" for new standard PO. -->

# <a name="negative-days-and-dynamic-negative-days"></a>マイナス在庫日数および動的マイナス在庫日数

[!include [banner](../includes/banner.md)]

この記事では、マイナス在庫日数および動的マイナス在庫日数に関する情報、およびこれらを使用してビジネスを支援する方法について説明します。 *マイナス在庫日数タイム フェンス* は、マイナス在庫がある場合に、新しい補充を注文するまでに待機する日数を表します。

この記事では、次の情報について説明します。

- 計画オーダーが作成される方法
- マイナス在庫日数タイム フェンスと品目のリード タイムとの相関関係
- 動的マイナス在庫日数タイムフェンスの計算方法と、品目のリード タイムを計算に含める方法
- マイナス在庫日数に関連する [原材料の必要量の計画 (MRP) (マスター プラン) の実行時間を改善するための提案](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) を解釈する方法

この記事では、この情報を理解するのに役立つ 3 つの仮想シナリオを使用します。 シナリオ間の違いは、品目のリード タイム期間の前、最中、または後のどの時点で需要が発生するかという点です。

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>シナリオ 1: 品目のリード タイム期間よりも前に需要が発生する場合

需要は、品目のリード タイムの比較的早い時点、またはリード タイム期間が始まる直前に発生する場合があります。 このシナリオの例を次に示します。

- DemoProduct 品目には、6 日間の購買リード タイムがあります。
- 0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫レベルは 0 (ゼロ) です。
- 0 日目 (1 月 1 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。
- 7 日目 (1 月 8 日) には、数量 10 の DemoProduct 品目に対する既存の発注書があります。

次の図は、このシナリオのグラフィカル表示を示します。

![シナリオ 1 のグラフィカル表示。](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>ケース A: マイナス在庫日数は品目のリード タイムより小さい

マイナス在庫日数を品目のリード タイムよりも小さい値に設定すると、MRP は、マイナス在庫日数タイム フェンス内で DemoProduct 品目の入庫を検索します。 入庫が見つからないため、MRP は新しい計画発注書を作成します。 この計画オーダーは、すぐに 6 日 (リード タイム) 遅延します。 したがって、1 月 7 日に入庫することになります。 新しい計画発注書の作成が必要でなくなったため、既存の発注書に **キャンセル** アクション メッセージが表示されます。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 1 のケース A スクリーンショット。](./media/negative-days-2.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 1 のケース A グラフィカル表示。](./media/negative-days-3.png)

MRP パフォーマンスとプランの違和感を考慮すると、このケースはうまく機能しません。 MRP は新しい計画オーダーを作成し、遅延とアクションを計算する必要があります。 これらのタスクには時間がかかります。 この場合、プランにはさらに 2 つのトランザクションが追加されます。 一方、販売注文の遅延は 7 日ではなく、6 日だけです。

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>ケース B: マイナス在庫日数は品目のリード タイムより大きい

MRP のパフォーマンスを向上させるために、マイナス在庫日数を品目のリード タイムよりも大きい数値に設定できます。 このシナリオではリード タイム内に供給を受けることができないため、この検索が理にかなっている限り、入庫を検索できます。 MRP の実行時間は短くなりますが、注文に対する追加の遅延には注意が必要です。

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け

品目のリード タイムをマイナス在庫日数タイム フェンスへ自動的に関連付けるには、動的マイナス在庫日数を使用します。 動的マイナス在庫日数を使用するには、**マスター プラン \> 設定 \> マスター プラン パラメーター** に移動してから、**一般** タブの **補充** セクションで、**動的マイナス在庫日数を使用する** オプションを **はい** に設定します。 次に、MRP は動的マイナス在庫日数タイム フェンス内の入庫を検索します。 このタイム フェンスは次の式を使用して計算されます。

動的マイナス在庫日数タイム フェンス = 購買のリード タイム + 動的マイナス在庫日数タイムフェンス + (現在の日付 – 要求日)

(DemoProduct 品目の既定の注文タイプが **生産** または **転送** である場合、リード タイムは **在庫** リード タイムになります。)

動的マイナス在庫日数が使用される場合、MRP が入庫を検索するタイム フェンスは 6 + 2 + 0 = 8 日になります。 MRP は既存の発注書を検索して、それに対する販売注文を関連付けます。 新しい計画オーダーは作成されません。 したがって、MRP の実行時間は短くなります。 次の図は、DemoProduct 品目の正味必要量を示します。

![シナリオ 1 のケース C 正味必要量。](./media/negative-days-4.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 1 のケース C グラフィカル表示。](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>ケース D: 動的マイナス在庫日数のみを使用

マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 + 0 = 6 日になります。 この場合、このシナリオのケース A と同じ結果になります。 MRP は新しい計画オーダーを作成し、遅延とアクションを計算する必要があります。 これらの作業には時間がかかり、もどかしい場合もあります。 さらに、処理対象のトランザクションがさらに 2 つあります。 品目が入庫に間に合うよう需要を満たすことができないので、この場合、プランに不要な煩雑さが加わります。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 1 のケース D スクリーンショット。](./media/negative-days-6.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 1 のケース D グラフィカル表示。](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する

マイナス在庫日数を品目のリード タイムより大きい数に設定した場合や、動的マイナス在庫日数のタイム フェンスも使用している場合は、動的マイナス在庫日数のタイム フェンスは 6 + 6 + 0 = 12 日になります。 この方法では、MRP が結果を検索する必要がある非常に長いタイム フェンスが生成される場合があります。 マイナス在庫日数を長いタイム フェンスに設定した場合に、ケース E がどのように関連しているかについては、この記事の [まとめ](#conclusion) を参照してください。

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>シナリオ 2: 品目のリード タイム期間中に需要が発生する場合

品目のリード タイム中に需要が発生することがあります。 このシナリオの例を次に示します。

- DemoProduct 品目には、6 日間の購買リード タイムがあります。 
- 0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫レベルは 0 (ゼロ) です。
- 品目のリード タイム内である 4 日目 (1 月 5 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。
- 7 日目 (1 月 8 日) には、DemoProduct 項目の数量 10 に対応する発注書があります。

次の図は、このシナリオのグラフィカル表示を示します。

![シナリオ 2 のグラフィカル表示。](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>ケース A: マイナス在庫日数は品目のリード タイムより小さい

マイナス在庫日数を品目のリード タイムよりも小さい値に設定すると、MRP は、マイナス在庫日数タイム フェンス内で DemoProduct 品目の入庫を検索します。 入庫が見つからないため、現在の日付を注文日として使用する新しい計画発注書が MRP によって作成されます。 この計画オーダーは、すぐに 6 日 (リード タイム) 遅延します。 したがって、1 月 7 日に入庫することになります。 新しい計画発注書の作成が必要でなくなったため、既存の発注書に **キャンセル** アクション メッセージが表示されます。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 2 のケース A スクリーンショット。](./media/negative-days-9.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 2 のケース A グラフィカル表示。](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>ケース B: マイナス在庫日数は品目のリード タイムより大きい

このケースは、シナリオ 1 のケース B に似ています。 マイナス在庫日数を品目のリード タイムよりも大きい値に設定すると、新しい計画オーダーは取得されません。 販売注文は、既存の発注書に関連付けられます。

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け

このケースは、動的マイナス在庫日数がそのケースと同様に機能するため、シナリオ 1 のケース C に似ています。 動的マイナス在庫日数のタイム フェンスは、6 + 2 – 4 = 4 日になります。 この方法を使用した場合、MRP は既存の発注書を検索し、販売注文をその発注書に関連付けます。 新しい計画オーダーが作成されないため、MRP の実行時間は短くなります。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 2 のケース C スクリーンショット。](./media/negative-days-11.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 2 のケース C グラフィカル表示。](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>ケース D: 動的マイナス在庫日数のみを使用

マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 – 4 = 2 日になります。 この場合、このシナリオのケース A と同じ結果になります。 何が起こるかのグラフィカル表示については、このシナリオのケース A を参照してください。

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する

マイナス在庫日数を品目のリード タイムより大きい数に設定した場合や、動的マイナス在庫日数のタイム フェンスも使用している場合は、動的マイナス在庫日数のタイム フェンスは 6 + 6 – 4 = 8 日になります。 この方法では、MRP が結果を検索する必要がある非常に長いタイム フェンスが生成される場合があります。 マイナス在庫日数を長いタイム フェンスに設定した場合に、ケース E がどのように関連しているかについては、この記事の [まとめ](#conclusion) を参照してください。

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>シナリオ 3: 品目のリード タイム期間後に需要が発生する場合

品目のリード タイム期間後に需要が発生する場合があります。 このシナリオの例を次に示します。

- DemoProduct 品目には、6 日間の購買リード タイムがあります。
- 0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫は 0 (ゼロ) です。
- 品目のリード タイム外である 7 日目 (1 月 8 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。
- 10 日目 (1 月 11 日) には、数量 10 の DemoProduct 品目に対する発注書があります。

次の図は、このシナリオのグラフィカル表示を示します。

![シナリオ 3 のグラフィカル表示。](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>ケース A: マイナス在庫日数は品目のリード タイムより小さい

マイナス在庫日数を品目のリード タイムより小さい値に設定すると、MRP は販売注文の要求日から 2 日先を検索します。 何も見つからないため、MRP は 1 月 2 日に新しい計画発注書を作成します。 この計画発注書は、販売注文の需要を満たすのにちょうど間に合うよう出荷されます。 既存の発注書には、必須ではないため **キャンセル** アクション メッセージが表示されます。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 3 のケース A スクリーンショット。](./media/negative-days-14.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 3 のケース A グラフィカル表示。](./media/negative-days-15.png)

> [!NOTE]
> 前のスクリーンショットでは、発注書の要求日は 1 月 12 日です。 このスクリーンショットは 2015 年に取られたものだったため、1 月 11 日が日曜日である場合、MRP は要求日を次の稼働日である 1 月 12 日の月曜日に移動しました。 ただし、発注書の配送日は 1 月 11 日になります。

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>ケース B: マイナス在庫日数は品目のリード タイムより大きい

マイナス在庫日数を品目のリード タイムよりも大きい値に設定すると、新しい計画オーダーは取得されません。 販売注文は、既存の発注書に対して関連付けられます。 したがって、販売注文は遅延します。 計画オーダーが作成されると、販売注文を期限遵守で出荷できます。

次の図は、このケースのスクリーンショットを示します。

![シナリオ 3 のケース B スクリーンショット。](./media/negative-days-16.png)

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 3 のケース B グラフィカル表示。](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>ケース C: 品目のリード タイムのマイナス在庫日数タイム フェンスへの自動的な関連付け

このケースは、シナリオ 1 のケース C に似ています。動的マイナス在庫日数がこのシナリオのケース B の場合と同様に機能するためです。

動的マイナス在庫日数のタイム フェンスは、6 + 2 – 7 = 1 日になります。 ただし、この場合、MRP では在庫日数リード タイムと動的マイナス在庫日数リード タイム間の最大値が考慮されるため、システムはマイナス在庫日数リード タイム (2) を考慮します。 したがって、このケースの結果は、このシナリオのケース A と同じ結果になります。

次の図は、このケースに何が起こるかのグラフィカル表示です。

![シナリオ 3 のケース C グラフィカル表示。](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>ケース D: 動的マイナス在庫日数のみを使用

マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数のタイム フェンスのみを使用した場合、動的マイナス在庫日数タイム フェンスは 6 + 0 – 7 = -1 日になります。 この場合、マイナス在庫日数リード タイム (2) が考慮されます。 したがって、このケースの結果は、このシナリオのケース A と同じ結果になり、すべて同じ短所があることになります。 何が起こるかのグラフィカル表示については、シナリオ 2 のケース A を参照してください。

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>ケース E: 品目のリード タイムを超えるマイナス在庫日数と、動的マイナス在庫日数タイム フェンスの両方を使用する

このケースは、シナリオ 1 および 2 のケース E と同じです。 基本的に、同じ長所と短所があります。

## <a name="conclusion"></a>まとめ

この記事で使用する 3 つのシナリオでは、マイナス在庫日数は、補充グループの品目のリード タイムよりも大きい数に設定することをお勧めします。 また、動的マイナス在庫日数のみを使用し、マイナス在庫がある場合は、マイナス在庫日数を新しい補充を注文するまで待機できる日数 (つまり、需要をさらに遅延させてもよい日数) に設定します。 また、同じ補充グループの品目には同じリード タイムを設定する必要があります。

マイナス在庫日数を **0** (ゼロ) に設定し、動的マイナス在庫日数を使用しない場合、MRP は常に新しい計画オーダーを作成して需要を満たすようにします。 この状況では、アクション メッセージを使用して、在庫がなくなるようにすることが重要です。

マイナス在庫日数を長いタイム フェンスに設定し、アクション メッセージを処理することができます。 この方法により、プランを適切に作成できますが、少し時間がかかります。 アクション メッセージを分析し適用する必要があるため、分析がより困難になる場合もあります。 次に例を示します。

- DemoProduct 品目には、6 日間の購買リード タイムがあります。
- 0 日目 (1 月 1 日) の時点では、DemoProduct 品目の在庫は 0 (ゼロ) です。
- 0 日目 (1 月 1 日) に、DemoProduct 品目の数量 10 の販売注文を取得します。
- 9 日目 (1 月 10 日) に、数量 10 の DemoProduct 品目に対する販売注文を取得します。
- 11 日目 (1 月 12 日) には、数量 10 の DemoProduct 品目に対する発注書があります。
- マイナス在庫日数は **20** に設定され、品目のリード タイムよりもかなり大きくなります。

次の図は、何が起こるかのグラフィカル表示です。

![例のグラフィカル レビュー。](./media/negative-days-19.png)

MRP では次の結果が生成されます。

![結果例 1。](./media/negative-days-20.png)

前のスクリーンショットでは、販売注文の要求日は 1 月 10 日ではなく、1 月 9 日になります。 このスクリーンショットは 2015 年に取られたものだったため、1 月 10 日が土曜日である場合、注文の要求日を前の稼働日である 1 月 9 日の金曜日にする必要があります。

MRP は、最初の販売注文で要求される需要を満たす計画発注書を作成しますが、その後、計画オーダーをキャンセルするよう勧めてきます。それは既存の発注書を繰り上げて数量を増やすことができるためです。

結果は間違っていませんが、MRP の実行時間は長くなります。それは MRP がすべての遅延と提案を作成する必要があるためです。 また、プランナーは MRP の結果を理解するためにより多くの時間を必要とする場合があります。 この場合、最も重要な点として、プランナーがアクション メッセージを理解して使用することが必須です。

マイナス在庫日数を品目のリード タイムに近い値に減らし、動的マイナス在庫日数を使用すると、MRP では次のような結果が生成されます。

![結果例 2。](./media/negative-days-21.png)

MRP では、最初の販売注文に関連付けられた計画オーダーが作成されます。 その後、予想されるように、2 番目の販売注文は、マイナス在庫日数の設定に基づいて既存の発注書に対して関連付けされます。 このプランニング結果も正しく、MRP の実行時間が短くなる可能性があります。 この場合、アクション メッセージをどのように処理するかを理解しておくことは必須ではありません。

業務に合った正しい値が確実に入力されるようにするには、機能と MRP の実行時間の両方について考慮する必要があります。 したがって、最適値を特定するには少し試行錯誤が必要です。

## <a name="see-also"></a>参照

詳しい解説については、元の [(動的) マイナス在庫日数の詳細](/archive/blogs/axmfg/more-about-dynamic-negative-days) ブログ投稿を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
