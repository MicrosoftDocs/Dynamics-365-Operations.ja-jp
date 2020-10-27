---
title: サービス作業関係の作成
description: サービス契約またはサービス注文で実行するサービス作業を記述するには、サービス作業をその契約または注文に関連付けることができます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e50b4322c65097ab4f8aba9c36e4d5e6cc4c01b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978633"
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

[サービス作業の概要](service-tasks.md)


  


