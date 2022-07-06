---
title: 管理者のアクセス権を使用しないクラウド ホスト環境での開発
description: この記事では、クラウドでホストされている開発マシンで作業している Commerce 開発者向けのコンフィギュレーション手順について説明します。
author: mugunthanm
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-12-08
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 488457ca486a64c5ef54350b9ed65c5d0a586572
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860278"
---
# <a name="development-in-cloud-hosted-environments-without-admin-access"></a>管理者のアクセス権を使用しないクラウド ホスト環境での開発

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition、プラットフォーム更新プログラム 12 では、Microsoft 定期購読を実行している開発または構築環境で仮想マシン (VM) 管理者アカウントにアクセスできなくなり、Microsoft サブスクリプションを使用して層 1 環境を配置することはできません。

リモート デスクトップ (RDP) を使用して、Lifecycle Services (LCS) 環境ページに用意されている非管理ユーザーを使用するこれらの制限された環境にアクセスすることができます。 管理者アクセスを許可しない環境の詳細については、[管理者アクセスを許可しない開発用 およびビルド用 VM に関するよく寄せられる質問](../../fin-ops-core/dev-itpro/sysadmin/vms-no-admin-access.md)を参照してください。

ご使用の環境で管理者アクセス権が必要な場合は、Azure サブスクリプションを使用し、LCS を使用して環境を配置してください。 ダウンロード可能な VHD を使用して Azure VM に配置したり、ローカルでホストしたりして完全な管理者権限を取得することもできます。

この環境に管理者アクセス権がない場合、Modern POS を使用してテストおよびデバッグすることはできません。 カスタマイズをテストしている場合は、POS のすべてのコマース カスタマイズを行うことができ、その環境でクラウド POS を使用する必要があります。 カスタマイズの観点からは、Cloud POS および Modern POS に違いはありません - どのカスタマイズも Cloud POS および Modern POS の両方で機能します。 ハードウェアおよびその他のシナリオの、ブラウザー固有もしくは UWP アプリ固有のロジックを追加しない限り、Modern POS か、その逆で作業するために Cloud POS で完了したカスタマイズの追加のロジックやコードはありません。 別のオプションは、Modern POS を使用した環境ですべての開発を実行し、MPOS をインストールするための管理者アクセス権限を持つ他の環境でテストすることです。 ほとんどの場合はクラウド POS を使用してテストすることが可能で、オフラインのシナリオをテストするか予想します。 オフライン シナリオをテストする場合は、ビルド スクリプトを使用して Modern POS インストーラーを作成し、テスト環境またはその他のいくつかの POS レジスターでテストできます。

**クラウド POS を開発に使用している場合は、クラウド POS プロジェクトを開く前に以下の設定を行います**

1. Visual Studio を開き、**表示** > **アプリケーション エクスプローラー** へ移動します。 インターネット インフォメーション サービス (IIS) Express が配置されているすべてのコマース Web サイトで開始するまで待ちます。 タスク バーに IIS トレー アイコンが表示され、クラウド POS や Commerce Scale Unit など、すべての Web サイトがすべて表示されます。
4. CRT/RS 拡張をデバッグするには、CRT/RS プロジェクトを IIS Express プロセスに添付します。
5. Retail SDK からクラウド POS プロジェクトを開くと、次のエラーで IIS Express が失敗することがあります。 

    ```Console
    Filename: redirection.config
    Error: Cannot read configuration file
    ``` 

**この問題を解決するには**

1. Visual Studio を閉じます。
2. **aspnet.config** および **redirection.config** ファイルを **%userprofile%\Documents\IISExpress\config** にコピーします。
3. **%userprofile%\Documents\IISExpress\config** フォルダー内の **applicationhost.config** ファイルを開きます。
4. **applicationhost.config** で、RetailCloudPos の physcialPath を変更し、SDK の場所をポイントするようにします。
   たとえば、physicalPath="K:\RetailSDK\POS\Web" です。 全体的なセクションは、次のようになります。
   
    ```xml
   <site name="RetailCloudPOs" id="4" serverAutoStart="true">
        <application path="/" applicationPool="Dynamics365">
            <virtualDirectory path="/" physicalPath="K:\RetailSDK\POS\Web" />
        </application>
    ```
5. 変更を **applicationhost.config** に保存します 
6. **%userprofile%\Documents\IISExpress\config** フォルダーの名前を変更します。 **ステップ 8** の新しい場所に **applicationhost.config** ファイルをコピーするため、ファイルを削除しないでください。
7. Cloud POS プロジェクトに対して、Visual Studio を再度起動します。 **%userprofile%\Documents\IISExpress\config** フォルダーが、既定の構成ファイルを使用して再作成されます。
8. **applicationhost.config** ファイルを、**ステップ 6** で名前を変更したフォルダーから、**ステップ 7** で作成したフォルダーにコピーします。 
9. \RetailSDK\POS\Web\Pos.Web.csproj を編集し、既定の **IISURL** ノードを使用しているクラウド POS URL に変更してから **UseIIS** を false に設定します。
```    
    Ex:  
    <UseIIS>False</UseIIS>
    <IISUrl>https://YourCPOSURL.com</IISUrl>
```
10. Pos.Web プロジェクトを右クリックし、**プロパティ** を選択します。
11. **プロパティ** ウィンドウで、**Web** タブを選択します。**URL の開始** を選び、URL の開始をクラウド POS URL として設定し、ドロップ ダウン メニューから **サーバー セクションで、IIS Express をサーバーとして選択** を実行し、**プロジェクト URL** をクラウド POS URL として設定します。 

開発に対して IIS を使用している場合は (管理者アクセス権を持つ VMs)、UseIIS ノード値を False に設定し、サーバー ドロップ ダウン メニューからローカル IIS を選択する必要があります。

たとえば、`https://usnconeboxax1pos.cloud.onebox.dynamics.com`。

12. 変更を保存します。
13. Pos Web プロジェクトを右クリックし、**StartUp プロジェクトとして設定** を選択ます。
14. F5 キーを押して Pos.Web プロジェクトを実行するか、Visual Studio メニューの **実行** ボタンをクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]