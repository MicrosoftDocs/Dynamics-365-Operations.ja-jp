---
title: 転記されたリース トランザクションの取消
description: この記事では、転記されたリース トランザクションを取り消す方法について説明します。 資産リースで作成されたすべてのトランザクションを取り消すことができます。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4f23b6cca6ddf4da7a0232a5bc61785dbd451d55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908070"
---
# <a name="reverse-posted-lease-transactions"></a>転記されたリース トランザクションの取消

[!include [banner](../includes/banner.md)]

資産リースで作成されたすべてのトランザクションを取り消すことができます。 資産リースで取り消されたトランザクションは、リース データを更新します。 したがって、リース負債および使用権 (ROU) 資産のキャリー額も更新されます。

リースのトランザクションを取り消すには、次の手順に従います。

1. **資産トランザクション** ページまたは **負債トランザクション** ページでトランザクションを選択し、**トランザクションの取り消し** を選択します。
2. 表示されるダイアログ ボックスで、逆仕訳入力が転記される日付を編集できます。 既定では、**日付** フィールドは、選択したトランザクションのトランザクション転記日付に設定されます。 逆仕訳入力は、選択されたトランザクションの元の転記日付よりも前に転記することはできません。
3. **OK** を選択します。 仕訳入力は、選択した入力の取消を転記します。 取消は **資産トランザクション** または **負債トランザクション** ページに表示され、そのページにある現在の正味残高合計は更新済みです。

**追跡の取消** を選択すると、*追跡番号* と呼ばれるリンク番号と一緒に、ダイアログ ボックスに元のトランザクションと取り消されたトランザクションの両方が表示されます。 取消をわかりやすくし、可視性を向上させるために、リース スケジュールを使用して取消を追跡することもできます。

**スケジュール** ページにある **最新の仕訳帳番号** フィールドに、トランザクションの仕訳帳番号が表示されます。 トランザクションが取り消されると、このフィールドは、取消トランザクションの仕訳帳番号で更新されます。 さらに、トランザクションの取り消しを意味する **取る消し済み** のチェック ボックスが選択され、**転記済み** フィールドが選択されます。

## <a name="revoke-a-reversed-transaction"></a>取り消されたトランザクションの破棄

取り消されたトランザクションを破棄するには、次の手順に従います。

1. **スケジュール** ページまたは **トランザクション** ページで、元のトランザクションを選択します。
2. 次の手順のいずれかを実行します。

    - **スケジュール** ページで、 [トランザクション] を選択した場合は、[月次仕訳入力のバッチ作成](create-monthly-journals-batch.md) で仕訳帳の作成手順に従います。 仕訳帳は手動で転記する必要があります。
    - **トランザクション** ページで [トランザクション] を選択した場合は **トランザクションの取消** を選択します。 この破棄が以前の取消の破棄であることが記載されたメッセージが表示されます。また、この破棄の転記日付を編集することもできます。 ただし、一般的な業務の検証は、 **日付** フィールドに入力された日付に影響を与えます。 

3. **OK** を選択します。 仕訳入力は、選択した入力の取消を転記します。 取消は **トランザクション** ページで表示され、現在の正味残高合計が最初の取消の前の金額に戻されます。 したがって、残高に対する取消の影響は否定されます。

**追跡の取消** を選択すると、リンクされた追跡番号と一緒に、ダイアログ ボックスに元のトランザクションと取り消されたトランザクションの両方が表示されます。

適切な **スケジュール** ページを使用すると、破棄を追跡することもできます。 **取消** フィールドはクリアですが、**仕訳転記済** フィールドが選択されます。 さらに、**最新の仕訳帳番号** フィールドが破棄トランザクションの仕訳帳番号で更新され、**仕訳帳番号** フィールドが取消仕訳帳番号で更新されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
