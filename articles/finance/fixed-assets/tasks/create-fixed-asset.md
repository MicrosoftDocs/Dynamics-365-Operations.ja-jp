---
title: 固定資産の作成
description: このトピックでは、固定資産リスト ページから新しい固定資産レコードを作成する方法について説明します。
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817104"
---
# <a name="create-a-fixed-asset"></a>固定資産の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、**固定資産** リスト ページから新しい固定資産レコードを作成する方法について説明します。

固定資産グループに割り当てられている番号順序に基づいて、システムが自動的に資産番号を割り当てます。 固定資産テンプレートを使用して Microsoft Excel アドインで資産をインポートする場合、または別のインポート ジョブを使用する場合は、システムが固定資産レコードを自動的に作成し、資産番号を増加させます。

資産レコードを手動で作成するには、次の手順に従います。

1. **ナビゲーション ウィンドウ \> モジュール \> 固定資産 \> 固定資産 \> 固定資産** の順に移動します。
2. **アクション ウィンドウ** で、**新規** を選択します。
3. **固定資産グループ** フィールドで、値を入力または選択します。 **固定資産パラメーター** および **固定資産グループ** で **固定資産の自動採番機能** を有効にした場合、**番号** は既定になります。 そうでない場合、固定資産を識別する固有番号を入力する必要があります。
4. **名前** フィールドに値を入力します。 この資産について業務に必要な追加情報を入力します。
5. **アクション ウィンドウ** で、**帳簿** を選択します。
6. **取得日付** フィールドに日付を入力します。
7. **取得価格** フィールドに数値を入力します。

    - この帳簿に業務上必要な追加情報を入力します。
    - 残りの帳簿に業務上必要な追加情報を入力します。

8. ページを閉じます。

Excel アドインを使用して、または **データ管理** ワークスペースからインポート ジョブを実行することによって、固定資産をインポートすることもできます。 インポートを実行する前に、テンプレートの必須フィールドの値を入力します。

Excel アドインのテンプレートに固定資産番号を定義していない場合、またはデータ管理で、インポートした資産ごとに固定資産番号が作成され、それぞれの番号順序が自動的に増やされます。 ただし、テンプレートで資産をインポートして資産番号を定義した場合、番号順序は自動的に **増えません**。 この場合、管理者が手動で番号順序を更新する必要があります。 Excel アドインのテンプレートで固定資産番号を定義した場合は、定義されている固定資産番号が使用され、番号順序が増加します。

> [!NOTE]                                                                                                         
> 減価償却を転記 すると、**帳簿** ページで  **サービスの開始** と **減価償却の実行日** フィールドがロックされます。 また、どちらのフィールドもデータ エンティティから更新されます。

> [!WARNING]
> トランザクションが関連付けられた帳簿に転記されている場合や、新たに作成された固定資産が仕訳帳明細行に入力済で転記されていない場合、固定資産レコードは削除されません。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]