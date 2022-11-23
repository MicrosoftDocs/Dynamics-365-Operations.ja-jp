---
title: マスター プランを開始する
description: この記事では、Dynamics 365 Supply Chain Management でマスター プラン機能の使用を開始する方法について説明します。
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780412"
---
# <a name="get-started-with-master-planning"></a>マスター プランを開始する

[!include [banner](../../includes/banner.md)]

Supply Chain Management のマスタ プランは、Dynamics 365 Supply Chain Management 向け計画の最適化アドインと呼ばれる外部サービスによって提供されます。 このトピックでは、そのサービスを取得および設定する方法について説明します。

## <a name="availability"></a>使用可能性

計画の最適化は現在、次の Azure の地域で利用可能です: 米国、カナダ、ブラジル、ヨーロッパ、フランス、英国、ノルウェー、スイス、オーストラリア、アジア太平洋、日本、およびインド。 他の地域からのアドインをインストールしようとすると、LCS ではこの地理的領域には対応していない旨のメッセージを表示します。 Azure の地域および関連地域の詳細については、[Azure](https://azure.microsoft.com/global-infrastructure/geographies/#geographies) の地域 を参照してください。

計画の最適化では、 Dynamics 365 Supply Chain Management の社内設置型の配置に対応していないことに注意してください。

## <a name="licensing"></a>ライセンス

現在のライセンスを使用してマスター プランを実行できる場合は、計画の最適化の使用を開始するために追加のライセンスを購入する必要はありません。

## <a name="install-and-enable-planning-optimization"></a>計画最適化をインストールまたは有効化できない

計画最適化を使用するには、すべての前提条件をシステムに設定し、ライセンス キーを有効にして、計画の最適化アドインをインストールする必要があります Dynamics 365 Supply Chain Management。

### <a name="prerequisites"></a>必要条件

計画最適化アドインをインストールする前に、次の前提条件を満たす必要があります。

- LCS が有効になっている高可用性環境の tier 2 またはそれ以降 (OneBox 環境ではなく)、Dynamics 365 Supply Chain Management バージョン 10.0.7 またはそれ以降で Supply Chain Management を実行する必要があります。 このアドインを OneBox 環境にインストールはできません。インストール処理をキャンセルする必要があります。

- システムは Power Platform 統合用に設定されている必要があります。 詳細については、[Microsoft Power Platform と財務と運用アプリの統合](../../../fin-ops-core/dev-itpro/power-platform/overview.md)を参照してください。

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
| 接続解除済 | 計画の最適化サービスへの接続はありません。 この記事で前述されているように、LCS から接続をオンにすることができます。 | 無効 |
| 接続を無効にしています | 計画の最適化サービスへの接続をオフにする要求が現在進行中です。 | いいえ |
| 状態を取得しています | システムは、計画の最適化サービスからのステータス情報を待機しています。 | いいえ |

### <a name="the-use-planning-optimization-option"></a>計画の最適化の使用オプション

**計画の最適化の使用** オプションの設定では、マスター プランに使用する計画エンジンを決定します。

- **はい** – 計画の最適化がマスター プランに使用されます。
- **いいえ** – 非推奨のマスター プラン エンジンがマスター プランに使用されます。

この設定は、すべての法人 (会社) に適用されます。 一部の法人およびその他の法人の非推奨のマスター プラン エンジンで、計画の最適化を使用することはできません。

> [!NOTE]
> **計画の最適化の使用** オプションが **はい** に設定されているときに、非推奨のマスター プラン エンジンに対して作成された既存のプラン バッチ ジョブがトリガーされた場合、これらのジョブは失敗します。

### <a name="integration-with-the-setup"></a>設定との統合

計画の最適化が有効になっている場合は、計画の最適化アドインを使用してマスター プランが実行されます。 この場合、マスター プランの結果と機能が影響を受けます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
