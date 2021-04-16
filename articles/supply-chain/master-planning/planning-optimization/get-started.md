---
title: 計画の最適化の使用を開始する
description: このトピックでは、計画の最適化機能の使用を開始する方法について説明します。
author: ChristianRytt
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e85c18e548d82b2a369a1e8a5573800067b1935c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808067"
---
# <a name="get-started-with-planning-optimization"></a>計画最適化の開始

[!include [banner](../../includes/banner.md)]

[すでに発表した](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) ように、計画の最適化は、既存の組み込みマスター プラン エンジンと置き換えるようにスケジュールされています。

現在、組み込みのマスター プラン エンジンを使用している場合は、すぐに計画の最適化への移行の計画を開始する必要があります。 廃止が適用されると操作が影響を受ける可能性があるため、移行プロセスをすぐに開始することが重要です。 廃止が実施された場合に、最新の問題を回避するために、2020 年 12 月 1 日までに移行を完了することを強くお勧めします。 

現時点では、計画の最適化機能では、Supply Chain Management に組み込まれている計画エンジンで利用可能なすべての機能がサポートされていません。 したがって、計画の最適化で現在利用可能な機能セットが要件を満たすかどうかを評価することが重要です。 現在、計画の最適化機能は Dynamics Lifecycle Services (LCS) で既定では有効になっていないため、機能を有効にする前に評価を行う機会があります。

> [!NOTE]
> マスター プラン プロセスに製造が含まれていない (マスター プランで生成された計画製造オーダー) 場合や、バージョン 10.0.15 以降の組み込みマスター プラン エンジンが必要な場合は、移行から計画の最適化に例外を要求する必要があります。 バージョン 10.0.16 以降、計画製造オーダーを生成せずに組み込みマスター プランを実行すると、環境にエラーが表示されます。 計画製造オーダーは、マスター プラン中に計画製造オーダーを生成しないすべての新しい配置に対して使用する必要があります。 計画製造オーダーを生成せずに組み込みマスター プラン エンジンを実行している既存の環境の所有者は、例外プロセスに関する詳細を含むメールを受信します。 パートナーと協力して、計画の最適化への移行を評価および計画することをお勧めします。

計画の最適化を有効にする前に、計画の最適化フィット分析の結果を評価することを強くお勧めします。 詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。

## <a name="availability"></a>使用可能性

計画の最適化はは現在、次の Azure の地域で利用可能です: 米国、カナダ、ヨーロッパ、英国、オーストラリア、アジア太平洋。 他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。

計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。

## <a name="licensing"></a>ライセンス

現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。

## <a name="install-and-enable-planning-optimization"></a>計画最適化をインストールまたは有効化できない

計画最適化を使用するには、すべての前提条件をシステムに設定し、ライセンス キーを有効にして、計画の最適化アドインをインストールする必要があります Dynamics 365 Supply Chain Management。

### <a name="prerequisites"></a>必要条件

計画最適化アドインをインストールする前に、次の前提条件を満たす必要があります。

- LCS が有効になっている高可用性環境の tier 2 またはそれ以降 (OneBox 環境ではなく)、Dynamics 365 Supply Chain Management バージョン 10.0.7 またはそれ以降で Supply Chain Management を実行する必要があります。 このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。

- システムは Power Platform 統合用に設定されている必要があります。 詳細については、[アドインを設定するための前提条件](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) および [アドインの設定](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins) を参照してください。

### <a name="enable-the-planning-optimization-license"></a>計画最適化ライセンスを有効化する

計画最適化を使用するには、構成キーを有効にする必要があります。 そのためには次の作業を行います。

1. [メンテナンス モード](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。
1. **システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。
1. **構成 キー** タブで、**計画最適化** のチェック ボックス をオンにします。
1. [メンテナンス モード](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。

### <a name="install-the-planning-optimization-add-in"></a>計画最適化アドインをインストールする

LCS プロジェクトからアドインをインストールし、Supply Chain Management ユーザー インターフェイスから計画最適化の機能を有効にすることができます。

計画最適化アドインをインストールするには:

1. LCS にサインインし、目的の環境を開きます。
1. **完全な詳細** に移動します。
1. **環境アドイン** クイック タブまで下にスクロールします。
1. **新しいアドインのインストール** を選択します。
1. **計画の最適化** を選択します。
1. インストール ガイドに従って、契約条件に同意します。
1. **インストール** を選択します。
1. **環境アドイン** クイック タブに、計画最適化がインストールされていることを確認する必要があります。
1. 数分後、**インストールしています** が **インストール済み** に変わります (ページを更新する必要があります)。 インストールすると、Dynamics 365 Supply Chain Management で計画最適化を有効にする準備が整います。

計画最適化アドインをインストールする主な目的は、サービスと環境をつなげることです。 したがって、環境間で移動したコードに関係なく、計画の最適化を使用する環境ごとにアドインを個別にインストールする必要があります。

## <a name="integrate-planning-optimization-with-your-system"></a>システムとの計画最適化を統合する

計画の最適化アドインをマスター プランに使用するかどうかを構成するには、**マスター プラン** \> **セットアップ** \> **計画最適化パラメーター** の順に進みます。

### <a name="connection-status"></a>接続状態

接続ステータスは、Supply Chain Management と計画の最適化サービスとの間の接続の現在のステータスを示します。 次の表は、使用可能な値を示しています。

| 接続状態 | 説明 | 計画の最適化は使用できますか? |
|---|---|---|
| 接続済 | 計画の最適化サービスと Supply Chain Management の間に接続が確立されています。 | はい |
| 接続の有効化 | 計画の最適化サービスへの接続を有効にする要求が現在進行中です。 | いいえ |
| 接続解除済 | 計画の最適化サービスへの接続はありません。 このトピックで前述されているように、LCS から接続をオンにすることができます。 | いいえ |
| 接続を無効にしています | 計画の最適化サービスへの接続をオフにする要求が現在進行中です。 | いいえ |
| 状態を取得しています | システムは、計画の最適化サービスからのステータス情報を待機しています。 | いいえ |

### <a name="the-use-planning-optimization-option"></a>計画の最適化の使用オプション

**計画の最適化の使用** オプションの設定では、マスター プランに使用する計画エンジンを決定します。

- **はい** – 計画の最適化がマスター プランに使用されます。
- **いいえ** – 組み込み Supply Chain Management 計画エンジンがマスター プランに使用されます。

> [!NOTE]
> **計画の最適化の使用** オプションが **はい** に設定されているときに、組み込みの Supply Chain Management 計画エンジンに対して作成された既存の計画バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。

### <a name="integration-with-the-setup"></a>設定との統合

計画の最適化が有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。 この場合、マスター プランの結果と機能が影響を受けます。

## <a name="additional-resources"></a>追加リソース

[プレビュー用の使用条件](https://go.microsoft.com/fwlink/?linkid=2015274)

[計画最適化の概要](planning-optimization-overview.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[プランへのフィルターの適用](plan-filters.md)

[計画ジョブのキャンセル](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]