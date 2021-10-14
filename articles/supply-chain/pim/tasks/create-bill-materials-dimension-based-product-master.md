---
title: 分析コード ベースの製品マスターの部品表の作成
description: この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86625821f8a01a6d4949f9dca538a279f52ce9c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565591"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>分析コード ベースの製品マスターの部品表の作成

[!include [banner](../../includes/banner.md)]

この手順で、この一連の 8 つの記録において既に 4 つのガイドを完了している必要があります。 最初の 4 つの記録がこの手順を完了するのに必要なデータを設定します。 この手順の作成に使用するデモ データの会社は USMF です。 このタスクは通常、製品デザイナーによって処理されます。

## <a name="select-the-product"></a>製品を選択します

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 一覧で、選択された行をマークします。
    * この順序による最初のタスク ガイドで作成した、分析コード ベースのコンフィギュレーション テクノロジ付きのリリース製品マスターを検索します。  
1. アクション ペインで、**エンジニア** を選択します。
1. **BOM バージョン** を選択します。

## <a name="create-new-bom-and-bom-version"></a>新しい BOM と BOM バージョンを作成します

1. **新規** を選択します。
1. **BOM と BOM バージョン** を選択します。
1. **名前** フィールドに値を入力します。
    * サイトの設定  
    * この手順では、BOM の特定のサイトは設定しません。  
1. **OK** を選択します。
1. **新規** を選択します。
    * この手順では、BOM に 4 つの明細行を追加します。 2 つの明細行はケーブル オプションを表し、もう 2 つの明細行はキャビネット オプションを表します。  
1. 一覧で、選択された行をマークします。
1. **品目番号グループ** フィールドで、値を入力または選択します。
    * 品目番号 A0001、HDMI 6' Cables を選択します。  
1. **コンフィギュレーション グループ** フィールドで、値を入力または選択します。
    * この順序のガイド 4 で作成されたケーブル コンフィギュレーション グループを選択します。  
1. **新規** を選択します。
    * 品目番号 A0002、HDMI 12' Cables を選択します。  
1. 一覧で、選択された行をマークします。
1. **品目番号グループ** フィールドで、値を入力または選択します。
1. **コンフィギュレーション グループ** フィールドで、値を入力または選択します。
    * もう一度ケーブル コンフィギュレーション グループを選択します。  
1. **新規** を選択します。
1. 一覧で、選択された行をマークします。
1. **品目番号グループ** フィールドで、値を入力または選択します。
    * 品目番号 D0002 Cabinet を選択します。  
1. **コンフィギュレーション グループ** フィールドで、値を入力または選択します。
    * この BOM 明細行のキャビネット コンフィギュレーション グループを選択します。  
1. **新規** を選択します。
1. 一覧で、選択された行をマークします。
1. **品目番号グループ** フィールドで、値を入力または選択します。
    * 最後の BOM 明細行として、品目番号 M0007 StandardCabinet を選択します。  
1. **コンフィギュレーション グループ** フィールドで、値を入力または選択します。
    * 最後の BOM 明細行にキャビネット コンフィギュレーション グループを選択します。  

## <a name="approve-and-activate"></a>承認と有効化

1. ページを閉じます。
1. **承認** を選択します。
1. **承認者** フィールドで、値を入力または選択します。
1. **部品表も承認しますか?** フィールドで、*はい* を選択します。
1. **OK** を選択します。
1. **有効化** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]