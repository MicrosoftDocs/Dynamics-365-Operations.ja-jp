---
title: "オンプレミス環境での小売チャネルのコンポーネントのインストール手順"
description: "このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。"
author: jashanno
manager: AnnBe
ms.date: 12/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: eeccbe753cd4adf86665a3c6a372fdbfca371799
ms.openlocfilehash: 1be5c062f41677a9a5e22d8bed871bdf9219de2a
ms.contentlocale: ja-jp
ms.lasthandoff: 12/19/2018

---

# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a>オンプレミス環境での小売チャネルのコンポーネントのインストール手順

[!include[banner](../includes/banner.md)]

このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。

## <a name="overview"></a>概要

オンプレミス環境では、小売チャネル機能は Retail Store Scale Unit の使用により排他的に有効になります。 Retail Store Scale Unit の概要については、[Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md) を参照してください。 

クラウド展開とは異なり、オンプレミス環境では Lifecycle Services (LCS) 経由で小売チャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。 Retail Store Scale Unit をインストールすることによってのみ、小売チャネル コンポーネントを使用できます。

## <a name="prerequisites"></a>前提条件 

小売チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。 この手順は、[オンプレミス環境の設定と配置 (Platform update 12 以降)](setup-deploy-on-premises-pu12.md)で説明されています。 さらに、Retail の全機能を使用するは、バージョン 8.1.1 をインストールする必要があります。 バージョン 8.1.2 に更新することをお勧めします。

> [!Note]
> パブリックにアクセスできないセキュリティで保護されたネットワークを使用して、Retail Store Scale Unit (RSSU) を小売用バック オフィスに接続することが重要です。 さらに、小売用バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の RSSU デバイスのみに許可されるように制限してください。 つまり、ファイアウォールが存在する必要があります。ホワイトリストへの追加を強くお勧めします。

## <a name="installation-steps"></a>インストール手順

