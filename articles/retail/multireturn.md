---
title: 複数の顧客注文および請求書間での品目の返品
description: このトピックでは、複数の顧客注文および請求書をまたいだ返品を有効にする Microsoft Dynamics 365 for Retail の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565303"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>複数の顧客注文および請求書間での品目の返品

[!include [banner](includes/banner.md)]


以前のリリースでは、一度に 1 つの請求書の返品しか処理できませんでしたが、Dynamics 365 for Finance and Operations バージョン 10.0 では、複数の注文および請求書をまたいだ返品の処理が可能です。 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>複数の顧客注文および請求書をまたいだ返品をサポートするように Retail を構成する

1. **小売パラメーター \> 顧客注文**に移動します。
1. **複数の注文の返品を有効化**パラメーターをオンにします。 

## <a name="process-returns"></a>返品の処理

パラメーターをオンにし、変更を店舗に同期させると、店舗のレジ担当者は、顧客の返品に対して複数の販売注文を選択できるようになります。

注文を選択すると、その注文のすべての請求書で返品可能なすべての商品の一覧が表示されます。 レジ担当者は、その一覧から返品する商品を選択できます。 選択したすべての商品に対して 1 つの返品注文が作成されます。
