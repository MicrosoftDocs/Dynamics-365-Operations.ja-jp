---
title: 例外の調査/解決
description: '[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。'
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189341"
---
# <a name="researchresolve-exceptions"></a>例外の調査/解決

[!include [task guide banner](../../includes/task-guide-banner.md)]

[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。 また、ワークフローに請求書を送信するたびに、仕入先請求書ワークフローを構成して仕入先請求書ポリシーを実行できます。 

仕入先請求ポリシーは仕入帳や請求仕訳帳で作成した請求書には適用しません。 

請求書照合の検証は、仕入先請求ポリシーを使用せず、[買掛金管理パラメーター] ページで設定します。

このレコードでは、USMF デモ会社を使用します。 買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。 始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。


## <a name="prepare-to-create-vendor-invoice-policies"></a>仕入先請求書ポリシーの作成準備
1. [買掛金勘定] > [設定] > [買掛金勘定パラメーター] の順に移動します。
2. [請求書検証] タブをクリックします。
3. [請求書ヘッダーの状態を自動的に更新] のチェック ボックスをオンまたはオフにします。
4. [OK] をクリックします。
5. [不一致のある請求書を転記] フィールドで、オプションを選択します。
6. ページを閉じます。
7. [買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー] の順に移動します。
8. [パラメーター] をクリックします。
9. [btnAdd] をクリックします。
10. ページを閉じます。

## <a name="create-policy-rule-types-for-vendor-invoices"></a>仕入先請求書のポリシー ルール タイプの作成
1. [買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー ルール タイプ] の順に移動します。
2. [新規] をクリックします。
3. [ルール名] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [クエリ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. [保存] をクリックします。
9. ページを閉じます。

## <a name="define-a-vendor-invoice-policy"></a>仕入先請求書ポリシーを定義します。
1. [買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [ポリシーの組織] のセクションを展開または折りたたみます。
6. ツリーで、「Contoso Entertainment System USA」を選択します。
7. [追加] をクリックします。
8. [ポリシー ルール] のセクションを展開または折りたたみます。
9. [ポリシー ルールの作成] をクリックします。
10. [ポリシー ルールの説明] フィールドに値を入力します。
11. [フィルター] をクリックします。
12. [追加] をクリックします。
13. 一覧で、選択された行をマークします。
14. [テーブル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
15. 一覧で、選択された行のリンクをクリックします。
16. [派生テーブル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
17. 一覧で、選択された行のリンクをクリックします。
18. [フィールド] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
19. [フィールド] フィールドに値を入力します。
20. ページを閉じます。
21. [基準] フィールドに値を入力します。
22. [OK] をクリックします。
23. [OK] をクリックします。
24. ページを閉じます。
25. ページを閉じます。

