---
title: "Retail ソフトウェア開発キット (SDK)"
description: "このトピックでは、Retail SDK に関する一般情報を提供します。 Retail SDK は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。"
author: RobinARH
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17771
ms.assetid: c54d34a5-32e2-4d0d-a1c2-4a9940d95ade
ms.search.region: Global
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d22fe0c9a38026350c839d1d7d35835bfc77d995
ms.openlocfilehash: abe276f5af5dbe5cfcb08f023aba62000b06e5e3
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="retail-software-development-kit-sdk"></a>Retail ソフトウェア開発キット (SDK)

[!include [banner](../../includes/banner.md)]

このトピックでは、Retail SDK に関する一般情報を提供します。 Retail SDK は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。

## <a name="overview"></a>概要

Retail ソフトウェア開発キット (SDK) は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。 SDK は、迅速な開発、完全な MSBuild 統合、パッケージの生成、およびコード分離をサポートします。

### <a name="download-the-retail-sdk"></a>Retail SDK をダウンロード

Retail SDK は、開発環境と、Retail SDK フォルダーにある修正プログラム パッケージで使用できます。 詳細については、「」を参照してください。

- 開発インスタンスから SDK を取得すると、構成および使用の準備がすぐに整います。 詳細については、「[アクセス インスタンス](../../../dev-itpro/dev-tools/access-instances.md)」を参照してください。 
- 修正プログラムから SDK を取得する場合は、修正プログラムのパッケージでは圧縮フォルダとして含まれています。 Retail 修正プログラムは、累積的であり、その他のすべての修正プログラムが含まれています。 

Visual Studio Online などのソース管理システムに SDK を配置することをお勧めします。

### <a name="rapid-development"></a>高速開発

Retail SDK の主な焦点は、カスタマイズを効率的かつ正しく作成するのに役立ちます。 SDK を使用すると、Microsoft Visual Studio の F5 機能 (実行とデバッグ) を使用して単一コンピューター デモ環境で直接アプリケーションを実行できます。 すべての必要な「配備雑用」が行われます。 したがって、ファイルをコピーする必要はありません。

### <a name="full-msbuild-integration"></a>完全な MSBuild 統合

Retail SDK は、ビルド システムです。 SDK のルートからの単純な MSBuild コマンドは、すべてを構築します。 この動作により、どのようにしてどこからビルドするかについての推測がなくなり、整合性と再現性が保証されます。 したがって、Retail SDK は、Microsoft Visual Studio Online などのアプリケーション ライフサイクル管理 (ALM) システムと共に簡単に使用できます。 この統合には、ビルドの自動化が含まれます。

### <a name="creation-of-final-update-packages-and-better-and-explicit-control-over-the-customization"></a>最終更新パッケージの作成、およびカスタマイズのより明示的なコントロール

Retail SDK には、サービスを配置するために必要なすべてのものが含まれる新しいパッケージを生成するツールが含まれます。 たとえば、Commerce Runtime が新しいカスタム サービス ダイナミックリンク ライブラリ (DLL) で拡張された場合、SDK は自動で新しい DLL をすべての適切なパッケージ (RetailServer および MPOSOffline) に追加します。 または、データベースが拡張された場合、アップグレード スクリプトは自動的に RetailServer と MPOSOffline パッケージの両方に追加されます。これらは、チャンネル データベースの更新を実行する必要がある (潜在的に) パッケージだからです。 共有されているファイルは、SDK に 1 度だけ存在します。 パッケージ プロジェクトは、パッケージの正しいファイルを引き出すように設定されています。 したがって、commerceruntime.config ファイルは 1 か所のみで編集します。 これらのファイルにカスタマイズが必要な場合はほとんどありませんが、展開関連のスクリプト ファイルにも同じことが適用されます。

### <a name="better-code-separation"></a>より良いコードの分離

Retail SDK の更新が必要なときはいつでも、潜在的なコード結合が必要です。 この要件は、既存のコードが変更された場合に適用されます。 SDK の実装とフォルダー構造のいくつかの機能は、サンプル コードからカスタム コードをより適切に分離するのに役立ちます。 したがって、これらの機能は、この問題の多くを削除します。 将来この領域がさらに改善されることを期待することができます。

### <a name="real-world-implementation-samples"></a>実際の実装サンプル

一部の Retail 実装のソース コードに加えて、Retail SDK には特定のシナリオを実装する方法を示すサンプル コードが含まれています。

