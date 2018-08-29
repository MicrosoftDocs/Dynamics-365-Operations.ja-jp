---
title: "Retail と Finance and Operations のビルド システムのマージ"
description: "この記事では、Visual Studio Team Services を使用して Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail のビルド システムをマージするステップについて説明します。"
author: andreash1
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: andreash
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: a35c4eb7259fda7ffb42a5802aa76bd168895298
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="merge-the-build-systems-for-retail-and-finance-and-operations"></a>Retail と Finance and Operations のビルド システムのマージ

[!include [banner](../../includes/banner.md)]

この記事では、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail のビルド システムをマージするステップについて説明します。 Lifecycle Services (LCS) に統合されたビルド エクスペリエンスは、コードのアップグレードと新しいプロジェクトの両方をサポートします。 Retail SDK は、自己完結型の MSBuild ベースのビルド システムです。 多くのカスタマイザーは、Microsoft Dynamics 365 for Finance and Operations および Retail の両方のコンポーネントに生産的な変更を加えます。 この記事では、Visual Studio Team Services を使用して両方のビルド システムをマージするための手動のステップを概説します。 

## <a name="enable-the-build-system"></a>ビルド システムの有効化

開始するには、すべてのステップを実行して、完全な連続ビルド システムを稼働させる必要があります。 詳細については、[継続的ビルドとテストの自動化を使用した開発者トポロジの展開](../../../dev-itpro/perf-test/continuous-build-test-automation.md) を参照してください。 配置した後、ビルド定義とビルド ステップを作成します。 それをよく理解してエラーなしでビルドできるように、少なくとも 1 回はビルドしてください。 その後、次の手順に移ります。

## <a name="prepare-the-retail-sdk"></a>Retail SDK を準備します。
### <a name="getting-the-retail-sdk"></a>Retail SDK の取得
同じ Microsoft Visual Studio チーム サービス (VSTS) プロジェクトで Retail ソフトウェア開発キット (SDK) がない場合は、ここで追加します。 どの開発者トポロジまたはビルド トポロジでも、Retail SDK が存在します。 [Retail SDK の概要](retail-sdk-overview.md) の分岐ドキュメントに従います。 この時点で、Retail SDK ミラーと Retail SDK カスタマイズ分岐を作成することをお勧めします。 Retail SDK カスタマイズ分岐が準備できた後、Retail と同じ VSTS プロジェクトで送信され開始できます。

## <a name="add-a-repository-mapping-for-the-retail-sdk"></a>Retail SDK のレポジトリ マッピングを追加します。
Retail SDK の場所が含まれるように、ビルド定義を編集します。 (つまり、マップを追加します。) [![Retail SDK のリポジトリ マッピングを追加](./media/build-map-addition.png)](./media/build-map-addition.png)

## <a name="add-a-new-build-step-to-build-the-retail-sdk"></a>Retail SDKを構築するための新しいビルド ステップの追加
次のスクリーン ショットに示すように、ビルド パイプラインの先頭に新しいステップを追加します。 [![小売 SDK を構築するための新しいビルド ステップの追加](./media/new-build-step-1024x527.png)](./media/new-build-step.png)

## <a name="add-a-copy-step-for-binaries-from-the-retail-sdk-to-the-retail--build"></a>Retail SDK から Retail ビルドにバイナリのコピー ステップの追加
このビルド ステップでは、Microsoft がファイル/バイナリを共有する場合、Microsoft は Retail bin フォルダに最新の構築済みRetail バイナリをコピーできます。 前のセクションで説明したように、Retail SDK のビルド ステップを追加した直後にこのステップを完了することを確認します。 [![小売 SDK から小売ビルドの Dynamics 365 へのバイナリのコピー ステップの追加](./media/binary-drop-to-ax.png)](./media/binary-drop-to-ax.png)

## <a name="add-a-copy-step-for-all-retail-packages"></a>すべての Retail パッケージのコピー ステップの追加
このステップが「PowerShell: パッケージの生成」ステップ後に発生することを確認します (以下の図を参照してください)。 その引数を次に示します。

    -BuildPackagePath "$(Agent.BuildDirectory)\Packages" -BuildVersion "$(Build.BuildNumber)"

[![すべての小売パッケージのコピー ステップの追加](./media/package-drop-1024x473.png)](./media/package-drop.png)

## <a name="optional-referencing-a-retail-dll-from-retail"></a>オプション: Retail から Retail DLL を参照します。
構築済み Retail バイナリを小売パッケージに追加する必要がある場合にのみ、このタスクを完了する必要があります。 この場合、これら 3 つの手順に従う必要があります。

1.  小売プロジェクトでは通常の AXReference を使用します。
2.  VSTS に、対応する AXReference フォルダーとその中の XML ファイルを追加します。
3.  Copy-RetailBinaries.ps1 ファイルを適切なファイル コマンドで更新し、バイナリ ファイルを Retail SDK から Retail bin フォルダーに取得します。 Microsoft Windows PowerShell ファイルには、ApplicationSuite bin フォルダーに PricingEngine.dll ファイルをコピーするサンプルが含まれます。 ビルドしているモジュールによっては、ファイルとフォルダーが異なる場所にあるように変更する必要があります。

