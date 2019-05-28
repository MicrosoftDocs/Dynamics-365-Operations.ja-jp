---
title: サービス対象関係の作成
description: このトピックでは、サービス契約またはサービス注文のサービス対象の関係を作成する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 792ceea52a9caa1a99217c77bb3fe4aafb80a0eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555016"
---
# <a name="create-service-object-relations"></a>サービス対象関係の作成 

[!include [banner](../includes/banner.md)]


このトピックでは、サービス契約またはサービス注文のサービス対象の関係を作成する方法について説明します。 サービス対象の関係を作成すると、サービス対象がサービス契約またはサービス注文に関連付けられます。 顧客がサービス対象である品目に対するサービスを要求すると、サービス対象の関係の一覧からサービス対象を選択できます。

## <a name="create-a-service-object-relation-for-a-service-agreement"></a>サービス契約に対するサービス対象の関係の作成

次の手順で、サービス契約に対してサービス対象の関係を作成します。

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。

2.  **サービス契約**一覧で、既存のサービス契約を選択するか、**新規**をクリックして新しいサービス契約を作成します。

3.  **関係**グループの**サービス契約**タブの、**アクション ウィンドウ**における、**サービス契約**フォームで、**サービス対象**をクリックします。

4.  **サービス対象**フォームで、**新規**をクリックし、このサービス契約に対するサービス対象を選択します。

5.  テンプレートの部品表 (BOM) をサービス契約に割り当てるには、**機能**をクリックし、**テンプレート BOM の添付**を選択します。 **テンプレート BOM の選択**フォームの**テンプレート**フィールドで、テンプレートを選択します。 

## <a name="create-a-service-object-relation-for-a-service-order"></a>サービス注文に対するサービス対象の関係の作成

次の手順で、サービス注文に対してサービス対象の関係を作成します。

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。

2.  **サービス注文**一覧で既存のサービス注文を選択するか、新しいサービス注文を作成します。

3.  **関係**グループの**サービス注文**タブの、**アクション ウィンドウ**における、**サービス注文**フォームで、**サービス対象**をクリックします。

4.  **サービス対象** フォームで、**新規**をクリックし、このサービス注文に対するサービス対象を選択します。

5.  テンプレート BOM をサービス契約に割り当てるには、**機能**をクリックし、**テンプレート BOM の添付**を選択します。 **テンプレート BOM の選択**フォームの**テンプレート**フィールドで、テンプレートを選択します。 


## <a name="see-also"></a>参照

[サービス対象](service-objects.md)

[サービス対象の関係](service-object-relations.md)

[テンプレート BOM](template-boms.md)

  