## <a name="retail-sdk-deep-dive"></a>Retail SDK の詳細な情報
### <a name="prerequisites"></a>前提条件

-   カスタマイズの**コード**を書いたり**ビルド**するには、次のツールが必要です。

    -   Typescript 1.5 付き Microsoft Visual Studio (LCS 開発者トポロジが許容可能)
    -   ASP.NET MVC 4.0 (LCS 開発者トポロジ受入可能) (店舗でのみ必須)
    -   150 MB 以上の使用可能なディスク領域 (LCS 開発者トポロジを受入可能)

    この要件のリストは非常に短く、開発者は簡単なラップトップで生産性を高めることができます。 検証ユーティリティの前提条件はなくなりました。

-   カスタマイズを**実行**するには、Retail を実行するための通常の前提条件が適用されます。 開発時に、シングル ボックスの開発者トポロジ (LCS クラウド ホストまたはダウンロードのいずれか) でカスタマイズを実行することをお勧めします。

### <a name="retail-sdk-contents"></a>Retail SDK のコンテンツ

次のフォルダーとファイルは、トップ レベルの Retail SDK の一部です。

> [!NOTE]
> 上記のフォルダー構造と説明は、Retail の 2017 年 7 月のアップデート (7.2) にのみ適用されます。 Retail 7.3 のリリースで、Retail プロキシおよびハードウェア ステーション プロジェクトが含まれました。 したがって、Retail 7.3 リリースでは、ハードウェア ステーションと小売プロキシのサンプルのみが表示されます。 プロキシは、新しい拡張性パターンに従って作成できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>フォルダー/ファイル</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>資産</td>
<td>スクリプトや構成ファイル (commerceRuntime.config、dllhost.exe.config など) などの共有アイテムが含まれています。 コンフィギュレーション ファイルは、この場所でカスタマイズおよび編集する必要があります。 作成されたワークスペースを使用するプロジェクトで、ワークスペースが適切にピッキングされます。</td>
</tr>
<tr class="even">
<td>BuildTools</td>
<td>MSBuild およびグローバル構成に関連するものがすべて含まれています。 Customization.settings は、ビルド システムを設定するために使用する主要なファイルです。 次のリストは、このファイルが制御し、カスタマイザーが変更する可能性が高い項目を示しています。
<ul>
<li>すべてのビルド済みアセンブリ (AssemblyNamePrefix) の接頭語</li>
<li>すべてのバイナリ (CustomAssemblyVersion) のアセンブリ バージョン</li>
<li>すべてのバイナリ (CustomVersion) のファイル バージョン</li>
<li>カスタマイズの名前 (CustomName)</li>
<li>カスタマイズの説明 (CustomDescription)</li>
<li>発行元 (CustomPublisher)</li>
<li>コード署名 (SignAssembly、AssemblyOriginatorKeyFile)</li>
<li>Modern POS の証明書パス (ModernPOSPackageCertificateKeyFile)</li>
<li>カスタマイズ (RetailServerLibraryPathForProxyGeneration、ISV_*) に関連付けられているファイル</li>
</ul></td>
</tr>
<tr class="odd">
<td>CommerceRuntime</td>
<td>Visual Studio ソリューション ファイル (CommerceRuntime.sln) および関連する C# プロジェクト (CommerceRuntime、PricingEngine) が含まれています。</td>
</tr>
<tr class="even">
<td> データベース</td>
<td>共有データベース スクリプトが含まれています。 完全なスクリプト CommerceRuntimeScripts_Create.sql は、新しい基本データベースの作成にのみ使用されます。 アップグレード フォルダーには、Microsoft とカスタマイザーの両方からの増分スクリプトが含まれています。 配置中にデータベースまたはデータベースのバージョンが存在すると、完全スクリプトまたは増分スクリプトの実行をコントロールします。 実行されたことのないスクリプトのみ実行されます。</td>
</tr>
<tr class="odd">
<td>ハードウェア ステーション</td>
<td>Visual Studio ソリューション ファイル (HardwareStation.sln) および関連する C# プロジェクト (HardwareStation ライブラリと Webhost) が含まれています。</td>
</tr>
<tr class="even">
<td>OnlineStore</td>
<td>Visual Studio ソリューション ファイル (OnlineStore.sln) および関連する C# プロジェクト (Ecommerce SDK) が含まれています。</td>
</tr>
<tr class="odd">
<td>パッケージ</td>
<td>パッケージ作成用の複数のプロジェクトが含まれています。 これらのパッケージは、LCS を介して配布するために使用されます。 これらのパッケージには、最終的な web.config ファイルも含まれています。</td>
</tr>
<tr class="even">
<td>PaymentExternals</td>
<td>支払に関連するすべてのアセンブリが含まれます。 次の 3 つのサブフォルダでは、さまざまな支払ファイルを保持します。
<ul>
<li><strong>IPaymentProcessor Assemblies</strong> – このフォルダーには、IPaymentProcessor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。</li>
<li><strong>支払 Web ファイル</strong> – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML、JavaScript、または CSS ファイルが含まれています。 支払い受付ページで求められる場合、支払コネクタ開発者がこれらの Web ファイルを提供します。</li>
<li><strong>IPaymentDevice Assemblies</strong> – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリと支払要求ハンドラー、およびインターフェイス依存アセンブリが含まれています。 これらのアセンブリは、支払のターミナル デバイスと通信するために、Retail ハードウェア ステーションおよび Retail Modern Point of Sale (モダン POS) で使用されます。
<p>さらに支払コネクタに関連するすべての拡張子は、配置パッケージを作成する前に、フォルダーに配置する必要があります。</p></li>
</ul>
</td>
</tr>
<tr class="odd">
<td>支払利息</td>
<td>Visual Studio ソリューション ファイル (PaymentSDK.sln) および関連する C# プロジェクト (PaymentSDK コネクタ、サンプル、機能テスト) が含まれています。</td>
</tr>
<tr class="even">
<td>POS</td>
<td>POS 用のファイルが含まれています。
<ul>
<li>CloudPos.sln</li>
<li>ModernPos.sln</li>
<li>フォルダ コア – 低レベルで共有する POS コード</li>
<li>フォルダー ViewModels – 共有する POS ビュー モデル</li>
<li>フォルダー SharedApp – 共有する POS ビュー</li>
<li>フォルダー アプリ – Modern POS– 特定のビューおよびその他の品目</li>
<li>フォルダー Web – クラウド POS– 特定のビューおよびその他の品目</li>
</ul></td>
</tr>
<tr class="even">
<td>プロキシ</td>
<td>他のユーザーが参照する 2 つの Visual Studio プロジェクトが含まれています。 これらのプロジェクトには、Retail Server のプロキシ クライアントとして機能するインターフェイスと生成されたコードが含まれています。 Proxies.Retail.TypeScript は TypeScript プロキシで、RetailProxy は C# プロキシです。 Modern POS/Cloud POS と ECommerce SDK で使用されています。</td>
</tr>
<tr class="odd">
<td>参照</td>
<td>すべてのバイナリが存在する単一の場所。 場所は、プロジェクトのバイナリ参照を解決するために使用されます。 ファイルのリストには、外部の非 Retail バイナリと Microsoft Retail バイナリが含まれています。 また、このディレクトリは、Retail SDK からビルドされているバイナリのグローバルな格納場所として使用されます。</td>
</tr>
<tr class="even">
<td>SampleExtensions</td>
<td>サンプル拡張子を含みます。</td>
</tr>
<tr class="odd">
<td>dirs.proj</td>
<td>ビルド順序を指示するトップレベルの MSBuild ファイル。</td>
</tr>
<tr class="even">
<td>Microsoft-version.txt</td>
<td>Retail SDK の Microsoft のバージョンを含むファイル。 ファイルを編集しないでください。</td>
</tr>
</tbody>
</table>

