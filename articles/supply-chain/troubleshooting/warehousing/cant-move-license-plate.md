---
title: 空の払出と空白の入庫が許可されている場合は、ライセンス プレートを移動できません
description: シリアル番号で空の払出と空白の入庫が許可されている場合は、ライセンス プレートを移動できません。 これは、シリアル番号フィールドをオプションにすることで固定されます。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476868"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>シリアル番号で空の払出と空白の入庫が許可されている場合は、ライセンス プレートを移動できません

## <a name="symptoms"></a>現象

追跡用分析コード グループでシリアル番号が *払出時空白可* および *受入時空白可* に設定されている場合、および同じ場所に複数のライセンス プレートがあり、シリアル番号があるものとないものがある場合、**移動** メニュー項目を使用してライセンス プレートを移動することはできません。

## <a name="resolution"></a>解決策

この問題は、[KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) で展開された変更によって修正されます。 この変更により、空白の受入と払出が許可されている場合に、**シリアル番号** フィールドがオプションとして設定されます。
