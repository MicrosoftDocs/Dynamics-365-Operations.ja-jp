---
title: 統合された税
description: この記事では、財務と運用と Dataverse 間の税データの統合について説明します。
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288797"
---
# <a name="integrated-tax"></a>統合された税

[!include [banner](../../includes/banner.md)]



税設定データでは、間接税 (VAT、GST、売上税) および源泉徴収税の両方の設定が定義されます。 税金計算ルール、税率、税務会計、決済、およびその他の概念について説明します。

## <a name="templates"></a>テンプレート

次の表に示すように、税データには、データ操作中に連携して動作するテーブル マップのコレクションが含まれています。

| 財務と運用アプリ | Customer Engagement アプリ | Description |
|-----------------------------|-----------------------------------|-------------|
[品目消費税グループ](mapping-reference.md#196) | msdyn_taxitemgroups | |
[消費税所轄官庁](mapping-reference.md#193) | msdyn_taxauthorities | |
[消費税非課税コード エンティティ CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[消費税グループ](mapping-reference.md#195) | msdyn_taxgroups | |
[消費税元帳転記グループ V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[源泉徴収税コード](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[源泉徴収税グループ](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