SDK の C\# ソース コードは、Contoso 名前空間を使用します。 したがって、Microsoft が Microsoft.Dynamics を使用するため、Microsoft の型と独自の型を区別する方が簡単です。 Microsoft バイナリからタイプを参照している場合は、Microsoft.Dynamics を参照します。 そのようにして、Retail SDK からではなく、参照先のバイナリからであることがわかります。 

[![RetailSDK02](./media/retailsdk02.png)](./media/retailsdk02.png)

### <a name="dependencies-build-order-and-full-build"></a>相互関係、ビルド順序、およびフル ビルド

次の図は、Retail SDK 内の高レベルの論理的な依存関係ツリーを示しています。 すべての Microsoft ファイルまたはアセットへの参照は示されません。 これらを確認するには、Visual Studio プロジェクトとソリューション ファイルを詳しく見てください。 

[![RetailSDK03](./media/retailsdk03.png)](./media/retailsdk03.png) 

次の重要な点を考慮してください。

-   RetailServer API は、自動的に生成されたクライアント プロキシ コードを使用していくつかのプロジェクトによって消費されます。 この動作により、より迅速な開発が可能になり、エラーやバグの機会が減ります。  既定では、Retail SDK は公式の Microsoft DLL を使用してクライアント コードを生成します。 カスタマイザーは独自の DLL (Customization.settings 内) に切り替えることができ、カスタマイズされた RetailServer API 用のプロキシ コードを自動的に生成することができます。 DLL を切り替えた後、開発者は、RetailProxy プロジェクト内のいくつかの実装を変更する必要がある場合があります。 その理由は、オフライン モードの Modern POS は Commerce Runtime と直接通信する必要があり、そのコードを実装する必要があるためです。 ただし、推測は必要ありません。 C\# コンパイラはこれを強制します。
-   パッケージ プロジェクトは、LCS で想定されている方法で配置パッケージを生成します。 既定では、これらのプロジェクトは Microsoft の資産 (カスタマイズされていない) とプロキシ DLL のみを出荷します。 含まれるべきものは、Customization.settings で明示的に記名される必要があります。 この動作は仕様です。 これは配置されたカスタム コードを削減して、バイナリ パッチを許可します。 たとえば、カスタマイズは、新しい CommerceRuntime サービスおよび新しい RetailServer コントローラーを追加します。 この場合、2 つの新しい DLL はパッケージの内容に登録され、関連するすべての場所に自動的に含まれます。 パッケージには、SDK のすべての再コンパイルされたバイナリは **ありません**。
-   すべてのプロジェクトを含む単一の Visual Studio ソリューションはありません。 さまざまな Visual Studio プロジェクト間にいくつかの結合があるため、複数のプロジェクトまたはソリューションを並べて開くことができ、変更後に適切なプロジェクトをコンパイルできます。
-   すべてのコンポーネントをカスタマイズしなくても、最終的な配置パッケージを入手する最も簡単な方法は、Retail SDK 全体を構築することです。 これを行うには、**VS2015 の MSBuild コマンド プロンプト** ウィンドウを開き、**msbuild** (または非デバッグ バージョンでは、**msbuild /p:Configuration=Release**) を入力します。 

