---
title: Regression Suite Automation Tool を使用したデータ認識不可能テスト
description: このトピックでは、Regression Suite Automation Tool を使用したデータ認識不可能テストに関する推奨事項について説明します。
author: kfend
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7fd1fc4756e74a5d07ffae533b6b9837b960f17a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693753"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool を使用したデータ認識不可能テスト

[!include [banner](../includes/banner.md)]

ERP アプリケーションの機能の検証は、完全にデータ認識不可能ではありませんが、テストをするために複数のフェーズとアプローチがあります。 テスト フェーズには次のものが含まれます。  

- SysTest フレームワーク
- ATL フレームワーク
- Regression Suite Automation Tool (RSAT)

[![テストの分類ピラミッド](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>概要
-   **SysTest フレームワーク** – SysTest フレームワークは、単体テストの書き込みに対して信頼性があります。 単体テストは一般にメソッドまたは関数のテストで、常にデータ認識不可能性があり、テストの一部として提供されている入力データにのみ依存しています。
-   **ATL フレームワーク** – Microsoft には SysTest フレームワークが抽象化された ATL フレームワークがあり、機能テストの書き込みをより簡易で信頼性のあるものにします。 このフレームワークは、コンポーネント テストまたは簡易な統合テストを書き込むために使用されます。
-   **RSAT** – RSAT は、統合テストおよび業務サイクル テストに使用されます。 回帰検証テストとも呼ばれる業務サイクル テストは、既存のデータに依存しています。 ただし、追加要素を考慮した場合、これらのテストがデータ認識不可能になることがあります。 

    - o 単体テストおよびコンポーネント テストのレベルが低く、完全にデータ認識不可能になる場合 (既存のデータセットに依存していない)、業務サイクルまたは再帰検証テストは一部の既存のデータに依存しています。 このデータには、設定、コンフィギュレーション設定 (パラメーター)、およびマスター データ (顧客、仕入先、品目など) が含まれますが、トランザクション データは含まれません。 テスト中にいずれかが変更中である場合、最終テストの一部として元に戻されることを確認してください。
    - 特定のレコードを選択する代わりに、特定の基準に基づいてマスター データを選択します。 たとえば、分析コード値および有効在庫数に基づいて品目を選択する場合、その値で製品リストをフィルター処理を行い、最初の品目を選択して、未来のテストに使用される番号をコピーします。 顧客、仕入先、または品目などの簡易なマスター データ明細行の場合、自動化の一部として作成され、連鎖による未来のテストで使用されます。 
    - o 請求書番号などを番号順序で、または =TEXT(NOW(),"yyyymmddhhmm") のような Microsoft Excel の関数により固有識別子入力をします。 この関数により、アクションが発生した時間を追跡できるように、毎分固有の番号が提供されます。 これは、製品受領書番号や仕入先請求書番号などの変数に使用することができます。 これらのテストは、復元を必要とせずに、同じデータベース上で幾度も継続して動作します。
    - 既定のオプションは **自動** であるため、常に環境の **編集モード** を設定して、最初のテスト ケースとして **読み取り** または **編集** を行います。**自動** オプションは常に以前の設定を使用することができ、信頼できないテストを引き起こすことがあります。 
 
    [![オプション ページ、パフォーマンス タブ](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - 一般的な検証の代わりに、特定のトランザクションに対するフィルター処理をした後にのみ検証します。 たとえば、レコード数について、検証が他のすべてのトランザクションを除外するように、トランザクション番号またはトランザクション日付に対してフィルター処理を行います。 
    - 顧客残高または予算チェックを確認している場合、値を先に保存してトランザクション値を追加することにより、固定の予測値を検証する代わりに、予測された結果を検証します。 
 
