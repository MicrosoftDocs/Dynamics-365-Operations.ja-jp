---
title: 原価会計の使用を開始する (プライベート プレビュー)
description: このトピックでは、原価計算サービスのライセンスの詳細とインストール手順を説明します。
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: b6756e3745aa4596bd5d63ad15aaf4385cfc4813
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813198"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>原価会計の使用を開始する (プライベート プレビュー)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> このトピックに記載されている機能は、プライベート プレビュー リリースの一部として提供されます。 このトピックの内容や記載されている機能は変更される可能性があります。 プレビュー リリースの詳細については、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。

原価会計サービスを利用することで、設定した原価計算台帳の中で複数の 棚卸し会計を行うことができます。 各原価計算台帳を *規則* に関連付けます。 規則とは、次のタイプの会計ポリシーの集合です。

- 原価オブジェクト
- 入力測定基準
- 原価フロー仮定
- 原価要素

> [!NOTE]
> 原価会計サービスを有効にした後でも、通常、Microsoft Dynamics 365 Supply Chain Management では棚卸し会計を行うことができます。

原価計算サービスはアドインです。 この機能を使用できるようにするには、Microsoft Dynamics Lifecycle Services (LCS) からインストールする必要があります。 したがって、本番環境で有効にする前に、テスト環境で評価することを選択できます。

現在原価会計サービスは、Dynamics 365 Supply Chain Management に組み込まれているすべての原価管理機能に対応していません。 したがって、現在使用可能な一連の機能が要件を満たすかどうかを評価することが重要となります。

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>原価会計サービスの取得方法 (プライベート プレビュー)

> [!IMPORTANT]
> 原価会計サービスを使用するには、(ワンボックス環境ではなく) LCSを有効にした高可用性環境を用意する必要があります。また、Dynamics 365 Supply Chain Management バージョン 10.0.11 またはそれ以降を実行する必要があります。

原価計算サービスのプライベート プレビューに登録するには、LCS 環境の ID を[原価計算サービス (プライベートプレビュー) ](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29)に電子メールで送信してください。 プログラムの承認時に、原価計算サービスのベータキーを含む電子メールの追跡を送信します。 ベータ キーを受け取ったら、[アドインをインストール](#install)して続行可能です。

## <a name="licensing"></a>ライセンス

原価会計サービスは、Supply Chain Management に使用できる棚卸し会計の標準機能と共にライセンス供与されます。 原価会計サービスの使用にあたっては、追加のライセンスを購入する必要はありません。

## <a name="install-the-add-in"></a><a name="install"></a>アドインのインストール

原価計算サービスを使用するには、次の手順に従って、Supply Chain Management 用の原価計算サービス アドインをインストールします。

1. 原価会計サービス (プライベート プレビュー) に[登録](#sign-up)します。

1. LCS にサインインします。

1. **プレビュー機能管理** に移動します。

1. プラス記号 (**+**) を選択してください。

1. **コード** フィールドに、原価会計サービス用のアドインのベータキーを入力します。 （事前にキーを電子メールで受け取っている必要があります）

1. **ブロック解除** を選択します。

1. サービスを追加する LCS 環境を開きます。

1. **完全な詳細** に移動します。

1. **環境アドイン** クイック タブまで下にスクロールします。

1. **新しいアドインのインストール** を選択します。

1. **原価会計サービス** を選択します。

1. インストール ガイドに従って、契約条件に同意します。

1. **インストール** を選択します。

1. **環境アドイン** クイックタブに、原価会計サービスがインストールされていることを確認します。 数分後、状態が **インストール中** から **インストール済** に変わります。 （この変更を表示するには、ページを更新する必要がある場合があります）その時点で、原価会計サービスを使用する準備が整います。

## <a name="set-up-the-integration"></a>統合を設定する

原価会計サービスと Dynamics 365 Supply Chain Management の統合を設定するには、次の操作を行います。

1. **システム管理 > 機能管理** の順に移動します。

1. **更新プログラムの確認** を選択します。

1. **すべて** タブを開き、*原価会計サービス* という機能を検索します。

1. **直ちに有効化** を選択します。

1. **原価管理 > 原価会計サービス > 設定 > 原価計算サービスパラメータ > 統合パラメータ** へと移動します。

1. **アプリケーション ID**  フィールドに、次のコードを入力します。<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. **データ サービス エンドポイント** フィールドに次の URL を入力します。<br>https://operationsdataservice.operations365.dynamics.com/

1. **原価会計サービス エンドポイント** フィールドに次の URL を入力します。<br>https://costaccountingservice.operations365.dynamics.com/

1. 以上で、原価会計サービスを使用する準備が整いました。

## <a name="related-resources"></a>関連するリソース

[原価会計サービス ホーム ページ](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]