[![RetailSDK04](./media/retailsdk04.png)](./media/retailsdk04.png)

このコマンドはすべてのプロジェクトをビルドします。 この方法は、実装やコードのバグがないことを確認する優れた方法も提供します。  バグがある場合は、ビルドが失敗し、コマンド プロンプト ウィンドウに失敗した内容が表示されます (この出力は Visual Studio に表示と似ています)。 

[![RetailSDK05](./media/retailsdk05.png)](./media/retailsdk05.png) MSBuild の詳細については、以下を参照してください[https://msdn.microsoft.com/en-us/library/0k6kkbsd.aspx](https://msdn.microsoft.com/en-us/library/0k6kkbsd.aspx)。 

ビルドによって作成されるバイナリは、自動的に SDK リファレンス フォルダーにコピーされます。 References フォルダーには、その他のすべてのバイナリも含まれます。 DLL には、すべて Customization.settings で定義できる名前 (この場合は「Contoso」) が接頭語にあるため上書きされないことに注意します。 

[![RetailSDK06](./media/retailsdk06.png)](./media/retailsdk06.png)

### <a name="minimal-required-configuration"></a>最小限必要なコンフィギュレーション

Retail SDK をすばやくビルドしたり、デモ マシンでデバッガーの POS を実行したいのですか。 Modern POS のみで、正しく構築するためのアプリ パッケージ署名証明書を作成する必要があります。 また、クラウド POS を使用することができます。 [https://msdn.microsoft.com/en-us/library/windows/desktop/jj835832(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/jj835832(v=vs.85).aspx) で PFX ファイルを作成する指示に従ってください。 PFX ファイルを BuildTools フォルダーにコピーし、 BuildTools\\Customization.settings ファイルを正しい名前 (ModernPOSPackageCertificateKeyFile) で更新します。 この時点で個々のソリューション、プロジェクト、または Retail SDK 全体を (MSBuild を使用して) ビルドするために必要なものはすべてあります。

### <a name="normal-configurationcode-signing"></a>通常の構成/コード署名

BuildTools\\Customization.settings には SDK のほとんどのコンフィギュレーション値が保持されています。 次の図の強調表示された項目はグローバル値です。 これらの値は、ビルド バイナリ、コンポーネント、パッケージの名前付け、バージョン管理、コード署名の方法を制御します。 

[![RetailSDK07](./media/retailsdk07.png)](./media/retailsdk07.png) これは必須ではありませんが、厳密な名前でアセンブリに署名することをお勧めします。 独自のキー ファイルをまだ作成していない場合に作成する方法については、[[https://msdn.microsoft.com/en-us/library/6f05ezxy(v=vs.110).aspx](https://msdn.microsoft.com/en-us/library/6f05ezxy(v=vs.110).aspx)] を参照してください。 正しくビルドするには、アプリ パッケージの署名証明書を作成する必要があります。 [https://msdn.microsoft.com/en-us/library/windows/desktop/jj835832(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/jj835832(v=vs.85).aspx) で PFX ファイルを作成するこれらの指示に従ってください。 厳密な名前のキー ファイルとアプリ パッケージの署名証明書の両方を BuildTools フォルダー内に保存することができます。 **RetailServerLibraryPathForProxyGeneration** プロパティは、プロキシ生成で異なる RetailServer DLL を設定するために使用することができます。 Customization.settings は、バイナリー、コンフィギュレーション ファイル、SQL 更新スクリプトなどの新しいカスタマイズ資産を定義する場所でもあります。 拡張子、バイナリ、および資産をここで指定した後、ファイルは作成された配置可能パッケージに追加されます。 

[![RetailSDK08](./media/retailsdk08.png)](./media/retailsdk08.png)

### <a name="customizing-the-build"></a>ビルドのカスタマイズ

#### <a name="adding-new-projects"></a>新しいプロジェクトの追加

新しいプロジェクトを Retail SDK のビルド システムに追加するのは簡単です。 多くの既存のプロジェクトのいずれかを複製するか、新しいプロジェクトを開始することができます。 次の図に示すように、テキスト エディタでいくつかの調整を加える必要があるだけです。 **Import** 要素の相対パスを調整する必要があり、**AssemblyName** 要素は定義済みの **AssemblyNamePrefix** プロパティを使用する必要があります。 これらの調整は、バージョン管理、コード署名、統一されたアセンブリ命名、[参照] フォルダーへの自動ドロップ、その他のタスクを無料で行うために必要です。 

[![RetailSDK09](./media/retailsdk09.png)](./media/retailsdk09.png)

#### <a name="changing-the-build-order-or-adding-to-the-build"></a>ビルド順序の変更またはビルドへの追加

Retail SDK のディレクトリ ツリー全体は、MSBuild トラバーサル ファイル (dirs.proj ファイル) サポートを受けて構築されています。 次の図は、Retail SDK の主なトラバーサルファイルを示しています。 類似したファイルは、サブディレクトリにも存在する場合があります。 Visual Studio ソリューション ファイル (.sln ファイル) がトラバーサル ファイルに非常に類似していることに注意します。 どちらも他のビルド スクリプトを処理することを MSBuild エンジンに「指示」します。 

[![RetailSDK10](./media/retailsdk10.png)](./media/retailsdk10.png) 

新しいコードを追加した後、そのほとんどは、新しいフォルダーに配置する必要があります (詳細は、「コード実装のベスト プラクティス」を参照してください)。また、1 つまたは複数の dirs.proj ファイルに追加することによって、トラバーサル構造に追加する必要があります。 拡張フォルダーは、前述の図の 10 行目で強調表示されています。 新しい dirs.proj ファイルを開始する最も簡単な方法は、既存のファイルをコピーし、**Import** 要素のパスを修正して、**ItemGroup** 要素の **ProjectFiles** 要素を更新することです。

#### <a name="build-script-customization"></a>ビルド スクリプトのカスタマイズ

新しいビルド ステップを実装する必要があるとき、既存のスクリプトが Retail SDK 更新プログラムで後で更新される可能性があることに留意してください後で、で更新します。 ベスト プラクティスはファイルの編集を最小限にするか、新しいファイルを代わりに追加します。 新しいグローバル MSBuild プロパティが必要な場合、BuildTools\\Microsoft.Dynamics.RetailSDK.Build.props はそれらを追加する上でお勧めです。 同様に、BuildTools\\Microsoft.Dynamics.RetailSDK.Build.targets は、新しいビルド処理のターゲットを追加するために使用できます。 1 つのプロジェクトで特別な処理が必要とならない場合は、明示的に変更を加えることをお勧めします。 新しいローカル MSBuild プロパティが必要な場合は、同じディレクトリに local.props という名前の新しいファイルを追加します。 または、ローカル ビルド処理ターゲットが必要な場合は、local.targets ファイルを追加します。

### <a name="developer-productivity"></a>開発者の生産性

この記事の前半のアーキテクチャ図に示すように、いくつかのものは RetailServer インターフェイスによって異なります。 他のユーザーがこのインターフェイスを変更することがあります。 開発者のトポロジ マシンでは、誰かがすぐに変更を試してみることができます。 この場合、任意の CommerceRuntime および RetailServer 拡張 DLL をローカルにインストールされた RetailServer Web アプリケーションの bin フォルダーにコピーする必要があります。 ユーザーは、Customization.setting ファイルをコンフィギュレーションして、これらのファイルの新しいバージョンがビルドされるたびに、DLL がローカルの RetailServer Web アプリケーションの bin フォルダーに自動的にコピーされるようにできます。 

[![RetailSDK11](./media/retailsdk11.png)](./media/retailsdk11.png)

### <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

優れた ALM ソリューションは、バージョン管理、ビルド、自動ビルド、プランニング ツール、追跡ツール、ダッシュ ボード、カスタマイズなどを提供します。 Retail SDK は、これらのタスクをサポートするように編成されています。 

[Azure DevOps](/Azure DevOps/) は、優れたツールでありお勧めします。

### <a name="branching-and-versioning"></a>分岐およびバージョン管理

チームで効率的に仕事をしたり、過去に行ったいくつかの変更を確認できるようにするには、適正な分岐戦略とバージョン管理の規範が必要です。 次の図は、ほとんどのチームでうまくいく単純な分岐戦略を示しています。 バージョン番号は、架空のものです。 [![RetailSDK12](./media/retailsdk12.png)](./media/retailsdk12.png)

#### <a name="retail-sdk-mirror-branch"></a>Retail SDK のミラー分岐

強調すべき非常に重要なポイントは、カスタマイズされていない Retail SDK をソース コントロールに保存する必要があるということです。 すべてのバージョンを保存する必要はありませんが、チームがスナップするバージョンを追加する必要があります (これらのバージョンは、累積的な更新または修正プログラムである場合があります)。 すべての変更 (追加、変更、および削除) の単純な結合のみ行う必要があります。 このブランチで発生する他の開発作業はありません。 Retail SDK には、独自のバージョンがあります。 すべての Retail バイナリおよびパッケージには同じバージョンが含まれています。 バージョンは、Microsoft-version.txt という名前のファイルの Retail SDK のルートにもあります。

#### <a name="customization-branch"></a>カスタマイズ分岐

配置を開発した後、新しい分岐を開始する必要があります (カスタマイズ分岐)。 初期分岐アウトの先頭において、この分岐は Retail SDK ミラー分岐の正確なコピーになります。 これは、チームの開発の分岐です。 カスタマイズ ブランチのバージョンは、少なくともテストのためにビルドが作成されるたびに増分する必要があります。また、毎日増分することもできます。 増分するファイル バージョンは、**CustomVersion** プロパティを使用して Customization.setting ファイルで定義されます。 それを更新し、すべてのバイナリ パッケージを再構築すると、マニフェスト ファイルはそれに応じて更新されます。 **CustomAssemblyVersion** プロパティは、更新プログラムに下位互換性がなく、主な新しいリリースに対して互換性がない場合のみ更新する必要があることに注意してください。 つまり、この更新プログラムはめったにありません。 たとえば、Microsoft のアセンブリ バージョンは、現在のバージョンの複数の CTP リリースに対して変わりませんでした。 同じ分岐には Microsoft の資産と独自の変更の両方が存在するため、分岐には基本的に 2 つのファイル バージョンがあります。 最初のバージョンは、現在の支店が基づいている Retail SDK の Microsoft バージョンで、2 番目のバージョンは、**CustomVersion** プロパティによって設定されたバージョンです。 前述の図では、カスタマイズ分岐の現在のファイル バージョンは、1.0.2\* です (Microsoft バージョン 7.0.2200.3 に基づく)。 展開された最初のリリースのファイル バージョンは 1.0.0.40 (7.0.2000.0 に基づく) でした。 テスト フェーズが完了し、最後のパッケージがそのバージョンで配置されるとき、バージョン番号を増分する (またはソース コントロールのラベルを作成する) ことが重要です。

