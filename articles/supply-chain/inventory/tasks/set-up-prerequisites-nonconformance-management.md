---
title: 不適合管理の前提条件を設定する
description: このトピックを使用して不適合管理プロセスを有効化します。
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961523"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>不適合管理の前提条件を設定する

[!include [banner](../../includes/banner.md)]

このトピックを使用して不適合管理プロセスを有効化します。 不適合とは、品質上の問題がある手順または品目を表し、その説明には問題の原因およびタイプが含まれます。 この手順では、デモ データの会社 USMF を使用します。 通常この手順は品質マネージャーが実施します。


## <a name="enable-quality-management-processes-within-the-company"></a>社内品質管理プロセスの有効化
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター** の順に移動します。
2. **品質管理** タブを選択します。
3. **品質管理を使用する** フィールドで **はい** を選択して、会社の品質管理プロセスを有効にします。
4. **時間レート** フィールドに、国内通貨で数値を入力します。 時給レートは、不適合に関連する工程の原価計算に使用されます。 時間あたりのレートと算出原価は、不適合の参照情報を提供するものであり、他の機能に作用することはありません。  
5. **レポートの設定** を選択して、異なる種類の品質管理レポートで使用される品質レポートのメモのタイプを定義することができます。

## <a name="enable-user-for-nonconformance-processing"></a>不適合処理に対しユーザーを有効化
1. ナビゲーション ウィンドウで、**モジュール > システム管理 > ユーザー > ユーザー** の順に移動します。 
2. クイック フィルターを使用して不適合のレコードを承認または否認するユーザーを検索します。 たとえば、値 `Ricardo` を含む **名前** フィールドをフィルター処理します。 不適合の承認を処理する場合、不適合を承認または否認するユーザーは、**ユーザー** ページで "名前" の値が割り当てられている必要があります。 ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。  
3. 目的のレコードの行をマークします。
4. **ユーザー オプション** を選択します。
5. **基本設定** タブを選択します。
6. **ドキュメントの処理の有効化** フィールドで **はい** を選択します。

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>不適合処理の診断タイプの定義
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 診断タイプ** の順に移動します。 診断アクションの分類を定義するためには、**診断タイプ** ページを使用します。 訂正は、承認された不適合に対して行う必要のある診断アクションのタイプ、担当者、要求された完了日、予定の完了日などを識別します。  
2. **新規** を選択します。
3. **診断** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。

## <a name="define-quality-charges-for-nonconformance-processing"></a>不適合処理の品質諸費用の定義
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 品質諸費用** の順に移動します。 **品質諸費用** ページを使用して、不適合に関連する行程で使用される請求の分類を定義します。  
2. **新規** を選択します。
3. **諸費用コード** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。

## <a name="define-the-operations-for-nonconformance-processing"></a>不適合処理の行程の定義
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 工程** の順に移動します。 **工程** ページを使用して、承認済の不適合に対して実行することができる作業の分類を定義します。 行程をを不適合に関連付ける際、その操作を実行するために必要な関連する材料、労働時間、雑費などの情報を定義することができます。 この情報は、この工程を実行するための見積原価を計算する基準を提供します。  
2. **新規** を選択します。
3. **工程** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。

## <a name="define-problem-types-for-nonconformance-processing"></a>不適合処理の問題タイプの定義
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 問題タイプ** の順に移動します。 **問題タイプ** ページを使用して、さまざまな不適合タイプで発生する品質上の問題の分類を定義します。 不適合タイプには、**内部**、**顧客**、**仕入先**、**サービス要求**、**生産** および **連産品の生産** があります。 1 つの問題タイプを複数の不適合タイプに関連付けることができます。  
2. **新規** を選択します。
3. **問題タイプ** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。
5. **不適合タイプ** を選択します。 **不適合タイプ** ページを使用して、1 つ以上の不適合タイプでの問題タイプの使用を承認します。 たとえば、欠陥コードに関連した問題タイプは、すべての不適合タイプに適用できます。一方、顧客の苦情に関する問題タイプは、顧客およびサービス要求の不適合タイプにしか適用できません。  
6. **新規** を選択します。
7. 新しい行の **不適合タイプ** フィールドで、オプションを選択します。

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>不適合処理の検査ゾーンの定義
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 検査ゾーン** の順に移動します。
2. **新規** を選択します。
3. **検査ゾーン** フィールドに値を入力します。
4. **説明** フィールドで、値を入力します。
5. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]