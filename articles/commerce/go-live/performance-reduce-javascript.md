---
title: 使用されていないモジュールを除外して JavaScript を削減する
description: このトピックでは、Microsoft Dynamics 365 Commerce 実装で使用される JavaScript の量を減らすことでパフォーマンスを向上させる方法について説明します。
author: mssle
ms.date: 01/28/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: sheaton
ms.search.validFrom: 2021-09-20
ms.openlocfilehash: d282d330b6992ef58f6b8dd137a86cf53b9ec76b
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100786"
---
# <a name="reduce-javascript-by-excluding-unused-modules"></a>使用されていないモジュールを除外して JavaScript を削減する

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 実装で使用される JavaScript の量を減らすことでパフォーマンスを向上させる方法について説明します。

Dynamics 365 Commerce には、Commerce [モジュール ライブラリ](../starter-kit-overview.md) と呼ばれる大規模なモジュール セットが含まれています。 電子コマース サイトで使用しないモジュールがある場合は、そのモジュールを除外して JavaScript のチャンク サイズを減らすることができます。 除外したモジュールは、実電子コマース サイトには表示されません。 ページを作成すると、Commerce サイト ビルダーでもこれらの情報を使用できません。

## <a name="applies-to"></a>適用先

このトピックは、次の構成に適用されます。

- **バージョン:** Commerce 10.0.16 またはそれ以降
- **コンポーネント:** 企業 とコンシューマー (B2C) または企業間 (B2B)
- **機能領域:** Commerce Web サイト パフォーマンス

## <a name="prerequisites"></a>必要条件

Dynamics 365 Commerce オンライン ソフトウェアの開発キット (SDK) をインストールします。 詳細については、[オンライン SDK をインストール](../dev-itpro/ecommerce-platform-sdk.md) を参照してください。

## <a name="steps-to-reduce-javascript"></a>JavaScript を削減するための手順

未使用のモジュールを除外するには、手順に従いモジュール名を SDK の **platform.settings.json** ファイル (/src/settings/platform.settings.json) の **excludeModules** プロパティに追加します。

1. Windows Command Prompt ウィンドウを開きます。
1. SDK インストールの場所で、**/src/settings** ディレクトリに移動します。
1. テキスト エディタで **platform.settings.json** ファイルを開きます。
1. 次のコードを JavaScript Object Notation (JAVA) 形式で挿入します。 除外するモジュール名で **\<EXCLUDED\_MODULE\_NAME...\>** を置換ます。 各モジュール名は、二重引用符で囲む必要があります。 複数のモジュールを除外する場合は、モジュール名をコンマで区切ります。

    ```json
    {
        "excludedModules": ["<EXCLUDED_MODULE_NAME1>","<EXCLUDED_MODULE_NAME2>"]
    }
    ```

## <a name="validate"></a>検証

モジュールが正常に除外されたことを検証するには、次のいずれかの方法または両方を使用します。

### <a name="method-1"></a>メソッド 1

- **説明または目的:** モジュールが正常に除外されたことを確認します。
- **実行する手順:** ビルド後に表示されるサイズを比較します。
- **合格の結果:** 新しいビルドを行った後は、チャンク サイズは小さくなります。

### <a name="method-2"></a>メソッド 2

- **説明または目的:** モジュールが正常に除外されたことを確認します。
- **実行手順:** これらの手順で、開発環境のモジュールをテストします。

    1. **yarn start** コマンドで、ノード サーバーを実行します。
    1. 次の URL: `http://localhost:4000/modules?type=<YOUR-MODULE-NAME>` を参照してください。

- **合格結果:** 除外したモジュールは Web ページに表示されません。

## <a name="additional-resources"></a>追加リソース

[オンライン SDK をインストール](../dev-itpro/ecommerce-platform-sdk.md)

[開発環境の設定](../e-commerce-extensibility/setup-dev-environment.md)
