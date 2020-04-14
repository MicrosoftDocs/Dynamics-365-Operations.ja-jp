---
title: 委託販売補充注文の作成
description: このトピックでは、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 766f29f7511c16eccd37e93f2de366ac23c35545
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145804"
---
# <a name="create-a-consignment-replenishment-order"></a>委託販売補充注文の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。 このほか、委託製品が仕入先所有の手持在庫として登録されるように製品の受領を記録する方法についても記述されています。 この作業は通常、調達担当者が行います。 デモ データの会社 USMF でこのガイドを使用できます。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。

## <a name="create-a-consignment-replenishment-order"></a>委託販売補充注文の作成
1. ナビゲーション ウィンドウで、**モジュール > 調達 > 委託販売 > 委託販売補充注文**の順に移動します。
2. **新規** を選択します。
3. **仕入先口座**フィールドで、仕入先 **US-104** (**在庫の所有者** ページで所有者として登録されている仕入先を選択する必要があります) を選択します。 
4. **OK** を選択します。
5. **明細行の追加**を選択します。
6. **品目番号**フィールドで、`M9211CI` (委託販売在庫に対して設定された品目を選択する必要があります) と入力します。
7. **数量**フィールドに、数値を入力します。
8. **配送希望日**フィールドに日付を入力します。 要求、確認された日付は、製品の予定着荷のMRPエンジンにより使用されています。  
9. **確認済配送日**フィールドに日付を入力します。
10. **行の詳細**セクションを展開します。
11. **在庫分析コード** タブを選択します。
12. **在庫規模所有者**フィールドで所有者を表示するには、ページを更新します。 仕入先US-104は所有者としてリストアップされています。  

## <a name="check-the-inventory-transaction-status"></a>在庫トランザクション状態をチェックします。
1. **在庫**を選択します。
2. **トランザクション**を選択します。
3. 目的の行で、**受領**フィールドが**注文済**に設定されていることを確認します。  
4. ページを閉じます。

## <a name="receive-items"></a>品目の受信 (複数)
1. **製品受領書**を選択します。
2. **外部製品受領**フィールドで、値を入力します。
3. **数量** フィールドにおいて、ここに表示される数値より小さい数値を入力します。 
4. **OK** を選択します。

## <a name="check-the-on-hand-inventory"></a>手持在庫を確認します。
1. **在庫**を選択します。
2. **手持**を選択します。
3. **概要**を選択します。 仕入先が所有する委託製品在庫として受領された品目は手持在庫として使用できます。 委託製品補充注文の残余数量は**発注済合計数**フィールドに表示されます。  
4. ページを閉じます。

