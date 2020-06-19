---
title: セルフサービス コンポーネントの一括配置
description: このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。
author: jashanno
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Application update 3
ms.openlocfilehash: 79dd9fc9c92b8e7d5ad4761373143e3d68654322
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426332"
---
# <a name="mass-deployment-of-self-service-components"></a>セルフサービス コンポーネントの一括配置

[!include [banner](../includes/banner.md)]

このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。 このトピックは、機能が開発され、より多くの機能が利用可能になると更新されます。 現在、サイレント サービス更新の機能のみが利用可能です。

## <a name="delimiters-for-mass-deployment"></a>一括配置の区切り記号

次のテーブルに、一括配置の実行コマンドで現在使用できる区切り記号を示します。 


| 区切り記号                 | 説明 |
|---------------------------|-------------|
| -S または -サイレント             | インストーラーをサイレントで実行します。 グラフィカル ユーザー インターフェイス (GUI) を使用しません。 **-Q** および **-Quiet** 区切り記号には同じ効果があり、使用することもできます。 |
| -C または -Config             | このインストールの一部として使用するコンフィギュレーション ファイルの場所とファイル名を指定します。 |
| -FilePath                 | カスタム インストールの場所を指定します。<p>標準のインストールにこの区切り記号を使用することをお勧めしません。</p> |
| -LogFile                  | インストール ログのカスタム ファイルの場所を指定します。<p>標準のインストールにこの区切り記号を使用することをお勧めしません。</p> |
| -SkipPrerequisiteCheck    | 前提条件および必須コンポーネントのインストールのチェックをスキップします。<p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |
| -SkipSystemInfoCollection | インストールの開始時にシステム情報を収集するプロセスをスキップします。<p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |
| -SkipMerchantInfo         | ハードウェア ステーションのセルフ サービス インストーラーの終わりにマーチャント アカウント情報のインストールをスキップします。<p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |
| -SkipAppxInstallation     | Dynamics 365 の2018 年 10 月のリリースから、この区切り記号は APPX Retail Modern POS アプリケーションのインストールをスキップします。 この区切り記号は、システム アカウントまたはサービス アカウント (ユーザー プロファイルがないアカウント) を使用してアプリケーションのインストールを実行するために必要です。 |

## <a name="silent-servicing"></a>サイレント サービス

### <a name="before-you-begin"></a>準備

サイレント サービスが現在インストールされているすべてのコンポーネントを維持していることに注意してください。 任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を開始する前に実行します。

### <a name="examples-of-commands-for-silent-servicing"></a>サイレント サービスのコマンド例

このセクションでは、セルフサービスの大量展開に使用されるコマンドの例を示します。 これらのコマンドは、Modern POS (オフラインでサポートされているインストーラーとオフラインでサポートされていないインストーラーの両方) 用インストーラー、ハードウェア ステーション、Commerce Scale Unit (自己ホスト) など、すべての標準セルフサービス インストーラーで動作します。

#### <a name="silently-update-the-current-installation-of-modern-pos"></a>Modern POS の現在のインストールをサイレントに更新

次のコマンドは、Modern POS の現在のインストールをサイレント更新します。 このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。 このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。

```Console
ModernPOSSetup_V72.exe -S
```

> [!NOTE]
> Retail Store Scale Unit ではコンフィギュレーション ファイルがまだ必要とされます。 ただし、インストーラーは可能な場合はいつでも、現在インストールされているすべての値を保持します。

#### <a name="silently-update-the-current-installation-of-commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (自己ホスト) の現在のインストールを自動的に更新

次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Commerce Scale Unit (自己ホスト) の現在のインストールをサイレント更新します。 (このコンフィギュレーション ファイルは、インストーラーの実行可能ファイルと同じ場所にない可能性があります。) このコマンドは、前提条件のチェックをスキップし、インストール手順に進みます。 テストおよび開発の目的にのみ、このコマンドを使用することをお勧めします。

```Console
StoreSystemSetup_V72.exe -S -C "C:\Temp\StoreSystemSetup_V72_Houston.xml" -SkipPrerequisiteCheck
```

## <a name="mass-deployment-of-modern-pos"></a>Modern POS の一括配置

### <a name="before-you-begin"></a>準備

この機能を使用するには、バージョン 7.3 以降が必要です。 本社でのすべての店舗、レジスター、およびデバイスのコンフィギュレーション、およびその他のコンフィギュレーションが既に完了したとみなされます。 任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を実行する前に実行します。

### <a name="examples-of-commands-for-silent-mass-deployment"></a>サイレント マス展開のコマンド例

このセクションでは、Modern POS のセルフサービスの一括配置に使用されるコマンドの例を示します。オフラインでの Modern POS およびオフライン サポートのないインストーラ―も含まれます。 Windows PowerShell スクリプトの例では、ユーザーがインストールを実行する支援も含まれます。

#### <a name="silently-install-modern-pos"></a>Modern POS をサイレント インストール

次のコマンドにより、Modern POS がサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。

このコマンドは、構成ファイルが存在する場合、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。 複数の構成ファイルが使用可能な場合は使用しないでください。

```Console
ModernPOSSetup_V73.exe -S
```

> [!NOTE]
> Modern POS ではコンフィギュレーション ファイルは必要ありません。 ただし、関連付けられている構成ファイルを読み込めない限り、インストールされた Modern POS アプリケーションは適切な方法では有効化されません。

#### <a name="silently-install-modern-pos-by-using-a-specific-configuration-file"></a>特定のコンフィギュレーション ファイルを使用して Modern POS をサイレント インストール

次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Modern POS の現在のインストールをサイレント インストールします。 この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。

```Console
ModernPOSSetup_V72.exe -S -C "C:\Temp\ModernPOSSetup_V73_Houston-3.xml"
```

#### <a name="silently-install-retail-hardware-station"></a>Retail ハードウェア ステーションのサイレント インストール

> [!NOTE]
> Retail ハードウェア ステーションをインストールすのに、**-SkipMerchantInfo** の区切り記号が必要です。 GUI ベースのハードウェア ステーションのインストールの最後に開く、Merchant Account Information Utility を使用する必要はありません。 機能上の理由で、Modern POS がハードウェア ステーションにペアリングされている場合、最新のマーチャント口座情報もコンポーネントにプッシュされます。

次のコマンドにより、Retail ハードウェア ステーションがサイレントでインストール (または更新) されます。 現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。 また、**-SkipMerchantInfo** の区切り記号を使用して、ユーティリティを通じたマーチャント口座情報のダウンロードをスキップすることもできます。 このコマンドは、インストーラーの実行可能ファイルと同じ場所にある構成ファイルを使用します。

```Console
HardwareStationSetup_V10.exe -S -SkipMerchantInfo
```

> [!NOTE]
> Retail ハードウェア ステーションをサイレントで配置するのに、構成ファイルが必要です。

#### <a name="silently-install-retail-hardware-station-by-using-a-specific-configuration-file"></a>特定の構成ファイルを使用して Retail ハードウェア ステーションをサイレント インストール

次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail ハードウェア ステーションの現在のインストールをサイレント インストールします。 この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。

```Console
HardwareStationSetup_V10.exe -S -SkipMerchantInfo -C "C:\Temp\HardwareStationSetup_V10__20-19-35.xml"
```
