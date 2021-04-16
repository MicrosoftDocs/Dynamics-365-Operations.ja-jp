---
title: 分析コード ベースの製品マスターの部品表の作成
description: この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820085"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>分析コード ベースの製品マスターの部品表の作成

[!include [banner](../../includes/banner.md)]

この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。 最初の 4 つの記録がこの手順を完了するのに必要なデータを設定します。 この手順の作成に使用するデモ データの会社は USMF です。 このタスクは通常、製品デザイナーによって処理されます。


## <a name="select-the-product"></a>製品を選択します
1. [リリース済製品の保守] をクリックします。
2. [リリース済製品] をクリックします。
3. 一覧で、選択された行をマークします。
    * この順序による最初のタスク ガイドで作成した、分析コード ベースのコンフィギュレーション テクノロジ付きのリリース製品マスターを検索します。  
4. アクション ペインで、[エンジニア] をクリックします。
5. [BOM バージョン] をクリックします。

## <a name="create-new-bom-and-bom-version"></a>新しい BOM と BOM バージョンを作成します
1. [新規] をクリックします。
2. [BOM と BOM バージョン] をクリックします。
3. [名前] フィールドに値を入力します。
    * サイトの設定  
    * この手順では、BOM の特定のサイトは設定しません。  
4. [OK] をクリックします。
5. [新規] をクリックします。
    * この手順では、BOM に 4 つの明細行を追加します。 2 つの明細行はケーブル オプションを表し、もう 2 つの明細行はキャビネット オプションを表します。  
6. 一覧で、選択された行をマークします。
7. [品目番号] フィールドで、値を入力または選択します。
    * 品目番号 A0001、HDMI 6' Cables を選択します。  
8. [コンフィギュレーション グループ] フィールドで、値を入力または選択します。
    * この順序のガイド 4 で作成されたケーブル コンフィギュレーション グループを選択します。  
9. [新規] をクリックします。
    * 品目番号 A0002、HDMI 12' Cables を選択します。  
10. 一覧で、選択された行をマークします。
11. [品目番号] フィールドで、値を入力または選択します。
12. [コンフィギュレーション グループ] フィールドで、値を入力または選択します。
    * もう一度ケーブル コンフィギュレーション グループを選択します。  
13. [新規] をクリックします。
14. 一覧で、選択された行をマークします。
15. [品目番号] フィールドで、値を入力または選択します。
    * 品目番号 D0002 Cabinet を選択します。  
16. [コンフィギュレーション グループ] フィールドで、値を入力または選択します。
    * この BOM 明細行のキャビネット コンフィギュレーション グループを選択します。  
17. [新規] をクリックします。
18. 一覧で、選択された行をマークします。
19. [品目番号] フィールドで、値を入力または選択します。
    * 最後の BOM 明細行として、品目番号 M0007 StandardCabinet を選択します。  
20. [コンフィギュレーション グループ] フィールドで、値を入力または選択します。
    * 最後の BOM 明細行に [キャビネット コンフィギュレーション グループ] を選択します。  

## <a name="approve-and-activate"></a>承認と有効化
1. ページを閉じます。
2. [承認] をクリックします。
3. [承認者] フィールドで、値を入力または選択します。
4. [部品表も承認しますか?] で [はい] を選択します。アクションを使用すると、このチェック ボックスは自動的にオンになります。
5. [OK] をクリックします。
6. [有効化] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]