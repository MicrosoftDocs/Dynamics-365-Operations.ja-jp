---
title: 仕入先請求ポリシーを設定します
description: この記事では、仕入先請求ポリシーを設定する方法について説明します。
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049b38b6feba5f4369d79b89b4c81a8195dd7758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904733"
---
# <a name="set-up-vendor-invoice-policies"></a>仕入先請求ポリシーを設定します

[!include [banner](../../includes/banner.md)]

この記事では、仕入先請求ポリシーを設定する方法について説明します。 仕入先請求ポリシーは、**仕入先請求書** ページを使用して仕入先請求書を転記するか、仕入先請求書の **ポリシー違反** ページを開いたときに実行されます。 また、ワークフローに請求書を送信するたびに、仕入先請求書ワークフローを構成して仕入先請求書ポリシーを実行できます。 

- 仕入先請求ポリシーは仕入帳や請求仕訳帳で作成した請求書には適用しません。  
- 請求書照合の検証は、仕入先請求ポリシーを使用せず、**買掛金管理パラメーター** ページで設定します。  
- このレコードでは、USMF デモ会社を使用します。 買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。 始める前に、**請求書照合** コンフィギュレーション キーが選択されていることを確認します。


## <a name="prepare-to-create-vendor-invoice-policies"></a>仕入先請求書ポリシーの作成準備
1. **ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > 設定 > 買掛金勘定パラメーター** の順に移動します。
2. **請求書検証** タブを選択します。
3. **請求書ヘッダーの状態を自動的に更新** チェック ボックスをオンまたはオフにします。
4. **OK** を選択します。
5. **不一致のある請求書を転記** フィールドで、オプションを選択します。
6. ページを閉じます。
7. **ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー** の順に移動します。
8. **パラメーター** を選択します。
9. **追加** を選択します。
10. ページを閉じて、ホーム ページに戻ります。

## <a name="create-policy-rule-types-for-vendor-invoices"></a>仕入先請求書のポリシー ルール タイプの作成
1. **ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー ルール タイプ** の順に移動します。
2. **新規** を選択します。
3. **ルール名** および **説明** フィールドに、値を入力します。
4. **クエリ名** フィールドで、ドロップ ダウン ボタンを選択してルックアップを開き、目的のレコードを選択します。
5. **保存** を選択します。
6. ページを閉じて、ホーム ページに戻ります。

## <a name="define-a-vendor-invoice-policy"></a>仕入先請求書ポリシーを定義します。
1. **ナビゲーション ウィンドウ > モジュール > 買掛金勘定 > ポリシー設定 > 仕入先請求書ポリシー** の順に移動します。
2. **新規** を選択します。
3. **名前** および **説明** フィールドに、値を入力します。
4. **ポリシーの組織** セクションを展開または折りたたみます。
5. ツリーで、**Contoso Entertainment System USA** を選択します。
6. **追加** を選択します。
7. **ポリシー ルール** セクションを展開または折りたたみます。
8. **ポリシー ルールの作成** を選択します。
9. **ポリシー ルールの説明** フィールドに、値を入力します。
10. **フィルター** を選択します。
11. **追加** を選択します。 目的のレコードを選択します。
12. **テーブル**、**派生テーブル**、および **フィールド** フィールドで、ドロップ ダウン メニューからオプションを選択または入力します。
13. ページを閉じます。
14. **基準** フィールドに値を入力します。
15. **OK** を選択します。
16. **OK** を選択します。
17. ページを閉じて、ホーム ページに戻ります。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
