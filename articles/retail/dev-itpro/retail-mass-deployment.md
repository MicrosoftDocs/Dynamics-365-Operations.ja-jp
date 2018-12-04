---
title: "Retail セルフサービス コンポーネントの一括配置"
description: "このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。"
author: jashanno
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-09-31
ms.dyn365.ops.version: Application update 3
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c871adec65c1e8f11a1285119772da3b9326b6ca
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="mass-deployment-of-retail-self-service-components"></a>Retail セルフサービス コンポーネントの一括配置

[!include [banner](../includes/banner.md)]

このトピックでは、セルフ サービスを使用してサイレント サービスの更新と初期展開を行う方法について説明します。 また、特別な配置のいくつかの側面についても説明します。 このトピックは、機能が開発され、より多くの機能が利用可能になると更新されます。 現在、サイレント サービス更新の機能のみが利用可能です。

## <a name="delimiters-for-mass-deployment"></a>一括配置の区切り記号

次のテーブルに、一括配置の実行コマンドで現在使用できる区切り記号を示します。 これらの区切り文字は、アプリケーションの更新プログラム 3、2017 年 7 月版以降に適用されます。

| 区切り記号                 | 説明 |
|---------------------------|-------------|
| -S または -サイレント             | インストーラーをサイレントで実行します。 グラフィカル ユーザー インターフェイス (GUI) を使用しません。 **-Q** および **-Quiet** 区切り記号には同じ効果があり、使用することもできます。 |
| -C または -Config             | このインストールの一部として使用するコンフィギュレーション ファイルの場所とファイル名を指定します。 |
| -FilePath                 | カスタム インストールの場所を指定します。<p><p>標準のインストールにこの区切り記号を使用することをお勧めしません。</p> |
| -LogFile                  | インストール ログのカスタム ファイルの場所を指定します。<p><p>標準のインストールにこの区切り記号を使用することをお勧めしません。</p> |
| -SkipPrerequisiteCheck    | 前提条件および必須コンポーネントのインストールのチェックをスキップします。<p><p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |
| -SkipSystemInfoCollection | インストールの開始時にシステム情報を収集するプロセスをスキップします。<p><p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |
| -SkipMerchantInfo         | ハードウェア ステーションのセルフ サービス インストーラーの終わりにマーチャント アカウント情報のインストールをスキップします。<p><p>この区切り記号は、開発とテストに対してのみ使用する必要があります。 標準のインストールにそれを使用することをお勧めしません。</p> |

## <a name="silent-servicing"></a>サイレント サービス

### <a name="before-you-begin"></a>準備

この機能を使用するには、アプリケーションの更新プログラム 3 の 2017 年 7 月のバージョン以降を使用する必要があります。 サイレント サービスが現在インストールされているすべてのコンポーネントを維持していることに注意してください。 任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を開始する前に実行します。

### <a name="examples-of-commands-for-silent-servicing"></a>サイレント サービスのコマンド例

このセクションでは、セルフサービスの大量展開に使用されるコマンドの例を示します。 これらのコマンドは、Retail Modern POS (オフラインでサポートされているインストーラーとオフラインでサポートされていないインストーラーの両方) 用インストーラー、ハードウェア ステーション、Retail Store スケール ユニットなど、すべての標準セルフサービス インストーラーで動作します。

#### <a name="silently-update-the-current-installation-of-retail-modern-pos"></a>Retail Modern POS の現在のインストールを自動的に更新

次のコマンドは、Retail Modern POS の現在のインストールをサイレント更新します。 このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。 このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。

```
ModernPOSSetup_V72.exe -S
```

> [!NOTE]
> Retail Store スケール ユニットにはまだコンフィギュレーション ファイルが必要です。 ただし、インストーラーは可能な場合はいつでも、現在インストールされているすべての値を保持します。

#### <a name="silently-update-the-current-installation-of-retail-store-scale-unit"></a>Retail Store Scale Unit の現在のインストールを自動的に更新

次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Store スケール ユニット の現在のインストールをサイレント更新します。 (このコンフィギュレーション ファイルは、インストーラーの実行可能ファイルと同じ場所にない可能性があります。) このコマンドは、前提条件のチェックをスキップし、インストール手順に進みます。 テストおよび開発の目的にのみ、このコマンドを使用することをお勧めします。

```
StoreSystemSetup_V72.exe -S -C "C:\Temp\StoreSystemSetup_V72_Houston.xml" -SkipPrerequisiteCheck
```

## <a name="mass-deployment-of-retail-modern-pos"></a>Retail Modern POS の一括配置

### <a name="before-you-begin"></a>準備

この機能を使用するには、バージョン 7.3 以降が必要です。 本社でのすべての店舗、レジスター、およびデバイスのコンフィギュレーション、およびその他のコンフィギュレーションが既に完了したとみなされます。 任意のコンフィギュレーションがまだ必要な場合は、このトピックの手順を実行する前に実行します。

### <a name="examples-of-commands-for-silent-mass-deployment"></a>サイレント マス展開のコマンド例

このセクションでは、Retail Modern POS、オフラインの Retail Modern POS、およびオフライン サポートのないインストーラのセルフサービスの大量展開に使用されるコマンドの例を示します。 Windows PowerShell スクリプトの例では、ユーザーがインストールを実行する支援も含まれます。

#### <a name="silently-install-retail-modern-pos"></a>Retail Modern POS をサイレント インストール

次のコマンドは、Retail Modern POS の現在のインストールをサイレント更新します。 このコマンドには、現在インストールされているコンポーネントのサイレント サービスに使用される標準的なコマンド構造があります。 この構造は **&lt;InstallerName&gt;.exe** の基本値とサイレント インストールのコマンド **-S** を使用します。 このコマンドは、構成ファイルが存在する場合は、インストーラーと同じファイルの場所にある構成ファイルを使用します。 このコマンドは、複数の構成ファイルを選択できる場合には使用しないでください。

```
ModernPOSSetup_V73.exe -S
```

> [!NOTE]
> Retail Modern POS にはコンフィギュレーション ファイルは不要です。 ただし、関連付けられている構成ファイルを読み込めない限り、インストールされた Retail Modern POS アプリは適切な方法では有効化されません。

#### <a name="silently-install-retail-modern-pos-by-using-a-specific-configuration-file"></a>特定のコンフィギュレーション ファイルを使用して Retail Modern POS をサイレント インストール

次のコマンドは、特定のコンフィギュレーション ファイルを使用して、Retail Modern POS の現在のインストールをサイレント インストールします。 この構成ファイルは、インストーラーの実行可能ファイルと同じ場所にないか、複数の構成ファイルが使用可能な場合があります。

```
ModernPOSSetup_V72.exe -S -C "C:\Temp\ModernPOSSetup_V73_Houston-3.xml"
```

