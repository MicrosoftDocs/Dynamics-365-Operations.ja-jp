---
title: "ISV ライセンス"
description: "このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。 これには、ISV のライセンス機能の長所および機能に関する情報が含まれており、ISV ソリューションのライセンスを有効にする方法、パッケージの作成方法、顧客固有のライセンスの生成方法およびテスト目的で自己署名証明書を作成する方法について説明しています。"
author: robadawy
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: b71f9a30ab5913349fd672c59d27dc24ededa75d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="isv-licensing"></a>ISV ライセンス

[!include [banner](../includes/banner.md)]

このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。 これには、ISV のライセンス機能の長所および機能に関する情報が含まれており、ISV ソリューションのライセンスを有効にする方法、パッケージの作成方法、顧客固有のライセンスの生成方法およびテスト目的で自己署名証明書を作成する方法について説明しています。

Microsoft Dynamics エコシステムには、独立系ソフトウェア ベンダー (ISV) が再パッケージ化可能な業種ソリューションをビルド、配置、販売して収益化できるようにするツールとフレームワークが用意されています。 ISV ライセンス機能には、次の利点があります。

-   これは、顧客およびパートナーに ISV ソリューションのより安全なライセンス メカニズムを提供します。 ISV ソリューションは、顧客が ISV から有効なライセンス キーを購入した場合にのみ有効になります。
-   これにより、顧客が異なる ISV からの ISV ソリューションのライセンスをどのように処理するかが調整されるため、総保有コスト (TCO) を削減します。
-   ISV は、業界標準のフレームワークを使用して、ISV ライセンスを個別に生成、管理、配布することができます。

この機能は、ISV 競合他社のコピー防止 (ソースベースの保護) を有効にしません。

## <a name="capabilities"></a>処理能力
このセクションでは、ISV ライセンス機能のさまざまな機能について説明します。

### <a name="isvs-can-generate-their-own-licenses"></a>ISV は独自のライセンスを生成可能

ISV は独自のライセンスを個別に生成し、ソリューションに適用し、これらのソリューションをパートナーおよび顧客に提供できます。 各 ISV ライセンスでは、ISV ソリューションを保護するためのランタイム機能を有効にします。 また、各 ISV ライセンスは、ソフトウェアが ISV によって配布されていることを保証する ISV Authenticode 証明書に関連付けられます。

### <a name="a-run-time-check-makes-sure-that-an-isv-generated-license-key-exists-in-the-customers-environment"></a>ランタイム チェックにより、ISV によって生成されたライセンス キーが顧客の環境に存在することを確認します。

ライセンスに関連付けられた各 ISV ソリューションは、有効なライセンス キーが顧客の環境に存在する場合にのみ実行されます。 したがって、ISV がソリューションをライセンスに結び付けても、顧客に有効なライセンス キーがない場合、ソリューションは実行されません。

### <a name="there-are-two-types-of-license-boolean-and-number"></a>ライセンスには、ブール値と数値の 2 種類があります

ISV は**ブール値**および**番号**の 2 つのタイプを作成できます。 ISV は、いずれかの種類のライセンスと有効期限を関連付けることができます。 この有効期限は ISV ライセンスにのみ適用され、システムの有効期限とは無関係です。 ブール値ライセンスは、単純な有効化ライセンスです。 ライセンスのタイプ (**ブール値** または**数字**) は、ライセンス コード ノードのプロパティによって設定されます。 ISV は、独自のカスタム ロジックを記述し、ISV ライセンスで提供されている数を確認し、そのソリューションがライセンス条件内で使用されていることを確認できます。 詳細については、「<https://msdn.microsoft.com/en-us/library/jj677284.aspx>」を参照してください。

### <a name="license-validation-errors"></a>ライセンス検証エラー

ISV ライセンスがインポート後に無効になったとき、ISV ソリューションはサーバーが再起動されるまで実行を継続します。 (サーバーの再起動後、ソリューションは無効になっています。) Application Object Server (AOS) のインスタンスの起動時にエラーがスローされます。 エラーはイベント ログに書き込まれます。

