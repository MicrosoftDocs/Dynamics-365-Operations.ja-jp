---
title: POS 拡張機能の使用を開始する
description: このトピックでは、販売時点管理 (POS) 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: intro-internal
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 1915417ec8b827644c3bf8b174c0702bdf281f5b2c307f2a4481614b3b4139a7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760862"
---
# <a name="getting-started-with-pos-extensions"></a>POS 拡張機能の使用を開始する

[!include [banner](../../includes/banner.md)]

このトピックでは、販売時点管理 (POS) 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

## <a name="independent-pos-extension-model"></a>独立した POS 拡張モデル

POS により SDK を使用した拡張機能が可能になります。 そのため、開発、配置、およびサービス拡張機能を独自に作成することができます。 拡張機能を作成した後、インストーラー パッケージを使用し、拡張機能を配置する拡張機能インストーラーを作成できます。 インストーラーは、拡張機能に対する変更または拡張が行われた後はべき等になります。 インストーラーを作成し、それを実行して拡張機能を配置するだけです。

拡張機能インストーラーは、コア POS インストーラーには依存しません。 これらは別個のもので、異なる方法でパッケージ化されます。 利点は、拡張機能およびコア POS のサービスを個別に提供できることです。 また、POS フレームワークでは複数の拡張機能インストーラーがサポートされます。 独立系ソフトウェア ベンダー (ISV)、パートナー、および顧客からの拡張機能は、すべて個別にインストールしてサービスを提供できます。

独立した POS 拡張モデルは Microsoft Dynamics 365 Commerce アプリケーションのバージョン 10.0.18 以降でサポートされています。 以前のバージョンでは、拡張機能とコア POS コードは 1 つのインストーラーとしてパッケージ化され、まとめてサービスが提供されています。 したがって、拡張機能の変更やコア POS の変更を個別に配置することはできません。

POS の独立した拡張モデルは、Modern POS (MPOS) および Cloud POS (CPOS) の POS 拡張フレームワーク用の Windows Optional パッケージ フレームワークを使用して、既成のコンポーネントから拡張されます。 Dynamics 365 Commerce の Store Commerce アプリ、iOS Hybrid アプリ、および Android Hybrid アプリは CPOS をホストするシェル (ラッパー) なので、他のアプリ タイプでは CPOS 拡張機能モデルが使用されます。

## <a name="get-started-with-pos-extensions"></a>POS 拡張機能の使用を開始する

ストア内トポロジに応じて、POS アプリ タイプを選択します。 一般に、1 つの POS アプリ タイプに対して開発された拡張機能は、他の POS アプリ タイプで使用することができます。 ただし、拡張機能が POS アプリ タイプに依存している場合は、別の POS アプリ タイプでは使用できません。 拡張機能の開発中にこのタイプの依存関係を回避することをお勧めします。

## <a name="set-up-the-pos-development-environment"></a>POS 開発環境の設定

### <a name="prerequisites"></a>必要条件

+ Windows 10 1809 以降、または MPOS 用 Windows Server 2019
+ 以下のワークロードとコンポーネントがある Visual Studio 2017 Community、Professional、または Enterprise。

    + Visual Studio ワークロード:

        + Visual Studioコア エディター (通常は既定で選択)
        + .NET デスクトップ開発
        +  C++ (POS) を使用したデスクトップ開発
        + ユニバーサル Windows プラットフォーム (UWP) 開発 (POS)
        + [ASP.NET](http://asp.net/) および Web 開発
        + Azure 開発
        + Node.js 開発 (POS)
        + .NET Core クロスプラットフォーム開発

    + Visual Studio のコンポーネント。 これらのコンポーネントは Visual Studio インストール時に選択できます。

        + C# Visual Basic および Roslyn コンパイラ
        + MSBuild
        + TypeScript 4.0 SDK
        + Visual C++ バージョン 15.8 + 最新の v141 ツール
        + Visual C++ ATL (x86 および x64 用)
        + Visual C++ MFC (x86 および x64 用)
        + Windows 10 SDK (10.0.17763.0)

+ .NET Framework/SDK

    + [.NET Core 3.1](https://dotnet.microsoft.com/download/dotnet/3.1)
    + [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net472-developer-pack-offline-installer)

+ SQL Server Express 2016 ローカル チャネル データベース (オフライン配置の場合のみ必要)
+ SQL Server Data Tools
+ Windows 用 Git (ソース コントロール管理)

## <a name="develop-a-pos-extension"></a>POS 拡張機能の開発

SDK およびサンプルのソース コードを [POS GitHub リポジトリ (repo)](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) からダウンロードします。

最初の拡張機能を開発するには、GitHub から既存のサンプルを使用します。 また、ステップ バイ ステップ ガイドに従って拡張機能を作成します。

## <a name="github-sample"></a>GitHub サンプル

このサンプルを使用するには、GitHub リポジトリから **リリース** 分岐サンプルを複製し、GitHub の readme ファイルの手順に従います。

## <a name="custom-extensions"></a>カスタムの拡張機能

独自の拡張機能を作成するには、[POS 拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md) の手順に従います。

拡張機能をデバッグするには、[POS 拡張機能のデバッグ](debug-pos-extension.md)の手順に従います。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
