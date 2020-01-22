---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Common Data Service 間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902728"
---
# <a name="switch-between-vendor-designs"></a>仕入先デザインの切り替え

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>仕入先データ フロー 

仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、顧客から仕入先情報を分離する場合は、この基本的な仕入先設計を使用します。  

![基本的な仕入先フロー](media/dual-write-vendor-data-flow.png)
 
仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、仕入先情報を格納するため**アカウント** エンティティを使用し続ける場合は、この拡張された仕入先設計を使用します。 この設計では、仕入先の保留ステータスや仕入先のプロファイルなどの拡張仕入先情報が Common Data Service の**仕入先**エンティティに格納されます。 

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)
 
次の手順に従って、仕入先の拡張設計を使用します。 
 
1. **SupplyChainCommon** ソリューション パッケージには、次の図に示すようなワークフロー プロセス テンプレートが含まれています。
    > [!div class="mx-imgBorder"]
    > ![ワークフロー プロセス テンプレート](media/dual-write-switch-3.png)
2. ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成します。 
    1. **アカウント エンティティで仕入先を作成**ワークフロー プロセス テンプレートを使用して、**仕入先**エンティティの新しいワークフロー プロセスを作成し、**OK** をクリックします。 このワークフローでは、**アカウント** エンティティの仕入先作成シナリオを処理します。
        > [!div class="mx-imgBorder"]
        > ![アカウント エンティティの仕入先の作成](media/dual-write-switch-4.png)
    2. **アカウント エンティティの更新**ワークフロー プロセス テンプレートを使用して、**仕入先**エンティティの新しいワークフロー プロセスを作成し、**OK** をクリックします。 このワークフローでは、**アカウント** エンティティの仕入先更新シナリオを処理します。 
        > [!div class="mx-imgBorder"]
        > ![アカウント エンティティの更新](media/dual-write-switch-5.png)
    3. **アカウント** エンティティで作成されたテンプレートから新しいワークフロー プロセスを作成します。 
        > [!div class="mx-imgBorder"]
        > ![仕入先エンティティで仕入先を作成](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![仕入先エンティティの更新](media/dual-write-switch-7.png)
    4. ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとして構成できます。 
        > [!div class="mx-imgBorder"]
        > ![バックグラウンド ワークフローへの変換](media/dual-write-switch-8.png)
    5. **アカウント** エンティティと**仕入先**エンティティで作成したワークフローを有効にして、仕入先情報を保管するために**アカウント** エンティティの使用を開始します。 
 
