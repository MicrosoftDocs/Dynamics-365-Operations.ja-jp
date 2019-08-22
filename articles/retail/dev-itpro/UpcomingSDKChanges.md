---
title: Retail SDK の今後の変更
description: このトピックでは、Retail ソフトウェア開発キット (SDK) の今後の変更の一覧を示します。
author: mugunthanm
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-09-11
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 2474f33474f07b60367ca0f789757c1d7ad6bbf5
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833205"
---
# <a name="upcoming-changes-in-the-retail-sdk"></a>Retail SDK の今後の変更
[!include [banner](../includes/banner.md)]

将来の Dynamics 365 for Retail のリリースでは、新しい一連の機能によって、小売チャネル カスタマイズの開発およびサービス プロセスが簡略化される予定です。 これらのいくつかの機能を取り込むため、構築した拡張機能をアップグレード、再コンパイル、または一部のマイナー コードの変更を行う必要がある場合があります。 拡張子ロジック ファイルや作成したマニフェストに変更は必要ありません。 ただし、新しいテンプレートに拡張機能ファイルを移動する、パッケージ モデルを更新する、および Commerce Runtime、プロキシ、Retail サーバー拡張機能を再コンパイルして新しいライブラリ参照モデルと統合開発環境 (IDE) にマップする必要があります。

Microsoft は、新しい機能の計画を行って取り込む準備ができるように、新しい機能がリリースされる前にこのトピックを公開します。

Retail ソフトウェア開発キット (SDK) の拡張が計画されている新機能と、取り込むためにお客様の側で作業が必要となる新機能の一覧を以下に示します。

## <a name="independent-packaging-model"></a>独立したパッケージ モデル
Microsoft は、*独立したパッケージ モデル*という名前の新しい機能を開発しています。 このパッケージ モデルは、コアとサービスから個別に拡張機能を分割するのに役立ちます。 Microsoft は、拡張機能の個別のパッケージも最終的にサポートする予定です。 独立系ソフトウェア ベンダー (ISV) ソリューションおよびパートナーの拡張機能がある場合は、パッケージ化して個別にサービスを提供できます。 ISV ソリューションおよびパートナー拡張機能は、結合する必要がなくなりました。 

Retail Modern POS でこの新しいパッケージ モデルをサポートできるようにするため、Microsoft は 販売時点管理 (POS) フレームワークを変更して、Microsoft Windows のオプションのパッケージ拡張モデルをサポートできるようにします。 拡張機能を開発する方法は変更されません。 拡張機能をパッケージ化し、配置する方法のみが変更されます。 新しいモデルでは、すべての Modern POS 拡張機能が個別の .appx ファイルとして作成されます。 コア POS は、それらのファイルをアドインとして読み込み、コア Modern POS アプリケーション ID の下で実行されます。 以前は、コア POS および拡張機能は、1 つの .appx ファイルとしてパッケージ化されました。 今回、開発者が .appx ファイルに対してだけ個別にサービスを提供できるように、コア アドインと拡張アドインの両方に .appx ファイルが用意されます。 開発された拡張機能は、クラウド POS と Modern POS の両方で機能します。 テンプレートが異なる場合がありますが、コードは両方のアプリケーション間で共有されます。

> [!NOTE] 
> 新しい機能を取り込むときは、以前に作成した拡張機能の変更が必要です。 拡張機能ファイルを別のパッケージの新しいプロジェクト タイプに移行した後、構成の更新を実行する必要があります。 拡張子ロジック ファイルや作成したマニフェストに変更は必要ありません。 ただし、拡張機能ロジック ファイルおよびマニフェストを新しいテンプレートにを移動し、それらを再構築、テスト、および検証する必要があります。

Windows Server オペレーティング システムまたは LCS 開発ボックスでは、独立したパッケージ モデル開発はサポートされていません。独自の Windows 10 ボックスを使用する必要があります。 

## <a name="prerequisites"></a>必要条件

- Visual Studio 2017、バージョン 15.1
- Windows 10、バージョン 1703
- Windows 10、バージョン 1703 SDK

## <a name="development-tools"></a>開発ツール
現時点では、Retail SDK サンプルと Retail SDK 内の他のテンプレートは、Microsoft Visual Studio 2015 でのみ動作します。 Retail SDK と新しい独立したパッケージ モデルでの今後の変更の一部をサポートするため、Microsoft は Visual Studio 2015 から Microsoft Visual Studio 2017 または最新バージョンのいずれかにアップグレードする計画です。

新しいテンプレートおよび Retail SDK サンプルは、Visual Studio 2017 またはサポートされる最新バージョンでのみコンパイルすることができます。 **したがって、この新機能がリリースされるとき、開発仮想マシン (VM) で Visual Studio 2015 から Visual Studio 2017 へのアップグレードを計画する必要があります。**

## <a name="retail-sdk-reference-folder-to-nuget-gallery"></a>NuGet ギャラリーへの Retail SDK 参照フォルダー
Commerce Runtime、Retail サーバー、Retail プロキシ、Commerce ツールなどのすべての参照バイナリ ファイルは、Retail SDK\\Reference でフォルダーで公開されます。 現時点では、拡張機能はそのフォルダーを参照できません。 ただし、Microsoft はこのモデルを終了し、代わりに NuGet ギャラリーで SDK 参照を公開する計画です。 **したがって、この新しいモデルの場合、Retail SDK\\reference フォルダーではなく NuGet ギャラリーを参照するように、拡張機能プロジェクトを変更する必要があります。この変更には、参照の更新と、拡張機能プロジェクトでの再コンパイルが必要です。**

この新しいモデルでは、更新プロセスが簡略化されます。 たとえば、Retail SDK で更新済の参照が必要な場合、現在のところ、Microsoft Dynamics Lifecycle Services (LCS) に移動し、最新のバイナリ更新プログラムなどを適用する必要があります。 NuGet のアプローチでは、右クリックするだけ更新バージョンを取得できます。

## <a name="retail-packaging-tool"></a>Retail パッケージ ツール
チャネル インストーラーは、それらを使用するだけで拡張機能をインストールできるように強化されます。 コアとすべての拡張機能用の 1 つの結合されたインストーラーを使用するか、または拡張機能とコアを別個にインストールするかを決定できるようになります。

## <a name="retail-sdk-samples-to-github"></a>Retail SDK のサンプルを GitHub に移動
Microsoft は、Retail SDK からサンプルを GitHub に移動する計画です。 サンプルはサンプル コードとしてのみ公開されているため、この変更は拡張機能に影響しません。 GitHub により、最新のサンプルが取得しやすくなります。 LCS プロセスを実行する必要がなくなります。
