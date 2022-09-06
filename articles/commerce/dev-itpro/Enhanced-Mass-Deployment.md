---
title: シールされた Commerce セルフサービス コンポーネントの一括配置
description: この記事では、セルフサービス コンポーネント インストーラーのフレームワークを使用して、サイレント インストールおよびサービス展開を行う方法について説明します。
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 66a711aff90221e594f4b2a0df3735eac93d0c9b
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387022"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>シールされた Commerce セルフサービス コンポーネントの一括配置

[!include [banner](../includes/banner.md)]

この記事は、10.0.18 リリース以降、毎月リリースされ、Microsoft Dynamics Lifecycle Services (LCS) の共用資産ライブラリで使用可能な、シールド フレームワーク、コンポーネント インストーラーに適用されます。 これらの新しいインストーラーの最初のいくつかのリリースが **(プレビュー)** として指定されることに注意してください。 ただし、この指定の唯一の目的は、新しいインストーラーを区別し、Microsoft が新しい機能要件を使用するかどうかを決定するために行います。 これは、インストーラーが生産に対して有効ではないという意味ではありません。 これらの新しいインストーラーのリリースに基づいて、Microsoft は 2023 年 10 月またはその前後に古い (レガシ) インストーラーを廃止する予定です。 

この記事では、新しいインストーラーを使用して、サイレント インストールおよびコマンド ライン引数によるサービスの更新を実行する方法について説明します。 これらの引数を使用すると、さまざまな方法で一括配置を行うことができます。

> [!NOTE]
> 新しいセルフサービスのシールド インストーラーは本社では使用できず、LCS によってのみダウンロードできます。

## <a name="delimiters-for-mass-deployment"></a>一括配置の区切り記号

次のテーブルに、コマンド ライン実行で使用できる区切り記号を示します。


