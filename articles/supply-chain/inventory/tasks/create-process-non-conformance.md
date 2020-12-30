---
title: 不適合の作成および処理
description: このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432227"
---
# <a name="create-and-process-a-conformance"></a>不適合の作成および処理

[!include [banner](../../includes/banner.md)]

このトピックでは、既存の品質指示に基づき不適合管理を実行する方法について説明します。 USMF のデモの会社でこの記録を実行することができ、提案された値を使用することができます。 通常この手順は品質担当者が実施します。  前提条件として、[商品の品質の調査](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) の手順に従ってください。 不適合の承認を処理する場合、タスクの記録を実行するユーザーには、[ユーザー] ページで 「名前」 の値が割り当てられている必要があります。 ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。


## <a name="select-a-quality-order"></a>品質指示の選択
1. ナビゲーション ウィンドウで **モジュール > 在庫管理 > 定期処理 > 品質管理 > 品質指示** に移動します。
2. 一覧で、[商品の品質の調査](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) で作成された品質指示を選択します。  

## <a name="create-a-nonconformance"></a>不適合の作成
1. アクション ウィンドウで、**照会** を選択します。
2. **不適合** を選択します。
3. **新規** を選択します。
4. **問題タイプ** フィールドのドロップダウン メニューで、検査プロセス中に検出された問題を選択します。  
5. **OK** を選択します。

## <a name="approvereject-a-nonconformance"></a>不適合の承認/否認
1. **機能** を選択します。
2. **不適合の承認** を選択します。 この例では、不適合を承認します。 承認された不適合は、不適合処理の一部としてまたはこのトピックと同様に修正処理として、処理される作業を記録するために、関連する工程に関連付けることができます。  
3. **はい** を選択します。

## <a name="create-a-correction-action"></a>訂正アクションの作成
1. **訂正** を選択します。
2. **新規** を選択します。
3. 新しい行の **個人番号** フィールドで、ドロップダウン メニューから目的のレコードを選択します。
4. **選択** をクリックします。
5. **添付** を選択します。 修正に関するメモを作成します。 この例では、アクションは、不適合のケースについて説明するために仕入先に連絡する必要があります。  
6. **新規** を選択します。
7. **注記** を選択します。 レポートの設定に応じて、異なるドキュメント タイプが不適合管理に関連付けられているレポートに印刷できます。  
8. **説明** フィールドで、値を入力します。
9. ページを閉じます。

## <a name="maintain-a-correction"></a>訂正の管理
1. **完了としてマーク** を選択します。
2. **OK** を選択します。
3. ページを閉じます。

## <a name="close-a-nonconformance"></a>不適合のクローズ
1. **機能** を選択します。
2. **不適合のクローズ** を選択します。
3. **はい** を選択します。
4. ページを閉じます。
