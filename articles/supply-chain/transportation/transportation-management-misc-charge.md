---
title: 輸送管理の雑費
description: この記事では、輸送によって生成される費用をどのように雑費コードに関連付ける必要があるかについて説明します。
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cc4c595d8b61cb9b6c81af4bf7f03faa1a12960
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849216"
---
# <a name="transportation-management-miscellaneous-charges"></a>輸送管理の雑費

[!include [banner](../includes/banner.md)]

すべての雑費と同様、輸送によって生成される費用は雑費コードに関連付ける必要があります。 そうしないと、雑費として注文に戻されません。 **雑費コード** によって、雑費コードが追加される注文および注文明細行に関連して雑費がどのように計上されるかが決まります。

**輸送管理 > 設定 > 評価 > 雑費** に移動し、特定の **雑費コード** をいつ料金に適用するかを決定するための資格条件を定義します。

**雑費タイプ** が *なし* に設定されている、関連する **雑費モジュール** 設定 (*顧客* および *仕入先*) ごとに少なくとも 1 つの設定が必要です。 これが存在しない場合、雑費は注文に追加され *ません*。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]