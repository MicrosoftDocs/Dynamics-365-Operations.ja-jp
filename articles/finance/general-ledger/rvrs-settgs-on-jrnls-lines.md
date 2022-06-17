---
title: 仕訳帳と明細行の逆仕訳設定
description: この記事では、一般仕訳帳に入力された逆仕訳入力が、転記済トランザクションに含まれない可能性がある理由を説明します。
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899845"
---
# <a name="reverse-settings-on-journals-and-lines"></a>仕訳帳と明細行の逆仕訳設定

[!include [banner](../includes/banner.md)]

この記事では、一般仕訳帳に入力された逆仕訳入力が、転記済トランザクションに含まれない可能性がある理由を説明します。  

## <a name="symptom"></a>現象

一般仕訳帳には、仕訳帳の逆仕訳入力と逆仕訳日が含まれます。 仕訳帳を転記しても、いずれの伝票も逆仕訳されません。 なぜこのようなことが起こるのでしょうか?

## <a name="resolution"></a>解決策

仕訳帳を転記すると、逆仕訳プロセスでは、伝票の **明細行** セクションの **逆仕訳入力** 設定と **逆仕訳日** 設定のみ確認されます。 この方法では、仕訳帳に、逆仕訳するようにマークされた一部の伝票を含めることができ、マークされていない伝票は含まれません。

仕訳帳の値は、*新しい* 明細行を追加する場合の既定値としてのみ使用されます。 仕訳帳の値を変更しても、既存の明細行には影響しません。 この例では、伝票の明細行が最初に入力されました。 仕訳帳を逆仕訳として指定する前に明細行の詳細を入力すると、逆仕訳入力および日付としての指定は既存の明細行には適用されません。

既存の明細行の逆仕訳入力または逆仕訳日付を変更すると、その変更が同じ伝票の他の明細行にも反映されます。 パフォーマンスを最適化するために、他の明細行に変更が反映された後にグリッドは更新されません。 グリッドを更新すると、更新後の値を表示できます。


