---
title: Finance and Operations アプリおよび Common Data Service の初期同期の実行順序
description: このトピックでは、初期データを作成するために従う必要がある同期の順序を指定します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184511"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Finance and Operations アプリおよび Common Data Service の初期同期の実行順序

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

データ統合を使用する前に、顧客、仕入先、および取引先担当者に必要な初期データを作成する必要があります。 たとえば、新しい**仕入先グループ**の品目を作成し、**支払条件**の値を **Net30** に設定するとします。 この場合、**仕入先グループ**の品目を作成する前に、**Net30** がアプリケーションおよび Common Data Service の両方に存在することを確認する必要があります。 (将来的には、Microsoft は初期同期と呼ばれるデュアル書き込みプラットフォーム機能をリリースする予定です。この機能によりデュアル書き込みセットアップの一部としてアプリケーションおよび Common Data Service 間で 1 回限りのデータ同期が行われます。)

> [!TIP]
> Microsoft は**支払条件** (支払条件) を含む、すべての参照データのデュアル書き込みマップをリリースします。 1 つのシステムに初期データが既に含まれる場合は、レコードの小さな更新操作によって、そのレコードのデュアル書き込みをトリガーできます。

次の優先順位に従い、初期データがアプリケーションと Common Data Service の両方で使用できるようにする必要があります。

## <a name="vendor"></a>仕入先

**仕入先**エンティティに対する実行の順序を次に示します。

1. 仕入先グループ

    1. 支払条件

        1. 支払期日および明細行
        2. 支払スケジュール

2. 仕入先支払方法

## <a name="customer-organization"></a>顧客 (組織)

**顧客**エンティティに対する実行の順序を次に示します。

1. 顧客グループ

    1. 支払条件

        1. 支払期日および明細行
        2. 支払 

2. 顧客支払方法

## <a name="contact-person"></a>連絡先 (名前)

**連絡先**エンティティに対する実行の順序を次に示します。

1. 顧客
2. 仕入先