## <a name="implementing-isv-licensing-in-a-solution"></a>ソリューションへの ISV ライセンスの実装
ISV には証明機関 (CA) から有効な Authenticode 証明書 (X.509) が必要です。 Microsoft が、特定の CA をお勧めすることはありません。 ただし、多くの企業がこれらの証明書を提供します。 Authenticode 証明書は、さまざまなキー サイズに役立ちます。 ISV ライセンス機能は、キー サイズが 1024 ビットと 2048 ビットの両方の証明書をサポートします。 既定では、多くのプロバイダーが 2048 ビット キー サイズを使用しており、より強固な暗号化を提供するために ISV はこのビット キー サイズを使用することをお勧めします。 ただし、ISV に既に既存の 1024 ビット キー サイズがある場合、そのキー サイズは ISV ライセンス機能で動作します。 **注記:** ISV ライセンス機能は、4096 ビット キー サイズをサポートしていません。 Authenticode 証明書はさまざまな暗号サービス プロバイダーを持つことができます。 ISV ライセンス機能は、Enhanced Cryptographic Provider を使います (Base Cryptographic Provider もカバーします)。 Authenticode 証明書を購入できる多くの独立したプロバイダーがあります。 Microsoft が、特定のプロバイダーをお勧めすることはありません。 頻繁に使用されるプロバイダーには、Symantec VeriSign、Thawte、Go Daddy があります。

## <a name="certificate-import-and-export"></a>証明書のインポートおよびエクスポート
証明書は、お客様のライセンス ファイルに署名し、インポート時にライセンス ファイルを検証するために使用されます。 Authenticode 証明書は、4 つのファイル形式をサポートします。 ISV ライセンス機能については、2 つの形式で証明書ファイルが必要です。

