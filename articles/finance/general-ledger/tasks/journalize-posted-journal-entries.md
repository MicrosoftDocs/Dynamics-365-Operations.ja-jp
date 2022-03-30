---
title: 転記された仕訳帳の仕訳入力
description: この手順では、転記された仕訳入力の仕訳を行う方法について説明します。
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400878"
---
# <a name="journalize-posted-journal-entries"></a>転記された仕訳帳の仕訳入力

[!include [banner](../../includes/banner.md)]

一般会計での仕訳プロセスを使用すると、一般会計に転記された伝票エントリをグループ化して報告できます。 あなたが指定した基準に基づいて、一意な番号順序を使用し、一般会計の **仕訳番号** の値を参照として使用する伝票の一覧が処理によって生成されます。

これらの手順に従って、転記された仕訳入力の仕訳を行う方法について説明します。 この手順では、デモ データ企業 **USMF** を使用します。

1. **一般会計** \> **元帳の設定** \> **総勘定元帳パラメーター** の順に移動します。
2. **拡張された元帳仕訳帳** フィールドで、値を入力または選択します。 **はい** を選択する場合は、レポートの出力が異なります。
3. 仕訳プロセスが実行されなかった場合に、期間を終了するかどうかを選択します。 **はい** を設定する場合、この期間は仕訳プロセスがその期間に対して完了するまで閉じることはできません。
4. ページを閉じます。
5. **一般会計** \> **定期処理タスク** \> **仕訳入力** に移動して、**フィルター** を選択します。
6. 定義するフィルター基準の行を選択します。
7. **基準** フィールドで、フィルター基準を入力または選択します。
8. **OK** を選択してページを閉じます。
9. **OK** を選択して仕訳入力プロセスを開始します。 レポートは、プロセスが完了した後生成されます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
