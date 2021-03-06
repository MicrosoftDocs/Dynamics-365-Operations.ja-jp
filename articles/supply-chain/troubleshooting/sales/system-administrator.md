---
title: システム管理者に権限がないため、注文の保留を解除できない
description: システム管理者に権限がないため、注文の保留を解除できません。
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026694"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>システム管理者に権限がないため、注文の保留を解除できない

KB 番号: 4614642

## <a name="symptoms"></a>現象

システム管理者は、注文の保留コードに特定のロールが割り当てられていない限り、販売注文の保留を解除できません。

## <a name="resolution"></a>解像度

販売注文の保留のクリアなど、一部の操作へのアクセスは、業務ポリシーの設定によって行われます。 システム管理者には通常、このタイプの操作は許可されていません。 

多くの場合、特定のタスクを実行するためのアクセスがビジネス ポリシーによって制御され、組織内の特定の人物だけがそのタスクを実行するよう承認されています。 たとえば、ワークフローの承認の結果である承認や、ワークフロー コンフィギュレーションの結果である特定のタスクなどがあります。

注文に関連付けられているワークフローがない場合でも、原則は類似しています。 関連する役割は、注文保留をクリアする権利を持つ組織内の特定のユーザー グループを示します。 そのアプローチは定義された業務ポリシーに違反するため、この権限は必ずすべての管理者に付与する必要があります。
