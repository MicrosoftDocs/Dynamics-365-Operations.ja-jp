---
title: 調達カテゴリ階層に対するポリシーの設定
description: カテゴリの製品を発注するルールを設定するには、この手順を使用します。
author: GalynaFedorova
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2a8248374f34e0937aa569259c5925506857ddd
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675910"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>調達カテゴリ階層に対するポリシーの設定

[!include [banner](../../includes/banner.md)]

カテゴリの製品を発注するルールを設定するには、この手順を使用します。 ルールは特定の購入ポリシーに定義されます。 カテゴリ アクセス ルールは、従業員が要求を作成したときにどの調達カテゴリにアクセス許可があるかを管理します。 要求が作成されると、購入ポリシーおよびカテゴリ アクセス ルールは、従業員が属している法人および業務単位によって適用され決定されます。 デモ データの会社 USMF でこの手順を使用できます。 通常、このタスクを実施するのは、購買マネージャーです。


## <a name="find-the-procurement-policy"></a>調達ポリシーを検索します。
1. ナビゲーション ウィンドウで、**モジュール > 調達 > 設定 > ポリシー > 購買ポリシー** の順に移動します。
2. 「調達ポリシー USMF 」ポリシーのリンクをクリックします。 これは、ルールを追加するポリシーです。 これは有効なポリシーである必要があります。  

## <a name="create-a-category-access-rule"></a>カテゴリにアクセスするルールを作成する
1. **ポリシー ルール** クイック タブを展開します。
2. **ポリシー ルール タイプ** 一覧で、**カテゴリ アクセス ポリシー ルール** を選択します。 **ポリシー ルールの作成** ボタンがグレー表示の場合は、カテゴリ アクセスに既に有効なポリシー ルールが存在するためです。 **有効日** および **有効期限** フィールドを確認し特定した後、それを選択し、**ポリシー ルールの破棄** をクリックします。 **ポリシー ルールの作成** ボタンが使用できる場合は、何もする必要はありません。  
3. **ポリシー ルールの作成** をクリックします。
4. **有効日** フィールドに日時を入力します。 すでに有効な別のルールと、時間は重複させることはできません。  
5. ルールが適用されるカテゴリを選択します。 これがどのカテゴリであるかをメモしておき、これは後で必要になります。 カテゴリを選択すると、その親カテゴリまたはカテゴリも選択したカテゴリ リストに追加されます。 選択したカテゴリのすべてのサブカテゴリにルールを適用する場合は、**サブカテゴリを含める** チェック ボックスを選択します。
6. 右矢印をクリックして、**選択されたカテゴリ** リストに追加します。  
4. **OK** をクリックします。 **親ルールを含める** オプションをはいに設定する場合、どのポリシー ルールも子カテゴリに対して定義されていないなら、その親カテゴリに対して定義するポリシー ルールはその子カテゴリにも割り当てられます。

## <a name="create-a-category-policy-rule"></a>カテゴリのポリシー ルールを作成する
1. **ポリシー ルール タイプ** 一覧で、**カテゴリ ポリシー ルール** を選択します。 **ポリシー ルールの作成** ボタンがグレー表示の場合は、有効なポリシー ルールを選択した後、**ポリシー ルールの破棄** をクリックします。  
2. **ポリシー ルールの作成** をクリックします。
3. **有効日** フィールドに日時を入力します。
4. **追加** をクリックします。
5. **カテゴリ** フィールドで、**カテゴリ アクセス ルール** に使用した同じカテゴリを選択します。
6. **仕入先の選択** フィールドで、オプションを選択します。 ルールを選択し、請求の作成時に、どのタイプの仕入先がカテゴリに対して選択できるかを管理します。  
7. **閉じる** をクリックします。 定義したポリシー ルールは消費タイプの要求に対応するものです。 タイプが補充の要求のポリシーを定義する場合は、"補充カテゴリ アクセス ポリシー ルール" というポリシー ルール タイプのルールを作成します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]