---
title: Microsoft Dynamics 365 Finance + Operations (オンプレミス) でサポートされるソフトウェア
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) と互換性のあるソフトウェア コンポーネントのバージョンについて説明します。
author: faix
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Platform update 44
ms.openlocfilehash: 9450f48125d1e3954e17bf5e1887d19a9a6bdb4d
ms.sourcegitcommit: f699dbc21a06dbfb3fb299b789b428ea8d643868
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2021
ms.locfileid: "7603112"
---
# <a name="microsoft-dynamics-365-finance--operations-on-premises-supported-software"></a>Microsoft Dynamics 365 Finance + Operations (オンプレミス) でサポートされるソフトウェア

[!include [banner](../includes/banner.md)]

このトピックでは、依存ソフトウェアのどのバージョンが、Microsoft Dynamics 365 Finance + Operations (on-premises) と互換性があるかについて説明します。

## <a name="microsoft-windows-server"></a>Microsoft Windows Server

Microsoft WindowsServer Standard と Microsoft Windows Server Datacenter がサポートされます。

| バージョン                       | サポート開始  | 有効期間   |
|-------------------------------|------------------|---------------|
| Microsoft Windows サーバー 2019 | 10.0.17          | 使用不可 |
| Microsoft Windows サーバー 2016 | 元のリリース | 10.0.26       |

> [!NOTE]
> en-US オペレーティング システムのインストールのみがサポートされます。

## <a name="microsoft-sql-server"></a>Microsoft SQL Server

Microsoft SQL Server Standard Edition と Enterprise Edition の両方がサポートされます。

このセクションは、次の SQL Server コンポーネントをカバーします。

- データベース エンジン
- SQL Server Reporting Services (SSRS)
- SQL Server Integration Services (SSIS)

| バージョン                       | サポート開始  | 有効期間   |
|-------------------------------|------------------|---------------|
| Microsoft SQL Server 2019     | 10.0.21          | 使用不可 |
| Microsoft SQL Server 2016 SP2 | 10.0.9           | 10.0.28       |
| Microsoft SQL Server 2016 SP1 | 元のリリース | 10.0.14       |

> [!IMPORTANT]
> 単一の環境での Microsoft SQL Serverの複数のバージョンの使用はサポートされていません。

## <a name="active-directory-federation-services-ad-fs"></a>Active Directory フェデレーション サービス (AD FS)

Active Directory フェデレーション サービス (AD FS) は、Windows Server を実行しているマシンにインストールできるサーバー ロールです。 

| バージョン                                                     | サポート開始  | 有効期間   |
|-------------------------------------------------------------|------------------|---------------|
| Windows Server 2019 での Active Directory フェデレーション サービス (AD FS) | 10.0.17          | 使用不可 |
| Windows Server 2016 での Active Directory フェデレーション サービス (AD FS) | 元のリリース | 10.0.26       |

> [!IMPORTANT]
> - Windows Server 2016 の AD FS は、Azure Active Directory 認証ライブラリ (ADAL) を介した認証のみをサポートします。
> - 今後の Microsoft 認証ライブラリへの移行を受け入れるには、AD FS を Windows Server 2019 (MSAL) に展開する必要があります。 詳細については、[アプリケーションを Microsoft 認証ライブラリ (MSAL) に移行する](/azure/active-directory/develop/msal-migration) を参照してください。

## <a name="minimum-azure-service-fabric-runtime"></a>最小 Azure Service Fabric 実行時間

Service Fabric Cluster は、公式ドキュメント [Service Fabric のサポートされているバージョン](/azure/service-fabric/service-fabric-versions)に沿って常にサポートされているバージョンである必要があります。

| 最小バージョン            | 以降で必要 |
|----------------------------|----------------|
| Service Fabric ランタイム 7.2 | 10.0.17        |
| Service Fabric ランタイム 7.1 | 10.0.14        |

## <a name="minimum-microsoft-net-framework-runtime"></a>最小 Microsoft .NET フレームワーク ランタイム

.NET Framework の要件はノードごとに指定します。 固有の機能とバージョンについては、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](./setup-deploy-on-premises-pu41.md#prerequisites) を参照してください。

| 最小バージョン                        | 以降で必要 |
|----------------------------------------|----------------|
| Microsoft .NET フレームワーク バージョン 4.7.2 | 10.0.11        |

## <a name="microsoft-office-server"></a>Microsoft Office Server

Office Server はオプションのコンポーネントです。 詳細については、[ドキュメント プレビューのコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md#for-a-microsoft-dynamics-365-finance--operations-on-premises-environment)を参照してください。

| バージョン                      | サポート開始 | 有効期間   |
|------------------------------|-----------------|---------------|
| Microsoft Office サーバー 2017 | 10.0.0          | 使用不可 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
