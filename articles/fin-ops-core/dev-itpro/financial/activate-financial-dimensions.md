---
title: 財務分析コードの有効化
description: この記事には、財務分析コード プロセスの有効化に関する情報が含まれています。
author: RyanCCarlson2
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 191363
ms.assetid: dd1dd40e-6bff-47b5-bf2e-55b9a4dcde1d
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 756e7f39fc6032a929a6a64cbfe8386cc0e5c35e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866804"
---
# <a name="financial-dimension-activation"></a>財務分析コードの有効化

[!include [banner](../includes/banner.md)]

この記事には、財務分析コード プロセスの有効化に関する情報が含まれています。

新しい財務分析コードがシステムに追加されると、分析コードの有効化が実行されるまで財務分析コードを使用できないことを示すメッセージがユーザーに表示されます。 分析コードの有効化を実行すると、**DimensionAttributeValueCombination** および **DimensionAttributeValueSet** テーブルで、データベースのスキーマの変更が実行されます。 スキーマの変更により、各財務分析コードのテーブルに新しい列が追加されます。 プロセス中に、スキーマロックは Microsoft SQL Server によって 2 つのテーブルに配置され、テーブルを更新することができます。 このプロセスが完了すると、テーブルはもはやロックされていません。 仕訳帳が開いたときにこのプロセスが実行されると、デッドロックが発生する可能性があります。 デッドロックが発生した場合、ユーザーはサーバーからメタデータ エラーを受け取る可能性があります。 セッションを最新の情報に更新して、更新されたメタデータを取得できます。 ユーザーが受け取るメッセージ。

- プロセスが実行されるまで、どの場所でも、財務分析コードを使用することはできません。 これには、勘定構造に追加することが含まれます。
- スキーマの変更が発生するため、有効化を実行するには、特別な権限である分析コードの有効化権限が必要です。
- 予定されたメンテナンスまたはダウンタイムの際に、これを行う必要があります。

財務分析コードを追加することは、通常、意図的なビジネス プロセスです。 ユーザー受け入れテストなどのマルチ ユーザー環境またはトレーニング環境がある場合、1 人だけがこのプロセスを試行する必要があります。 2 番目のオプションは、有効化オプション、**財務分析コードの再構築** を選択したときに使用できます。 

[![財務分析コードの有効化。](./media/actwiki2.png)](./media/actwiki2.png) 

**財務分析コードを再構築** オプションは、初期有効化プロセス中予期しない結果が発生した場合にのみ実行されるプロセスであるため、既定で **いいえ** に設定されます。 再構成することにより、テーブルにすべての財務分析コードと値がドロップされ、再追加されます。

## <a name="additional-resources"></a>追加リソース

[財務分析コードの定義](../../../finance/general-ledger/tasks/define-financial-dimensions.md)

[メンテナンス モード](../sysadmin/maintenance-mode.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
