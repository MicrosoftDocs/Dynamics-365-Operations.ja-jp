---
title: "オンプレミス環境での小売チャネルのコンポーネントのインストール手順"
description: "このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。"
author: aamirallaqaband
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 0967b10c2037c24c044f38c49b1b998f6771c66b
ms.openlocfilehash: 09fdcb014c010a79ba92f8578cc7e1207bb6e238
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a>オンプレミス環境での小売チャネルのコンポーネントのインストール手順

[!include[banner](../includes/banner.md)]

このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。

## <a name="overview"></a>概要

オンプレミス環境では、小売チャネル機能は Retail Store Scale Unit の使用により排他的に有効になります。 Retail Store Scale Unit の概要については、[Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md) を参照してください。 

クラウド展開とは異なり、オンプレミス環境では Lifecycle Services (LCS) 経由で小売チャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。 Retail Store Scale Unit をインストールすることによってのみ、小売チャネル コンポーネントを使用できます。

## <a name="prerequisites"></a>前提条件 

小売チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。 この手順は、[オンプレミス環境の設定と配置 (Platform update 12 以降)](setup-deploy-on-premises-pu12.md)で説明されています。

必ず、セキュリティで保護されたネットワークを使用して、Retail Store Scale Unit (RSSU) を、パブリックにアクセスできない小売用バック オフィスに接続するようにもしてください。 さらに、小売用バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の RSSU デバイスのみに制限してください。

## <a name="installation-steps"></a>インストール手順

1.  以前に作成した[ファイル共有](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/deployment/setup-deploy-on-premises-pu8-pu11#setupfile)で、**RetailSelfServicePackages** と呼ばれる新しいフォルダーを作成します。
2.  各 AOS コンピューターで、次の PowerShell スクリプトを実行します。

```powershell
.\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database -DatabaseName 'Database name for AOS database ' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages>’ -SendProductSupportTelemetryToMicrosoft <True/False>
```
  
3.  LCS からバイナリ更新プログラムをダウンロードします。 手順については、[Lifecycle Services (LCS) から更新プログラムを入手](../migration-upgrade/download-hotfix-lcs.md)を参照してください。
4.  zip ファイルを展開し、上記のファイル共有の場所に作成した RetailSelfServicePackages フォルダーにある ModenPOSSetup.exe および StoreSystemSetup.exe をコピーします。
5.  Retail Store Scale Unit をインストールするためのインストール手順に従います。 手順については、[Retail Store Scale Unit のコンフィギュレーションとインストール](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md)を参照してください。


