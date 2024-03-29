---
title: 会社間勘定の設定
description: この記事は、日次仕訳帳、ベンダー請求書仕訳帳、支払仕訳帳などの会計割り当ておよび財務仕訳帳の会社間仕訳帳を使用できるように会社間の会計を設定する方法に関して説明します。
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 309c121c1ef4b3814d676cad6f3c2b6826b59843
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871220"
---
# <a name="intercompany-accounting-setup"></a>会社間勘定の設定

[!include [banner](../includes/banner.md)]

この記事は、日次仕訳帳、ベンダー請求書仕訳帳、支払仕訳帳などの会計割り当ておよび財務仕訳帳の会社間仕訳帳を使用できるように会社間の会計を設定する方法に関して説明します。

会社間仕訳帳は、日次仕訳帳、ベンダー請求書仕訳帳、会計割り当ておよび一括支払など、さまざまなタイミングで作成できます。 これらのシナリオを有効にするには、会社間会計を設定する必要があります。

## <a name="define-main-accounts"></a>主勘定を定義する
最初に、貸し勘定項目および借り勘定項目に使用する会社間主勘定を作成する必要があります。 会社間勘定項目の調整および削除を簡略化するために、会社ごとに固有の主勘定を使用することをお勧めします。 トレーディング パートナまたはカウンターパート ディメンションを使用して内部取引先を識別する場合、このディメンションは、内部取引会計で定義されている主勘定の固定ディメンションとして定義することができます。 主勘定を設定するときは、**主勘定** ページで、**主勘定タイプ** フィールドを **貸借対照表** に設定する必要があります。

## <a name="define-journal-names"></a>仕訳帳名の定義
次に、仕訳帳名を定義する必要があります。 **仕訳帳名** ページで、**仕訳帳タイプ** フィールドを **毎日** に設定します。 会社間会計に対して特定の仕訳帳名を使用することをお勧めします。

## <a name="define-intercompany-accounting-setup"></a>会社間会計設定を定義する
**会社間会計** ページは、お互いに取引できる法人のペアを作成するために使用されます。 会社間会計設定は共有されているため、すべての法人内から設定が表示されます。 新しい法人のペアを作成する場合、目的とする会社に対して、どの法人を元の会社とするかを把握している必要があります。 会社間のトランザクションが行われる場合、トランザクションはどの法人がトランザクションを開始するかまたは起源となるかについて決定します。 たとえば、会社間会計が USMF (元) および USSI (目的先) に対して設定されています。 ある USSI がアクティブなユーザーが、USMF との内部取引を開始すると、内部会社会計は発信元である USMF に対してのみ定義されるため、取引は転記されません。 いずれかの会社が取引を開始することができる場合は、相互設定のための第 2 の法人のペアを作成する必要があります。 

元の法人と目的の法人の両方の、**借方取引先企業 (元)** および **クレジット取引先企業 (目的先)** を選択します。 宛先の会社でトランザクションが作成されたときに使用する **仕訳帳名** を定義します。 元の会社の仕訳帳は、会社間取引の作成時にユーザーによって選択されているので、すでにわかっています。 

最後に、現金割引や集中支払の実現損益などの金額を支援する会計をどの法人が受け取るかを選択します。 

相互的な関係は、最初の法人ペアが作成された後に、**会社間会計** ページで **相互的関係の作成** ボタンを使用することにより簡単に設定できます。 相互的なペアが作成された場合、目的先の会社の情報が元の会社にコピーされ、その更新が相互に反映されます。 目的先の会社に対して定義された仕訳帳は残ります。 ほとんどの組織では、仕訳帳の名前に対して同じ命名規則を使用しているので、仕訳帳名は同じです。 仕訳帳の名前が異なる場合、仕訳帳が存在せず異なる仕訳帳が選択されているということを注意するために、フィールドに警告が発せられます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