1.  以前に作成した[ファイル共有](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu12#setupfile)で、共有の場所のルート ディレクトリに **selfservicepackages** と呼ばれる新しいフォルダーを作成します。  
2.  各 AOS コンピューターで、簡単にアクセスできるディレクトリを作成します (**C:/selfservicepackages** など)。  次に、その AOS コンピューターで次の PowerShell スクリプトを実行します。

```powershell
.\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database>' -DatabaseName '<Database name for AOS database>' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages, such as **C:/selfservicepackages**>’ -SendProductSupportTelemetryToMicrosoft
```
  > [!NOTE]
  > - パラメーター **-DatabaseServer** および **-DatabaseName** が環境設定に基づいて既知である必要があります。
  > - パラメーター **- envName** は、環境が生成されるときに作成時に既知である必要があります。
  > - パラメーター **-RetailSelfServicePackages** は、この手順の最初で作成したフル パスの場所です (**C:/selfservicepackages**)。
  > - パラメーター **-SendProductSupportTelemetryToMicrosoft** は、Microsoft へのテレメトリを有効にするための必須の値です。  これは、Microsoft によるサポートを最大限に受けるために不可欠です。
  > - このスクリプトはと、Retail サービスのユーザーとロールの更新や、Retail レジストリ キーの更新を含むさまざまなアクションを実行します。
  
3.  LCS からバイナリ更新プログラムをダウンロードします。 手順については、[Lifecycle Services (LCS) から更新プログラムを入手](../migration-upgrade/download-hotfix-lcs.md)を参照してください。
4.  ZIP ファイルを展開し、すべてのセルフ サービス インストーラーを、手順 2 において各 AOS コンピューターで定義および作成された **C:/selfservicepackages** フォルダーにコピーします。 6 つのセルフ サービス インストーラーは次のとおりです。 
    - AsyncServerConnectorServiceSetup.exe
    - RealtimeServiceAX63Setup.exe
    - HardwareStationSetup.exe
    - ModernPosSetup.exe
    - ModernPosSetupOffline.exe
    - StoreSystemSetup.exe
5.  ADFS コンピューターに移動し、インフラストラクチャ フォルダーに移動します。 これは、以前に実行した Retail PowerShell スクリプトがあったのと同じファイル ディレクトリです (**RetailUpdateDatabase.ps1**)。 PowerShell スクリプト **Create-ADFSServerApplicationForRetail.ps1** を見つけます。
6.  現在表示している ADFS コンピューターで、**.\Create-ADFSServerApplicationForRetail -HostUrl 'https://ax.d365ffo.onprem.contoso.com'** コマンドを使用して、新しい PowerShell ウィンドウ内においてこのスクリプトを実行します。**HostUrl** 値は Service Fabric にあります。  **HostUrl** 値を見つけるには、**Service Fabric** &gt; **アプリケーション ファブリック:/AXSF** &gt; **詳細** &gt; **Aad_AADValidAudience** に移動します。
7.  AD FS 管理の **アプリケーション グループ** から新しく生成されたサーバー アプリケーションにアクセスします。
8.  新しく生成されたサーバー アプリケーションを編集し、**シークレットをリセット** を選択します。

  > [!NOTE]
  > これは、各 Retail Store Scale Unit でこのスクリプトを実行する重要なセキュリティ手法です。  これにより、セキュリティが最大化され、セキュリティ侵害が発生した場合のワークロードが最小化されます。 
  >
  > このシークレットを安全に保つことが重要です。 このシークレットは、1 回だけコピーしてください。システムに保存しないでください。  生成されたクライアント ID とシークレットは、Retail Store Scale Unit インストーラーの実行中に使用されるため、後で使用する必要があります。  シークレットはいつでも再度リセットできますが、前のシークレットを使用した Retail Store Scale Unit で更新する必要があります。

9.  **Retail** &gt; **小売本社の設定** &gt; **小売用スケジューラ** &gt; **Connector for Microsoft Dynamics AX** に移動します。
10.  アクション ウィンドウで **編集** を選択します。
11.  **プロファイル** フィールドに、**既定**値を入力します。  必要に応じて、**説明** フィールドに説明を入力します。

  > [!NOTE]
  > 手順 12 ～ 14 の以下のフィールドには既に値が入っている可能性があります。 これが発生した場合、この手順を省略し、そこから先に進みます。 選択可能なプロファイル タイトル (この場合は既定値) があることが重要です。

12.   **Web アプリケーション名** フィールドに、**RetailCDXRealTimeService** と入力します。
13.  **プロトコル** フィールドで、**https** を選択します。
14.  **共通名** フィールドに、**AXServiceUser@contoso.com** と入力します。
15.  アクション ウィンドウで、**保存** を選択します。
16.  小売用バックオフィスで、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
17.  **セキュリティ** タブを選択します。
18.  下位ヘッダー **取引サービスのレガシ プロパティ** で **Real-time Service プロファイル** フィールドを選択し、新たに作成した **既定** 値を選択します。
19.  **ID プロバイダー** タブを選択します。
20.  **ID プロバイダー**クイック タブで、**追加**を選択します。
21.  新しい **発行者** 行で、新しい ID プロバイダー値 **https://sts.windows.net/** をフィールドに入力します。
22.  アクション ウィンドウで、**保存** を選択します。
23.  **小売** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売パラメーター**の順にを移動します。
24.  **全般** タブで、**初期化** リンクを選択し、Retail 機能のシード データを構成します。

  > [!NOTE]
  > 初めてダウンロードが試みられるとき、インストーラーは関連するページからダウンロードされません。  これは、インストーラーはダウンロードの場所に配置されているだけであり、関連付けられているデータベースの値がまだ存在しないためです。  本社で、**ダウンロード**機能が試行されると (たとえば、Retail Store Scale Unit または Retail Modern POS)、エラーが表示され、2 回目にダウンロードが試みられたときにインストーラーをダウンロードできるようにする自動アップロード機能が開始されます。 (インストーラーのダウンロードがもう一度試みられるまで 1 分待ってください)。

25. Retail Store Scale Unit をインストールするためのインストール手順に従います。 手順については、[Retail Store Scale Unit のコンフィギュレーションとインストール](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md)を参照してください。  このドキュメントの複数の場所に、オンプレミス配置の指示に対する変更を参照するメモがあります。 これらの変更を記録することが重要です。 

