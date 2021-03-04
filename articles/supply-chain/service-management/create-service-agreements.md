---
title: サービス契約の作成
description: このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a1a47761869a4190eac6dc9e069a6b520bf7a1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432153"
---
# <a name="create-service-agreements"></a>サービス契約の作成

[!include [banner](../includes/banner.md)]

このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。

## <a name="create-a-service-agreement-from-service-management"></a>サービス管理からのサービス合意の作成

1. **サービス管理** に移動します。
2. **サービス契約** をクリックして、ページ ヘッダーで新しいサービス契約項目を作成します。 
3. **新規** をクリックします。 説明を入力し、**プロジェクト ID** フィールドでプロジェクトへの参照を選択し、サービス合意の残りのフィールドおよび項目に情報を入力します。 **保存** をクリックします。
4. **関係** タブで、**サービス対象** または **サービス タスク** を選択して、サービス合意のサービス対象関係またはサービス作業関係を作成します。 関係を作成したサービス対象およびサービス作業は、サービス合意項目で関連付けることができます。
5. ページの下半分で、サービス テンプレートまたは別のサービス契約から明細行をコピーするか、またはサービス契約項目を手動で作成して、サービス契約項目を作成します。

> [!NOTE]
> あるサービス合意に別のサービス合意項目をコピーする場合は、サービス対象やサービス タスク関係もコピーするかどうかを指定できます。 これらの関係をコピーすると、これらの関係がサービス合意の既存の関係に追加されます。 サービス テンプレートからサービス合意項目をコピーする場合は、サービス対象関係およびサービス作業関係が、新しいサービス合意項目のサービス対象関係およびサービス作業関係として自動的にコピーされます。

## <a name="create-service-agreement-lines-manually"></a>手動によるサービス契約項目の作成

1. **サービス契約** ページから、行グリッドにサービス契約項目を追加します。 
2. このサービス契約項目の適切な情報を入力します。 
3. **CTRL + S** キーを押して項目を保存し、ページを閉じます。

## <a name="create-a-service-agreement-from-project"></a>プロジェクトからのサービス合意の作成

1. **プロジェクト管理と会計** をクリックします。
2. **すべてのプロジェクト** をクリックします。
3. リストからプロジェクトを選択します。
4. **アクション ウィンドウ** で、**管理** をクリックします。 **新規** アクション グループで、**サービス** をクリックして **サービス契約** を選択します。
5. このトピックで前述されているように、**サービス契約の作成** というタイトルのセクションで手順に従ってプロジェクト参照を入力します。


## <a name="related-topics"></a>関連トピック

[サービス契約の作成および締結の概要](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]