| 区切り記号                 | 説明 |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | Microsoft Azure Active Directory (Azure AD) トークン発行者の接頭語。 |
| -AsyncClientAadClientId | Async Client が本社との通信中に使用する必要がある Azure AD クライアント ID。 |
| -AsyncClientAppInsightsInstrumentationKey | Async Client AppInsights インストルメンテーション キー。 |
| -AsyncClientCertFullPath | 本社との通信のために Azure AD で認証するために使用する必要がある、Async Client ID 証明書の場所の検索メトリックとして拇印を使用する完全に書式設定された URN パス。 たとえば、`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` が正しく書式設定された URN です。 値 **\<MyThumbprint\>** は、使用する必要のある証明書の拇印に置き換えられます。 このパラメータは、**-AsyncClientCertThumbprint** パラメータと一緒に使用しないでください。 |
| -AsyncClientCertThumbprint | 本社との通信で Azure AD でするために使用する必要がある Async Client ID 証明書の拇印。 この拇印は、**LocalMachine/My ストア** の場所と名前を検索して、使用する正しい証明書を見つけるために使用します。 このパラメータは、**-AsyncClientCertFullPath** パラメータと一緒に使用しないでください。 |
| -ClientAppInsightsInstrumentationKey | クライアント AppInsights インストルメンテーション キー。 |
| -CloudPosAppInsightsInstrumentationKey | Cloud POS AppInsights インストルメンテーション キー。 |
| -コンフィギュレーション | インストール時に使用する構成ファイル。 ファイル名の例は **Contoso.CommerceScaleUnit.xml** です。 |
| -CposAadClientId | デバイスの有効化中に Cloud POS が使用する必要がある Azure AD クライアント ID。 このパラメータは、オンプレミスの配置に必要ありません。 |
| -デバイス | 本社の **デバイス** ページに表示されるデバイス ID。 |
| -EnvironmentId | 環境 ID。 |
| -HardwareStationAppInsightsInstrumentationKey | Hardware Station AppInsights インストルメンテーション キー。 |
| インストール | このインストーラーが提供するコンポーネントをインストールするかどうかを指定するパラメーター。 インストールを実行する際にはこのパラメータが必要で、先頭にダッシュ文字はありません。 |
| -InstallOffline | Modern POS の場合、このパラメータは、オフライン データベースもインストールして構成する必要があることを指定します。 **-SQLServerName** パラメータも使用します。 それ以外の場合、インストーラーは前提条件を満たす既定のインスタンスを見つけようとします。 |
| -ポート | Retail Server 仮想ディレクトリに関連付けられて使用されるポート。 ポートが設定されてない場合、既定のポート 443 が使用されます。 |
| -登録 | 本社の **登録** ページに表示される登録 ID。 |
| -RetailServerAadClientId | Retail Server が本社との通信中に使用する必要がある Azure AD クライアント ID。 |
| -RetailServerAadResourceId | デバイスの有効化中に使用するRetail Server Azure AD アプリ リソース ID。 このパラメータは、オンプレミスの配置に必要ありません。 |
| -RetailServerCertFullPath | 本社との通信のために Azure AD で認証するために使用する必要がある、Retail Server ID 証明書の検索メトリックとして拇印を使用する完全に書式設定された URN パス。 たとえば、`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` は正しく書式設定された URN であり、値 **\<MyThumbprint\>** は使用する必要のある証明書の拇印に置き換えられます。 このパラメータは、**-RetailServerCertThumbprint** パラメータと一緒に使用しないでください。 |
| -RetailServerCertThumbprint | 本社との通信で Azure AD でするために使用する必要がある Retail Server ID 証明書の拇印。 この拇印は、**LocalMachine/My** ストアの場所と名前を検索して、使用する正しい証明書を見つけるために使用します。 このパラメータは、**-RetailServerCertFullPath** パラメータと一緒に使用しないでください。 |
| -RetailServerURL | インストーラーが使用する Retail Server URL。 (この URL は Commerce Scale Unit \[CSU\] URLとも呼ばれています。) Modern POS の場合、この値はデバイスの有効化中に使用されます。 |
| -SkipAadCredentialsCheck| Azure AD 資格情報の前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipCertCheck | 証明書の前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipIisCheck | インターネット インフォメーション サービス (IIS) の前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipNetFrameworkCheck | .NET Framework の前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipScaleUnitHealthcheck | インストールされているコンポーネントの正常性チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipSChannelCheck | セキュリティ チャネルの前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipSqlFullTextCheck | フル テキスト検索を必要とする SQL Server の前提条件の検証をスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SkipSqlServerCheck | SQL Server の前提条件チェックをスキップする必要があるかどうかを示す切り替え。 既定値は **false** です。 |
| -SqlServerName | SQL Server 名。 名前が指定されていない場合、インストーラは既定のインスタンスを見つけようとします。 |
| -SslcertFullPath | スケール ユニットへの HTTP トラフィックを暗号化するために使用する必要がある証明書の場所の検索メトリックとして拇印を使用する、完全に書式設定された URN パス。 たとえば、`store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` は正しく書式設定された URN であり、値 **\<MyThumbprint\>** は使用する必要のある証明書の拇印に置き換えられます。 このパラメータは、**-SslCertThumbprint** パラメータと一緒に使用しないでください。 |
| -SslCertThumbprint | スケール ユニットに対する HTTP トラフィックを暗号化するために使用する必要がある証明書の拇印。 この拇印は、**LocalMachine/My ストア** の場所と名前を検索して、使用する正しい証明書を見つけるために使用します。 このパラメータは、**-SslCertFullPath** パラメータと一緒に使用しないでください。 |
| -StoreSystemAosUrl | 本社 (AOS) URL。 |
| -StoreSystemChannelDatabaseId | チャネル データベース ID (名前)。 |
| -TenantId | Azure AD テナント ID。 |
| -TransactionServiceAzureAuthority | Transaction Service Azure AD オーソリティ。 |
| -TransactionServiceAzureResource | Transaction Service Azure AD リソース。 |
| -TrustSqlServerCertificate | SQL Server への接続が確立されている間にサーバー証明書を信頼する必要があるかどうかを示す切り替え。 セキュリティ リスクを回避するために、運用配置は、ここで **true** の値を指定しないでください。 既定値は **false** です。 |
| -Verbosity | インストール中に要求されるログのレベル。 通常、この値は使用しないでください。 |
| -WindowsPhoneAppInsightsInstrumentationKey | Hardware Station AppInsights インストルメンテーション キー。 |

## <a name="general-overview"></a>一般的な概要

セルフサービス インストーラーの新しいフレームワークには、さまざまな機能と改善があります。 新しいフレームワークは現在、Modern POS、ハードウェア ステーション、および CSU (自己ホスト) のインストーラーのみを生成します。 シールド インストーラーの基本的なコマンド ラインの使用法を理解することは重要です。それは次の例で使用されているもののようになります。 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

