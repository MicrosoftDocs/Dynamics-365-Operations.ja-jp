---
title: 支払のリベートの処理
description: この手順は、承認済および処理済の顧客リベートを貸方票に変換する方法を示します。
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617b5d99973e630cca2973227c2e54a63bd1ec4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263303"
---
# <a name="process-rebates-for-payment"></a>支払のリベートの処理

[!include [banner](../../includes/banner.md)]

この手順は、承認済および処理済の顧客リベートを貸方票に変換する方法を示します。 USMF デモ データ会社でこのガイドを使用できます。 このガイドの前提条件は、[マーク] の状態のリベート要求が 1 つ以上あることです。 USMF を使用している場合は、このガイドを開始する前に、"顧客リベートの生成と処理" ガイドを実行する必要があります。


## <a name="convert-rebate-claims-to-credit-note"></a>リベート要求の貸方票への変換
1. [すべての顧客] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [アクション] ウィンドウで、[回収] をクリックします。
5. [トランザクションの決済] をクリックします。
6. [機能] をクリックします。
7. [リベート プログラム] をクリックします。
    * [リベート] ページには、顧客リベートワークベンチで処理され、「マーク」が付いた状態になっているリベート請求が一覧表示されます。    
8. [編集] をクリックします。
    * 貸方票に含める要求の [マーク] フィールドにチェックマークを付けます。   
9. [機能] をクリックします。
10. [訂正票の作成] をクリックします。
    * 仕訳帳が転記されたことを通知するメッセージが表示されます (これは、[売掛金勘定パラメーター] ページで指定された売掛金管理消費仕訳帳です)。 これにより、実際の負債 (貸方) 金額が顧客残高に移動します。 つまり、顧客勘定は貸方に転記され、リベート見越計上勘定は借方に転記されます。  
11. ページを閉じます。
12. [キャンセル] をクリックします。
    * これによっては、ページを更新し、更新を確認できます。  
13. [アクション] ウィンドウで、[回収] をクリックします。
14. [トランザクションの決済] をクリックします。
    * 合計リベート金額を表す請求書参照のないマイナスの金額のトランザクションが顧客残高に追加されたことに注意してください。   
15. [キャンセル] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]