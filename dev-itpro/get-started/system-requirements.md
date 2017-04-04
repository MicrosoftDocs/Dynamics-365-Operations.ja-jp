---
title: "システム要件"
description: "このトピックでは、Microsoft Dynamics 365 for Operationsの最新のバージョンのシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>システム要件

このトピックでは、Microsoft Dynamics 365 for Operationsの最新のバージョンのシステム要件を一覧表示します。

<a name="supported-web-browsers"></a>サポートされている Web ブラウザー
----------------------

工程のWebアプリケーションのMicrosoft Dynamics 365が指定オペレーティング システムで実行するには、次のWebブラウザのいずれかになります:

-   Windows 10の、Microsoftの終了 (最新の共有利用可能なバージョン) 
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7、またはGoogleの関連10のタブレットのGoogle Chrome (最新の共有利用可能なバージョン) 
-   Mac OS x 10.10 (ヨセミテ)、10.11 (El Capitan) または10.12 (山脈)、またはAppleのiPadのApple Safari (最新の共有利用可能なバージョン) 

各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。 **メモ :**

-   タスク レコーダから、をMicrosoft Wordドキュメントに含めるために生成される画像をキャプチャするには、Chrome拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   現在の作業エディタはClickOnceアプリケーションが開始されます。 Microsoft終了、Internet Explorerのみ (Microsoft WindowsでサポートされているバージョンでClickOnceアプリケーションをサポートします。 現在の作業エディタでClickOnceアプリケーションは64ビットの互換性のあるオペレーティング システムが必要です。
-   財務報告に関するレポート デザイナーはClickOnceアプリケーションが開始されます。 これは64ビットの互換性のあるオペレーティング システムが必要です。 Chromeを使用すると、レポート デザイナのクライアントをダウンロードするにClickOnce拡張機能をインストールする必要があります。 incognitoモードのChromeを使用する場合は、ClickOnceの拡張もincognitoモードを有効になることを確認します。

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS でサポートされている Web ブラウザー

工程365 for Operationsの小売クラウドPOSは、指定されたオペレーティング システムで実行するには、次のWebブラウザのいずれかになります:

-   Windows 10の、Microsoftの終了 (最新の共有利用可能なバージョン) 
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、またはWindows 7のChrome (最新の共有利用可能なバージョン) 

## <a name="network-requirements"></a>ネットワーク要件
-   Dynamics 365 for Operationsは(ms) 150未満にミリ秒の待機時間のネットワークに設計されています。 これは、ブラウザのクライアントのMicrosoftのAzureのデータ センターに待機時間工程のそのホストのDynamics 365です。 ただし、http://www.azurespeed.comにネットワーク待ち時間を確認することを<お>勧めします。
-   工程365 for Operationsの帯域幅の要件はシナリオによって異なります。 最も一般的なシナリオ (キロビット/秒) /50 Event秒以上の帯域幅が必要です。 ただし、の伝送の要件がある広範なカスタマイズを含むシナリオまたはワークスペースのような場合に、追加の帯域幅をお勧めします。

一般に、Dynamics 365 for Operationsは、インターネットに対して最適化されます。 ブラウザーのクライアントのAzureのデータ センターにラウンド トリップの数は非常に小さく、すべての積荷は、圧縮されます。 **警告されます: **最小の帯域幅の要件に応じてユーザーの数を掛けてクライアントの場所から帯域幅要件を計算しないでください。 指定した場所によっては計算してよくに行うです。 帯域幅の要件について心配する顧客について、Dynamics 365 for Operationsのプレビュー バージョンを使用します。

## <a name="net-framework-requirements"></a>.NET Frameworkの要件
Dynamics 365 for Operationsはすべてに.NET Framework Versionをクリック4.6.2ドキュメントの工順の代理店などのアプリケーション必要です。 インストール手順については、表示、[.NET Framework] (https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx)をインストールします。

## <a name="supported-microsoft-office-applications"></a>Microsoft Officeサポートされているアプリケーション
-   Microsoft Excelと、アドインを実行するには、インストールするWindowsまたはMacのMicrosoft Office 2016年が必要です。 詳細については、バージョン要求については、" "を参照してください[会社の連結のトラブルシューティング] (/dynamics365/operations/dev itpro/office integration/office統合トラブルシューティング)。
-   機能を言い表わすするには、Excelへのエクスポートまたはエクスポートによって生成されたドキュメントを表示するには、インストールされているMicrosoft Office 2007年後である。

## <a name="retail-modern-pos-requirements"></a>Retail POSの現代の要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail POSの現代は32ビット アプリケーションですが、x86またはx64両方のアーキテクチャ実行されます。
-   Windows 10でのみRetail POSの現代プロは、Enterprise、および企業の長期的なサービスの分岐(LTSB) Editionサポートされます。

### <a name="minimum-system-requirements"></a>最小システム要件

-   最小でサポートされて決済のは1280 × 1024です。
-   コンピュータは現代Retail POSのする必要があります。これらの条件を満たす実行します:
    -   これは、少なくとも小数点以下2ギガヘルツ(GHz)に実行されていない二重コア プロセッサが必要です。
    -   これは、少なくとも、RAMの(GB) 3ギガバイトの必要です。
    -   これは、インターネット アクセス許可が必要です。

## <a name="retail-hardware-station-requirements"></a>Retailのハードウェア ステーションの要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retailのハードウェア ステーションは32ビット アプリケーションですが、x86またはx64両方のアーキテクチャ実行されます。
-   Retailのハードウェア ステーションは、オペレーティング システムでサポートされます:
    -   Windows 7プロフェッショナル、Enterprise Edition **および最終の注記: ** Internet Explorer 11をシステムで手動でインストールされている場合にのみ、Windows 7がサポートされます。
    -   Windows 8.1、1人のプロおよび埋め込み、Enterprise Editionが更新されます
    -   Windows 10プロ、Enterprise、LTSB Enterprise Edition

### <a name="minimum-system-requirements"></a>最小システム要件

コンピュータは次の項目をインストールして使用するすべてのシステム要件を満たす必要があります:

-   インターネット インフォメーション サービス (IIS)
-   サード パーティのハードウェア

## <a name="retail-store-scale-unit-requirements"></a>Retail Storeのスケールの単位の要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail Storeのスケールの単位は32ビット アプリケーションですが、x86またはx64両方のアーキテクチャ実行されます。
-   Retail Storeのスケールの単位は、オペレーティング システムでサポートされます:
    -   Windows 7プロフェッショナル、Enterprise、最終Edition
    -   Windows 8.1、1人のプロおよび埋め込み、Enterprise Editionが更新されます
    -   Windows 10プロ、Enterprise、LTSB Enterprise Edition

### <a name="minimum-system-requirements"></a>最小システム要件

-   の4 GB RAM
-   コアごとの速度1.6 GHzのピーク (CPU、のコアは、最小です)。
-   空き領域の少なくとも10 GB (チャンネルのデータベースが大量の領域を要求できます)。

### <a name="recommended-system-requirements"></a>推奨システム要件

-   の6 GB RAM
-   コアごとの速度2.4 GHzのi7 (または現金) ピークCPU (4つのコアをお勧めします)。
-   空き領域の少なくとも10 GB (チャンネルのデータベースが大量の領域を要求できます)。

## <a name="requirements-for-development-on-local-vms"></a>ローカルVMsの開発の要件
ローカル コンピュータ仮想(VMs)の開発の要件については、" "を参照してください[VMの連続した分割前提] (/dynamics365/operations/dev itpro/dev tools/access instances#vmことあ実行前提)。

<a name="see-also"></a>参照
--------

[アクション発生させる] (/dynamics365/operations/dev itpro/dev tools/get評価コピー) 365 for Operationsの評価をコピー