インストーラーには、パラメーター **インストール** (またはインストールを削除するには **アンインストール**) とそのインストールに固有のパラメーターが必要です。 **パラメーター名** には、レジスター、CSU URL、または証明書情報などの必要なパラメーターを含める必要があります。 **パラメーター情報** には、パラメーターに関する追加情報が含まれる必要があります。

シールド フレームワークは、次の変更ができるように作成されています。
- **シールド** – 新しいインストーラー フレームワークは、Microsoft 基本コンポーネント インストーラーを、拡張性ベースのカスタマイズから完全に分離します。 カスタマイズは後でインストールされますが、更新に関しては解除されます (そのため、更新は Microsoft 基本コンポーネントのみ、カスタマイズのみ、またはその両方で許可されます)。
- **GUI-less** – ユーザー インターフェイス (UI) は使用されなくなりました。 代わりに、各コンポーネント インストーラーに完全にコマンド ライン駆動型の実行可能ファイルがあります。 この変更は、一括配置で使用する新しいインストーラー フレームワークに焦点を合わせるために使用されるいくつかのキー変更または機能の 1 つです。
- **より深いログ** – 強化されたインストーラー ログにより、インストールの完了または失敗、実行された手順、および生成された警告またはエラーをより適切に検証できます。
- **クリーンアップ** – 新しいフレームワークでは、コンポーネント インストーラーは、新しいコンポーネントをインストールする前に、コンポーネント フォルダーの内容全体をクリアすることにより、インストール ディレクトリのクリーン性を維持するために一生懸命作業します。 このクリーンアップにより、問題を引き起こしてインストールの成功を妨げる可能性のあるファイルが残っていないことが保証されます。

3つのコンポーネントは新しいフレームワークに移行されていません: 仮想周辺機器シミュレーター、Async Server Connector Service (Dynamics AX 2012 R3 サポートに使用)、およびリアル タイム サービス交換 (Dynamics AX 2012 R3 サポートに使用)。

> [!NOTE]
> インストーラはローカルに保存され、保持されます。  ディスク領域を浪費しないように、保持されているインストーラーを管理または削除することが、時間の経過とともに重要になります。 極端な状況からの回復のために、基本コンポーネントの現在のインストーラーと最新バージョンの拡張機能インストーラーを保持することをお勧めします。

## <a name="migration"></a>移行

古いセルフサービス フレームワーク コンポーネント インストーラーから新しいフレームワーク コンポーネント インストーラーに移行するには、古いコンポーネントをアンインストールする必要があります。

- **Modern POS** – 新しいインストーラー フレームワークにより、アプリケーションは新しいアプリケーション署名 ID を受け取ります。 したがって、新しいフレームワーク Modern POS コンポーネントがインストールされる前に、古いコンポーネントの完全なアンインストールが必要です。 完全なアンインストールが必要なので、デバイスの有効化が再度必要になります。 (このデバイスの最有効化は、アンインストールが再度発生しない限り、1 回限りの要件です。)
- **ハードウェア ステーション** – IIS Web サイトとして、新しいインストーラー フレームワークでは、基本フォルダー構造を再作業する必要があります。 したがって、新しいフレームワーク ハードウェア ステーション コンポーネントがインストールされる前に、古いコンポーネントの完全なアンインストールが必要です。
- **Commerce Scale Unit (CSU、セルフ ホスト型)** – 一連の IIS Webサイトとして、新しいインストーラー フレームワークでは、基本フォルダー構造を再作業する必要があります。  したがって、新しいフレームワーク CSU (自己ホスト) コンポーネントがインストールされる前に、古いコンポーネントの完全なアンインストールが必要です。

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>準備

古いセルフ サービス Modern POS コンポーネントを削除することが重要です。 詳細については、この記事で前述した移行手順を参照してください。

