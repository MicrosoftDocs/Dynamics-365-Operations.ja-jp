---
title: Retail チャネル拡張機能を最新の Retail SDK にアップグレード
description: このトピックでは、以前のリリースから Retail チャネル拡張機能を Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: kfendd
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 209/07/2018
ms.dyn365.ops.version: AX 7.3.5
ms.openlocfilehash: c17bc5028af55f6270da9c798f1b79e7e45dc78d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537572"
---
# <a name="upgrade-the-retail-channel-extension-to-the-latest-retail-sdk"></a>Retail チャネル拡張機能を最新の Retail SDK にアップグレード

[!include [banner](../includes/banner.md)]

このトピックでは、以前のリリースから Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。 プロセス全体とサポートされるシナリオの情報が含まれていますが、このトピックではプロセスの各ステップに関する詳細な指示は提示しません。 このトピックは、Dynamics 365 for Retail および Dynamics 365 for Finance and Operations 7.3 バージョンおよびそれ以上に適用されます。
以下のセクションは新しい Retail SDK に拡張機能を手動で移動する方法を説明しますが、Azure DevOps または Git などのソース管理システムを使用してこれを行うことができます。

## <a name="update-the-retail-sdk"></a>Retail SDK の更新
新しいバイナリの修正プログラムを適用することで Retail SDK を更新するときに、既存の Retail SDK フォルダー内に新しい **更新** フォルダーと、更新済の SDK のコピーが作成されます。 新しい環境を配置する場合、新しい Retail SDK は仮想マシン (VM) のサービス ボリュームまたはダウンロード可能な VHD の C ドライブにあります。

### <a name="retail-sdk-components"></a>Retail SDK のコンポーネント

Retail SDK の更新は、主に次のコンポーネントで構成されます。

-   資産: 拡張機能に関連するコンフィギュレーション ファイル変更。
-   ビルド ツール: カスタマイズ パッケージおよびバージョン管理設定。
-   データベース: 拡張 DB スクリプト。
-   ドキュメント: サンプルを実行する方法。
-   パッケージ: 配置パッケージ。
-   支払の外部参照: 支払パッケージング フォルダー。
-   支払: 支払のサンプル コード。
-   POS: Modern POS および Cloud POS のアプリケーション コードとサンプル
-   参照: すべてのバイナリ参照およびコマース アナライザー プロキシ ツール。
-   サンプル拡張機能: 拡張機能のサンプル プロジェクト。

## <a name="upgrade-scenarios"></a>アップグレード シナリオ
次のシナリオのいずれかでアップグレードを完了することができます。

  - 特定のバイナリ修正プログラムを更新する。
  - カスタム コードをアップグレードする。
  - 最新のアプリケーション リリースにアップグレードする。

SDK アップグレード プロセスは、バージョンによって異なります。 バージョン 7.3 以降では、すべての Retail コンポーネントがシールされており、拡張点を使用してのみカスタマイズを完了する必要があります。 これにより、コード アップグレード作業が容易になります。 ただし、7.0、7.1、または 7.2 からアップグレードした場合と、インライン変更を行った場合、インラインを拡張機能に移動する必要があります。 これには追加の作業が必要になります。

次の表では、コードがシールされているバージョンに関する一部の概要情報を提供します。 アンシールド バージョンからシールド バージョンにアップグレードする場合は、すべてのカスタマイズを識別し、拡張機能にインライン カスタマイズを移動する必要があります。 インライン カスタマイズを移動するには、これを行うために必要な拡張ポイントがすべてあることを確認します。 ない場合は、拡張機能の要求を送信します。 

> [!NOTE]
> バージョン 7.3 以上にアップグレードする際、7.1 で行った POS インラインの変更の一部を書き換える必要がある場合があります。

| **アプリケーションのバージョン**                 | **CRT シールド** | **HWS シールド** | **POS シールド** | **DB シールド** | **Retail プロキシ シールド** |
|-----------------------------------------|----------------|----------------|----------------|---------------|-------------------------|
| アプリケーション リリース 8.1                 | 有            | 有            | 有            | 有           | 有                     |
| アプリケーション リリース 8.0                 | 有            | 有            | 有            | 有           | 有                     |
| アプリケーション 7.3                         | 有            | 有            | 有            | 有           | 有                     |
| 2017 年 7 月のリリース (アプリケーション 7.2)     | 有            | 有            | 有            | 有           | 無                      |
| リリース 1611 (アプリケーション 7.1)          | 有            | 無             | 無             | 無            | 無                      |
| 2016 年 2 月リリース (アプリケーション 7.0) | 無             | 無             | 無             | 無            | 無                      |

## <a name="upgrade-the-retail-channel-extension-from-73-to-a-higher-version"></a>7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする

コード アップグレードを実行している場合、Retail SDK の次のコンポーネントをアップグレードする必要があります。 これらの各コンポーネントは、Retail SDK 内のフォルダーです。

> [!NOTE]
> ソース管理/マージ ツールを使用してコード アップグレードを完了できます。 変更を追跡して必要に応じて戻すことができるように、このプロセスでソース コード管理ツールを使用することをお勧めします。 ソース管理を使用していない場合、コードをアップグレードする前に、古いおよび新しい Retail SDK フォルダーのバックアップを作成することを確認します。

- **資産:** カスタム アセンブリを含めるために次の拡張構成ファイルのいずれかを変更した場合、これらの変更を新しい**資産フォルダー**にある同じ構成ファイルに移動する必要があります。

  - CommerceRuntime.Ext.config - CRT 拡張。
  - CommerceRuntime.MPOSOffline.Ext.config - CRT オフライン拡張。
  - HardwareStation.Extension.config - ハードウェア ステーションと支払拡張機能。
  - RetailProxy.MPOSOffline.ext.config - Retail プロキシ拡張機能。

