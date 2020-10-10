---
title: 計画の最適化の使用を開始する
description: このトピックでは、計画の最適化機能の使用を開始する方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887267"
---
# <a name="get-started-with-planning-optimization"></a>計画の最適化の使用を開始する

[!include [banner](../../includes/banner.md)]

現時点では、計画の最適化機能では、Microsoft Dynamics 365 Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。 したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。 既定では、Dynamics Lifecycle Services (LCS) で、計画の最適化機能は有効になっていません。 したがって、オンにする前に評価を行う機会があります。

最終的に、既存の組み込み Supply Chain Management 計画エンジンは、計画の最適化によって置き換えられます。

計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。 詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。

### <a name="availability"></a>使用可能性
計画の最適化はは現在、次の Azure の地域で利用可能です：米国、カナダ、ヨーロッパ、英国、オーストラリア。 他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。

計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。

### <a name="licensing"></a>ライセンス

現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。

### <a name="install-the-add-in"></a>アドインのインストール

計画の最適化を使用するには、Dynamics 365 Supply Chain Management 用の計画の最適化アドインをインストールします。 LCS プロジェクトからアドインにアクセスし、Supply Chain Management ユーザーインターフェイス (UI) から計画の最適化機能を有効にすることができます。

> [!NOTE]
> 計画最適化の要件は、LCS が有効になっている高可用性環境の tier 2 またはそれ以降で、(OneBox 環境ではなく) Dynamics 365 Supply Chain Management バージョン 10.0.7 、またはそれ以降です。 このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。

1. LCS にサインインし、目的の環境を開きます。
1. **完全な詳細**に移動します。
1. **環境アドイン** クイック タブまで下にスクロールします。
1. **新しいアドインのインストール**を選択します。
1. **計画の最適化**を選択します。
1. インストール ガイドに従って、契約条件に同意します。
1. **インストール**を選択します。
1. **環境アドイン** クイック タブに、計画最適化がインストールされていることを確認する必要があります。
1. 数分後、**インストールしています**が**インストール済み**に変わります (ページを更新する必要があります)。 インストールすると、Dynamics 365 Supply Chain Management で計画最適化を有効にする準備が整います。

### <a name="planning-optimization-integration"></a>計画の最適化の統合

計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画最適化パラメーター**の順に進みます。

#### <a name="connection-status"></a>接続状態

接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。 次の表は、使用可能な値を示しています。

| 接続状態 | 説明 | 計画の最適化は使用できますか? |
|---|---|---|
| 接続済 | 計画の最適化サービスと Supply Chain Management の間に接続が確立されています。 | はい |
| 接続の有効化 | 計画の最適化サービスへの接続を有効にする要求が現在進行中です。 | いいえ |
| 接続解除済 | 計画の最適化サービスへの接続はありません。 このトピックで前述されているように、LCS から接続をオンにすることができます。 | いいえ |
| 接続を無効にしています | 計画の最適化サービスへの接続をオフにする要求が現在進行中です。 | いいえ |
| 状態を取得しています | システムは、計画の最適化サービスからのステータス情報を待機しています。 | いいえ |

#### <a name="the-use-planning-optimization-option"></a>計画の最適化の使用オプション

**計画の最適化の使用**オプションの設定では、マスター プランに使用する計画エンジンを決定します。

- **はい** – 計画の最適化がマスター プランに使用されます。
- **いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。

> [!NOTE]
> **計画の最適化の使用**オプションが**はい**に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。

### <a name="integration-with-the-setup"></a>設定との統合

計画の最適化のプレビューが有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。 この場合、マスター プランの結果と機能が影響を受けます。

## <a name="additional-resources"></a>追加リソース

[プレビュー用の使用条件](https://go.microsoft.com/fwlink/?linkid=2015274)

[計画最適化の概要](planning-optimization-overview.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[プランへのフィルターの適用](plan-filters.md)

[計画ジョブのキャンセル](cancel-planning-job.md)
