---
title: Financial Reporting に関するよく寄せられる質問
description: このトピックでは、よく寄せられる Financial Reporting に関する質問の一覧を示します。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923028"
---
# <a name="financial-reporting-faq"></a>Financial Reporting に関するよく寄せられる質問 

このトピックでは、よく寄せられる Financial Reporting に関する質問に対する回答を提供します。 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。

次の例は、ツリー セキュリティを使用してレポートへのアクセスを制限する方法を示しています。

USMF デモ会社には、Financial Reporting のすべてのユーザーがアクセスすべきではない貸借対照表レポートがあります。 アクセスを制限するには、ツリー セキュリティを使用して、1 つのレポートへのアクセスを制限し、特定のユーザーのみがレポートにアクセスできるようにします。 アクセスを制限するには、次の手順に従います。 

1. Financial Reporter Report Designer にサインインします。
2. 新しいツリー定義を作成します。 **ファイル > 新規 > ツリー定義** に移動します。
3. **ユニットのセキュリティ** 列の **集計** 行をダブルクリックします。
4. **ユーザーとグループ** を選択します。  
5. このレポートにアクセスする必要があるユーザーまたはグループを選択します。 
6. **保存** を選択します。
7. レポート定義で、新しいツリー定義を追加します。
8. ツリー定義で、**設定** を選択します。 **レポート ユニットの選択** で、**すべてのユニットを含む** を選択します。

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>残高と一致しない勘定は、どのように識別できますか。

残高が一致しないレポートがある場合は、以下の手順に従って、それぞれの勘定と差異を識別できます。 

**Financial Reporter Report Designer**
1. Financial Reporter Report Designer で、新しい行定義を作成します。 
2. **編集 > 分析コードからの行の挿入** を選択します。
3. **MainAccount** を選択します。  
4. **OK** を選択します。
5. 行定義を保存します。
6. 新しい列定義を作成します。
7. 新しいレポート定義を作成します。
8. **設定** を選択し、このオプションのマークを解除します。  
9. レポートを生成します。 
10. レポートを Microsoft Excel にエクスポートします。

**Dynamics 365 Finance** 
1. Dynamics 365 Finance で、**一般会計 > 照会およびレポート > 試算表** をクリックします。
2. 次のパラメーターを設定します。
   - **開始日** - 会計年度の開始日を入力します。
   - **終了日** - レポートを生成する日を入力します。
   - **財務分析コード** - このフィールドを **主勘定セット** に設定します。
 3. **計算** を選択します。
 4. レポートを Microsoft Excel にエクスポートします。

これで、Financial Reporter Excel レポートから試算表レポートにデータをコピーして、**決算残高** 列を比較できます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]