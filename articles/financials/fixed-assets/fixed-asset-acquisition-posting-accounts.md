---
title: "固定資産の取得の転記勘定"
description: "この記事は、資産の取得について総勘定元帳の転記勘定を設定する方法を説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a1a7da48b45566217399bc1d01a9c6e87ad56ec8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-acquisition-posting-accounts"></a>固定資産の取得の転記勘定

[!include [banner](../includes/banner.md)]

この記事は、資産の取得について総勘定元帳の転記勘定を設定する方法を説明します。

固定資産の取得の転記に使用される勘定は、資産を取得するのに使用された方法によって異なる場合があります。 [固定資産転記プロファイル] ページの [勘定科目] タブで、元帳に転記する固定資産勘定を設定するための取得と取得原価調整を選択します。 

仕訳帳および発注書では、通常、勘定科目は貸借対照表の勘定で、新しい固定資産の取得金額は借方に転記されます。 この勘定は仕訳帳に表示されず、トランザクションで置き換えることができません。 

相手勘定も貸借対象表の勘定です。 一般的な仕訳帳および固定資産仕訳帳では、この勘定は、資産の取得の支払に使用される銀行口座になることがよくあります。 相手勘定は、仕訳帳で提示される既定の勘定です。 相手勘定は、仕訳帳で勘定科目表の他のどの勘定にも変更でき、また固定資産を仕入先から購入した場合は仕入先勘定にも変更できます。 

買掛金勘定の [請求仕訳帳] または [発注書] が固定資産の取得に使用される場合、固定資産トランザクションの相手勘定は、そのトランザクションで選択された仕入先勘定に置き換えられます。

[総勘定元帳] の [固定資産の在庫仕訳帳] を使用して転記された取得の場合、固定資産は外部のソースから購入されたのではなく、会社の在庫から移動されています。 したがって、相手勘定は、在庫管理の在庫品目に対する在庫払出勘定になります。

詳細については、「[調達によって取得される資産の取得](acquire-assets-procurement.md)」を参照してください。