- **ビルド ツール:** **ビルド ツール** フォルダーには、パッケージング、ビルド設定と pfx、および snk ファイルに関連するファイルが含まれています。 以前のバージョンで変更を加えた場合は、以下のファイルをマージおよび更新します。

  - Customization.settings
  - Microsoft.Dynamics.RetailSdk.Build.props
  - 作成したカスタム pfx または snk ファイル。

- **データベース:** カスタム SQL スクリプトをすべてコピーしてドロップします: ...\\RetailSDK\\Database\\Upgrade\\Custom

- **オンライン ストア:** オンライン ストア Web プロジェクトまたはオンライン拡張コードがある場合、このフォルダーに含めます。 
  > [!NOTE]
  > Retail 配置可能パッケージには、パッケージ用のオンライン ストア コードは含まれません。

- **支払の外部参照**: 支払拡張アセンブリすべてをコピーして以下の**支払アセンブリ** フォルダーに貼り付けます。

  - IPaymentDeviceAssemblies
  - IPaymentProcessorAssemblies
  - PaymentWebFiles

- **支払:** このフォルダーにすべての支払拡張プロジェクトをマージします。

  > [!NOTE]
  > 新しい支払拡張機能プロジェクトを作成したが、このフォルダーは何も変更しなかった場合、ビルドとパッケージング プロセスの一部として含めることができます。 **RetailSDK** フォルダーで **dirs.proj** を更新し、カスタム プロジェクトをビルドします。 次に、支払拡張機能の格納場所で **Customization.settings** ファイルを更新し、パッケージの作成時にカスタム プロジェクトがビルドされるようにします。 必ず、パッケージの一部として拡張機能を含めます。

- **POS:** 生成されたプロキシを含む任意の POS 拡張機能がある場合、POS 拡張機能を *…\\RetailSDK\\POS\\Extensions* から新しい Retail SDK POS 拡張子フォルダー *RetailSDK\\POS\\Extensions* にコピーします。 拡張機能をコピーしたら、*POS\\Extensions* フォルダー内の extension.json ファイルを更新して、コピーした新しい POS 拡張機能とマージします。

  たとえば、**CustomExtension** フォルダーをコピーした場合、以下に示すように extension.json を更新します。
  ```Typescript

   {
   "extensionPackages": [
   {
     "baseUrl": "SampleExtensions"
   },
   {
    "baseUrl": "SampleExtensions2"
   },
   {
    "baseUrl": "CustomExtension"
   }
  ]
   }
  ```
 
 ビルド中に変更を POS がコンパイルできるように、カスタム拡張機能パッケージで tsconfig.json を更新する必要もあります。

- **参照:** **Commerce ランタイム**、**ハードウェア ステーション**、**プロキシ** などのすべての拡張機能出力アセンブリと、へのすべての外部アセンブリを参照フォルダーにコピーします。 配置およびパッケージの一部として含めようとしているすべてのアセンブリを含めます。

- **Commerce ランタイム (CRT) と小売サーバー (RS) 拡張:** CRT および RS 拡張機能プロジェクトすべてを **Retail SDK** フォルダーの下にコピーします。 msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、CRT および RS 拡張ソリューション ファイルの詳細を **RetailSDK フォルダー**にある dirs.proj ファイルに含めてください。

- **ハードウェア ステーション (HWS) および支払拡張機能:** すべてのハードウェア ステーション (HWS) と支払拡張プロジェクトを **Retail SDK** フォルダーの下にコピーします。 msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、HWS および支払拡張ソリューション ファイルの詳細を **RetailSDK** フォルダーにある dirs.proj ファイルに含めてください。

- **Retail プロキシ拡張:** すべての Retail プロキシ拡張プロジェクトを **Retail SDK** フォルダーにコピーします。 msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、プロキシ ソリューション ファイルの詳細を **RetailSDK** フォルダーにある dirs.proj ファイルに含めてください。

> [!NOTE]
> Retail SDK フォルダーのルートで **msbuild** を実行します。 配置可能小売パッケージを生成するために、Microsoft Visual Studio 開発者コマンド ライン ツールを使用します。

すべてのコンポーネントをアップグレードしたら、Retail 配置可能パッケージを配置し、配置を検証して、Retail SDK ファイルをリポジトリに追加します。

## <a name="upgrade-the-retail-channel-extension-from-72-to-a-higher-version"></a>7.2 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする
前のセクション **7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする**で説明した手順は、Retail プロキシを除くすべての小売コンポーネントでも同じです。 RS 拡張機能を持つ CRT があり、**customization.settings** ファイルに基づいて TypeScript セッションが自動生成された場合、7.2 では、Retail プロキシ プロジェクトでインライン変更を完了している必要があります。

プロキシを 7.3 にアップグレードするには、[Typescript および小売販売時点管理 (POS) の C# プロキシ](typescript-proxy-retail-pos.md)のトピックの手順を完了した後、Retail SDK フォルダーにプロキシを移動し、構成ファイル **RetailProxy.MPOSOffline.ext.config** を更新します。

## <a name="upgrade-the-retail-channel-extension-from-71-to-a-higher-version"></a>7.1 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする
7.1 では、POS およびプロキシ カスタマイズ インラインのほとんどを完了している必要があります。 それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。 バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。

## <a name="upgrade-the-retail-channel-extension-from-70-to-a-higher-version"></a>7.0 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする
7.0 では、カスタマイズ インラインのほとんどを完了している必要があります。 それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。 バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。

## <a name="generate-a-deployable-package-for-validation"></a>検証用の配置可能パッケージを生成する
トピック[配置可能な小売パッケージの作成](retail-sdk/retail-sdk-packaging.md)の手順を完了し、検証用の配置可能パッケージを生成します。
