---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: RamaKrishnamoorthy
ms.date: 01/14/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6793b516546ea54854a274bf2398e29cfd2f236
ms.sourcegitcommit: 79d19924ed736c9210fa9ae4e0d4c41c53c27eb5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2021
ms.locfileid: "7581803"
---
# <a name="system-requirements-for-dual-write"></a>二重書き込みのシステム要件

[!include [banner](../../includes/banner.md)]

デュアル書き込みの接続設定には、次の要件があります。

+ Finance and Operations アプリのビルド バージョン 10.0.9 (10.0.383.20013) (品質更新プログラム)、および Platform update 33 以降
+ プラットフォーム バージョン 9.1.0000.11732 以降の Customer Engagement アプリ

二重書き込みには、次の制限があります:

+ データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](../../../../supply-chain/sales-marketing/accounts-template-mapping-direct.md) を並行して実行することはできません。 データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。
+ 二重書き込み設定は、Finance and Operations アプリの試用版インスタンスではサポートされていません。
+ 単一の Finance and Operations アプリ インスタンスおよび単一の Customer Engagement アプリ インスタンスを統合するには、二重書き込みを使用する必要があります。
+ 二重書き込みには現在、40 の法人を限度とする初期同期があります。
+ 二重書き込みのライブ同期は現在、250 の法人に制限されています。
+ 二重書き込みは、[会社間のデータ共有](../../sysadmin/cross-company-data-sharing.md) をサポートしていません。
+ 二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure Active Directory (Azure AD) テナントに含める必要があります。
+ 二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure データセンター テナントに配置する必要があります。
+ 二重書き込みは、Finance and Operations アプリの **doInsert**、**doUpdate**、および **doDelete** イベントによりトリガーされません。 二重書き込みをトリガーする場合は、Finance and Operations アプリの **挿入**、**更新**、**削除** イベントを使用します。 
+ 二重書き込みでは、分散トランザクションはサポートされません。 たとえば、[製品受領書の転記プロセスがキャンセルされた](scm-field-service-procurement.md#cancelling-the-posting-process)場合、二重書き込みは製品受領書を Dataverse で作成する場合がありますが、Supply Chain Management では作成しません。 



## <a name="one-version"></a>1 つのバージョン

将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
