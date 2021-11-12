---
title: 固定資産の処分の転記勘定
description: このトピックは、資産の処分の総勘定元帳の転記勘定を設定する方法について説明します。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c82cb8b82f2cc8424675f76c68613a2b5aa76745
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675521"
---
# <a name="fixed-asset-disposal-posting-accounts"></a>固定資産の処分の転記勘定

[!include [banner](../includes/banner.md)]

このトピックでは、資産を処分する際の総勘定元帳の計上科目の設定について説明します。

資産を処分する際に使用する一般会計の転記勘定を設定するには、**固定資産転記プロファイル** ページの **元帳勘定** クイックタブで **処分 - 売却** と **処分 - 仕損** を選択します。

両方の取引タイプ (売却または仕損による資産の処分) において、元帳勘定には固定資産の処分価額が入金されます。 借方は、たとえば銀行口座などのオフセット口座に計上されます。 固定資産を顧客に売却する場合は、相手勘定ではなく顧客勘定が使用されます。 詳細については、[固定資産の仕損としての処分](dispose-of-a-fixed-asset-as-scrap.md)を参照してください。

**処分** をクリックし、次に **売却** または **仕損** をクリックして、固定資産の正味簿価額を元に戻す具体的な勘定を設定します。 また、**処分パラメーター** ページで、**転記金額** フィールドや **売却額のタイプ** フィールドに情報を入力できます。 

低価格プール内の資産に対する処分トランザクションは、低価格プールの正味簿価額を処分金額分だけ減額します。 ただし、資産の売却額が低価格プールの正味簿価額を超えた場合、正味簿価額はゼロに減額されます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
