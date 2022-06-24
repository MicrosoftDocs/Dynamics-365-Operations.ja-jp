---
title: 配送業者グループ
description: この記事では、配送業者グループのデータ設定方法について説明します。
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d3f8618de520880aa807a21f49f164e8483274ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871865"
---
# <a name="carrier-groups"></a>配送業者グループ

[!include [banner](../../includes/banner.md)]

配送業者グループは、出荷の配送業者と配送業者のサービスの集合体です。 各配送業者グループは、配送業者とそれに属する配送業者サービスの優先順位を指定します。

同じ工順セグメントの配送業者と配送業者サービスが複数存在する場合は、特定の配送業者と配送業者サービスの代わりに、工順計画または工順指示書で配送業者グループを指定することができます。

## <a name="create-a-carrier-group"></a>配送業者グループの作成

1. **輸送管理 &gt; 設定 &gt; 配送業者 &gt; 配送業者グループ** に移動します。
1. **新規** を選択します。
1. **配送業者グループ** フィールドで、そのグループに対して一意識別子 (ID) を入力します。
1. **名前** フィールドに、グループの内容を示す名前を入力します。
1. **詳細** クイックタブで、行を追加し、その行の配送業者と配送業者サービスを選択します。 グループに必要な数の配送業者を追加するまで、この手順を繰り返します。
1. ページを閉じます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]