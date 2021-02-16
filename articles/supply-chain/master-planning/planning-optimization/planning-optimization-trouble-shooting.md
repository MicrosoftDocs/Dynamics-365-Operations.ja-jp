---
title: 計画最適化のトラブルシューティング
description: このトピックでは、計画の最適化を実行する際に発生する可能性がある問題の修正方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431743"
---
# <a name="troubleshoot-planning-optimization"></a>計画最適化のトラブルシューティング 

[!include [banner](../../includes/banner.md)]

このトピックでは、計画の最適化を実行する際に発生する可能性がある一般的な問題の修正方法について説明します。

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>計画の最適化アドインのインストールが完了しない

計画の最適化には、Dynamics 365 Supply Chain Management バージョン 10.0.7 以降で、Lifecycle Services (LCS) が有効な高可用性環境、Tier 2 以上（OneBox 環境ではありません）が必要です。 アドインを OneBox 環境にインストールしようとしても、インストールが完了しない。

**修正**: インストールをキャンセルし、高可用性環境、Tier 2 以上 (OneBox 環境ではありません) を使用します。

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>計画の最適化を有効にすると、バッチジョブの計画が失敗する

計画の最適化を有効にすると、組み込みのマスター プラン エンジンが自動的に無効になる。 組み込みの Supply Chain Management 計画エンジン用に作成されたマスター計画バッチ ジョブは、計画の最適化が有効な状態でトリガーされると失敗します。 *この操作は、計画の最適化が有効な場合に対応していないマスター計画をトリガーしました* のようなメッセージが表示される場合があります。

**修正**:組み込みの Supply Chain Management プラン エンジンに対して作成されたすべてのマスター計画バッチ ジョブをキャンセルします。

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>計画の最適化の結果が、以前の結果とは異なる

計画の最適化は、一部の領域における組み込みマスタープランのデザインとは異なります。 また、保留されている機能が原因で発生することもあります。

**修正** : [分析計画の最適化] を実行して結果を分析し、関連ドキュメントを参照して影響を理解してください。 詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a>マスター計画では、補充タイム フェンスを考慮しません

これは、最適化の計画の保留中の機能が原因で発生します。

**修正**: 保留機能が利用できるようになるまで、計画された注文をフィルター処理または削除して、補充タイムフェンス以外からの提案を削除します。

## <a name="cant-enable-planning-optimization"></a>計画の最適化を有効化できない

**計画の最適化** を使用する設定を **はい** にする前に、**接続ステータス** を **接続済** とする必要があります。 詳細については、[計画の最適化を開始する](get-started.md) を参照してください。

**修正** : 計画最適化アドインが正常にインストールされていることを確認してください。

## <a name="error-message-is-shown-during-ctp"></a>CTP の実行中にエラーメッセージが表示される

計画の最適化が有効化されているときに、販売注文から生産可能在庫量 (CTP)を実行しようとすると、次のようなエラーメッセージが表示されます : *この操作は、プランニングの最適化が有効な場合に対応していないマスター計画をトリガーしました*。

これは、製造オーダー サポートの一環として計画されている保留機能に関連しています。

**修正 :** 計画の最適化を有効にしている場合は、CTP サポートが利用できるようになるまでは、CTP の計算を回避します。

## <a name="additional-resources"></a>追加リソース

[計画最適化の開始](get-started.md)

[計画最適化適合分析](planning-optimization-fit-analysis.md)
