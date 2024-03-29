---
title: グローバル在庫会計の使用を開始する
description: この記事では、グローバル在庫会計の使用を開始する方法について説明します。
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 463a66002ec7a6536c9ff829f9ea2c3734138eae
ms.sourcegitcommit: 6221a25f81aa83ab335de7cb6b6c3014dbec0116
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177151"
---
# <a name="get-started-with-global-inventory-accounting"></a>グローバル在庫会計の使用を開始する

[!include [banner](../includes/banner.md)]

グローバル在庫会計を利用することで、設定したグローバル在庫会計元帳の中で複数の在庫会計を行うことができます。 各グローバル在庫会計元帳を *規則* に関連付ける必要があります。 規則とは、次のタイプの会計ポリシーの集合です。

- 原価オブジェクト
- 入力測定基準
- 原価フロー仮定
- 原価要素

> [!NOTE]
> グローバル在庫会計を有効にした後でも、通常の方法で Microsoft Dynamics 365 Supply Chain Management で在庫会計を行うことができます。

グローバル在庫会計はアドインです。 この機能を使用できるようにするには、Microsoft Dynamics Lifecycle Services (LCS) からインストールする必要があります。 運用環境で有効にする前に、テスト環境で評価することを選択できます。

グローバル在庫会計は、Supply Chain Management に組み込まれているすべての原価管理機能に対応していません。 したがって、現在使用可能な一連の機能が要件を満たすかどうかを評価することが重要となります。

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>グローバル在庫会計アドインの取得方法

> [!IMPORTANT]
> グローバル在庫会計を使用するには、LCS が有効になっている高可用性環境 (OneBox 環境ではない) が必要です。 また、Supply Chain Management バージョン 10.0.19 以降を実行している必要があります。

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management バージョン 10.0.19 から 10.0.26

Supply Chain Management バージョン 10.0.19 から 10.0.26 のグローバル在庫会計をインストールするには、まず [アドインをインストール](#install) します。 その後、LCS 環境 ID と会社名をメールで [グローバル在庫会計チーム](mailto:GlobalInvAccount@microsoft.com) に送信します。 チームはグローバル在庫会計サービス エンドポイントを含むフォローアップ メールを送信します。

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management バージョン 10.0.27 以降

Supply Chain Management バージョン 10.0.27 以降のグローバル在庫会計をインストールするには、[アドインをインストール](#install) するだけです。 これらのバージョンの Supply Chain Management では、グローバル在庫会計サービス エンドポイントが自動的に設定されるため、手動で検索する必要はありません。 アドインの設定中に問題が発生する場合は、[グローバル在庫会計チーム](mailto:GlobalInvAccount@microsoft.com) に問い合わせください。

## <a name="licensing"></a>ライセンス

グローバル在庫会計は、Supply Chain Management に使用できる棚卸し会計の標準機能と共にライセンス供与されます。 グローバル在庫会計を使用するのに、追加のライセンスを購入する必要はありません。

## <a name="prerequisites"></a>必要条件

### <a name="set-up-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合の設定

アドイン機能を有効にする前に、次の手順に従って Microsoft Power Platform と統合する必要があります。

1. サービスを追加する LCS 環境を開きます。
1. **完全な詳細** に移動します。
1. **Power Platform の統合** セクションで、**設定** を選択します。
1. **Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、**設定** を選択します。 通常、設定には 60分 から 90分かかります。
1. Microsoft Power Platform 環境の設定が完了すると、環境の名前がページに表示されます。 また、**Power Platform 統合セクション** に、「Power Platform 環境の設定が完了しました」と表示されます。 グローバル在庫会計に、二重書き込みアプリケーションは必要ではありません。

詳細については、[環境のデプロイ後の有効化](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy)を参照してください。

## <a name="install-or-update-the-add-in-and-solution"></a><a name="install"></a> アドインおよびソリューションのインストールまたは更新

グローバル在庫会計アドインおよびソリューションをインストールまたは更新するには、次の手順に従います。 実行する手順の一部は、初めてインストールする場合なのか、既存のインストールにソリューションを更新する必要があるだけなのかによって異なります。

- 以前にアドインをインストールしたことがない場合、完全な手順に従って、アドインとソリューションの両方をインストールします。
- すでにグローバル在庫会計を使用しているが、[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)でソリューションを更新する必要がある場合、手順 6 のみを実行し、他のすべての手順をスキップします。

アドインおよびソリューションのインストールまたは更新を行う

1. [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
1. サービスを追加する LCS 環境を開きます。
1. **完全な詳細** に移動します。
1. **Power Platform 統合** に移動し、**設定** を選択します。
1. **Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、**設定** を選択します。 通常、設定には 60分 から 90分かかります。
1. Microsoft Power Platform 環境の設定が完了したら、[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)にログインし、次の手順に従ってグローバル在庫会計ソリューションのインストールまたは更新を行います。
   1. ソリューションのインストールまたは更新を行う環境を選択します。
   1. **Dynamics 365 アプリ** を選択します。
   1. **アプリをインストールする** を選択します。
   1. **Dynamics 365 グローバル在庫会計** を選択します。
   1. **次へ** を選択してインストールします。
1. ソリューションが完全にインストールされた後、LCS 環境に戻ります。 **環境アドイン** クイックタブで、**新しいアドインのインストール** を選択します。
1. **グローバル在庫会計** を選択します。
1. インストール ガイドに従って、契約条件に同意します。
1. **インストール** を選択します。
1. **環境アドイン** クイックタブで、グローバル在庫会計がインストール中であることを確認できます。 数分後、状態が *インストール中* から *インストール済* に変わります。 (この変更を表示するには、ページを更新する必要がある場合があります。) その時点で、グローバル在庫会計を使用する準備が整っています。

Dataverse インストールの既定の言語が英語ではない場合、次の手順に従います。

1. **詳細設定 \> 管理 \> 言語** に移動します。
1. *英語* (*LanguageCode=1033*) を選択し、**適用** を選択します。

## <a name="set-up-the-integration"></a>統合を設定する

以下の手順に従って、グローバル在庫会計と Supply Chain Management の統合を設定します。

1. Supply Chain Management にサインインします。
1. **システム管理 \> 機能管理** の順に移動します。
1. **更新プログラムの確認** を選択します。
1. **すべて** タブで、*(プレビュー) グローバル在庫会計* という名前の機能を検索します。
1. **直ちに有効化** を選択します。
1. **グローバル在庫会計 \> 設定 \> グローバル在庫会計パラメーター \> 統合パラメーター** に移動します。
1. 実行している Supply Chain Management のバージョンに応じて、次のいずれかの手順を実行します:
    - **Supply Chain Management バージョン 10.0.19 から 10.0.26**: **データ サービス エンドポイント** および **グローバル在庫会計エンドポイント** のフィールドで、グローバル在庫会計チームからメールで送信された URL を入力します ([グローバル在庫会計アドインの取得方法](#sign-up) も参照してください)。
    - **Supply Chain Management バージョン 10.0.27 以降**: エンドポイントを入力する必要はないので、この手順を省略できます。

グローバル在庫会計を使用する準備が整いました。
