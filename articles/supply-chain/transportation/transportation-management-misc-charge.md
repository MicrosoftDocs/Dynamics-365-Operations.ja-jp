---
title: 輸送管理の雑費
description: このトピックでは、輸送によって生成される費用をどのように雑費コードに関連付ける必要があるかについて説明します。
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
ms.openlocfilehash: e54c94baeba487ccd8fe26e58d3e891e5e3a1088
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672601"
---
# <a name="transportation-management-miscellaneous-charges"></a>輸送管理の雑費

[!include [banner](../includes/banner.md)]

すべての雑費と同様、輸送によって生成される費用は雑費コードに関連付ける必要があります。 そうしないと、雑費として注文に戻されません。 **雑費コード** によって、雑費コードが追加される注文および注文明細行に関連して雑費がどのように計上されるかが決まります。

**輸送管理 > 設定 > 評価 > 雑費** に移動し、特定の **雑費コード** をいつ料金に適用するかを決定するための資格条件を定義します。

**雑費タイプ** が *なし* に設定されている、関連する **雑費モジュール** 設定 (*顧客* および *仕入先*) ごとに少なくとも 1 つの設定が必要です。 これが存在しない場合、雑費は注文に追加され *ません*。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]