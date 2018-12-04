--- 
title: "元の予算を作成し、公的機関の暫定予算エントリをリバースします"
description: "元の予算エントリを作成し、予算モデルおよび暫定予算金額を含む分析コード値を使用している場合、暫定予算金額を取り消すことができます。"
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9d1c34ac2bd94196b7bad599e9aca7ed942ae9c8
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>元の予算を作成し、公的機関の暫定予算エントリをリバースします

[!include [task guide banner](../../includes/task-guide-banner.md)]

元の予算エントリを作成し、予算モデルおよび暫定予算金額を含む分析コード値を使用している場合、暫定予算金額を取り消すことができます。 この手順は、公的機関部門の PSUS のデモ会社のデータを使用して作成されました。

1. [予算作成] > [予算登録エントリ] の順に移動します。
2. [新規] をクリックします。
3. [予算モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [予算コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. リストで [元の予算] をクリックします。
7. [保存] をクリックします。
8. [明細行の追加] をクリックします。
9. オプション: ヘッダーの日付を変更する場合は、新しい日付を入力します。 この日付により、予算が記録される会計年度期間が決まります。
10. [勘定構造] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、目的のレコードを見つけ、選択します。
12. [分析コード値] フィールドで、任意の値を指定します。
13. [金額] フィールドに数値を入力します。
14. [通貨] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
15. 一覧で、選択された行のリンクをクリックします。
16. [保存] をクリックします。
17. [予算残高の更新] をクリックします。
    * オプション: [暫定予算のリバース] オプションを選択できます。 すべての暫定予算エントリ、または指定した予算コードを持つ暫定予算エントリのみを取り消しできることに注意してください。  
    * オプションを選択するには、ページ上部の [ロック解除] のアイコンをクリックします。  
18. [更新] をクリックします。


