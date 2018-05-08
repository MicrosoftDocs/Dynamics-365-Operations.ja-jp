--- 
title: "データ ソースとして財務分析コードを使用するレポートを実行する"
description: "次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 47ba48461a1c502a93df416d1acac1e85a841079
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source"></a>データ ソースとして財務分析コードを使用するレポートを実行する

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。 これらのステップは DEMF 会社で実行できます。

これらの手順を実施するには、まず「データ ソース (パート3：レポートのデザイン）手順としてのER使用・財務分析コード」にある手順を実施する必要があります。 また、電子レポート パラメーターのページで既定のドキュメント タイプを環境設定する必要があります。 既定のドキュメントタイプは、ERのコンフィギュレーションがダウンロード、インポートされるときにも設定されます。 


## <a name="run-report"></a>レポートを実行する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「Financial dimensions sample model」を展開します。
3. ツリーで、「Financial dimensions sample model\Ledger journal report」を選択します。
4. [実行] をクリックします。
5. [ディメンション名] フィールドに値を入力または選択します。
    * 現在の会社のすべての分析コードを選択するには、次を入力します: 事業単位、コストセンター、部門、品目グループ、主勘定、プロジェクト  
6. [対象に含めるレコード] セクションを展開します。
7. [フィルター] をクリックします。
8. 仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。
9. [基準] フィールドで、「00057」と入力します。
10. [OK] をクリックします。
11. [OK] をクリックします。
    * 生成された出荷を確認します。 選択したバッチの各トランザクションについては、相当する分析コードの財務分析コードが表示されます。 このレポートを実行し異なる分析コードを選択して、レポートが選択した分析コードの数または Dynamics 365 for Finance and Operations インスタンスに構成した分析コードの数に依存していないことを確認します。  


