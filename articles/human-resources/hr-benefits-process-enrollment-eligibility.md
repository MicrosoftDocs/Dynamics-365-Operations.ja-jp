---
title: 登録の適格性を処理
description: この記事では、登録資格のプロセスを実行する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009621"
---
# <a name="process-enrollment-eligibility"></a>登録の適格性を処理

[!include [banner](includes/preview-feature.md)]

この記事では、登録資格のプロセスを実行する方法について説明します。

1. **給付金管理**ワークスペースにて、**処理**の下の**登録適格性の処理**を選択します。

2. **給付金登録の適格性の処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 登録期間 | 登録適格性を処理する登録期間。 |
   | 法人エンティティ | 登録適格性を処理する法人が変更されます。 |
   | ワーカー | 登録適格性を処理する作業者が変更されます。 このフィールドを空白のままにすると、登録適格性がすべての作業者に対して処理されます。 |
   | 給付金計画 | 登録適格性を処理する給付金プランが変更されます。

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。
