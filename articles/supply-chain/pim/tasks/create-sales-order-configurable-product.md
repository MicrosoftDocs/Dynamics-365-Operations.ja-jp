---
title: コンフィギュレーション可能な製品の販売注文の作成
description: この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570588"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>コンフィギュレーション可能な製品の販売注文の作成

[!include [banner](../../includes/banner.md)]

この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。 この例では、デモ データの会社 USMF の D0006 スピーカー モデルが使用されています。 通常、販売注文担当者がこの手順を使用します。

## <a name="create-a-sales-order"></a>販売注文の作成

1. **販売とマーケティング\>ワークスペース\>販売注文の処理と照会** の順にクリックします。
1. **新規** を選択します。
1. **販売注文** を選択します。
1. **顧客口座** フィールドで、*US-001* を選択します。 
1. **OK** を選択します。
1. **品目番号** フィールドで、*D0006* を選択します。
    * このタスクでは、コンフィギュレーション可能な製品を選択する必要があります。  
1. **製品と供給** を選択します。
1. **コンフィギュレーション明細** を選択します。
    * 選択されたコンフィギュレーションに基づいて価格が変更され、**ケーブルを含める** フィールドが *True* に設定されることに注意してください。  
    * ケーブルに対して選択された既定の価格および設定に注意してください。  
1. **読み込みテンプレート** を選択します。
    * この例では、事前定義済のコンフィギュレーションを選択するためにどのようにテンプレートを追加できるかを示します。 この手順をタスク ガイドとして使用し、使用できる他の属性値を確認する場合は、**ロック解除** ボタンを選択する必要があります。  
1. **OK** を選択します。
1. **OK** を選択します。
1. **行の詳細** セクションを展開します。
1. **製品** タブを選択します。
    * 品目のコンフィギュレーションは、製品分析コードの下に一覧表示されます。  
1. ページを閉じます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]