---
title: 場所と関係者のリレーションシップ タイプの追加
description: このトピックでは、新規の場所および関係者のリレーションシップ タイプを追加する方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "357499"
---
# <a name="add-location-roles-and-party-relationship-types"></a>場所および関係者のリレーションシップ タイプの追加 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>場所のロールの追加

住所および連絡先情報について、新たに場所ロールを追加するには 2 つの方法があります。

-  **住所および連絡先情報の目的**ページに追加します。 新規ロールは **LogisticsLocationRole** テーブルにタイプ = 0 で保存されます。これは、ロールが **LogisticsLocationRoleType** 列挙型とその拡張で定義されたシステム ロールではないことを示しています。 ユーザーは住所や連絡先情報を作成するときに、このロールを使用できるようになります。

    ![住所とコンテンツ情報の目的](media/Address-Contact.PNG)

-  **LogisticsLocationRoleType** 列挙型拡張に追加し、データベースの同期プロセスで設定します。

    1.  **LogisticsLocationRoleType** 列挙型に拡張を作成し、新規ロールを追加します。 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. 新規ロールのリソース ファイルを新たに作成し、そのプロパティの値を割り当てます。
     
     ![新規リソース ファイル](media/Resource.PNG)
        
    3.  データ設定クラスを作成し、新規ロールを設定するハンドラー メソッドを指定します。 

        ![データ設定](media/Dirdata.PNG)

    4.  新規場所ロールの設定をテストするには、実行可能なクラスを作成し、Main() の DirDataPopulation::insertLogisticsLocationRoles() を呼び出します。 このプロセスが完了すると、**LogisticsLocationRole** テーブルでタイプ \>0 で設定した新規ロールが表示されます。 **住所と連絡先情報の目的**ページに新規ロールが表示されます。

        ![新規の場所の挿入](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>関係者のリレーションシップ タイプの追加 

新規リレーションシップ タイプを追加するには次の 2 つの方法があります。

-   **リレーションシップ タイプ**ページに追加します。 新規リレーションシップは **DirRelationshipTypeTable** に、systemtype = 0 で保存されます。

    ![関係タイプ](media/Relationship.PNG)

-  **DirSystemRelationshipType** 列挙型拡張に追加し、データベースの同期プロセスで設定します。

    1.  **DirSystemRelationshipType** 列挙に拡張を作成して、新規リレーションシップ タイプを追加します。

    2. この新規タイプの初期化子を作成します。 コア コードで複数の例を見つけることができます。そのうちの 1 つが **DirRelationshipTypeChildInitialize** です。 これは、関係者のリレーションシップ タイプが「子ども」の初期化子のクラスです。 このコードをコピーして貼り付けることで、初期化子を使って開始し、強調表示されたエリアを更新することができます。
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  新規リレーションシップ タイプの設定をテストするには、実行可能なクラスを作成し、Main() の DirDataPopulation::insertDirRelationshipTypes() を呼び出します。 **DirRelationshipTypeTable** に新規リレーションシップ タイプが表示され、**リレーションシップ タイプ**ページでこの新規リレーションシップ タイプが利用可能となります。

        ![実行可能なクラス](media/Runnable.PNG)
