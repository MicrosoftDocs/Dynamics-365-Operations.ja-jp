---
title: "データのインポート/エクスポート フレームワーク (DIXF) のインストール"
description: "このトピックでは、データ インポート/エクスポート フレームワークをインストールする方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 17631
ms.assetid: 1d778366-1b39-464d-92b2-0f6ec08bfe5a
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8ee680bd41a0d46f6ed30cbb42c97f6b8e13e3cb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="install-the-data-importexport-framework-dixf"></a>データのインポート/エクスポート フレームワーク (DIXF) のインストール

[!include [banner](../../includes/banner.md)]

**注:** このタスクを完了する手順は、Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 以降では変更されました。 更新された手順は、AX 2012 R3 にも適用されます。 詳細については、このトピックで後のセクションを参照してください。 開始する前に、環境には次のコンポーネントが含まれている必要があります。

-   業務に合わせてコンフィギュレーションされた実行中の AX 2012 のバージョン。
-   Microsoft Dynamics AX ビジネスとモデル ストア データベースをホストしている SQL Server の同じバージョンを実行している実行中の Microsoft SQL Server Integration Services のバージョン

**重要:** ステージング環境は高度に正規化されており、処理帯域幅がかなり必要な場合があるため、データを移行する際には、環境の最大バッファー サイズ設定を増やすことをお勧めします。 サーバー構成ユーティリティを使用して値を設定します。

## <a name="install-the-version-of-the-data-importexport-framework-that-is-available-in-microsoft-dynamics-ax-2012-r3"></a>Microsoft Dynamics AX 2012 R3 で利用できるデータのインポート/エクスポート フレームワークのバージョンをインストールする
Microsoft Dynamics AX 2012 R3 で使用可能なバージョンのフレームワークをインストールするには、[[データ インポート/エクスポート フレームワーク (AX 2012 R3) をインストール](install-ax-2012-r3.md)] の手順に従ってください。

