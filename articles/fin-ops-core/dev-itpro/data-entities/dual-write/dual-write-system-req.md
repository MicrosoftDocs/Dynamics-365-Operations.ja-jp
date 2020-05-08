---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63bb9e2ed43300f274102eac43326288df3152a2
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275712"
---
# <a name="system-requirements-for-dual-write"></a>二重書き込みのシステム要件

[!include [banner](../../includes/banner.md)]



デュアル書き込みの接続設定には、次の要件があります。

+ Finance and Operations アプリのビルド バージョン 10.0.9 (10.0.383.20013) (品質更新プログラム)、および Platform update 33 以降
+ プラットフォーム バージョン 9.1.0000.11732 またはそれ以降の Microsoft Dynamics 365 モデル駆動型アプリ

二重書き込みには、次の制限があります:

+ データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。 データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。
+ 二重書き込み設定は、Finance and Operations アプリの試用版インスタンスではサポートされていません。 
+ 二重書き込みは、会社間データをサポートしていません。

## <a name="one-version"></a>1 つのバージョン

将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。
