---
title: サービス注文の自動作成
description: 1 つのサービス契約または複数のサービス契約に対して、サービス注文を作成できます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
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
ms.openlocfilehash: 7d91ccc6a3ebaff220c8a876944b90d910399660
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814032"
---
# <a name="create-service-orders-automatically"></a>サービス注文の自動作成    

[!include [banner](../includes/banner.md)]


1 つのサービス契約または複数のサービス契約に対して、サービス注文を作成できます。 作成したサービス注文は、**サービス注文**フォームで表示できます。

サービス注文は、サービス契約の有効期間に対してのみ作成されます。 **サービス注文の作成**フォームで指定する範囲がサービス契約の開始日の前または終了日の後である場合、サービス注文は、その範囲のうちサービス契約日の期間内にある期間に対してのみ作成されます。

サービス注文を手動で作成する場合、またはサービス合意項目から自動的に作成する場合、その項目に対して終了日が指定されていない場合を除き、サービス注文は、その項目の開始日と終了日で定義された時間間隔内に該当する必要があります。

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>サービス契約に対するサービス注文の自動作成

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。

2.  サービス合意を選択します。

3.  **出荷**タブをクリックし、**計画されたサービス注文**をクリックします。

4.  **開始日**および**終了日**フィールドに日付を指定して、サービス期間を定義します。

5.  **情報ログの表示**チェック ボックスをオンにして、作成されたサービス注文の一覧を表示します。

6.  **トランザクション タイプを含む**フィールド グループで、トランザクション タイプを選択します。 トランザクション タイプは、サービス契約で作成された項目を表し、選択した各トランザクション タイプは、サービス契約項目で指定されたサービス期間に応じて複数のサービス注文を生成します。

7.  連続する一連のサービス注文に不足しているサービス注文を作成するには、**継続**チェック ボックスをオンにします。

8.  **OK** をクリックします。

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>複数のサービス契約に対するサービス注文の自動作成

1.  **サービス管理** \> **定期処理** \> **サービス注文** \> **サービス注文の作成**の順にクリックします。

2.  **選択**をクリックして、サービス注文の作成に使用する基準を追加または削除するための選択を行います。

3.  **OK**をクリックします。

## <a name="see-also"></a>参照

[サービス注文](service-orders.md)

[サービス注文の自動作成](auto-create-service-orders.md)

  