> [!NOTE]
> 開発者トポロジまたはデモ環境などのシングル コンピュータ システム上、または Commerce Scale Unit と Modern POS が同じコンピュータにインストールされている場合、Store Commerce がデバイス有効化を完了できない場合があります。 この問題は、Store Commerce が同じコンピュータへのネットワーク コール (つまり、それ自体の呼び出し) を行うことができないために発生します。 これは生産設定のシナリオではないはずですが、同じコンピュータに通信が行われるように、AppContainer ループバック例外を有効にして、この問題を軽減することができます。 この Lookback を可能にするのに役立つさまざまなアプリケーションが公開されています。 ループバックの詳細については、[ループバックの有効化およびネットワーク分離のトラブルシューティングの方法](/previous-versions/windows/apps/hh780593(v=win.10))を参照してください。 セキュリティ リスクの可能性があるため、絶対に必要な場合を除き、ループバックを使用することは推奨されないことを理解するのが重要となります。

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、Modern POS のインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-modern-pos"></a>Modern POS をサイレント インストール

次のコマンドにより、Modern POS がサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

次の基本的なコマンドは、インストールが要求された場合に使用可能なオプションを示しています。 最初にインストーラーをテストまたは使用する際に、このコマンドを使用することを強くお勧めします。

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Modern POS ではコンフィギュレーション ファイルは必要ありません。 インストーラーには、デバイスの有効化中に使用されるさまざまな値のパラメーター (この記事の前半で示した) があります。

次のコマンドは、Modern POS アプリケーションがインストールされた後にデバイスの有効化中に使用する必要があるすべてのパラメータを指定します。 この例では、Dynamics 365 Commerce デモ データで一般的に使用される値である、**Houston-3** レジスター を使用します。

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

次のコマンドは、オフライン データベースのインストールおよび構成に使用する必要があるパラメータを指定します。 SQL Server は、使用する必要のある構成ファイルと一緒に指定されます。

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

これらの概念を組み合わせて、必要なインストール結果を達成できます。

## <a name="hardware-station"></a>Hardware station

### <a name="before-you-begin"></a>準備

古いセルフ サービス ハードウェア ステーション コンポーネントを削除することが重要です。 詳細については、この記事で前述した移行手順を参照してください。 マーチャント アカウント情報ツールは使用されなくなりました。 代わりに、POS 端末がハードウェア ステーションとペアリングされると、マーチャント アカウント情報がインストールされます。 このインストーラーを最初にテストする際に、次のコマンドを実行することを強くお勧めします。

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、ハードウェア ステーションのインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-hardware-station"></a>ハードウェア ステーションのサイレント インストール

次のコマンドにより、ハードウェア ステーションがサイレントでインストール (または更新) されます。 現在インストールされているサービス コンポーネントに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

次の基本的なコマンドは、実行可能ファイル インストーラーを実行します。

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> ハードウェア ステーションでは構成ファイルは必要ありません。 インストーラーには、必要なさまざまな値のパラメーター (この記事の前半で示した) があります。

次のコマンドでは、標準インストール中に前提条件チェックをスキップするために必要なすべてのパラメータを指定します。 

> [!NOTE]
> 事前に詳細なテストを行わずに、または開発状況で、チェックをスキップすることはお勧めしません。

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

慣例として、これらの概念を組み合わせて、目的のインストール結果を達成するのが一般的です。

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (自己ホスト)

このインストーラーを最初にテストする際に、次のコマンドを実行することを強くお勧めします。

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>準備

古いセルフ サービス CSU (自己ホスト) コンポーネントを削除することが重要です。 詳細については、この記事で前述した移行手順を参照してください。

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、CSU (自己ホスト) のインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-csu-self-hosted"></a>CSU (自己ホスト) をサイレント インストール

次のコマンドにより、CSU (自己ホスト) がサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

他のセルフサービス インストーラーと比較すると、Commerce Scale Unit (CSU) の方が複雑で、大量の追加情報が必要になります。 次のコマンドは、コンフィギュレーション ファイルが存在しない場合に実行可能ファイル インストーラーを実行するために最低限必要なコマンド (パラメーターを含む) です。

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> CSU (自己ホスト) では構成ファイルがまだ必要とされます。

次のコマンドは、いくつかの代替パラメーターを使用して実行可能ファイル インストーラーを実行するより完全なコマンドです。

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

次のコマンドは、標準インストール中に前提条件チェックをスキップするために必要なパラメーターを指定します。 

> [!NOTE]
> 事前に詳細なテストを行わずに、または開発状況で、チェックをスキップすることはお勧めしません。


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

これらの概念を組み合わせて、必要なインストール結果を達成できます。

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
