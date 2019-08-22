---
title: 転記された仕訳帳の仕訳入力
description: この手順では、転記された仕訳入力の仕訳を行う方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbf7ee8063487303cd4c8d2b76a8b44bacc86193
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846394"
---
# <a name="journalize-posted-journal-entries"></a>転記された仕訳帳の仕訳入力

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、転記された仕訳入力の仕訳を行う方法について説明します。 この手順では、デモ データの会社 USMF を使用します。

1. [総勘定元帳] > [元帳の設定] > [総勘定元帳パラメーター] で仕訳入力の設定を検証します。
2. 拡張仕訳元帳フィールドは、[はい] または [いいえ] に設定します。 [はい] の場合は、レポートの出力が異なります。
3. 仕訳プロセスが実行されなかった場合に、期間を終了するかどうかを選択します。
    * このオプションが [はい] に設定されている場合、期間は仕訳プロセスがその期間に対して完了するまで、閉じることはできません。  
4. ページを閉じます。
5. [総勘定元帳] > [定期処理タスク] > [仕訳入力] の順に移動します。
6. [フィルター] をクリックします。
7. 定義するフィルター基準の行を強調表示します。
8. [基準] フィールドで、フィルター基準を入力または選択します。
9. [OK] をクリックして、フィルター ページを閉じます。
10. [OK] をクリックして仕訳入力プロセスを開始します。
    * レポートは、プロセスが完了した後生成されます。  

