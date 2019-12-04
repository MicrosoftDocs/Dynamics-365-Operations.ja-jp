---
title: 仕入先設計を切り替える
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772367"
---
# <a name="switch-between-vendor-designs"></a>仕入先設計を切り替える

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>仕入先データ フロー 

仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、顧客から仕入先情報を分離する場合は、この基本的な仕入先設計を使用します。  

![基本的な仕入先フロー](media/dual-write-switch-1.png)
 
仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、仕入先情報を格納するため**アカウント** エンティティを使用し続ける場合は、この拡張された仕入先設計を使用します。 この設計では、仕入先の保留ステータスや仕入先のプロファイルなどの拡張仕入先情報が Common Data Service の**仕入先**エンティティに格納されます。 

![拡張された仕入先データ フロー](media/dual-write-switch-2.png)
 
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
    5. **アカウント** エンティティと**仕入先**エンティティで作成したワークフローを有効にして、仕入先情報を保管するために Customer Engagement **アカウント** エンティティの使用を開始します。 
 
