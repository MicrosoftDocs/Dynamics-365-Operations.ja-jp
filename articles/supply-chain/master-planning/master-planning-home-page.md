---
title: マスター プランのホーム ページ
description: マスター プランにより、会社が原材料および会社の目標を満たす能力に対する将来の必要性を特定し調整することができます。
author: ShylaThompson
manager: tfehr
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7829c09696fc5619f1652cbfbde5ae88eaa3ab32
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224502"
---
# <a name="master-planning-home-page"></a>マスター プランのホーム ページ

[!include [banner](../includes/banner.md)]

その中心に、マスター プランにより、会社が原材料および会社の目標を満たす能力に対する将来の必要性を特定し調整することができます。 マスター プランを以下の点を評価します。 

-  現在どのような原材料および能力を使用できますか。 
-  生産を完了するのに、どのような原材料および能力が必要ですか。 たとえば、製造、購入、転送または生産を完了する前に安全在庫を取り分ける必要があるものは何ですか。

マスター プランは必要量を計算し、計画オーダーを生成するための情報を使用します。

3 つの主要な計画プロセスは次のとおりです。

-  **マスター プラン** - マスター プランは正味必要量を計算します。 実際の現在の注文に基づき、会社が在庫補充を短期的、日常的なベースで管理できるようにします。 これを説明する別の用語は、*正味必要量プラン* です。 詳細については、[マスター プランの概要](master-plans.md) を参照してください。 

-  **予測計画** - 予測スケジュールは総必要量を計算します。 将来の予想 (または予測) に基づき、会社が材料と能力の長期計画を実行できるようにします。 詳細については、[需要予測の概要](introduction-demand-forecasting.md) を参照してください。 

-  **会社間マスタ計画** - 会社間マスター プランは法人間の正味必要量を計算します。 会社間の需要および供給を、短期的な確定需要と供給だけでなく、長期的で計画された (まだ確定されてはいない) 需要と供給を関連付けます。 詳細については、[会社間マスター プラン](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (e ラーニング) (CustomerSource アカウントが必要です) を参照してください。 

会社は、計画の出力を変更できます。 再生式、差分変更、またはその両方を実行できます。 再生式計画はすべての要件を更新しますが、差分変更計画は最後のスケジューリングの実行の後に入ってきた新しい要件を持つ品目の計画のみ更新します。

マスター スケジューリング計画には、通常は、1 週間から 6 か月の間で任意の短期間が含まれます。 マスター プラン モジュールが供給 (材料) を特定し、容量 (リソース) は現在の需要 (正味必要量) を満たします。 ほとんどの企業では、受け取る製品の中で最長の累積的なリード タイムを含むようこれが拡張されます。

## <a name="learning-map"></a>学習マップ

次の学習マップは、マスター プラン モジュールのフレームワークを構成する主要な概念とタスクについて説明します。 「[クイック リンク](#quick-links)」セクションにあるリンクをクリックして、モジュールの使用方法について学習します。

[![マスター プランの学習マップ](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>クイック リンク

- [マスター プランの概要](master-plans.md)  
- [制約付き計画の生成](./tasks/constrained-plan.md)
- [連産品の材料計画の作成](./tasks/create-material-plan-co-products.md)
- [マスター プランとマルチサイト機能の概要](master-plan-multisite-functionality.md)
- [会社間計画の作成](./tasks/create-intercompany-plan.md)
- [需要予測の概要](introduction-demand-forecasting.md)
- [予測下方修正キー](reduction-keys.md)
                                  
## <a name="additional-resources"></a>追加リソース

### <a name="roadmaps"></a>ロードマップ
リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/)を参照してください。

### <a name="blogs"></a>ブログ
[Dynamics AX Manufacturing R&D Team Blog (Dynamics AX 製造研究開発チーム ブログ)](https://blogs.msdn.microsoft.com/axmfg) および [Supply Chain Management in Dynamics AX R&D Team Blog (Dynamics AX のサプライ チェーン マネジメント研究開発チーム ブログ)](https://blogs.msdn.microsoft.com/dynamicsaxscm) で、マスター プランやその他のソリューションに関する意見、ニュース、その他の情報を見つけることができます。

### <a name="task-guides"></a>タスク ガイド
追加のヘルプは、タスク ガイドとして使用できます。 タスク ガイドにアクセスするには、ページの **ヘルプ** ボタンをクリックします。

### <a name="webinars"></a>ウェビナー
[需要予測用 Azure Machine Learning の使用](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>技術会議の記録
-  [Extend the demand forecasting functionality (需要予測機能の拡張)](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Master planning - tips and tricks for troubleshooting performance (マスター プラン - パフォーマンスのトラブルシューティングに関するヒントとコツ)](https://youtu.be/7v8BPmEs9Dg)
-  [Help! MRP is slow! (MRP の処理に時間がかかる!)](https://youtu.be/RLXybx20B5o)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]