--- 
title: "資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力 (日本)"
description: "日本では、資産除去責務 (ARO) ドキュメントは資産除去責務の 1 つのタイプを識別します。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 858cbf5f5beee4c02ebbb670f35386d26a0883f4
ms.openlocfilehash: bf550371c6a373b4145ebc7b84a2714296256daf
ms.contentlocale: ja-jp
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-asset-retirement-obligation-documents-and-enter-aro-amount-on-a-fixed-asset-japan"></a>資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力 (日本)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

日本では、資産除去責務 (ARO) ドキュメントは資産除去責務の 1 つのタイプを識別します。 固定資産帳簿に ARO ドキュメントを割り当てると、資産除去時に責務を履行すると予測されるキャッシュ フローを指定することができます。 



この手順では、ARO ドキュメントの作成、固定資産への割り当て、および見積除去減価の入力方法について説明します。



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="setup-asset-retirement-obligation-document"></a>資産除去責務ドキュメントの設定
1. [固定資産] > [資産除去責務] > [資産除去責務ドキュメント] に移動します。
2. [新規] をクリックします。
3. [ドキュメント ID] フィールドに値を入力します。
4. [文書日付] フィールドに日付を入力します。
    * 文書の日付は、固定資産帳簿に ARO ドキュメントを割り当てる際に使用される既定値です。  
    * [転記頻度] フィールドで、資産除去責務の支払利子発生頻度を選択します。  
5. [説明] フィールドに値を入力します。
6. [保存] をクリックします。

## <a name="create-a-fixed-asset-and-assign-the-asset-retirement-obligation-document-to-it"></a>固定資産の作成および資産除去責務ドキュメントの割り当て
1. [固定資産] > [資産除去責務] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドで、固定資産に適用する固定資産グループを選択します。
4. [名前] フィールドに固定資産の名前を入力します。
5. [アクション] ウィンドウで、[固定資産] をクリックします。
6. [資産除去責務] をクリックします。
7. [帳簿] フィールドで、固定資産の帳簿を選択します。
8. [ドキュメント ID] フィールドで、固定資産に添付する資産除去ドキュメントの ID を選択します。

## <a name="enter-the-asset-retirement-obligation-amounts"></a>資産除去責務金額の入力
1. [作成] をクリックしてドロップ ダイアログを開きます。
2. [トランザクション日付] フィールドで、資産除去責務を認識する日付を入力します。
3. [見積除去原価調整] フィールドにキャッシュ フロー金額を入力します。
4. [OK] をクリックします。


