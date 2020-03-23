---
title: モバイル プラットフォームのリソース
description: モバイル プラットフォームを使用して、ワークスペースのモバイル アプリを作成できます。
author: RobinARH
manager: AnnBe
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 6e2601f863bc35e10b3e83d64efb6022c8524d43
ms.sourcegitcommit: 74d05a3a3de2e421eeab7117f2fd1fdaeb23f083
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117159"
---
# <a name="mobile-platform-resources"></a>モバイル プラットフォームのリソース

[!include [banner](../../includes/banner.md)]

モバイル アプリケーションを使用することにより、ビジネス ロジックおよびモデリングを再利用することができます。 モバイル アプリで、豊富なオフラインおよびモバイルの相互関係と、扱いやすいデザイナー体験を可能にします。 開発者は、Microsoft Visual Studio で簡単なフォームを作成し、この機能を公開するモバイル アプリを設計することができます。 モバイル プラットフォームを使用すると、フォームやモバイル アプリの定義を簡単に変更して、クラウド アプリに加えられたカスタマイズを組み込むことができます。 

## <a name="get-started"></a>はじめに

+ [はじめに](mobile-platform-getting-started.md) 
+ [アーキテクチャ](mobile-platform-architecture.md) 
+ [ページ デザインのガイドライン](page-design-guidelines.md)
+ [アクション デザインのガイドライン](action-design-guidelines.md)
+ [フォーム デザインの要件](form-design-requirements.md)

モバイル アプリの作成方法を示す次のハウツー ビデオ シリーズをチェック アウトしてください。

