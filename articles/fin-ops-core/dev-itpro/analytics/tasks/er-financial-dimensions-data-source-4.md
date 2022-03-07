---
title: ER 財務分析コードをデータ ソースとして使用する (第 4 部 - レポートの実行)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 4 部)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f14be560ab014224e32169b4ac97682a669249b4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605308"
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
![ER コンフィギュレーション ページ。](../media/er-financial-dimensions-guides-run1.png)
5. [分析コード名] フィールドで、値を入力または選択します。
    * 現在の会社のすべての分析コードを選択するには、次の情報を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![電子レポート パラメータのスライド (分析コード名のドロップダウン)。](../media/er-financial-dimensions-guides-run2.png)
6. [対象に含めるレコード] セクションを展開します。
7. [フィルター] をクリックします。
8. 仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。
9. [基準] フィールドで、「00057」と入力します。
10. [OK] をクリックします。
11. [OK] をクリックします。
![電子レポート パラメータのスライド (セクションに含めるレポート)。](../media/er-financial-dimensions-guides-run3.png)
    * 生成された出荷を確認します。 選択したバッチの各トランザクションについては、対応する分析コードの財務分析コードが表示されます。 このレポートを実行して、レポートが選択した分析コード数またはインスタンスに構成した分析コード数に依存していないことを確認するために異なる分析コードを選択します。  
![ER 構成で生成された出力。](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
