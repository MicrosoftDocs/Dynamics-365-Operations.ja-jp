---
title: Microsoft Dynamics 365 Finance + Operations (オンプレミス) でサポートされるソフトウェア
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (on-premises) と互換性のあるソフトウェア コンポーネントのバージョンについて説明します。
author: faix
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Platform update 44
ms.openlocfilehash: c3602a39f83de4db77c13df73722f4f13932e60d
ms.sourcegitcommit: 41a5d18552bcc94cb1ddbbe3f3278eaf9d05f418
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617085"
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

## <a name="microsoft-sql-server"></a>Microsoft SQL Server

このセクションは、次の SQL Server コンポーネントをカバーします。

- データベース エンジン
- SQL Server Reporting Services (SSRS)
- SQL Server Integration Services (SSIS)

| バージョン                       | サポート開始  | 有効期間   |
|-------------------------------|------------------|---------------|
| Microsoft SQL Server 2016 SP2 | 10.0.9           | 使用不可 |
| Microsoft SQL Server 2016 SP1 | 元のリリース | 10.0.14       |

## <a name="minimum-azure-service-fabric-runtime"></a>最小 Azure Service Fabric 実行時間

Service Fabric Cluster は、公式ドキュメント [Service Fabric のサポートされているバージョン](/azure/service-fabric/service-fabric-versions)に沿って常にサポートされているバージョンである必要があります。

| 最小バージョン            | 以降で必要 |
|----------------------------|----------------|
| Service Fabric ランタイム 7.2 | 10.0.17        |
| Service Fabric ランタイム 7.1 | 10.0.14        |

## <a name="microsoft-office-server"></a>Microsoft Office Server

Office Server はオプションのコンポーネントです。 詳細については、[ドキュメント プレビューのコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md#for-a-microsoft-dynamics-365-finance--operations-on-premises-environment)を参照してください。

| バージョン                      | サポート開始 | 有効期間   |
|------------------------------|-----------------|---------------|
| Microsoft Office サーバー 2017 | 10.0.0          | 使用不可 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