## <a name="install-the-version-of-the-data-importexport-framework-that-is-available-in-cumulative-update-7-for-microsoft-dynamics-ax-2012-r2"></a>Microsoft Dynamics AX 2012 R2 の累積更新 7 で利用できるデータのインポート/エクスポート フレームワークのバージョンをインストールする
**重要:** Microsoft Dynamics AX 2012 R2 を実行している場合は、累積更新 7 で利用可能なバージョンのデータ インポート/エクスポート フレームワークを使用することを強くお勧めします。 Integration Services を実行しているコンピュータ、Microsoft Dynamics AX Application Object Server (AOS) のインスタンスを実行しているコンピュータ、および Microsoft Dynamics AX クライアントを実行しているコンピュータに、データインポート/エクスポート フレームワークのコンポーネントをインストールする必要があります 。 インストーラーは、各コンピューターにローカルで実行する必要があります。 **注意:** InformationSource からデータのインポート/エクスポート フレームワークを以前にインストールした場合は、それを完全にアンインストールしてから、Microsoft Dynamics AX 2012 R2 の累積更新 7 用に再インストールする必要があります。 完全アンインストールの一環として、プログラムの追加と削除を使用してすべてのバイナリ ファイルを削除し、データのインポート/エクスポート フレームワーク モデルをアンインストールする必要があります。 詳細については、[方法: モデルの削除 (アンインストール)](http://msdn.microsoft.com/library/6552673a-a386-4349-9438-64c0de94ca7d(AX.60).aspx) を参照してください。

## <a name="install-the-data-importexport-framework-from-informationsource"></a>InformationSource からのデータのインポート/エクスポート フレームワークのインストール
**重要:** AX 2012 RTM または Microsoft Dynamics AX 2012 Feature Pack のみを使用して InformationSource から入手可能なデータのインポート/エクスポート フレームワークのバージョンを使用してください。

### <a name="install-the-data-importexport-framework-binary-components-informationsource"></a>データのインポート/エクスポート フレームワークのバイナリ コンポーネント (InformationSource) のインストール

**重要:** Microsoft Dynamics AX 2012 R2 または AX 2012 R3 の累積更新 7 のデータのインポート/エクスポート フレームワークをインストールしている場合は、この手順を使用しないでください。 次の手順を使用して Integration Services を実行しているコンピューター、AOS のインスタンスを実行しているコンピューター、および Microsoft Dynamics AX クライアントを実行しているコンピューターに、データのインポート/エクスポート フレームワークのバイナリ コンポーネントをインストールします。 インストーラーは、各コンピューターにローカルで実行する必要があります。

1.  Data Import/Export Framework、DataImportExportFramework.zip のインストール パッケージをダウンロードし、パッケージをローカル フォルダーに展開してください。
2.  ファイルを展開した場所を参照して、**Setup.exe** を右クリックし、**管理者として実行**をクリックします。
3.  **設定**ウィザードで、ライセンス条項に同意してから**同意して続行する**をクリックします。
4.  **コンポーネントの選択**ページで、ローカル コンピューターにインストールできるデータのインポート/エクスポート フレームワークのコンポーネントを選択し、**次へ**をクリックします。
5.  前提条件の検証チェックを実行します。 前提条件の確認がインストーラーの外部に検出された問題に対処します。 すべての前提条件に対応したら、**設定** を再起動します。
6.  Microsoft SQL Server の統合サービスを実行するコンピューターにインストールしている場合は、サービス アカウントおよび実行中の SQL Server のバージョンを指定します。 AOS サービス アカウントを使用することをお勧めします。 AOS コンピューターにインストールする場合は、SQL Server の統合サービスを実行しているサーバーの名前を指定します。
7.  **インストールの準備ができました**ページで、概要を確認し、**インストール**をクリックします。
8.  **インストール完了**ページで、**ログの表示**を選択してログ ファイルを表示し、ファイルが正常にインストールされていることを確認してから、**完了**をクリックします。 ログファイルは、**設定** が実行されたのと同じ場所に保存されます。
9.  すべてのコンポーネント (統合サービス、AOS インスタンス、およびクライアント) がインストールされるまで繰り返します。

### <a name="install-the-data-importexport-framework-model-informationsource"></a>データのインポート/エクスポート フレームワーク モデルのインストール (InformationSource)

**重要:** Microsoft Dynamics AX 2012 R2 または AX 2012 R3 の累積更新 7 のデータのインポート/エクスポート フレームワークをインストールしている場合は、この手順を使用しないでください。 すべてのコンポーネントがインストールされた後、データのインポート/エクスポート フレームワーク モデルをインストールする必要があります。

1.  クライアント コンピューターで、データのインポート/エクスポート フレームワークをインストールした場所から、DataImportExportFramework.axmodel ファイルをインポートします。 詳細な指示については、[方法: モデルのインポートとエクスポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx) を参照してください。 **注記:** Microsoft Dynamics AX 管理シェルが、モデルをインストールするデータベースを指し示していることを確認します。
    1.  使用している AOS インスタンスへのクライアント接続を排除します。
    2.  AOS を停止します。
    3.  モデルをインポートするには、次のコマンド ライン ツールのいずれかを使用します。 インポートするモデルのバージョンは、実行している Microsoft Dynamics AX のバージョンによって異なります。

        -   AX 2012 で、2012 ディレクトリからモデルをインストールします。
        -   AX 2012 Feature Pack で、2012 FP ディレクトリからモデルをインストールします。
        -   AX 2012 R2 で、2012 R2 ディレクトリからモデルをインストールします。

        Windows PowerShell

            Install-AXModel -File "C:\Program Files\Microsoft Dynamics AX 2012 Data Import Export Framework Client Component<version number>modelDataImportExportFramework.axmodel"

        AXUtil

            axutil import /file: "C:\Program Files\Microsoft Dynamics AX 2012 Data Import Export Framework Client Component <version number>modelDataImportExportFramework.axmodel"

2.  AOS サービスを再起動します。
3.  クライアントを起動します。
4.  **モデル ストアが変更されました**のダイアログ ボックスで、**コンパイルして同期**をクリックします。
5.  同期が完了したら、**.Net Framework CIL にコンパイル** をクリックします。
6.  単独で、ダイアログ ボックスが表示されない場合は、これらの手順に従います。
    1.  **システム管理** &gt; **定期処理** &gt; **コンパイル** からアプリケーションをコンパイルします。
    2.  **システム管理** &gt; **定期処理** &gt; **データベース** &gt; **SQL 管理**の順にクリックします。 **テーブル アクション**メニューで、**データベースの同期**をクリックします。

7.  **システム管理** &gt; **定期処理** &gt; **コンパイル** から .NET CIL にコンパイルします。 モデルが .NET CIL にコンパイルされた後、**データのインポート / エクスポート フレームワーク** ボタンは、ナビゲーション ウィンドウに追加されます。

## <a name="troubleshoot-an-installation-of-the-data-importexport-framework-from-cumulative-update-7-for-microsoft-dynamics-ax-2012-r2"></a>Microsoft Dynamics AX 2012 R2 の累積更新プログラム 7 からのデータのインポート/エクスポート フレームワークのインストールのトラブルシューティング
このセクションでは、Microsoft Dynamics AX 2012 R2 用の累積的な更新 7 からのデータ インポート/エクスポート フレームワーク インストールの問題のトラブルシューティング方法について説明します。

### <a name="you-receive-an-assembly-containing-type-microsoftdynamicsaxdmfserviceproxydmfentityproxy-is-not-referenced-error"></a>"Microsoft.Dynamics.AX.DMF.ServiceProxy.DmfEntityProxy タイプを含むアセンブリが参照されていません" というメッセージを受け取ります。 エラー

Microsoft Dynamics AX 2012 R2 の累積的な更新 7 をスリップストリームした後、データのインポート/エクスポート フレームワークがインストールされているように表示されますが、多くのフォームを開いたときにエラー メッセージが表示されます。 **解決策** Microsoft Dynamics AX 2012 R2 の累積的な更新プログラム 7 をスリップストリーム インストールする場合、インストールされるシステム管理者ロールのメンバに、データのインポート/エクスポート フレームワークが表示されます。 ただし、フレームワークのバイナリ コンポーネントは存在しません。 データ インポート/エクスポート フレームワークを完全にインストールするには、更新プログラムのインストーラーを実行する必要があります。

## <a name="troubleshoot-an-installation-of-the-data-importexport-framework-from-informationsource"></a>InformationSource からのデータ インポート/エクスポート フレームワークのインストールのトラブルシューティング
このセクションでは、InformationSource からのデータ インポート/エクスポート フレームワーク インストールの問題をトラブルシューティングする方法について説明します。

### <a name="the-data-importexport-framework-does-not-compile"></a>データのインポート/エクスポート フレームワークはコンパイルしません

データのインポート/エクスポート フレームワークをインストールした後、コンパイルできない場合は、データのインポート/エクスポート フレームワークが正常にインストールされていることを検証します。

1.  Microsoft Dynamics AX のデータ インポート/エクスポート フレームワーク サービスが動作していることを確認します。
2.  C:\Program Files (x86)\Microsoft Dynamics AX60\Client\Bin フォルダーに次のデータ インポート/エクスポート フレームワーク DLL が存在することを確認します。
    -   Microsoft.Dynamics.AX.DMF.Mapper.dll
    -   Microsoft.Dynamics.AX.DMF.PreviewGrid.
    -   Microsoft.Dynamics.AX.DMF.ServiceProxy.dll
    -   DMFConfig.xml
    -   Microsoft.Dynamics.AX.DMF.DriverHelper.dll

**解決策** DLLs をインストール場所 (C:\Program Files\Microsoft Dynamics AX 2012 Data Import Export Framework Client Component) から C:\Program Files (x86)\Microsoft Dynamics AX60\Client\Bin フォルダにコピーします。

### <a name="exception-message-while-you-use-data-importexport-framework"></a>データのインポート/エクスポート フレームワークを使用中の例外メッセージ

データのインポート/エクスポート フレームワークを使用しているとき、次のエラー メッセージが表示される場合があります。

> System.Reflection.TargetInvocationException: 呼び出しのターゲットによって例外がスローされました。 ---&gt; System.InvalidOperationException

AOS インスタンスを実行しているサーバーの C:\Program Files (x86) \Microsoft Dynamics AX60\Server\Bin フォルダーに次のファイルが存在していることを確認します。

-   DMFConfig.xml
-   DMFClientConfig.xml
-   Microsoft.Dynamics.AX.DMF.ServiceProxy.dll.config

**解決策** .xml ファイルと設定ファイルをインストール場所 (C:\Program Files\Microsoft Dynamics AX 2012 Data Import Export Framework Server Component) から AOS インスタンスを実行しているサーバーの C:\Program Files (x86)\Microsoft Dynamics AX60\Server\Bin フォルダにコピーします。

### <a name="changes-to-the-location-of-the-data-importexport-framework-service"></a>データのインポート/エクスポート フレームワーク サービスの場所の変更

統合サービスおよびデータのインポート/エクスポート フレームワーク サービスを実行する場所を更新する必要がある場合、Microsoft.Dynamics.AX.DMF.ServiceProxy.dll.config ファイルのエンドポイント アドレスを更新し、新しいサーバー名を使用します。 &lt;エンドポイント アドレス ="http://&lt;&lt;NEW MACHINE NAME&gt;&gt;:7000/DMFService/DMFServiceHelper.svc"**注記:** The Microsoft.Dynamics.AX.DMF.ServiceProxy.dll.config ファイルは、 AOS インスタンスを実行しているサーバーの C:\Program Files (x86)\Microsoft Dynamics AX60\Server\Bin フォルダーにあります。




