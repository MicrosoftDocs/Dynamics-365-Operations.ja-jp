---
title: 財務分析コードの有効化
description: このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 191363
ms.assetid: dd1dd40e-6bff-47b5-bf2e-55b9a4dcde1d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad3944d6815d7c15b90beea03b112b2ceee1895d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510975"
---
# <a name="financial-dimension-activation"></a>財務分析コードの有効化

[!include [banner](../includes/banner.md)]

このトピックには、財務分析コード プロセスの有効化に関する情報が含まれています。

新しい財務分析コードがシステムに追加されると、分析コードの有効化が実行されるまで財務分析コードを使用できないことを示すメッセージがユーザーに表示されます。 分析コードの有効化を実行すると、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** テーブルで、データベースのスキーマの変更が実行されます。 スキーマの変更により、各財務分析コードのテーブルに新しい列が追加されます。 プロセス中に、スキーマロックは Microsoft SQL Server によって 2 つのテーブルに配置され、テーブルを更新することができます。 このプロセスが完了すると、テーブルはもはやロックされていません。 仕訳帳が開いたときにこのプロセスが実行されると、デッドロックが発生する可能性があります。 これが発生した場合、ユーザーはサーバーからメタデータ エラーを受け取る可能性があります。 セッションを最新の情報に更新して、更新されたメタデータを取得できます。 ユーザーが受け取るメッセージ。

-   プロセスが実行されるまで、どの場所でも、財務分析コードを使用することはできません。 これには、勘定構造に追加することが含まれます。
-   スキーマの変更が発生するため、有効化を実行するには、特別な権限である分析コードの有効化権限が必要です。
-   予定されたメンテナンスまたはダウンタイムの際に、これを行う必要があります。

財務分析コードを追加することは、通常、非常に意図的な業務プロセスです。 ユーザー受け入れテストなどのマルチ ユーザー環境またはトレーニング環境がある場合、1 人だけがこのプロセスを試行する必要があります。 2 番目のオプションは、有効化オプション、**財務分析コードの再構築**を選択したときに使用できます。 

[![ActWiki2](./media/actwiki2.png)](./media/actwiki2.png) 

**財務分析コードを再構築** オプションは、初期有効化プロセス中予期しない結果が発生した場合にのみ実行されるプロセスであるため、既定で **いいえ** に設定されます。 これにより、すべての財務分析コードと値がドロップされ、テーブルに再追加されます。

## <a name="additional-resources"></a>その他のリソース

[財務分析コード を設定する (タスク ガイド)](../../financials/general-ledger/tasks/define-financial-dimensions.md)

[メンテナンス モード](../sysadmin/maintenance-mode.md)



