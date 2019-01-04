---
title: "ハイブリッド顧客注文"
description: "ハイブリッド顧客注文は 1 つの注文で、顧客によって店舗で処理できる製品と、集配や後日出荷される製品を含みます。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 88d12641fa05953f7082158303237b7ba40c3fe2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="hybrid-customer-orders"></a>ハイブリッド顧客注文

[!include [banner](includes/banner.md)]

ハイブリッド顧客注文は 1 つの注文で、顧客によって店舗で処理できる製品と、集配や後日出荷される製品を含みます。

Microsoft Dynamics 365 for Retail では、顧客注文のすべての製品または選択された製品の処理を選択できます。 注文が作成されると、処理としてマークされた製品ラインが自動的に請求され、これは注文が作成された後集荷される注文の場合も同じです。 ハイブリッド注文の支払金額は、処理行の総額のある集荷および出荷製品ラインに預金率を追加することによって決まります。 ハイブリッド注文の場合、システムは顧客注文モードと現金売りモードとを次のように切り替えます。

- カート内の全製品を **配送実行** に設定する場合、注文は現金売りトランザクションとして処理されます。
- カート内のいくつかまたはすべての製品を **集配** または **出荷配送** に設定する場合、注文は顧客注文トランザクションとして処理されます。

カート行が選択され、**選択されたピッキング**、**選択された出荷**、または **選択対象の実行** が選択されている場合、特定のカート行はその配送方法で設定されます。 この場合、工程の下流の流れは通常どおり続きます。 ただし、選択されているカート行がない状態で **選択されたピッキング**、**選択された出荷**、または **選択対象の実行** が選択された場合、すべてのカート行を一覧化する新しいページが開きます。 この画面で、一度に複数行を選択して、配送方法を設定できます。 選択している行にその方法を使用する場合、行に割り当てられた前の配送方法は上書きされます。

## <a name="additional-resources"></a>その他のリソース

[顧客注文の概要](customer-orders-overview.md)

