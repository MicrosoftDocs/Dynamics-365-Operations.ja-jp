---
title: 配送業者グループ
description: このトピックでは、配送業者グループのデータ設定方法について説明します。
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646410"
---
# <a name="carrier-groups"></a>配送業者グループ

配送業者グループは、出荷の配送業者と配送業者のサービスの集合体です。 各配送業者グループは、配送業者とそれに属する配送業者サービスの優先順位を指定します。

同じ工順セグメントの配送業者と配送業者サービスが複数存在する場合は、特定の配送業者と配送業者サービスの代わりに、工順計画または工順指示書で配送業者グループを指定することができます。

## <a name="create-a-carrier-group"></a>配送業者グループの作成

1. **輸送管理 &gt; 設定 &gt; 配送業者 &gt; 配送業者グループ** に移動します。
1. **新規** を選択します。
1. **配送業者グループ** フィールドで、そのグループに対して一意識別子 (ID) を入力します。
1. **名前** フィールドに、グループの内容を示す名前を入力します。
1. **詳細** クイックタブで、行を追加し、その行の配送業者と配送業者サービスを選択します。 グループに必要な数の配送業者を追加するまで、この手順を繰り返します。
1. ページを閉じます。
