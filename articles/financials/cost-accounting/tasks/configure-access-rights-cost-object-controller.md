--- 
title: "原価オブジェクト コントローラーのアクセス権のコンフィギュレーション"
description: "この手順を使用して、コスト オブジェクト コントローラーのアクセス権を設定します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b0647e1ec55d23607d07f38105e42af498ad1174
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>原価オブジェクト コントローラーのアクセス権のコンフィギュレーション

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順を使用して、コスト オブジェクト コントローラーのアクセス権を設定します。 この記録では、USP2 デモ データ会社を使用します。


## <a name="assign-the-cost-object-controller-role"></a>原価オブジェクト コントローラー ロールを割り当て
1. [システム管理] > [ユーザー] > [ユーザー] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「アリシア」の値で [ユーザー名] フィールドをフィルターします。
3. 一覧で、選択された行のリンクをクリックします。
4. [ロールの割り当て] をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。
6. [OK] をクリックします。

## <a name="enable-access-list-security"></a>リスト セキュリティのアクセスを有効
1. [原価会計] > [分析コード] > [分析コード階層] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * [組織] を選択します。  
3. [編集] をクリックします。
4. [アクセス リスト階層] のフィールドで、[はい] を選択します。
5. [階層の表示] をクリックします。

## <a name="assign-access-rights-to-user"></a>ユーザーへのアクセス権を割り当て
1. [新規] をクリックします。
2. 一覧で、選択された行をマークします。
3. [ユーザー ID] フィールドで、値を入力または選択します。
    * [管理者] を選択します。  
4. ツリーで、「組織\CEO\CFO\FIM」を選択します。
5. [新規] をクリックします。
6. 一覧で、選択された行をマークします。
7. [ユーザー ID] フィールドで、値を入力または選択します。
    * [アリシア] を選択します。  
8. [保存] をクリックします。

## <a name="enable-access-rights-in-cost-accounting"></a>原価会計のアクセス権を有効化
1. [原価会計] > [設定] > [パラメーター] へ移動します。
2. [一般] タブをクリックします。
3. 原価オブジェクト分析コード メンバー フィールドに対する [表示アクセスの有効化] で、[はい] を選択します。
4. [保存] をクリックします。
5. ページを閉じます。
6. [原価会計] > [設定] > [原価管理ワークスペース コンフィギュレーション] へ移動します。
7. [編集] をクリックします。
8. [公開済] フィールドで、[はい] を選択します。
    * [はい] を選択すると、次の 4 つのロールのいずれかに割り当てられているユーザーは、原価管理ワークスペースでレポートを確認できます: 原価会計マネージャー、原価経理担当、原価経理担当係および原価オブジェクト コントローラー。 [いいえ] を選択すると、次のロールのいずれかに割り当てられているユーザーのみが、レポートを確認できます: 原価会計マネージャー、原価経理担当、および原価経理担当係。    
9. [保存] をクリックします。


