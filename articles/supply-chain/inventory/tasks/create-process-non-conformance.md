---
title: 不適合の作成および処理
description: この手順を使用して、既存の品質指示に基づき不適合管理を実行します。
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572814"
---
# <a name="create-and-process-a-conformance"></a>不適合の作成および処理

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順を使用して、既存の品質指示に基づき不適合管理を実行します。 USMF のデモの会社でこの記録を実行することができ、提案された値を使用することができます。 通常この手順は品質担当者が実施します。  前提条件として、「商品の品質の調査」タスクの記録を実行します。 不適合の承認を処理する場合、タスクの記録を実行するユーザーには、[ユーザー] ページで「名前」の値が割り当てられている必要があります。 ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。


## <a name="select-a-quality-order"></a>品質指示の選択
1. [品質指示] に移動します。
2. 一覧で、選択された行をマークします。
    * 「商品の品質の調査」タスク記録から作成された品質指示を選択します。  

## <a name="create-a-nonconformance"></a>不適合の作成
1. [照会] をクリックします。
2. [不適合] をクリックします。
3. [新規] をクリックします。
4. [問題タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 検査プロセス中に検出された問題を選択します。  
5. [問題タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. [OK] をクリックします。

## <a name="approvereject-a-nonconformance"></a>不適合の承認/否認
1. [機能] をクリックします。
2. [不適合の承認] をクリックします。
    * この例では、不適合を承認します。 承認された不適合は、不適合処理の一部としてまたはこのタスクの記録と同様に修正処理として、処理される作業を記録するために、関連する工程に関連付けることができます。  
3. [はい] をクリックします。

## <a name="create-a-correction-action"></a>訂正アクションの作成
1. [訂正] をクリックします。
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [個人番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、選択された行のリンクをクリックします。
6. [選択] をクリックします。
7. [添付] をクリックします。
    * 修正に関するメモを作成します。 この例では、アクションは、不適合のケースについて説明するために仕入先に連絡する必要があります。  
8. [新規] をクリックします。
9. [メモ] をクリックします。
    * レポートの設定に応じて、異なるドキュメント タイプが不適合管理に関連付けられているレポートに印刷できることに注意してください。  
10. [説明] フィールドに値を入力します。
11. ページを閉じます。

## <a name="maintain-a-correction"></a>訂正の管理
1. [完了としてマーク] クリックします。
2. [OK] をクリックします。
3. ページを閉じます。

## <a name="close-a-nonconformance"></a>不適合のクローズ
1. [機能] をクリックします。
2. [不適合のクローズ] をクリックします。
3. [はい] をクリックします。
4. ページを閉じます。
5. ページを閉じます。
