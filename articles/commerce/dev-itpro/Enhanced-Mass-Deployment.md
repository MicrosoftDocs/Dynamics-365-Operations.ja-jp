---
title: シールド Commerce セルフサービス コンポーネントの一括配置
description: このトピックでは、セルフサービス コンポーネント インストーラーのフレームワークを使用してサイレント インストールおよびサービス配置の方法について説明します。
author: jashanno
manager: AnnBe
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9f0e1725fa6efe14d2864f233bd12cc64ddf24bc
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937026"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>シールド Commerce セルフサービス コンポーネントの一括配置

[!include [banner](../includes/banner.md)]

このトピックは、10.0.18 リリース以降、毎月リリースされるシールド フレームワーク コンポーネント インストーラーを対象としています。 この記事では、これらのインストーラーを使用して、サイレント インストールおよびコマンドライン引数によるサービスの更新を実行する方法について説明します。 これらの引数を使用すると、さまざまな方法で一括配置を実行できます。

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
| -インストール | このインストーラーが提供するコンポーネントをインストールするかどうかを指定するパラメーター。 このパラメーターは必須ではありません。 |
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

セルフサービス インストーラーの新しいフレームワークには、さまざまな機能と改善があります。 新しいフレームワークは現在、Modern POS、ハードウェア ステーション、および CSU (自己ホスト) のインストーラーのみを生成します。

- **シールド** – 新しいインストーラー フレームワークは、Microsoft 基本コンポーネント インストーラーを、拡張性ベースのカスタマイズから完全に分離します。 カスタマイズは後でインストールされますが、更新に関しては解除されます (そのため、更新は Microsoft 基本コンポーネントのみ、カスタマイズのみ、またはその両方で許可されます)。
- **GUI-less** – ユーザー インターフェイス (UI) は使用されなくなりました。 代わりに、各コンポーネント インストーラーの完全なコマンド ライン駆動型の実行可能ファイルがあります。 この変更は、一括配置で使用する新しいインストーラー フレームワークを焦点を合わせるために使用されるいくつかのキー変更または機能の 1 つです。
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

古いセルフ サービス Modern POS コンポーネントを削除することが重要です。 詳細については、このトピックで前述した移行手順を参照してください。

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、Modern POS のインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-modern-pos"></a>Modern POS をサイレント インストール

次のコマンドにより、Modern POS がサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

次の基本的なコマンドは、実行可能ファイル インストーラーを実行します。

```Console
ModernPOS.exe
```

> [!NOTE]
> Modern POS ではコンフィギュレーション ファイルは必要ありません。 インストーラーには、デバイスの有効化中に使用されるさまざまな値のパラメーター (このトピックの前半で示した) があります。

次のコマンドは、Modern POS アプリケーションがインストールされた後にデバイスの有効化中に使用する必要があるすべてのパラメータを指定します。 この例では、Dynamics 365 Commerce デモ データで一般的に使用される値である、**Houston-3** レジスター を使用します。

```Console
ModernPOS.exe -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

次のコマンドは、オフライン データベースのインストールおよび構成に使用する必要があるパラメータを指定します。 SQL Server は、使用する必要のある構成ファイルと一緒に指定されます。

```Console
ModernPOS.exe -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

これらの概念を組み合わせて、必要なインストール結果を達成できます。

## <a name="hardware-station"></a>Hardware station

### <a name="before-you-begin"></a>準備

古いセルフ サービス ハードウェア ステーション コンポーネントを削除することが重要です。 詳細については、このトピックで前述した移行手順を参照してください。 マーチャント アカウント情報ツールは使用されなくなりました。 代わりに、POS 端末がハードウェア ステーションとペアリングされると、マーチャント アカウント情報がインストールされます。

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、ハードウェア ステーションのインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-hardware-station"></a>ハードウェア ステーションのサイレント インストール

次のコマンドにより、ハードウェア ステーションがサイレントでインストール (または更新) されます。 現在インストールされているサービス コンポーネントに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

次の基本的なコマンドは、実行可能ファイル インストーラーを実行します。

```Console
HardwareStation.exe -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "mysslcertificatethumbprintoftenhasnumberstoo"
```

> [!NOTE]
> ハードウェア ステーションでは構成ファイルは必要ありません。 インストーラーには、必要なさまざまな値のパラメーター (このトピックの前半で示した) があります。

次のコマンドでは、標準インストール中に前提条件チェックをスキップするために必要なすべてのパラメータを指定します。

```Console
HardwareStation.exe -Config "HardwareStation.Houston.xml"
```

これらの概念を組み合わせて、必要なインストール結果を達成できます。

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (自己ホスト)

### <a name="before-you-begin"></a>準備

古いセルフ サービス CSU (自己ホスト) コンポーネントを削除することが重要です。 詳細については、このトピックで前述した移行手順を参照してください。

### <a name="examples-of-silent-deployment"></a>サイレント配置の例

このセクションでは、CSU (自己ホスト) のインストールに使用されるコマンドの例を示します。

#### <a name="silently-install-csu-self-hosted"></a>CSU (自己ホスト) をサイレント インストール

次のコマンドにより、CSU (自己ホスト) がサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造では、**&lt;InstallerName&gt;.exe** の基本値を使用します。

次の基本的なコマンドは、実行可能ファイル インストーラーを実行する基本的なコマンドです。

```Console
CommerceScaleUnit.exe -port 446 -SSLCertThumbprint "mysslcertificatethumbprintoftenhasnumberstoo" -retailservercertfullpath "store:///My/LocalMachine?FindByThumbprint=B48FCB4C8A6D6D54CF02D62D9EBFDF9A5929A469" -AsyncClientAadClientId "d3150d79-1d84-4f22-a9c3-5a6a3a41b1de" -RetailServerAadClientId "d3150d79-1d84-4f22-a9c3-5a6a3a41b1de" -CposAadClientId "bb8751eb-70c2-4410-a462-6dadb5b50e57" -RetailServerAadResourceId "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> CSU (自己ホスト) では構成ファイルがまだ必要とされます。

次の基本的なコマンドは、実行可能ファイル インストーラーを実行する完全なコマンドです。

```Console
CommerceScaleUnit.exe -port 446 -sslcertfullpath \"store:///My/LocalMachine?FindByThumbprint=7F506987C32A752E20E297C6E6E20943744439B3\" -asyncclientcertfullpath \"store:///My/LocalMachine?FindByThumbprint=B48FCB4C8A6D6D54CF02D62D9EBFDF9A5929A469\" -retailservercertfullpath \"store:///My/LocalMachine?FindByThumbprint=B48FCB4C8A6D6D54CF02D62D9EBFDF9A5929A469\" -AsyncClientAadClientId \"d3150d79-1d84-4f22-a9c3-5a6a3a41b1de\" -RetailServerAadClientId \"d3150d79-1d84-4f22-a9c3-5a6a3a41b1de\" -CposAadClientId \"bb8751eb-70c2-4410-a462-6dadb5b50e57\" -RetailServerAadResourceId \"https://retailstorescaleunit.retailserver.com\" -TrustSqlServerCertificate -Verbosity Trace -config \"Contoso.StoreSystemSetup.xml\"
```

次のコマンドは、オフライン データベースのインストールおよび構成に使用する必要があるパラメータを指定します。 SQL Server は、使用する必要のある構成ファイルと一緒に指定されます。

```Console
ModernPOS.exe -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

これらの概念を組み合わせて、必要なインストール結果を達成できます。

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
