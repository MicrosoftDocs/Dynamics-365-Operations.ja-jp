---
title: 複数の顧客注文および請求書間での品目の返品
description: この記事では、複数の顧客注文および請求書をまたいだ返品を有効にする Dynamics 365 Commerce の機能について説明します。
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890324"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>複数の顧客注文および請求書間での品目の返品

[!include [banner](includes/banner.md)]


複数の顧客注文および請求書間で返品が可能です。 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>複数の顧客注文および請求書をまたいだ返品をサポートするように Commerce を構成する

1. **コマース パラメーター \> 顧客注文** に移動します。
1. **複数の注文の返品を有効化** パラメーターをオンにします。 

## <a name="process-returns"></a>返品の処理

パラメーターをオンにし、変更を店舗に同期させると、店舗のレジ担当者は、顧客の返品に対して複数の販売注文を選択できるようになります。

注文を選択すると、その注文のすべての請求書で返品可能なすべての製品の一覧が表示されます。 レジ担当者は、その一覧から返品する商品を選択できます。 選択したすべての商品に対して 1 つの返品注文が作成されます。
