---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: ramasri
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
ms.author: ''
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6cf815247b8499f302b5f7b7b5659222f6e5f62
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172773"
---
# <a name="system-requirements-for-dual-write"></a>二重書き込みのシステム要件

[!include [banner](../../includes/banner.md)]



デュアル書き込みの接続設定には、次の要件があります。

+ Finance and Operations アプリのビルドバージョン 10.0.9、およびプラットフォーム更新プログラム 33 またはそれ以降
+ プラットフォーム バージョン 9.1.0000.11732 またはそれ以降の Microsoft Dynamics 365 モデル駆動型アプリ

> [!IMPORTANT]
> データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。 データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。

## <a name="one-version"></a>1 つのバージョン

将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。
