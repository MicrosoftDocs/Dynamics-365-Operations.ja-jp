---
title: "AX 2012 R2 CU7 DIXF for SQL Server 2014 のインストール"
description: "Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) のデータ インポート/エクスポート フレームワークを SQL Server 2014 Integration Services またはそれ以降で使用するには、AX 2012 R2 CU7 をインストールして、更新プログラム KB 3018235KB 3018235 を適用する必要があります。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 71103
ms.assetid: ee28572c-e38d-4c2a-a191-f2631f291e5f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 4dec45384fad3e3f3ef84d32dcb69c04d418ed87
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="install-the-ax-2012-r2-cu7-dixf-for-sql-server-2014"></a>AX 2012 R2 CU7 DIXF for SQL Server 2014 のインストール

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 (CU7) のデータ インポート/エクスポート フレームワークを SQL Server 2014 Integration Services またはそれ以降で使用するには、AX 2012 R2 CU7 をインストールして、更新プログラム <a href="https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235">KB 3018235</a> を適用する必要があります。

次の手順は、SQL Server 2014 またはそれ以降のバージョンがインストールされている環境に適用されます。 SQL Server 2008 または SQL Server 2012 統合サービスを実行している場合は、更新プログラムのインストーラーを使用して Dynamics AX 2012 R2 CU7 のデータのインポート/エクスポート フレームワークをインストールすることができます。 詳細については、[データのインポート/エクスポート フレームワーク バイナリ更新プログラム (CU7) のインストール](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall) を参照してください。 データのインポート/エクスポート フレームワークでサポートされる統合サービスのバージョンを確認するには、[[Microsoft Dynamics AX 2012 のシステム要件](http://go.microsoft.com/fwlink/?LinkId=165377)] を参照してください。

## <a name="before-you-begin"></a>準備
1.  CU7 hotfix パッケージをダウンロードしてローカル フォルダーに展開します。 ダウンロードを抽出するには、[ダウンロードの手順に従い、CustomerSource、PartnerSource、または Lifecycle Services ](https://technet.microsoft.com/en-us/library/hh538446.aspx#Download) から更新プログラムを抽出します **。**
2.  [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) の修正プログラム パッケージをダウンロードしてローカル フォルダーに展開してください。

## <a name="install-the-ax-2012-r2-cu7-data-importexport-framework-for-use-with-sql-server-2014-integration-services"></a>SQL Server 2014 Integration Services で使用する AX 2012 R2 CU7 データのインポート/エクスポート フレームワークのインストール
Integration Services を実行しているコンピューターで、次の手順に従います。

1.  Windows PowerShell を実行します。
2.  修正プログラムのパッケージの Support フォルダーに移動します。
3.  次のスクリプトを実行します。

        Install-DIXFService.ps1.

4.  画面の指示に従ってください。
5.  Microsoft Dynamics AX 2012 R2 CU7 からデータ インポート/エクスポート フレームワーク サービス MSI を検索するように求められます。 このファイルは、**MSI\\ DIXF \_サービス\_x64** または **MSI\\DIXF\_サービス\_x86** フォルダーにあります。  スクリプトが対応する MSP を見つけることがない場合、探すように求められます。 MSP は、修正プログラム パッケージ フォルダー ([KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235))の **MSI\\DIXF\_Service\_x64** または **MSI\\DIXF\_Service\_x86** フォルダーにあります。 データ インポート/エクスポート フレームワーク サービスを、**ネットワーク サービス** アカウントでインストールするかどうかを求められます。 回答が**いいえ**である場合、サービスを実行するにはユーザー名とパスワード (ドメイン\\ユーザー名の形式) を入力するように求められます。 インストールを開始してください。

## <a name="verify-installation"></a>インストールの確認
既定では、スクリプトのログは **InstallDIXFService-&lt; 日付 &gt;\_&lt; 時間 &gt;.log** という名前のファイルに書き込まれます。 ファイルから正常なインストールの報告があったことを確認します。 インストールに失敗すると、**DIXFService\_インストール -&lt;日付&gt;\_&lt;時間 &gt;.log** という名前の MSI によりログが生成されます。 検索を行い、一覧表示された問題を調査します。

## <a name="install-the-data-importexport-framework-client-and-server-components"></a>データのインポート/エクスポート フレームワークのクライアントおよびサーバー コンポーネントのインストール
pw\_DMF サービス コンポーネントのインストールが完了した後、データのインポート/エクスポート フレームワーク クライアントと AOS コンポーネントを通常の方法でインストールします。

1.  適切なコンピューターにコンポーネントの CU7 バージョンをインストールします。 [データのインポート/エクスポート フレームワーク バイナリ更新プログラム (CU7) のインストール](https://technet.microsoft.com/en-us/library/hh538446.aspx#DIXFInstall) を参照してください。
2.  修正プログラム [KB 3018235](https://mbs2.microsoft.com/Knowledgebase/KBDisplay.aspx?scid=kb;en-us;3018235) を適切なコンピューターに適用します。

## <a name="optional-create-a-silent-installation-windows-powershell-script"></a>オプション: サイレント インストール Windows PowerShell スクリプトを作成します。
適切なパラメーターで **Install-DIXFService.ps1** スクリプトを指定した場合、サイレント インストールを行うには、スクリプトを使用することができます。 次のテーブルに、利用可能なパラメーターとその使用方法の簡単な説明を示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>パラメーター名</td>
<td>説明</td>
</tr>
<tr class="even">
<td>UseNetworkService</td>
<td>これは切り替えです。
<ul>
<li>ネットワーク サービス アカウントでサービスをインストールする場合は、コマンドに <strong>UseNetworkService</strong> を含めます。</li>
<li><strong>UseNetworkService</strong> が指定されている場合、<strong>ServiceAccount</strong> および <strong>ServicePassword</strong> に対して指定された値は無視されます。</li>
</ul></td>
</tr>
<tr class="odd">
<td>ServiceAccount</td>
<td>サービスが実行されるアカウントを指定します。 UseNetworkService が使用されていない場合は、このパラメーターを指定する必要があります。 これは、ドメイン \ ユーザー名の形式にする必要があります。</td>
</tr>
<tr class="even">
<td>ServicePassword</td>
<td>サービスが実行されるアカウントのパスワードを指定します。 <strong>UseNetworkService</strong> が使用されていない場合は、このパラメーターを指定する必要があります。</td>
</tr>
<tr class="odd">
<td>MSIFileName 必須</td>
<td>Microsoft Dynamics AX 2012 R2 CU7 修正プログラムの <strong>dixf_service_</strong><em>&lt;アーキテクチャ&gt;</em><strong>.msi</strong> のパス。 これは、相対パスまたは絶対パスにできます。</td>
</tr>
<tr class="even">
<td>MSPFileName</td>
<td><strong>dixf_service_</strong><em>&lt;アーキテクチャ&gt;</em><strong>.msp</strong> ファイルのパス。 修正プログラムのパッケージでサポート フォルダーの Install-DIXFService.ps1 スクリプトを実行すると、スクリプトがファイルを自動的に見つけることができる必要があるため、このパラメータは必須ではありません。</td>
</tr>
<tr class="odd">
<td>LogFileName</td>
<td>スクリプトのログ ファイルのパス。 このパラメータが設定されていない場合は、現在のディレクトリが使用されています。</td>
</tr>
<tr class="even">
<td>MSIExecLogFileName</td>
<td>実際のインストール ログが存在する場所である MSIExec のログ ファイルのパス。 このパラメータが設定されていない場合は、現在のディレクトリが使用されています。</td>
</tr>
</tbody>
</table>



### <a name="example-1-install-under-network-service-and-use-default-log-file-paths"></a>例 1: ネットワーク サービスの下でインストールし、既定のログ ファイルのパスを使用

    Install-DIXFService.ps1 -UseNetworkService -MSIFileName "C:\CU7Package\MSI\dixf_service_x64\dixf_service_x64.msi"

### <a name="example-2-install-as-a-specific-user-and-specify-log-file-paths"></a>例 2: 特定のユーザーとしてインストールおよびログファイルパスを指定

    Install-DIXFService.ps1 -ServiceAccount "MYDOMAIN\myuser" -ServicePassword "VerySecure.1234" 
    -MSIFileName "C:\CU7Package\MSI\dixf_service_x64\dixf_service_x64.msi" 
    –LogFileName "C:\MyLogs\DIXFService-script-log.txt" -MSIExecLogFileName "C:\MyLogs\DIXFService-MSIExec-log.txt"

<a name="additional-resources"></a>その他のリソース
--------

[複数のバージョン (DIXF) がある環境でデータのインポート / エクスポート フレームワークで使用される SQL Server Integration Services のバージョンを構成する](configure-sql-server-integration-services-multiple-versions-dixf.md)




