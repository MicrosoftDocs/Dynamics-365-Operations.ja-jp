---
title: 住所をサービス注文に追加する
description: このトピックでは、サービス注文に顧客の住所を追加する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "311913"
---
# <a name="add-an-address-to-a-service-order"></a>住所をサービス注文に追加する    

[!include [banner](../includes/banner.md)]


このトピックでは、サービス注文に顧客の住所を追加する方法について説明します。 サービス注文を作成する際、住所情報は、そのサービス注文が関連付けられているプロジェクトから転送されます。 ただし、顧客、仕入先、サイト、倉庫、サービス注文およびプロジェクトの Microsoft Dynamics AX に既に入力した住所から別の場所を選択することができます。

また、新しい住所を作成することもできます。 既定では、新しい住所はプロジェクトに転送されます。 ただし、新しい住所がサービスのこのインスタンスにのみ関連するよう指定できます。 その場合、新しい住所はプロジェクトに転送されません。

## <a name="create-a-customer-address-for-a-service-order"></a>サービス注文に対する顧客の住所の作成

サービス注文に住所を追加するには、次の手順に従います。

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。

2.  住所を作成するサービス注文を開きます。

3.  **アクション ペイン**で**編集**をクリックして、**ヘッダー ビュー**をクリックします。

4.  **アドレス**クイック タブで、**住所の追加**をクリックします。

5.  **新しい住所**フォームに、住所の一意の名前を入力し、残りのフィールドに入力します。 
    

    > [!WARNING]
    > <P>既存の住所と同じ名前を入力した場合、残りのフィールドに入力した情報が、既存の住所の情報に上書きされます。</P>


6.  自分のサービス注文に新しい住所をコピーするには **OK** をクリックします。

## <a name="specify-an-alternative-address-on-a-service-order"></a>サービス注文に対する代替住所の指定

サービス注文に別の住所を追加するには、次の手順に従います。

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。

2.  別の住所を入力するサービス注文を開きます。

3.  **アクション ペイン**で**編集**をクリックして、**ヘッダー ビュー**をクリックします。

4.  **アドレス**クイック タブで、**その他の追加**をクリックします。

5.  **レコード タイプ**フィールドの**アドレスの選択**フォームで、**サービス注文**を選択します。

6.  住所を選択して **OK** をクリックし、自分のサービス注文にコピーします。


  


