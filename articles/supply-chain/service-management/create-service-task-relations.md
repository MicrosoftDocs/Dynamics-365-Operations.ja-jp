---
title: "サービス作業関係の作成"
description: "サービス契約またはサービス注文で実行するサービス作業を記述するには、サービス作業をその契約または注文に関連付けることができます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0892161605401420c0817b3b644271357446a99b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-task-relations"></a>サービス作業関係の作成    

[!include [banner](../includes/banner.md)]

サービス契約またはサービス注文で実行するサービス作業を記述するには、サービス作業をその契約または注文に関連付けることができます。 この情報は、サービス技術者および顧客が利用できます。

## <a name="create-a-relation-with-a-service-agreement"></a>サービス合意との関係の作成

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。

2.  既存のサービス合意を選択するか、新しいサービス合意を作成します。

3.  アクション ウィンドウで、**サービス作業**ボタンをクリックします。

4.  **サービス作業**フォームで Ctrl + N キーを押して新しい行を作成し、**サービス作業**リストからサービス作業を選択して、サービス作業をサービス契約に関連付けます。

5.  **説明**タブで、自由書式のフィールドに内部または外部の任意のメモ説明を入力します。

6.  フォームを閉じてレコードを保存します。

この手順を繰り返して、必要なすべてのサービス作業をサービス合意に関連付けます。 これらのサービス作業は、関連付けられた任意の合意明細行に対して指定できます。

サービス合意に対して作成したサービス作業関係は、そのサービス合意に関連付けられているすべてのサービス注文から使用できます。

## <a name="create-a-relation-with-a-service-order"></a>サービス注文との関係の作成

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。

2.  既存のサービス注文を選択するか、新しいサービス注文を作成します。

3.  アクション ウィンドウで、**サービス作業**ボタンをクリックします。

4.  **サービス作業**フォームから、Ctrl + N キーを押して新しい行を作成し、**サービス作業**リストからサービス作業を選択して、サービス作業をサービス注文に関連付けます。

5.  **説明**タブで、自由書式のフィールドに内部または外部の任意のメモ説明を入力します。

6.  フォームを閉じてレコードを保存します。

この手順を繰り返して、必要なすべてのサービス作業をサービス注文に関連付けます。 関係を作成したサービス作業は、サービス注文明細行の作成時に選択できます。

サービス注文に対して作成されたサービス作業関係は、そのサービス注文でのみ使用できます。

## <a name="see-also"></a>参照

[サービス作業](service-tasks.md)


  



