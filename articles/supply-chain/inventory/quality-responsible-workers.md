---
title: 不適合の承認を担当する作業者
description: このトピックでは、不適合の承認を担当する作業者を構成する方法について説明します。
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b764baf0983dbca75d52ea9cdd063cebda80a08d39cf3a5c929f15858e2597c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768170"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>不適合の承認を担当する作業者

[!include [banner](../includes/banner.md)]

このトピックでは、不適合の承認を担当する作業者を構成する方法について説明します。

ユーザーが修正や操作などの詳細の入力を開始する前に、不適合を承認する必要があります。 ユーザーが不適合を承認または否認する前に、ユーザー ID (ユーザー レコード) は作業者レコードにリンクされている必要があります。 オプションで、品質を担当する作業者を構成し、ある作業者が別の作業者の代わりに作業を承認できるようにします。

## <a name="enable-a-user-for-nonconformance-processing"></a>不適合処理に対しユーザーを有効化

ユーザーが不適合を承認または否認する前に、ユーザー レコードを作業者レコードにリンクする必要があります。 その後、承認フィールドが自動的に設定され、現在のユーザーがタイムシートに自動的に入力されます。 ユーザーがドキュメントのメモを使用する前に、ユーザー オプションでドキュメント処理を有効化する必要があります。

1. **システム管理 \> ユーザー \> ユーザー** の順に移動します。
1. 不適合を承認または否認できるユーザーを検索して開きます。
1. **個人** フィールドに、現在のユーザー レコードに関連付けらた作業者の名前を設定します。
1. アクション ウィンドウで、**ユーザー オプション** を選択します。
1. 現在のユーザー レコードの **オプション** ページの **基本設定** タブで、**ドキュメントの処理の有効化** オプションを *はい* に設定します。
1. ページを閉じます。

## <a name="define-workers-that-are-responsible-for-quality"></a>品質を担当する作業者の定義

1. **在庫管理 \> 設定 \> 品質管理 \> 品質の担当作業者** の順に移動します。
2. アクション ウィンドウで、**新規** を選択します。
3. **作業者** フィールドで、品質データを入力する作業者を選択します。
4. **担当作業者** フィールドで、選択した作業者が代わりに作業を入力する作業者を選択します。 不適合が作成および更新されると、この作業者は既定で **作業者** フィールドに入力されます。

## <a name="additional-resources"></a>追加リソース

- [品質管理の概要](quality-management-processes.md)
- [品質および不適合管理の有効化](enable-quality-management.md)
- [品質諸費用](quality-charges.md)
- [不適合の検査ゾーン](quality-quarantine-zones.md)
- [不適合の診断タイプ](quality-diagnostic-types.md)
- [不適合の品質諸費用](quality-charges.md)
- [不適合の工程](quality-operations.md)
- [倉庫プロセスに対する品質管理](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
