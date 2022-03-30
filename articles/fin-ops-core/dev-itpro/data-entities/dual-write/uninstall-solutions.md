---
title: 二重書き込みアプリケーション オーケストレーション ソリューションのアンインストール
description: このトピックでは、二重書き込みアプリケーション オーケストレーション ソリューションをアンインストールする方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 781b2cb19a563d5712fa65718c93bfdc242f0c4a
ms.sourcegitcommit: abfaef124c8747827d6f297821f01f1f6fbca6b7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455324"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>二重書き込みアプリケーション オーケストレーション ソリューションのアンインストール

[!include [banner](../../includes/banner.md)]

このトピックでは、二重書き込みアプリケーション オーケストレーション ソリューションをアンインストールする方法について説明します。

一部の顧客は、Microsoft Dataverse 環境に複数のソリューションをインストールする二重書き込みアプリケーション オーケストレーション パッケージを意図せずにインストールします。 パッケージに特別なソリューションをインストールすると、予期しない問題や問題が発生する場合があります。

二重書き込みアプリケーション オーケストレーション パッケージのインストールに関連する問題を修正するには、次の順序で不要な二重書き込みソリューションをアンインストールします。

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (存在する場合)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (このソリューションをアンインストールするには、Microsoft とサポート チケットを開く必要があります)。
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

当事者向けおよびグローバル用のアドレス帳ソリューションがインストールされている場合は、次の順序でソリューションをアンインストールしてください。

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. 関係者
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
