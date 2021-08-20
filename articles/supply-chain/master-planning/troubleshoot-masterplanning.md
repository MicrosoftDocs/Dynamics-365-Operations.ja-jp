---
title: マスター プランのトラブルシューティング
description: このトピックでは、マスター プランを操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4dc3c5c8a1597fce4cc61461d16cd11ad80426eb8841871278772fcd7b8c86b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766634"
---
# <a name="troubleshoot-master-planning"></a>マスター プランのトラブルシューティング

このトピックでは、マスター プランを操作する際に発生する可能性がある問題の修正方法について説明します。

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>部品表の展開は、確定した製造オーダーと、手動で作成された作業の見積製造オーダーの間で動作が異なります。

### <a name="issue-description"></a>問題の説明

製造オーダーを確定すると、部品表 (BOM) を展開しても品目が展開されません。 ただし、手動で作業指示を作成してから製造オーダーを見積すると、品目が展開されます。

### <a name="issue-resolution"></a>問題の解決

システムは正常に機能しています。 製造オーダーが確定されたときに発生する展開は計画オーダーを指していますが、この場合、計画オーダーが現在確定されていることを示しているわけではありません。 ただし、製造オーダーが見積済みの場合は、計画オーダーが存在しないリリース済製造オーダーから展開が開始されます。

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>計画オーダーを再スケジューリングする場合、遅延値は更新されません。

計画オーダーの遅延を更新するには、計画オーダーの **再スケジュール** ダイアログ ボックスを開きます。 **展開** クイック タブで、**再スケジュール後に展開を実行する** オプションが *はい* に設定されていることを確認します。

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>生産のスケジューリングでは、ペギングされた供給に対して品目補充で設定されている安全マージンは考慮されません。

### <a name="issue-description"></a>問題の説明

マスター プランでは安全マージンが考慮されます。 ただし、計画製造オーダーのスケジューリング時に安全マージンは無視されます。

### <a name="issue-resolution"></a>問題の解決

マージンは、マスター プラン中にのみ考慮され、手動のスケジューリングでは考慮されません。 マージンは、計画フェーズでバッファーとして機能するように設計されており、実際のプロセスのために "マージン" を提供します。

目的の結果を得るには、マージンを削除します。 次に、目的の時間 (待ち時間など) を含めるように工順を更新する必要があります。 その後、マスター プランと手動のスケジューリングの両方で同じ結果が生成される必要があります。

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>在庫および製造オーダーの品目が既に存在している場合でも、計画オーダーが生成されます。

この問題を解決するには、**補充グループ** ページで該当するグループの **プラス在庫日数** の値を大きくします。 この変更により、需要に手持在庫を使用できるかどうかがシステムによって判断されます。 この場合、在庫のある品目に対して新しい計画オーダーは生成されません。

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>マスター プランがキャパシティ制限を考慮していないように見え、利用可能なキャパシティを超えてスケジューリングしています。

### <a name="issue-description"></a>問題の説明

有限キャパシティを持つ工程スケジューリングを使用していて、工順がリソース グループと個々のリソースの両方で混在する要件を指定している場合は、アルゴリズムがキャパシティ競合を検証する方法のため、予約超過の可能性が小さくなります。 この予約超過は、ヘルパーを使用してマスター プランを実行するときに発生する可能性があります。 実行時間が比較的短いジョブが多数存在する場合に、この問題が発生する可能性が最も高くなります。

### <a name="issue-resolution"></a>問題の解決

工程のスケジューリングに対して予約超過を行わないことが必須である場合、**マスター プラン パラメーター** ページで **工程のスケジューリングの正確な有限キャパシティ** オプションをオンにして、マスター プランのスケジューリングの一部を行うことができます。 このオプションは、既定では使用できません。 この機能は、パーソナル化機能を使用してページに手動で追加する必要があります。 このオプションを使用すると、並列処理が行われないため、スケジューリングの実行速度が遅くなります。

## <a name="planned-orders-take-a-long-time-to-update"></a>計画オーダーの更新には長い時間がかかります。

### <a name="issue-description"></a>問題の説明

計画オーダーの要求数量または出荷日、あるいはその両方を更新する場合、更新を保存するために、通常はオーダーあたり少なくとも 30 秒かかります。

### <a name="issue-resolution"></a>問題の解決

これは、組み込みのマスター プラン エンジンに関する既知の問題です。 編集中に BOM 構造を通じた基になる自動展開によって発生します。 この問題は、計画の最適化で修正されます。計画の最適化では、プランナーが関連するオーダーを更新および承認し、必要に応じて計画実行をトリガーして基になる BOM 構造の計画オーダーを更新できます。

組み込みのマスター プラン エンジンを使用してパフォーマンスを向上させる方法の 1 つは、次のとおりです。

1. **マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。
1. プランを選択します。
1. **タイム フェンス (日)** クイックタブを展開します。
1. **展開** を *はい* に設定し、この設定の下にあるフィールドを 0 (ゼロ) に設定します。

> [!NOTE]
> これにより、このマスター プランに対して実行される展開の期間が 1 日に制限されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]