---
title: ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 2 部 - 形式の実行)
description: 次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66c2a97a068ed83f93699f14e827bdc2fb580d93
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141836"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 2 部 - 形式の実行)

[!include [banner](../../includes/banner.md)]

次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。 これらのステップは DEMF 会社で実行できます。

これらの手順を完了するには、まず 「ER 水平方向に拡張可能な範囲を使用して、Excelレポートで列を動的に追加する（パート1：デザイン フォーマット）」に記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="find-created-format"></a>作成されたフォーマットを検索する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「Financial dimensions sample model」を展開します。
3. ツリーで、「Financial dimensions sample model\Sample report with horizontally expandable ranges」を選択します。

## <a name="execute-format-to-create-excel-output"></a>フォーマットを実行してExcel出力を作成する
1. [実行] をクリックします。
2. [分析コード名] フィールドに、「事業単位、コストセンター、部門」を入力します。
    * [分析コード名] フィールドで、値を入力または選択します。  現在の会社のすべての分析コードを選択するには、次を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. [対象に含めるレコード] セクションを展開します。
4. [フィルター] をクリックします。
5. 仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。
6. [基準] フィールドに、「00057..00058」と入力します。
    * 00057..00058  
7. [OK] をクリックします。
8. [OK] をクリックします。
    * 生成された出荷を確認します。 新しく作成したExcel ファイルには、財務分析コードに対して選択された同じ数の列が含まれることに注意してください。 これらの列のレポート ヘッダーは財務分析コードの名称を表します。 これらの列のトランザクションの明細行は財務分析コードを表します。 このレポートを実行して、レポートが選択した分析コード数またはインスタンスに構成した分析コード数に依存していないことを確認するために異なる分析コードを選択します。  