-   **個人情報交換 (pfx または PKCS \#12 とも呼ばれる)** – .pfx ファイル名拡張子を使用して、証明書、秘密キー、および証明書パスのすべての証明書のセキュリティ保護された保管をサポートする PKCS \#12 形式。 PKCS \#12 形式は、証明書とそのプライベート キーをエクスポートするために使用される唯一のファイル形式です。
-   **Base64 エンコード X.509** - Base64 形式では、単一の証明書の格納がサポートされています。 この形式では、秘密キーまたは証明書パスの格納はサポートされていません。

形式に制限があります。 PFX (PKCS \#12) 形式は、署名/生成目的でプライベート キーと共に証明書をエクスポートする場合にのみ使用する必要があります。 絶対に ISV 組織外に共有しないようにする必要があります。 .cer ファイル名拡張子を使用する DER でエンコードされたバイナリ X.509形式は、アプリケーション オブジェクト ツリー (AOT) ライセンスに埋め込まれる必要がある証明書の公開キーをエクスポートするために使用してください。 この公開キーは、モデルを介して顧客に配布されます。 これは、ライセンスが秘密キーを所有する ISV ライセンスによって署名されていることを確認するために、ライセンスのインポート時に使用されます。

## <a name="enable-licensing-for-your-isv-solution"></a>ISV ソリューションのライセンスの有効化
ソリューションのライセンスを有効にするには、これらの手順に従います。

1.  ISV ソリューションを作成します。 

    ![ISV ソリューションを作成しています](./media/isv1.png)

2.  リソースとしてプロジェクトに証明書の公開キー (.cer ファイル) を追加します。
    1.  新しい品目を追加します。 

        ![新しい品目の追加](./media/isv2.png)

    2.  **ラベルおよびリソース**をクリックし、次に**リソース**をクリックします。 

        ![リソースをクリックする](./media/isv3.png)

    3.  リソースとして証明書の公開キーを選択します。 

        ![リソースとして証明書の公開キーを選択](./media/isv4.png)

    4.  リソースとして、証明書を追加します。 

        ![リソースとして証明書を追加](./media/isv5.png)


3.  ライセンス コードを作成します。 

    ![ライセンス コードを作成しています](./media/isv6.png)

4.  ライセンス コードに証明書をマップします。 

    ![ライセンス コードへの証明書のマッピング](./media/isv7.png)

5.  1 つまたは複数のコンフィギュレーション キーを作成します。 

    ![コンフィギュレーション キーを作成しています](./media/isv8.png)

6.  ライセンス コードをコンフィギュレーション キーに関連付けます。 

    [![ライセンス コードとコンフィギュレーション キーの関連付け](./media/isv9.png)

7.  コンフィギュレーション キーをソリューションの要素に関連付けます。 たとえば、新しいフォームを作成します。 

    ![新しいフォームを作成しています](./media/isv10.png)

8.  フォームにボタンを追加します。 

    ![新しいフォームへのボタンの追加](./media/isv11.png)

    このボタンは、最初はコンフィギュレーション キーで制御されていないため、表示されます。 

    ![最初に追加されるときに、新しいボタンが表示されます](./media/isv12.png)

9.  コンフィギュレーション キーをボタンに関連付けます。 

    ![コンフィギュレーション キーとボタンの関連付け](./media/isv13.png) 

    コンフィギュレーション キーが有効になり、利用可能になると、ボタンは表示されなくなります。 

    ![ボタンが表示されていません](./media/isv14.png)


## <a name="create-a-package-and-generate-a-customer-specific-license"></a>パッケージを作成し、顧客固有のライセンスを生成する
1.  ライセンスを発行する顧客のテナント名と ID を収集します。 (この情報は、**設定**&gt;**情報**で見つけることができます。) 

    ![顧客のテナント名および ID](./media/isv15.png)

2.  顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。 ライセンス ファイルを作成するには、**axutil genlicense** コマンドに、以下のパラメーターを渡す必要があります。

    | パラメーター名  | 説明                                                                  |
    |-----------------|------------------------------------------------------------------------------|
    | ファイル            | ライセンス ファイルの名前。                                               |
    | licensecode     | Microsoft Visual Studio のライセンス コードの名前。                |
    | certificatepath | 証明書のプライベート キーのパス。                                  |
    | パスワード        | 証明書のプライベート キーのパスワード。                             |
    | 顧客        | (手順 1 のスクリーン ショットから) 顧客のテナント名。              |
    | serialnumber    | 顧客のテナント ID (スクリーン ショットに「シリアル番号」と表示されています)。       |
    | expirationdate  | オプション: ライセンスの有効期限。                               |
    | usercount       | オプション: カスタム検証ロジックが必要に応じて使用できる数値。 これはユーザーになる可能性がありますが、必ずしもユーザーに限定されません。 |

    次に例を示します。

        C:\AOSService\PackagesLocalDirectory\Bin\axutil genlicense /file:c:\templicense.txt /certificatepath:c:\tempisvcert.pfx /licensecode:ISVLicenseCode /customer:TAEOfficial.ccsctp.net /serialnumber:4dbfcf74-c5a6-4727-b638-d56e51d1f381 /password:********



3.  ライセンスをターゲット環境にインポートします。 **注記:** 運用システムでは、配置可能パッケージを使用して、Microsoft Dynamics Lifecycle Services (LCS) からこの手順を完了します。 詳細については、この記事の後半の「実稼働環境」セクションを参照してください。

    | パラメーター名                | 説明                                                                                            |
    |-------------------------------|--------------------------------------------------------------------------------------------------------|
    | --setupmode importlicensefile | ライセンスが読み込まれることをセットアップ ツールに通知するには、このパラメーターを使用します。                             |
    | --metadatadir                 | メタデータ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。   |
    | --bindir                      | バイナリ ディレクトリ を指定するには、このパラメーターを使用します。 既定のパッケージ ディレクトリを使用する必要があります。   |
    | --sqlserver                   | Microsoft SQL Server を指定するには、このパラメーターを使用します。 1 ボックス環境では、ピリオド (**.**) を使用します。 |
    | --sqluser                     | SQL Server のユーザーを指定するには、このパラメーターを使用します。 **AOSUser** に渡す必要があります。                     |
    | --sqlpwd                      | SQL Server のパスワードを指定するには、このパラメーターを使用します。                                                 |
    | --licensefilename             | 読み込むライセンス ファイルを指定するには、このパラメーターを使用します。                                    |

    次に例を示します。

        C:\AOSService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --setupmode importlicensefile --metadatadir c:\packages --bindir c:\packages --sqlserver . --sqldatabase axdbrain --sqluser AOSUser --sqlpwd ******** --licensefilename c:\templicense.txt

4.  対応するコンフィギュレーション キーは、**ライセンス コンフィギュレーション** ページで使用可能になり、有効になります。 既定では、コンフィギュレーションが有効です。 たとえば、次のスクリーン ショットで **ISVConfigurationKey1** コンフィギュレーション キーを参照してください。 

    ![ライセンス設定ページで ISVConfigurationKey1 コンフィギュレーション キーを有効にする](./media/isv18.png)

5.  非実稼働インストールでは、Visual Studio からデータベースの同期プロセスを開始する必要があります。

コンフィギュレーション キーを有効にした後、次のスクリーン ショットに示すように、ボタンは表示されるようになります。 

![コンフィギュレーション キーを有効にするとボタンが表示されます](./media/isv19.png)

## <a name="protection-best-practices"></a>保護のベスト プラクティス
ソリューションは、2つの形式で配布することができます。

-   モデル ファイル (ソース コード)
-   配置可能パッケージ (binary)

構成キーとライセンス コードを保護するには、展開可能なパッケージを使用してバイナリ形式でリリースすることをお勧めします。 顧客は Visual Studio のこれらの要素をインストールして対話することができます。 顧客が配置可能パッケージ内の項目を参照することはできますが、ソース コードにアクセスしたり項目を変更することはできません。 (ただし、拡張機能を作成できます。) バイナリ形式でソリューションをリリースする機能の詳細は、すぐに利用可能になります。 配置可能パッケージ (バイナリ) には、顧客がアクセスを必要とせず、カスタマイズできないようなクラスやその他のロジックも含めることができます。 

![保護されている ISV ソリューションと保護されていない ISV ソリューション](./media/isv20.png)

## <a name="production-environments"></a>実稼働環境
実稼働システムに ISV ライセンスをインストールするには、LCS によって展開可能なパッケージを使用する必要があります。 構成モード用テンプレート パッケージは、すべてのインストールの &lt;PackagesFolder&gt;\\bin\\CustomDeployablePackage\\ImportISVLicense.zip (パッケージ フォルダーは通常 j:\\AOSService\\PackagesLocalDirectory または c:\\AOSService\\PackagesLocalDirectory\\ の下にあります) で見つけることができます。 

![コンフィギュレーション モードのテンプレート パッケージの場所](./media/isv21.png)

1.  パッケージ テンプレートのコピーを作成します。
2.  パッケージ テンプレート内の次のフォルダーにライセンス ファイルを配置: ImportISVLicense.zipAosServiceScriptsLicense

一度に複数のライセンスをインストールすることができます。 別のライセンスがいずれかに依存する場合は、それに応じた名前を確認します。 (ライセンスはアルファベット順にインストールされます。)

## <a name="appendix-create-self-signed-certificates-for-test-purposes"></a>付録: テスト目的での自己署名証明書の作成
**注記:** 自己署名証明書は、開発時にのみ使用できます。 これらは、実稼働環境でサポートされていません。

1.  テストの目的で、 自己署名の CA 証明書を作成することができます。 Visual Studio のツール プロンプトを使用して、次のコマンドを実行します。

        makecert -r -pe -n "CN=IsvCertTestAuthority O=IsvCertTestAuthority" -ss CA -sr LocalMachine -a sha256 -len 2048 -cy authority -sky signature -b 01/01/2016 -sv c:\temp\CA.pvk c:\temp\CA.cer

    詳細については、「<https://msdn.microsoft.com/en-us/library/windows/desktop/aa386968(v=vs.85).aspx>」を参照してください。

2.  CA を使用して証明書を作成します。

        makecert -pe -n "CN=IsvCertTest O=IsvCertTest" -ss ISVStore -sr LocalMachine -a sha256 -len 2048 -cy end -sky signature -eku 1.3.6.1.5.5.7.3.3 -ic c:\temp\ca.cer -iv c:\temp\ca.pvk -b **/**/**** -sv c:\temp\isvcert.pvk c:\temp\isvcert.cer

3.  ISV 証明書を PFX 形式に変換します。

        pvk2pfx -pvk c:\temp\isvcert.pvk -spc c:\temp\isvcert.cer -pfx c:\temp\isvcert.pfx -po ********

4.  テスト シナリオでは、すべての AOS インスタンスに手動で自己署名 CA 証明書をインポートします。

        certutil -addstore root c:\temp\ca.cer

    ただし、自己署名 ISV 証明書を使用していた場合、CA 証明書ではなくその証明書をインポートする必要があります。

        certutil -addstore root c:\temp\isvcert.cer