+ [チュートリアル 1: 販売注文のページを構築する](https://youtu.be/PdegfBxifl8)
+ [チュートリアル 2: 販売注文詳細ページを構築する](https://youtu.be/mF-vlbnRte0)
+ [チュートリアル 3: 新しい販売注文アクション作成を構築する](https://youtu.be/VYw9oTv9t3o)
+ [チュートリアル 4: 新しい販売注文アクション作成にルックアップを追加する](https://youtu.be/eNJKd0IYmZk)
+ [チュートリアル 5: ルックアップの追加し、モバイル ビジネス ロジックを使用してページを非表示にする](https://youtu.be/kIJKk9J8FvI)

## <a name="common-configurations"></a>一般的な構成
これらのトピックでは、モバイル アプリに追加できる一般的なカスタマイズについて説明します。

+ [モバイル ワークスペースのローカライズ](scenarios/localize-workspaces-on-server.md)
+ [モバイル ワークスペースのセキュリティを強化する](scenarios/secure-mobile-workspace.md)
+ [クリック可能なフィールドを設定する](scenarios/make-workspace-field-clickable.md)
+ [ワークスペース クラスを使用して必須フィールドを設定する](scenarios/make-field-mandatory.md)
+ [フィールドに品目数を表示する](scenarios/display-count-workspace.md)

## <a name="client-side-development"></a>クライアント側の開発

クライアント側の API はビジネス ロジック ファイルで使用されます。この API は、カスタマイズ可能なモバイルワーク スペースに拡張レイヤーを提供します。 クライアント側の API を通じてアクセスしたり操作したりできるものは次のとおりです。
+ メタデータ
+ ランタイム コントロール/ページ インスタンス
+ 業務データ
+ オフライン-最初の業務動作
+ レイアウトおよびスタイル

クライアント側の開発のプロセスは次のトピックで説明します。
+ [クライアント側の設計 API の概要](scenarios/client-api-design-overview.md)
+ [ビジネス ロジック イベントの概要](business-logic-events-overview.md)
+ [クライアント API](client-apis/client-apis-reference.md)

引当管理ワークスペースのためにサンプルのビジネス ロジック ファイル (.js ファイル名拡張子付き) をダウンロードすることができます。 [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**business_logic フォルダ**を開き、FM.js ファイルを指定します。

## <a name="server-side-development"></a>サーバー側の開発

ワークスペースの属性とクラスは、サーバー上でワークスペースを作成、構成、および公開するために使用されます。 タスク レコーダー ベースのメカニズムを使用してワークスペースを構築する代わりに、これらのサーバー側 X++ API を使用できます。 いずれかのメカニズムを使用して作成されたワークスペースは、クライアント側 API を使用してスタイルを設定して強化することができます。

サーバー側開発は、次のトピックで説明します。
+ [ワークスペース クラスの概要](scenarios/mobile-workspace-configuration.md)
+ [サーバー APIs (X++)](mobile-workspace-server-apis.md)

フリート管理モバイル アプリのサンプル プロジェクト (.axpp ファイル名拡張子付き) をダウンロードすることができます。 [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**FMMobileApp.axpp** ファイルをダウンロードします。

## <a name="debugging-during-development"></a>開発時のデバッグ

展開中に、バックグラウンドで何が起きているのかをより詳細な情報と洞察を得るために、デバッガーを添付すると便利です。 Web デバッガーは、クライアント側の JavaScript ロジックとスタイルで使用することができ、Visual Studio デバッガーは、サーバー側の X++ ビジネス ロジックで使用できます。

### <a name="debugging-the-client-side"></a>クライアント側のデバッグ 

#### <a name="prerequisites"></a>必要条件
- Android デバイスに加えて PC
- Azure でホストされた開発マシン (モバイル デバイスで指定できます)

#### <a name="steps-to-debug-the-client-side"></a>クライアント側をデバッグする手順
1. Azure でホストされた開発マシンで公開されている Web クライアントで、Finance and Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。 モバイル ワークスペースを公開する方法については、 [モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。

2. Android デバイスで、Finance and Operations アプリの Android デバッグ apk をインストールします。
    - 1 回のみ、apk ファイルのインストールを許可 -  **メニュー** > **設定** > **セキュリティ**の順に移動し、電話が Google Play ストア以外のソースからアプリをインストールするのを許可するよう**未知のソース**を確認します。
    - Finance and Operations アプリのアンインストール - Finance and Operations アプリの以前のバージョンがアンインストールされていることを確認します。
    - apk ファイルのダウンロード - デバイスのブラウザーから、最新の [GitHub 上の Finance and Operations Android デバッグ apk](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/blob/master/android-debug.apk) に移動し、**ダウンロード** (または [ファイルへの直接リンク](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/raw/master/android-debug.apk)) をクリックします。
    - Finance and Operations apk ファイルのインストール - apk ファイル経由で Finance and Operations アプリのインストールを確認します。
    - デバイスのデバッグ Finance and Operations アプリを実行し、サインインします。

3. デバッグ マシンからデバイスに接続します。

    - Azure でホストされた開発マシンまたは別の PC で、「[リモート デバッグ Android デバイスで開始](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/)」する Android 開発者指示に従います。 また、「[Android 用 Chrome のリモート デバッグ](https://www.youtube.com/results?search_query=chrome+for+android+remote+debugging)」を検索することにより、YouTube 上で多様な説明ビデオを見つけることができます。 
    
4. デバッガーに接続した後は、デバイスの有効タブを見つけます。 Android で**その他のタブを表示**をクリックすることが必要な場合があります。 タブのいずれかは、`/www.index.html#/app/appList`または`/www.index.html#/app/app_landing`のようになります。 

    **ファイル** > (ドメインなし) > **ExpenseMobile.js** などのワークスペース JavaScript を表示するには、ノードを展開します。 JavaScript ファイルをクリックして表示し、ブレークポイントを追加します。
    
    ![経費管理モバイル ワークスペース](./media/expense-management-mobile-workspace.png)
    
5. デスクトップ画面に操作できるように、デスクトップにモバイル デバイスを反映します。 

6. 目的のワークスペースとフォームを通して移動します。

7. ブレークポイントが発生した場合、ブラウザーの開発者ツールにより実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。 

8. 実行時にスタイル設定を変更するのにには、要素タブを使用してスタイル設定を変更します。 これは、JavaScript がどの要素を対象にすべきかを決定し、要素のスタイルを設定する方法を決定するのに役立ちます。

9. 必要な変更が指定された場合は、JavaScript では、それらの変更がなされ、環境にこれらの変更をプッシュします。

10. 詳細の変更や検証が必要な場合は、プロセスを繰り返します。

### <a name="debugging-the-server-side"></a>サーバー側のデバッグ

#### <a name="prerequisites"></a>前提条件
- Azure でホストされた開発マシン (モバイル デバイスで指定できます)

#### <a name="steps-to-debug-the-server-side"></a>サーバー側をデバッグする手順
1. Azure でホストされた開発マシンで公開されている Web クライアントで、Finance and Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。 モバイル ワークスペースを公開する方法については、 [モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。

2. アプリをデバイスで開いて、Azure でホストされた開発マシンを参照し、サインインします。

3. 開発マシンでホストされる Azure で Visual Studio を開き、w3wp プロセスにデバッガーを追加します。

4. デバッガーに接続した後、目的のビジネス ロジックを見つけ、必要に応じてブレークポイントを挿入します。

5. 通常どおりデバイスでアプリを使用するか、またはデスクトップにモバイル デバイスを反映させて、デスクトップ画面でモバイル デバイスとやりとりすることが可能です。

6. 目的のワークスペースとフォームを通して移動します。

7. ブレークポイントが発生した場合、Visual Studio により実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。 

8. 必要な変更が指定された場合は、X++ では、それらの変更がなされ、環境にこれらの変更をプッシュします。

9. 詳細の変更や検証が必要な場合は、プロセスを繰り返します。

## <a name="troubleshooting-the-app"></a>アプリ の トラブルシューティング
### <a name="the-mobile-client-app-is-not-working-on-particular-devices"></a>モバイル クライアント アプリ が 特定のデバイスで動作しない
アプリと関連付けられているキャッシュが動作不良の原因となる場合があるため、これらを削除してください。 ただし、アプリケーションに関連付けられているデータをクリアする唯一の方法は、アプリケーションをアンインストールすることです。
アプリケーションを完全にアンインストールするには、"長押ししてゆらゆらした状態でアプリ アイコンの x を押す" 方法を使用しないでください。 代わりに、**設定** > **全般** > **iPhone ストレージ** > **Finance and Operations (Dynamics 365)** の順に移動し、**アプリの削除**をクリックしてアプリを完全にアンインストールします。 10 ～ 15秒後、アプリケーションを再インストールすることができます。

### <a name="on-android-devices-with-non-english-regions-the-comma-cant-be-used-as-the-decimal-separator-in-an-amount-field"></a>英語圏以外の Android デバイスでは、カンマが金額フィールドで小数点の記号として使用できない場合があります
英語圏以外の Android デバイスでは、カンマを小数点の記号として標準使用してください。 金額フィールドで発生するカンマの問題は、 Android 固有の問題であり、iPhone では発生していません。 Android における金額フィールドのカンマ問題は、既定のキーボードとされている「gboard」やその他のキーボードが原因で発生しています。 SwiftKey キーボード (Microsoft 製) をインストールすることで、iPhone のようなカンマ入力が可能となります: [SwiftKey キーボード](https://www.microsoft.com/swiftkey)。

### <a name="change-needed-for-adfs-to-support-mobile-client-in-on-premises-environments"></a>ADFS がオンプレミス環境でモバイル クライアントをサポートするために必要な変更 
Active Directory フェデレーション サービス (AD FS) がドメインで使用されていて、かつオンプレミス環境の場合は、 Windows Integrated Authentication (WIA) ではなく、 **ADFS を構成して従来のフォームを使用した認証画面** を使用してください。 iOS と Android の Finance and Operations アプリには、標準のフォーム ベースの認証画面が必要です。 ADFS は、ブラウザー クライアント (ユース ケース) のみ WIA を提供するように構成する必要があります。 このスクリプトおよび問題の詳細については、[WIA に対応していないデバイスに向けたイントラネットのフォームベースの認証を構成する](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/configure-intranet-forms-based-authentication-for-devices-that-do-not-support-wia)を参照してください。

### <a name="using-multi-factor-authentication-with-the-finance-and-operations-app"></a>Finance and Operations アプリで多要素認証を使用する
Finance and Operations (モバイル クライアント) アプリでは、埋め込みブラウザー内に Azure AD サインインの Web ページを表示することにより、Azure Active Directory (Azure AD) でのユーザー認証を容易に行えるようにします。 正常にサインインをすると、クッキーからユーザーのトークンを取得して、これは対話サービスでのやりとりに使用されます。またこれは web クライアントに共有されます。 多要素認証の仕様上、デバイス内で別のアプリへの切り替えを行うと埋め込みブラウザが閉じられてしまうため、サインインができなくなることがあります。 この問題を回避するには:

- 別のデバイス - 別のデバイスを使って多要素認証への応答をすることで、元のデバイス上ではアプリ がアクティブな状態を維持することができます。
- 電話を使った多要素認証 - 多要素認証の応答に電話を使用することでアプリの切り替えが不要になります。
- これを回避するには、認証通知を「長押し」したまま**承諾**オプションをクリックします。 通知の承諾ではアプリの切り替えは必要ないため、サインインが通常どおりに実行されます。

MFA 認証で継続的な問題がある場合は、[Microsoft Authenticator アプリ ログの送信](https://github.com/AzureAD/azure-activedirectory-library-for-objc/wiki/Instructions-on-Collecting-Microsoft-Authenticator-Logs) に役立ち、結果のインシデント ID に対するサポートを提供します。

### <a name="intune-support-and-conditional-access"></a>Intune サポートと条件付きアクセス
Finance and Operations (モバイル クライアント) アプリには Microsoft intune ポリシーが実装されていないため、Intune は最初はサポートされません。 ただし、このアプリは無料で [Intune ](https://docs.microsoft.com/mem/intune/apps/store-apps-ios) に追加して、[Intune を持つ条件的なアクセス](https://docs.microsoft.com/mem/intune/protect/conditional-access#use-conditional-access-with-intune) を使用するようなシナリオをサポートすることができます。

### <a name="trouble-signing-out-of-the-app-and-signing-in-with-new-credentials"></a>新しい資格情報でアプリからサインアウト、またはログインすると問題が発生します。
新しい資格情報を使用してアプリからサインアウト、またはログインすることで問題が発生する場合は、 Azure AD サインイン画面にて [古い資格情報の破棄] を選択する必要があります。
- アプリからサインアウトするには、次の手順に従ってください
    - アプリを開く
    - アプリからサインアウトします。
    - アプリを強制終了します。
- 古い資格情報を破棄するには、次の手順に従ってください。
    - アプリを開く
    - サーバーに接続します。
    - Azure AD のサインイン画面で、資格情報が保存されている場合は、そのカードの省略記号 (...) ボタンをクリックし、 **資格情報の破棄** を選択します。
    - アプリを強制終了します。
- アプリにサインインするには、次の手順に従ってください
    - アプリを開く
    - サーバーに接続します。
    - Azure AD のサインイン画面にてログインします。

## <a name="troubleshooting-app-content"></a>アプリ コンテンツ に関する トラブルシューティング

### <a name="i-cant-figure-out-how-to-build-or-change-something-in-my-mobile-client-content"></a>モバイル クライアント コンテンツをビルドまたは変更する方法がわかりません
多くのリソースを活用して、モバイル クライアントのコンテンツをビルドまたは変更する方法を理解できます。
- ヘルプ システムに用意されているドキュメントを確認します。
- 例については、[フリート管理のサンプル](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples)を確認してください。
- たとえば、経費管理ワークスペース、および他の標準ワークスペースを発行して確認します。 USSI 企業のデモ データは、経費管理ワークスペースを使用する場合に便利です。 経費管理ワークスペースを構成するフォームおよび X++ コードは、接頭語 "ExpenseMobile" を検索してアプリケーション エクスプローラーで見つけることができます。
- 答えを検索し、必要に応じて質問することにより、[Dynamics コミュニティ フォーラム](https://community.dynamics.com/ax/f/33)を活用してください。

### <a name="tips-for-workspace-creation-and-modification"></a>ワークスペースの作成および変更に関するヒント
ワークスペースの作成および変更に関するヒントを以下に示します。
- 大規模で複雑なフォームを記録するのではなく、記録用の簡略化されたフォームを新しく作成します。
- フォームを記録したら、**完了**をクリックする代わりにフォームを閉じる必要があります。そうしないと、フォームは開いたままです。
- "ジョブ ステップ" を使用して記録が正しいことを確認します。
- タスク レコーダーの再生を使用して記録を再生し、確認します。
- 前のページのコンテキストをキャプチャする必要があるため、記録を開始する前にページに移動しないでください。
- グリッドのあるページを記録し直す場合は、[詳細] ページへのリンクをもう一度記録する必要があります。そうしないと、リンクがページに含まれないためです。
- アクションを記録するときは、フィールドに追加する値を変更します。 記録が完了したら、**保存**をクリックする代わりににフォームを閉じます。
- 携帯のルックアップは、記録済みのリスト ページです。 **保存する値としてフィールドを使用する** (データ) および**ユーザーに表示するフィールド** (表示) を選択するには、それぞれ**フィールド データの選択**および**表示するフィールドを選択します**を使用します。
- ルックアップ フィールドを追加する場合は、ルックアップ フィールドを追加するだけでなく、ルックアップで値を選択します。 これにより、正しい値が選択されます。
- ルックアップを再記録する場合は、ルックアップの GUID が変更されるため、すべての参照も再記録する必要があります。
- ページにフィールドを追加する場合は、すべてのフィールドをもう一度追加する必要があります。これは、各編集の最初にリストがクリアされるためです。 これは、タスク レコーダーの制限です。 並べ替えもできないことに注意してください。
- XML のワークスペースでは、フォームやコントロールへの参照に名前ではなく GUID が使用されます。 GUID は一意性を確保するために使用されますが、これは保守に影響します。 これらの GUID は変更ごとに再生成されるため、部分的な編集は非常に困難です。 GUID の使用を変更するには多大なコストがかかるため、より簡単な文字列名の参照を使用するための変更が将来加えられる可能性はあまりありません。
- フォームのデータソースの間のリレーションシップは、文字列ではなく RecordId を介する必要があります。 たとえば、データソースの主キーは文字列にできません。
- 顧客やパートナーは、ワークスペースのコピーを作成してワークスペースをフォークしてから、必要に応じて変更を加えることができます。
- モバイルにはチェック ボックスはありません。 JavaScript で、フィールドを Yes/No 列挙型に手動でバインドする必要があります。

### <a name="common-problems-with-form-recordings"></a>フォームの記録に関する一般的な問題
ワークスペースの記録を作成するときは、次のパターンやコントロールをフォームで使用しないでください。
- DelayedJoin を使用するデータソース (トランザクション フォームに共通)。
- クイック タブ (既存のフォームに共通)。
    - クイック タブの展開状態が再生を妨げる可能性があるため、記録されたフォームにクイック タブを含めることはできません。
- 展開可能なリージョン、リージョンの表示/非表示などの状態を持つユーザー インターフェイス (UI)。
- モバイルにはチェック ボックスはありません。 JavaScript で、フィールドを Yes/No 列挙型に手動でバインドする必要があります。
