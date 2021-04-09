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
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811313"
---
# <a name="financial-reporting-faq"></a>Financial Reporting に関するよく寄せられる質問 

このトピックでは、よく寄せられる Financial Reporting に関する質問の一覧を示します。 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。

シナリオ: USMF デモ会社では、一部の貸借対照表レポートを、Financial Reporting のすべてのユーザーが D365 で表示できるようにしたくないと考えています。 解決策: ツリー セキュリティを利用すると、あるレポートへのアクセスを制限して、特定のユーザーのみがレポートにアクセスできるようにすることができます。 

1.  Financial Reporter レポート デザイナーにログインします

2.  新しいツリー定義を作成します (ファイル | 新規 | ツリー定義)。a.    **ユニットのセキュリティ** 列の **集計** 行をダブルクリックします。
  i.    ユーザーとグループをクリックします。  
          1. このレポートにアクセスするユーザーまたはグループを選択します。 
          
[![ユーザー画面](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![セキュリティ画面](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    **保存** をクリックします。
  
[![保存ボタン](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  レポート定義で、新しいツリー定義を追加します

[![ツリー定義フォーム](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  ツリー定義で、設定をクリックし、レポート ユニットの選択で、すべてのユニットを含むのチェックボックスをオンにします

[![レポート ユニットの選択フォーム](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**変更前:** [![変更前のスクリーンショット](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**変更後:** [![変更後のスクリーンショット](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

注: 上記のメッセージの理由は、ユニットのセキュリティを適用した後、ユーザーがそのレポートにアクセスできないためです。



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>D365 の残高と一致しない勘定を特定するにはどうすればよいですか。

D365 で予想される値と一致しないレポートがある場合、それらの勘定との差異を特定するために実行できるいくつかの手順を次に示します。 

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter レポート デザイナーでの操作

1.  新しい行定義を作成します。a.    編集 | 分析コードからの行の挿入をクリックします。i.  MainAccount を選択します。[![主勘定の選択の画面](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. OK をクリックします。b.    行定義を保存します。

2.  新しい列定義を作成します。[![新しい列定義の作成](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  新しいレポート定義を作成します。a.    設定をクリックして、次のチェックボックスをオフにします。[![設定フォーム](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  レポートを生成します。 

5.  レポートを Excel にエクスポートします。

### <a name="in-d365"></a>D365 で: 
1.  一般会計 | 照会およびレポート | 試算表をクリックします。a.    パラメーター i.  開始日: 会計年度の開始日 ii. 終了日: レポート作成の対象日 iii.    財務分析コード: 主勘定セットを設定します。[![主勘定フォーム](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    計算をクリックします。

2.  レポートを Excel にエクスポートします。

これで、FR Excel レポートから D365 試算表レポートにデータをコピーして、[決算残高] 列を比較できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]