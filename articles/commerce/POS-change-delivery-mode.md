---
title: POS の荷渡方法の変更
description: このトピックでは、POS の荷渡方法の変更操作のコンフィギュレーション方法および使用方法について説明します。
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: eaffe7821b60dd787a7d8b7533c1b8599033ba68
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594140"
---
# <a name="change-mode-of-delivery-in-pos"></a>POS の荷渡方法の変更

[!include [banner](includes/banner.md)]

このトピックでは、販売時点管理 (POS) の「荷渡方法の変更」機能の設定方法および使用方法について説明します。 

Dynamics 365 Commerce バージョン 10.0.10 以降では、POS 画面レイアウトへの **荷渡方法の変更** 操作 (647) の追加が使用可能です。

荷渡方法の変更機能により、POS トランザクションで 1 つ以上の出荷コンフィギュレーションの販売明細行に対して、荷渡方法を変更するオプションが提供されます。 以前のバージョンの Commerce では、出荷用にコンフィギュレーションされた既存の明細行の荷渡方法を変更する場合、**すべて出荷** または **選択された出荷** のコンフィギュレーション フロー全体を使用する必要がありました。 この処理には時間がかかり、明細行の配送元または配送日が誤って変更される可能性がありました。 この新しい機能により、これら販売明細行の荷渡方法を効率的に更新する代替方法が提供されます。

POS ボタン グリッドのボタンに操作を追加する方法の詳細については、[販売時点管理の画面レイアウト](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) を参照してください。

POS でこの機能がコンフィギュレーションされた後、**荷渡方法の変更** を選択すると、荷渡方法を変更するトランザクションの明細行を選択できる一覧のページが表示されます。 明細行の一部またはすべてを選択するか、または何も変更せずに終了することができます。 変更可能なリストの明細行は、以前に出荷用にコンフィギュレーションされた販売明細行のみです。 集荷または Carryout に指定された明細行を変更する場合、**すべて出荷** または **選択された出荷** 操作を使用する必要があります。 逆に、出荷として指定された明細行を集荷または Carryout に変更する場合、**すべて集荷**、**選択された集荷**、**すべて Carryout**、または **選択された Carryout** 操作を使用する必要があります。

変更する明細行を選択した後、**荷渡方法の変更** をクリックすると、荷渡方法のオプションの選択を求められます。 変更する明細行を複数選択した場合、POS は、選択した製品すべてが許容できるようにコンフィギュレーションされた荷渡方法のみが表示されます。 荷渡方法をコンフィギュレーションして、特定の製品および配送先住所をサポートすることができます。 ある製品と住所の組み合わせには受け入れられる荷渡方法が、選択した別の製品と住所の組み合わせでは受け入れられない場合、その荷渡方法は使用できません。 ある製品に別の製品でサポートされていない荷渡方法を選択する場合、各明細行に対して別々に 1 つずつ荷渡方法を変更する必要があります。  

新しい荷渡方法を選択した後、トランザクション ページが表示されます。 新しい荷渡方法の選択を確認するには、トランザクション リストの **荷渡** タブを選択します。

## <a name="additional-resources"></a>追加リソース

[コール センター注文の作成](tasks/create-call-center-orders.md)

[配送モードによるトランザクション メールのカスタマイズ](customize-email-delivery-mode.md)
