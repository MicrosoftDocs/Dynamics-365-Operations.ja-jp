---
title: ファントム製品の計画オーダーが生成されるマスター プラン
description: マスター プランが実行された後にファントムの計画オーダーが生成されます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026684"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>ファントム製品の計画オーダーが生成されるマスター プラン

KB 番号: 4614729

## <a name="symptoms"></a>現象

マスター プランが実行された後にファントムの計画オーダーが生成されます。

## <a name="resolution"></a>解像度

リリース済製品の **ファントム** オプションの設定が、部品表 (BOM) の既定の行タイプを決定します。 **ファントム** オプションが *はい* に設定されている場合は、システムが品目の計画オーダーを作成しますが、各計画オーダーの **直接派生要件** オプションは *はい* に設定されます。 したがって、計画製造オーダーは自身を確定できません。 代わりに、親製造オーダーが確定された場合は常に自動的に追加されます。 また、計画ファントム オーダーの BOM 明細行が親製造オーダーの BOM に含まれます。
