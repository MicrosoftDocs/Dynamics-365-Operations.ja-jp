---
title: ER 財務分析コードをデータ ソースとして使用する (第 4 部 - レポートの実行)
description: 次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684742"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER 財務分析コードをデータ ソースとして使用する (第 4 部 - レポートの実行)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。 これらのステップは DEMF 会社で実行できます。

この手順を実施するには、まず「ER 財務分析コードをデータソースとして使用する（パート 3：レポートのデザイン）」に記載の手順を実施する必要があります。 また、電子レポート パラメーターのページで既定のドキュメント タイプを環境設定する必要があります。 既定のドキュメントタイプは、ERのコンフィギュレーションがダウンロード、インポートされるときにも設定されます。 


## <a name="run-report"></a>レポートを実行する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「Financial dimensions sample model」を展開します。
3. ツリーで、「Financial dimensions sample model\Ledger journal report」を選択します。
4. [実行] をクリックします。
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run1.png)
5. [分析コード名] フィールドで、値を入力または選択します。
    * 現在の会社のすべての分析コードを選択するには、次の情報を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run2.png)
6. [対象に含めるレコード] セクションを展開します。
7. [フィルター] をクリックします。
8. 仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。
9. [基準] フィールドで、「00057」と入力します。
10. [OK] をクリックします。
11. [OK] をクリックします。
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run3.png)
    * 生成された出荷を確認します。 選択したバッチの各トランザクションについては、対応する分析コードの財務分析コードが表示されます。 このレポートを実行して、レポートが選択した分析コード数またはインスタンスに構成した分析コード数に依存していないことを確認するために異なる分析コードを選択します。  
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]