---
title: 輸送管理の雑費
description: このトピックでは、輸送によって生成される費用をどのように雑費コードに関連付ける必要があるかについて説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432433"
---
# <a name="transportation-management-miscellaneous-charges"></a>輸送管理の雑費

[!include [banner](../includes/banner.md)]

すべての雑費と同様、輸送によって生成される費用は雑費コードに関連付ける必要があります。 そうしないと、雑費として注文に戻されません。 **雑費コード** によって、雑費コードが追加される注文および注文明細行に関連して雑費がどのように計上されるかが決まります。

**輸送管理 > 設定 > 評価 > 雑費** に移動し、特定の **雑費コード** をいつ料金に適用するかを決定するための資格条件を定義します。

**雑費タイプ** が *なし* に設定されている、関連する **雑費モジュール** 設定 (*顧客* および *仕入先*) ごとに少なくとも 1 つの設定が必要です。 これが存在しない場合、雑費は注文に追加され *ません*。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]