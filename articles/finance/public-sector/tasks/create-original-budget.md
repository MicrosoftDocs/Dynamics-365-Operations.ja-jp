---
title: 元の予算を作成し、公的機関の暫定予算エントリをリバースします
description: このトピックでは、予算モデルおよび暫定的な予算金額を持つ分析コード値を使用して、元の予算エントリを作成する方法、取り消す方法について説明します。
author: twheeloc
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7758a1c9edfa129ba8b63a146b38ed3f119fd051
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119429"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>元の予算を作成し、公的機関の暫定予算エントリをリバースします

[!include [banner](../../includes/banner.md)]

元の予算エントリを作成し、予算モデルおよび暫定予算金額を含む分析コード値を使用している場合、暫定予算金額を取り消すことができます。 この手順は、公的機関部門の PSUS のデモ会社のデータを使用して作成されました。

1. **予算作成 > 予算登録エントリ** の順に移動します。
2. **新規** をクリックします。
3. **予算モデル** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. **予算コード** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. リストで **元の予算** をクリックします。
7. **保存** をクリックします。
8. **行の追加** をクリックします。
9. オプション: ヘッダーの日付を変更する場合は、新しい日付を入力します。 この日付により、予算が記録される会計年度期間が決まります。
10. **勘定構造** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、目的のレコードを見つけ、選択します。
12. **分析コード値** フィールドで、任意の値を指定します。
13. **金額** フィールドに数値を入力します。
14. **通貨** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
15. 一覧で、選択された行のリンクをクリックします。
16. **保存** をクリックします。
17. **予算残高の更新** をクリックします。
    * オプション: **暫定予算の取り消し** オプションを選択できます。 すべての暫定予算エントリ、または指定した予算コードを持つ暫定予算エントリのみを取り消しできることに注意してください。  
    * オプションを選択するには、ページ上部の **ロック解除** のアイコンをクリックします。  
18. **更新** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
