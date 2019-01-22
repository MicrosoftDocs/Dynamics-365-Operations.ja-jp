---
title: "法人間でのネットワーク プリンターへのアクセスの管理"
description: "このトピックでは、新しいシステム管理ユーティリティを使用してネットワーク プリンターを設定する方法に関する情報が提供されます。"
author: tjvass
manager: AnnBe
ms.date: 12/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-12-04
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b2a7a0724ddb2f5640a10eb43a999f8e21fb47f7
ms.openlocfilehash: 8bbea1299d3e2fc4e2123b93d1d3f22fb7426f1d
ms.contentlocale: ja-jp
ms.lasthandoff: 12/12/2018

---

# <a name="manage-access-to-network-printers-across-legal-entities"></a>法人間でのネットワーク プリンターへのアクセスの管理

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 新しいシステム管理ユーティリティへのアクセスは、Carbon Flighting Service によって管理されます。 Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新 23 (2018 年 12 月) には、システム管理者用の **システム ネットワーク プリンター管理** ページが含まれています。

ドメイン管理者は、ドキュメント回覧エージェント (DRA) を使用して、Microsoft Dynamics 365 for Finance and Operations サービスにネットワーク プリンターを登録します。 プリンターが登録されると、組織管理者がユーザーに利用できるようにします。 設定は **ネットワーク プリンターの管理**ページで管理されます (**組織管理** \> **設定** \> **ネットワーク プリンター**)。

**ネットワーク プリンターの管理** ページの設定は、組織の管理者用であるため、データは有効な法人に限定されます。 システム管理者は、法人間でネットワーク プリンターの設定を管理することはできないので、場合によっては、ネットワーク プリンターの変更が発生したときなど、法人間での設定の更新が困難です。 たとえば、ネットワーク プリンター パスが更新されたときやハードウェアを交換したとき、またはユーザーがプリンター キュー内のすべてのドキュメントを削除しようとしたときに、ネットワーク プリンター インスタンスが削除されます。

システム管理ユーティリティは、誤った印刷手順の復旧ツールです。 また、特定の法人からのアクセスなど、ネットワーク プリンター設定の管理のタスクが簡単になります。

## <a name="access-the-feature"></a>機能にアクセスする
機能がオンになると、**ネットワーク プリンターの管理** ページのアクション ウィンドウの **オプション** タブに **プレビュー** グループが表示されます。

![アクション ペインのプレビュー グループ](./media/network-printer-01.png)

1. **組織管理** > **設定** > **ネットワーク プリンター**の順に選択します。
2. アクション ウィンドウの **プレビュー** グループで、**システム ネットワーク プリンター** を選択します。
3. **システム ネットワーク プリンター** ページで、DRA を使用してサービスにネットワーク プリンターを登録します。 組織の各法人のコンフィギュレーション情報が表示されます。

## <a name="supported-operations"></a>サポートされている操作
現時点では、システム管理ユーティリティでは削除工程のみサポートされています。 **システム ネットワーク プリンター** ページを使用してネットワーク プリンターを削除した場合の結果を以下に示します。

- プリンターで指示されたプリンター キュー内のすべてのドキュメントが削除されます。
- 組織内のすべての法人のネットワーク プリンターが削除されます。
- ドメイン管理者は、古いプリンター名を使用してデバイスを登録することができます。
- 組織管理者、引き続き既存のツールを使用して、1 つの法人のネットワーク プリンターの設定を管理できます。

