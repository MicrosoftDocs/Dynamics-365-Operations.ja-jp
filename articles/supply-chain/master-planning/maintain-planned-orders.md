---
title: "計画オーダーの管理"
description: "この記事は、計画オーダーの管理方法について説明します。 計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8931908fbf643a8154da70d2ad065ea47d2aa4e6
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="maintain-planned-orders"></a>計画オーダーの管理

[!include[banner](../includes/banner.md)]


この記事は、計画オーダーの管理方法について説明します。 計画オーダーの状態の更新と確定、選択した計画オーダーとして同じ状態である計画オーダーをフィルター処理する方法について説明します。

**マスター プラン** ワークスペース、**計画オーダー** リスト、または**計画製造オーダー**、**計画発注書**、および**計画移動**リストから計画オーダーを管理できます。 [**ステータス**] フィールドを使用して、進捗状況を追跡できます。 次の値が使用されます。

-   マスター プランによって計画オーダーが生成されたとき、計画オーダーのステータスは [**未処理**] になります。
-   計画オーダーを確定しない場合は、ステータスを [**完了済み**] に設定できます。
-   計画オーダーを確定しない場合は、ステータスを [**承認済**] に設定できます。 このステータスは、計画オーダーの確定を承認し、確定がまだ行われていない状態を示します。

**注記:** 承認された計画オーダーは、その現在の状態から次のマスター プランの計算に転送されます。 [**確定**] をクリックして、計画オーダーを確定します。 確定できる計画オーダーは次のとおりです。

-   選択されている計画オーダー。
-   複数の計画オーダー。
-   **展開** ページからの展開によって生成された計画オーダー。 [**計画オーダー**] をクリックし、計画オーダーを選択した後、[**確定**] をクリックします。

計画オーダーが確定されると、関連するモジュールの注文セクションにその計画オーダーが移動します。 **注記:** 特定のステータスにある計画オーダーを右クリックし、同じステータスにある他の計画オーダーをフィルター処理することができます。 この機能は、たとえば、[**承認済み**] のステータスにあるすべての計画オーダーをフィルター処理して確定する場合などに便利です。

<a name="see-also"></a>参照
--------

[マスタ プラン](master-plans.md)




