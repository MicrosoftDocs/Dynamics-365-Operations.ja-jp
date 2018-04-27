---
title: "サービス契約の作成"
description: "このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: ja-jp
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a>サービス契約の作成

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。

## <a name="create-a-service-agreement-from-service-management"></a>サービス管理からのサービス合意の作成

1. **サービス管理**に移動します。
2. **サービス契約** をクリックして、ページ ヘッダーで新しいサービス契約項目を作成します。 
3. [**新規**] をクリックします。 説明を入力し、**プロジェクト ID** フィールドでプロジェクトへの参照を選択し、サービス合意の残りのフィールドおよび項目に情報を入力します。 [**保存**] をクリックします。
4. **関係** タブで、**サービス対象** または **サービス タスク** を選択して、サービス合意のサービス対象関係またはサービス作業関係を作成します。 関係を作成したサービス対象およびサービス作業は、サービス合意項目で関連付けることができます。
5. ページの下半分で、サービス テンプレートまたは別のサービス契約から明細行をコピーするか、またはサービス契約項目を手動で作成して、サービス契約項目を作成します。

> [!NOTE]
> あるサービス合意に別のサービス合意項目をコピーする場合は、サービス対象やサービス タスク関係もコピーするかどうかを指定できます。 これらの関係をコピーすると、これらの関係がサービス合意の既存の関係に追加されます。 サービス テンプレートからサービス合意項目をコピーする場合は、サービス対象関係およびサービス作業関係が、新しいサービス合意項目のサービス対象関係およびサービス作業関係として自動的にコピーされます。

## <a name="create-service-agreement-lines-manually"></a>手動によるサービス契約項目の作成

1. **サービス契約** ページから、行グリッドにサービス契約項目を追加します。 
2. このサービス契約項目の適切な情報を入力します。 
3. **CTRL + S** キーを押して項目を保存し、ページを閉じます。

## <a name="create-a-service-agreement-from-project"></a>プロジェクトからのサービス合意の作成

1. **プロジェクト管理と会計**をクリックします。
2. **すべてのプロジェクト**をクリックします。
3. リストからプロジェクトを選択します。
4. **アクション ウィンドウ**で、**管理**をクリックします。 **新規** アクション グループで、**サービス** をクリックして **サービス契約**を選択します。
5. このトピックで前述されているように、**サービス契約の作成** というタイトルのセクションで手順に従ってプロジェクト参照を入力します。


## <a name="related-topics"></a>関連トピック

[サービス合意 ](service-agreements.md)



