---
title: Retail Experience アプリにブランディングを作成し適用する
description: このトピックでは、ブランディングを Retail Experience アプリに適用して Google Play と Apple App Store にリリースする方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 251594
ms.assetid: 922881a2-f12a-41b4-8ef9-a5b31b464ef1
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e965940a36cc3eaf0d3201be5ff8b23e3475016e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004590"
---
# <a name="create-and-apply-branding-to-the-retail-experience-app"></a>ブランドの作成と Retail Experience アプリへの適用

[!include [banner](../includes/banner.md)]
 
ブランディングを Retail Experience アプリに適用して、Google Play と Apple App Store にリリースすることができます。 このトピックでは、アプリを作成して接続し、ブランディングを適用する方法について説明します。

## <a name="development-tools"></a>開発ツール
Retail Experience アプリは、Android および iOS スマートフォン プラットフォームをサポートします。 アプリは、Xamarin.Forms を使用して構築され、開発用コンピューターには Xamarin をインストールする必要があります。 iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。 Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。 Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。 開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (SDK) をインストールする必要があります。

### <a name="install-xamarin"></a>Xamarin のインストール

Xamarin は [Xamarin 用の Visual Studio Tools](https://www.xamarin.com/download) からダウンロードできます。 

Windows に Xamarin をインストールする方法を示すチュートリアルについては 「[Xamarin のリソース](https://docs.microsoft.com/xamarin/get-started/installation/index?pivots=windows)」 を参照してください。

### <a name="update-xamarin"></a>Xamarin の更新

Xamarin をインストールした後は、最新の安定バージョンに更新する必要があります。

-   **Windows:** Microsoft Visual Studio で、**ツール** &gt; **オプション** &gt; **環境** &gt; **Xamarin** &gt; **その他** を順にクリックします。
-   **Mac:** Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。 詳細については、[更新チャンネルの変更](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/) を参照してください。

### <a name="connecting-to-a-mac"></a>Mac に接続しています

Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。 手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。

## <a name="loading-the-solution-in-visual-studio"></a>Visual Studio へのソリューションの読み込み
Visual Studio に Retail Experience アプリを正しく読み込むことができるようにするには、その前に、そのアプリを修正する必要があります。 以下の手順を実行します。

1.  Retail SDKフォルダー**全体**を Xamarin が有効なコンピューターにコピーします。 たとえば、C:\RetailSdk にコピーします。
2.  C:\RetailSdk\SampleExtensions\ShoppingApp\Sample.ShoppingApp.sln を開き、次の行を削除します。

    ```
    Project("{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}") = "RetailSdk.Sample.ShoppingApp", "RetailSdk.Sample.ShoppingApp.csproj", "{D88688FA-C42E-48BE-8334-5A5855561913}" .
    ```

3.  C:\RetailSdk\SampleExtensions\ShoppingApp\iOSShoppingApp.iOS.csproj を開き、次の行を削除します。

        <Import Project="......BuildToolsMicrosoft.Dynamics.RetailSdk.Build.props" />
        <Import Project="......BuildToolsMicrosoft.Dynamics.RetailSdk.Build.settings" />
        <Import Project="$(SdkRootPath)BuildToolsMicrosoft.Dynamics.RetailSdk.Build.targets" />
        <HintPath>......ReferencesXamarin.iOS.0.0.0Xamarin.iOS.dll</HintPath>

4.  Visual Studio で、Sample.ShoppingApp.sln を開き、Droid および iOS フォルダーから既存のプロジェクトを追加します。 (ソリューションを右クリックし、**追加** &gt; **Visual Studio の既存のプロジェクト**を選択します)。
5.  Xamarin.Forms はアプリに必要なバージョン 2.3.2.127 の問題を修正しました。 以下の説明に従って Xamarin.Forms バージョンをアップグレードしてください:
    1.  Android と iOS の両方のプロジェクトの .csproj ファイルを開いて、明細行「&lt;PkgXamarin\_Forms&gt;$(NugetPackagesRoot)Xamarin.Forms.2.3.1.114&lt;/PkgXamarin\_Forms&gt;」を &lt;PkgXamarin\_Forms&gt;$(NugetPackagesRoot)Xamarin.Forms.2.3.2.127&lt;/PkgXamarin\_Forms&gt; と置き換えます
    2.  Android と iOS の両方のプロジェクトのファイル package.config ファイルを開いて、明細行「&lt;package id="Xamarin.Forms" version="2.3.1.114" targetFramework="monoandroid60" /&gt;」を「&lt;package id="Xamarin.Forms" version="2.3.2.127" targetFramework="monoandroid60" /&gt;」と置き換えます

## <a name="connect-to-an-online-channel"></a>オンライン チャネルへ接続する
小売エクスペリエンス アプリでは、オンライン チャネルを使用して製品を表示します。 任意のオンライン チャネルを使用することができます。 要件に応じて、アプリごとに異なるオンライン チャネルを使用することも、両方のアプリに対して同じオンライン チャネルを使用することもできます。 オンライン チャネルに類別されているリリースされた製品は、アプリに表示されます。 

> [!NOTE]
> アプリはギフト カードの発行に使用できません。 したがって、ギフト カードは、アプリケーションが使用するオンライン チャネルの品揃えから除外する必要があります。 Commerce Scale Unit のエンドポイントおよびオンライン チャネルに関する情報は、各アプリ プロジェクトに存在する config.xml ファイルに追加されます。 config.xml ファイルを次のように変更する必要があります。

-   **&lt;DataServiceUrl&gt;** タグで、Commerce Scale Unit の URL を追加します。
-   **&lt;MediaBaseUrl&gt;** タグで、メディア サーバーの URL を追加します。 この URL の最後にスラッシュ (/) があることを確認します。
-   **&lt;OperatingUnitNumber&gt;** タグで、アプリと組み合わせて使用するオンライン チャネルの事業単位番号を追加します。 

> [!NOTE]
> 完全な作業単位数を入力します。 たとえば、デモ データでは、Contoso オンライン ストアの作業単位番号は 068 です。

## <a name="connect-to-a-payment-connector"></a>支払コネクタへ接続する
アプリからの支払を受け入れるには、アプリで使用されているオンライン チャネルに支払コネクタを設定する必要があります。 支払コネクタは、カード関連のコントロールをホスト HTML ページに読み込みます。 Retail SDK に CardPaymentHost.html という名前のホスト ページを追加しました。 このホスト ページが Mastercard コネクタで動作することも確認しました。 ただし、他の支払プロバイダーの要件を満たすためには、このページを編集する必要がある場合があります。 異なるコネクタがページを提供する可能性があります。 ホスト ページは、選択した任意の Web サイトでホストすることができます。 ただし、電子商取引サイトがある場合、電子商取引サイトでホストすることをお勧めします。 ページがホストされた後、ホスト ページの URL を **&lt;CardPaymentHostPageUrl&gt;** タグに追加します。

## <a name="update-the-about-page"></a>詳細ページの更新
ページに次のリンクを追加します。

-   **&lt;TermsOfUseUrl&gt;** タグで、ライセンス条項へのリンクを追加します。
-   **&lt;PrivacyPolicyUrl&gt;** タグで、プライバシー ポリシーへのリンクを追加します。
-   **&lt;ThirdPartyNoticesUrl&gt;** タグで、サード パーティ通知へのリンクを追加します。

> [!NOTE]
> これらのリンクが存在しない場合に、ユーザーがクリックするとアプリが応答を停止することがあります。 したがって、これらのタグへのリンクを必ず追加してください。 情報ページには **&lt;EvaluationModeEnabled&gt;** タグがあり、これを使用して評価モード ビューを有効化できます。 評価モードを使用すると、小売業者はコードを変更せずに Commerce Scale Unit エンドポイントを簡単に変更できます。 この機能により、小売業者はさまざまなチャネルのアプリを評価できます。 **評価モードは、アプリケーションの生産バージョンで無効にする必要があります。** 既定では、評価モードは Retail SDK で無効になります。

## <a name="apply-branding"></a>ブランディングを適用
Microsoft サンプル ブランドを使用して小売エクスペリエンス アプリを正常にビルトした後、アイコン、ラベル、および色を変更して独自のブランド要件を満たすアプリを作成することができます。 以下のリストは、小売業者が変更する場合のあるアイコン、ラベル、および色の一部について示しています。 このリストは、包括的ではありません。 

**アイコン**

-   **アプリケーション** - アプリを電話にインストールした後にユーザーに表示されるアイコン。
-   **小売業者のブランド** – Android のポップアップメニューに表示されるアイコン。
-   **ショップ** – Android のポップアップメニュー、および Apple iPhone のタブバーに表示されるアイコン。
-   **情報** – Android のポップアップメニュー、および iPhone のタブバーに表示されるアイコン。
-   **ショッピング カート** – Android の右上隅、および iPhone のタブバーに表示されるアイコン。
-   **検索** – Android および iPhone の右上隅に表示されるアイコン。
-   **スプラッシュ スクリーン** – Android および iPhone の読み込みイメージとして表示されるアイコン。

**ラベル/テキスト**

-   アプリ名 (アプリが電話にインストールされている場合に、アプリ アイコンの下に表示される名前)。
-   店舗アイコンの名前と、対応するページ タイトル。
-   情報アイコンの名前と、対応するページ タイトル。
-   トースト通知として表示される確認メッセージ。
-   "カートに追加" ボタンのテキストと、対応するページのタイトル。
-   "精算" ボタンのテキストと、対応するページのタイトル。
-   "注文する" ボタンのテキスト。
-   ページ ラベルと対応するページ タイトルについて。

**色**

-   アプリ バー (アプリ バーはアクション バーまたはツール バーとも呼ばれます。)
-   ステータス バーの色
-   アクセント色
-   基本アクション ボタンの色。 たとえば、**カートに追加**、**チェック アウト**、**注文**、および**続行**ボタンすべてが同じ色です。

### <a name="applying-branding-to-the-android-app"></a>Android アプリにブランディングを適用

#### <a name="icons"></a>アイコン

Android アプリのアイコンを変更するには、Resource フォルダーを開き、それぞれのドローアブル フォルダーのアイコンを更新します。 これらのドローアブル フォルダーには、Android 用の画像がさまざまな解像度で含まれています。 これらのフォルダー内のイメージのサイズを保持するか、要件を満たすように変更することができます。 Android がさまざまな画面サイズを処理する方法については [画面互換性の概要](https://developer.android.com/guide/practices/screens_support.html) を参照してください。 スプラッシュ スクリーンは、ドローアブル フォルダーに置かれ、Android に必要な特別な種類の画像です。 スプラッシュ スクリーンの詳細については、[サイズを変更できるビットマップの作成](https://developer.android.com/studio/write/draw9patch.html) を参照してください。

#### <a name="labeltext"></a>ラベル/テキスト

Android アプリのテキスト ラベルを変更するには、TextResources.resx ファイルを開き、使用可能なリソースの値を編集します。 次のテーブルに、Android デバイスに表示されるラベル/テキストの名前と、TextResources.resx で変更する必要がある対応するプロパティ/キーを示します。 アプリ名は、strings.xml ファイル内で指定されます。

| ラベル/テキスト                                                 | プロパティ名/キー                                                                                        |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| アプリ名                                                   | **アプリケーション\_名**。 このプロパティは、../ShoppingAppDroidResourcesvalues の strings.xml ファイルにあります。 |
| 店舗アイコンの名前と、対応するページ タイトル            | それぞれ、**MenuPage\_Products** と **Pages\_CategoryListPage\_Products**                           |
| 情報アイコンの名前と、対応するページ タイトル     | それぞれ、**MainTabs\_Account** と **Pages\_AccountPage\_AccountInformation**                       |
| トースト通知として表示される確認メッセージ   | TextResources.resx での複数のメッセージ                                                                  |
| 「カートに追加」ボタンのテキストと、対応するページのタイトル | **Pages\_ProductDetail\_AddToCart** および **Pages\_CartPage\_Title**                         |
| 「チェック アウト」ボタンのテキストと、対応するページのタイトル    | **Pages\_CartPage\_Checkout** および **Pages\_CheckoutPage\_Title**                           |
| 「プレース ホルダー」ボタンのテキスト                                  | **Pages\_CheckoutPage\_PlaceOrder**                                                                      |
| ページ ラベルと対応するページ タイトルについて          | **Pages\_AccountPage\_About** および **Pages\_AboutPage\_Title**                              |

> [!NOTE]
> TextResources.resx ファイルの一部のリソースは Android アプリでは使用されませんが、iOS アプリで使用されます。 例では、**MainTabs\_Cart** および **MainTabs\_Products** があります。 iOS アプリに影響を与えずに、Android アプリからこれらのリソースを変更することができます。

#### <a name="colors"></a>色

Android アプリに表示される色を変更するには、config.xml ファイルと colors.xml ファイルを開きます (colors.xml は Resources-&gt;values フォルダーにあります)。 ここで、両方のファイルの **Primary** (アプリ バーの色)、**PrimaryDark** (ステータス バーの色)、**Accent**、および **ActionButtonBackground** の値を変更して統一させます。 

> [!NOTE]
> 製品価格は、商品リスト ページと製品の詳細ページの 2 つのページに表示されます。 製品リスト ページに表示される価格は緑に設定 (\#008A00) に設定され、変更することはできません。 ただし、製品の詳細ページで表示される価格は、「PrimaryDark」プロパティで設定される値によって管理されます。

### <a name="applying-branding-to-the-ios-app"></a>iOS アプリにブランディングを適用

#### <a name="icons"></a>アイコン

iOS アプリのアイコンを変更するには、Resource フォルダーを開き、アイコンを更新します。 フォルダー内のイメージのサイズを保持するか、要件を満たすように変更することができます。

#### <a name="labeltext"></a>ラベル/テキスト

iOS アプリのテキストを変更するには、TextResources.resx ファイルを開き、使用可能なリソースの値を編集します。 次のテーブルに、iOS デバイスに表示されるラベル/テキストの名前と、TextResources.resx で変更する必要がある対応するプロパティ/キーを示します。 アプリ名は、info.plist ファイル内で指定されます。

| ラベル/テキスト                                                 | プロパティ名/キー                                                                                    |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| アプリ名                                                   | **CFBundleDisplayName**。 このプロパティは、アプリの iOS プロジェクトの info.plist ファイル にあります。 |
| 店舗アイコンの名前と、対応するページ タイトル            | それぞれ、**MainTabs\_Products** と **Pages\_CategoryListPage\_Products**                       |
| 情報アイコンの名前と、対応するページ タイトル     | それぞれ、**MainTabs\_Account** と **Pages\_AccountPage\_AccountInformation**                   |
| トースト通知として表示される確認メッセージ   | TextResources.resx での複数のメッセージ                                                              |
| 「カートに追加」ボタンのテキストと、対応するページのタイトル | **Pages\_ProductDetail\_AddToCart** および **Pages\_CartPage\_Title**                     |
| 「チェック アウト」ボタンのテキストと、対応するページのタイトル    | **Pages\_CartPage\_Checkout** および **Pages\_CheckoutPage\_Title**                       |
| 「プレース ホルダー」ボタンのテキスト                                  | **Pages\_CheckoutPage\_PlaceOrder**                                                                  |
| ページ ラベルと対応するページ タイトルについて          | **Pages\_AccountPage\_About** および **Pages\_AboutPage\_Title**                          |

> [!NOTE]
> info.plist ファイルの一部のリソースは、iOS アプリでは使用されませんが、Android アプリで使用されます。 たとえば **MenuPage\_ 製品**です。 Android アプリに影響を与えずに、iOS アプリからこれらのリソースを変更することができます。

#### <a name="colors"></a>色

iOS アプリに表示される色を変更するには、config.xml ファイルを開き、**Primary** (アプリ バーの色)、**PrimaryDark** (ステータス バーの色)、<**Accent**、および **ActionButtonBackground** の値を変更します。 

> [!NOTE]
> 製品価格は、商品リスト ページと製品の詳細ページの 2 つのページに表示されます。 製品リスト ページに表示される価格は緑に設定 (\#008A00) に設定され、変更することはできません。 ただし、製品の詳細ページで表示される価格は、「PrimaryDark」プロパティで設定される値によって管理されます。

## <a name="build-test-and-distribute-apps"></a>アプリのビルド、テスト、および配布
次のステップでは、アプリを構築してデバイスでテストします。 テストは、パブリック アプリケーション格納にアプリケーションを発行することによって行われます。 Android および iOS のアプリの配布の基本を説明する、Xamarin と Apple からの標準の外部リンクを追加しました。

### <a name="android"></a>Android

エミュレータで Android アプリをテストするには、Visual Studio で次の手順を実行します

1.  スタートアップ プロジェクトとして Droid、Android デバイスとして Marshmallow を選択します。
2.  ビルド リリース | すべての CPU。
3.  Marshmallow エミュレーターで実行します。

署名証明書で署名できる **.apk ファイルを作成** するために Visual Studio でアーカイブ マネージャを使用する方法については、[アプリケーションをリリースする準備](https://developer.xamarin.com/guides/android/deployment,_testing,_and_metrics/publishing_an_application/part_1_-_preparing_an_application_for_release/#_Archive_for_Publishing_) を参照してください。

アドホックや Google Play ストア配布用の署名証明書および **.apk ファイルへの署名** を作成する方法の詳細は、[Android アプリケーション パッケージの署名](https://developer.xamarin.com/guides/android/deployment,_testing,_and_metrics/publishing_an_application/part_2_-_signing_the_android_application_package/#_Signing_the_APK_) を参照してください。

メール、プライベート Web サーバー、Google Play、または Android 用の Amazon App Store などのチャネルを介して Xamarin.Android で作成された **アプリケーションの公的配布** に関する手順の詳細は、[アプリケーションの公開](https://developer.xamarin.com/guides/android/deployment,_testing,_and_metrics/publishing_an_application/) を参照してください。

### <a name="ios"></a>iOS

エミュレータで iOS アプリをテストするには、Visual Studio で次の手順を使用します。

1.  iOS をスタートアップ プロジェクトとして選択します。
2.  上記の説明に従って Mac に接続する。
3.  ビルド リリース | iPhone。
4.  Visual Studio でアプリを実行します。

Xamarin.iOS アプリケーションで利用可能な配布方法の詳細は、[Xamarin.iOS アプリ配布の概要](https://developer.xamarin.com/guides/ios/deployment,_testing,_and_metrics/app_distribution/) を参照してください。

署名の ID と証明書を管理する方法の詳細は、[アプリの署名とは](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppDistributionGuide/MaintainingCertificates/MaintainingCertificates.html) を参照してください。 

> [!NOTE]
> 証明書を Apple 開発者エンタープライズ プログラムの一部として使用していて、手動でアプリをインストールする場合 (テストなど) は、手動で信頼を確立する必要があります。 詳細については [iOS にカスタム エンタープライズ アプリをインストールする](https://support.apple.com/HT204460) を参照してください。
