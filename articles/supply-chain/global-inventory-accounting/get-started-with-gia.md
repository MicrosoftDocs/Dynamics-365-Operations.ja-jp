---
title: グローバル在庫会計の使用を開始する
description: このトピックでは、グローバル在庫会計の使用を開始する方法について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88f1e9ef8c8b2aa494c44ea3b33713adc470eb96
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384800"
---
# <a name="get-started-with-global-inventory-accounting"></a>グローバル在庫会計の使用を開始する

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

グローバル在庫会計を利用することで、設定したグローバル在庫会計元帳の中で複数の在庫会計を行うことができます。 各グローバル在庫会計元帳を *規則* に関連付ける必要があります。 規則とは、次のタイプの会計ポリシーの集合です。

- 原価オブジェクト
- 入力測定基準
- 原価フロー仮定
- 原価要素

> [!NOTE]
> グローバル在庫会計を有効にした後でも、通常の方法で Microsoft Dynamics 365 Supply Chain Management で在庫会計を行うことができます。

グローバル在庫会計はアドインです。 この機能を使用できるようにするには、Microsoft Dynamics Lifecycle Services (LCS) からインストールする必要があります。 本番環境で有効にする前に、テスト環境で評価することを選択できます。

グローバル在庫会計は、Supply Chain Management に組み込まれているすべての原価管理機能に対応していません。 したがって、現在使用可能な一連の機能が要件を満たすかどうかを評価することが重要となります。

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>グローバル在庫会計のパブリック プレビューの取得方法

> [!IMPORTANT]
> グローバル在庫会計を使用するには、LCS が有効になっている高可用性環境 (OneBox 環境ではない) が必要です。 また、Supply Chain Management バージョン 10.0.19 以降を実行している必要があります。

グローバル在庫会計パブリック プレビューにサインアップするには、[グローバル在庫会計チーム](mailto:GlobalInvAccount@microsoft.com)に電子メールで LCS 環境 ID を送信します。 プログラムに承認された後、チームはグローバル在庫会計ベータ キーおよびサービス エンドポイントを含むフォローアップ電子メールを送信します。 ベータ キーを受信した後に、[アドインをインストール](#install)できます。

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

### <a name="set-up-dataverse"></a>Dataverse を設定する

Dataverse を設定する前に、次の手順に従って、グローバル在庫会計サービス プリンシプルをテナントに追加します。

1. [Graph 用 Azure Active Directory PowerShell をインストールする](/powershell/azure/active-directory/install-adv2)に記載の手順に従って Windows PowerShell v2 用 Azure AD モジュールをインストールします。
1. 次の PowerShell コマンドを実行します。

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

次に、次の手順に従って、Dataverse でグローバル在庫会計用のアプリケーション ユーザーを作成します。

1. Dataverse 環境の URLを開きます。
1. **詳細設定 \> システム \> セキュリティ \> ユーザー** の順に移動し、アプリケーション ユーザーを作成します。 **表示** フィールドを使用して、ページ ビューを *アプリケーション ユーザー* に変更します。
1. **新規** を選択します。
1. **アプリケーション ID** を *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* に設定します。
1. **ロールの割り当て** を選択してから、*システム管理者* を選択します。 *Common Data Service ユーザー* という名前のロールがある場合は、それも選択します。
1. 上記の手順を繰り返しますが、**アプリケーション ID** フィールドは *5f58fc56-0202-49a8-ac9e-0946b049718b* に設定します。

詳細については、「[アプリケーション ユーザーの作成](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)」を参照してください。

Dataverse インストールの既定の言語が英語ではない場合、次の手順に従います。

1. **詳細設定 \> 管理 \> 言語** に移動します。
1. *英語* (*LanguageCode=1033*) を選択し、**適用** を選択します。

## <a name="install-the-add-in"></a><a name="install"></a>アドインのインストール

グローバル在庫会計を使用できるようにするには、以下の手順に従ってアドインをインストールします。

1. グローバル在庫会計のパブリック プレビューへの[サインアップ](#sign-up)。
1. [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。
1. **プレビュー機能管理** に移動します。
1. プラス記号 (**+**) を選択してください。
1. **コード** フィールドに、グローバル在庫会計用のアドイン ベータ キーを入力します。 (サインアップ時に電子メールでベータ キーを受け取っている必要があります。)
1. **ブロック解除** を選択します。
1. サービスを追加する LCS 環境を開きます。
1. **完全な詳細** に移動します。
1. **Power Platform 統合** に移動し、**設定** を選択します。
1. **Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、**設定** を選択します。 通常、設定には 60分 から 90分かかります。
1. Microsoft Power Platform 環境の設定が完了した後、**環境アドイン** クイックタブで、**新しいアドインをインストール** を選択します。
1. **グローバル在庫会計** を選択します。
1. インストール ガイドに従って、契約条件に同意します。
1. **インストール** を選択します。
1. **環境アドイン** クイックタブで、グローバル在庫会計がインストール中であることを確認できます。 数分後、状態が *インストール中* から *インストール済* に変わります。 (この変更を表示するには、ページを更新する必要がある場合があります。) その時点で、グローバル在庫会計を使用する準備が整っています。

## <a name="set-up-the-integration"></a>統合を設定する

以下の手順に従って、グローバル在庫会計と Supply Chain Management の統合を設定します。

1. Supply Chain Management にサインインします。
1. **システム管理 \> 機能管理** の順に移動します。
1. **更新プログラムの確認** を選択します。
1. **すべて** タブで、*(プレビュー) グローバル在庫会計* という名前の機能を検索します。
1. **直ちに有効化** を選択します。
1. **グローバル在庫会計 \> 設定 \> グローバル在庫会計パラメーター \> 統合パラメーター** に移動します。
1. **データ サービス エンドポイント** および **グローバル在庫会計エンドポイント** フィールドに、プレビューへのサインアップ時にグローバル在庫会計チームが送信した電子メールの URL を入力します。

グローバル在庫会計を使用する準備が整いました。
