---
title: 画像の最適化
description: このトピックでは、Microsoft Dynamics 365 Commerce で使用する画像を最適化して Web サイトのパフォーマンスを向上させる方法について説明します。
author: mssle
ms.date: 01/28/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: sheaton
ms.search.validFrom: 2021-09-20
ms.openlocfilehash: 15b1fcdd884d8e1207ea118b8da4fb4fe1233dd9
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100785"
---
# <a name="optimize-images"></a>画像の最適化

[!include[banner](../includes/banner.md)]

このトピックでは、更新または移動プロセス中に Microsoft Dynamics 365 Commerce で使用する画像を最適化して Web サイトのパフォーマンスを向上させる方法について説明します。

## <a name="applies-to"></a>適用先

このトピックは、次の構成に適用されます。

- **バージョン:** Commerce 10.0.16 またはそれ以降
- **コンポーネント:** 企業 とコンシューマー (B2C) または企業間 (B2B)
- **機能領域:** Commerce Web サイト パフォーマンス

## <a name="prerequisites"></a>必要条件

Dynamics 365 Commerce オンライン ソフトウェアの開発キット (SDK) をインストールします。 詳細については、[オンライン SDK をインストール](../dev-itpro/ecommerce-platform-sdk.md) を参照してください。

## <a name="steps-to-optimize-images"></a>画像を最適化するための手順

Web ページの最大パフォーマンス ヒットの 1 つが、画像をダウンロードするときに発生する場合があります。 画像のサイズを小さくし、Web サイトの実際のパフォーマンスおよび認識されるパフォーマンスを改善するには、次の手順に従います。

1. Casing Style Sheets (CSS) を使用し、できる限りボタンなどのアイテムのイメージを生成します。
1. 高い品質/高解像度のマーケティング画像または製品画像を、Commerce サイト ビルダー[メディア ライブラリ](../dam-overview.md) にアップロードします。 イメージのサイズ変更者は、レンダリング中に自動的に使用されます。
1. 各画像の幅および高さプロパティが含まれます。

    1. 画像を使用する各モジュールについては、SDK インストールの場所の **/src/settings** ディレクトリから **theme.settings.json** ファイルを開きます。
    1. 更新するモジュールを検索します。
    1. 画像プロパティに幅と高さのパラメータを含む必要があります。 詳細については、[テーマ設定を構成する](../e-commerce-extensibility/configure-theme-settings.md) を参照してください。

1. 画像の負荷開始を無効にします。

    1. Commerce サイト ビルダーを開きます。
    1. 読み込まれるはずの画像を含むモジュールに移動します。
    1. 製品収集モジュールの場合は、**モジュールの遅延読み込みを有効化** チェックボックスを解除します。 その他のモジュールについては、**遅延読み込みを無効化** チェックボックスを選びます。
    1. コンテンツを保存、プレビュー、および公開します。

## <a name="validate"></a>検証

画像の使用が最適化された場合に、次の方法を使用して検証します。

- **説明または目的:** ページ パフォーマンスを検証します。
- **実行する手順:** 画像を最適化する前と後にパフォーマンス テストを実行します。
- **結果を渡す:** イメージを最適化するとパフォーマンスが向上します。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 開発のベスト プラクティス](../e-commerce-extensibility/best-practices-dev.md)
