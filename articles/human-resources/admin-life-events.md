---
title: ライフ イベントの管理者権利を設定する
description: この記事では、Microsoft Dynamics 365 Human Resources でライフ イベントの管理者の権限を構成する方法について説明します。
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229901"
---
# <a name="set-administrator-rights-for-life-events"></a>ライフ イベントの管理者権利を設定する

[!include [banner](../includes/preview-banner.md)]

管理者は構成設定により、ライフ イベントのオプションを更新できます。 **人事リソース パラメーター** ページでは、管理者が計画の選択に変更を加えることを許可するパラメーターを構成できます。 管理者による変更を完全に制限することもできます。

**人事管理パラメータ** ページで、確認済の計画およびライフ イベント オプションに対して計画変更制限を設定できます。

**確認済計画** オプションが選択されている場合は、登録期間が有効な場合にのみ変更できます。 (登録期間の例として、オープン登録期間、新規採用登録期間、ライフ イベント登録期間があります。)このオプションを選択しない場合は、いつでも変更できます。

**ライフ イベント オプション** オプションが選択されている場合、ライフ イベント中の計画の変更は、計画のタイプに定義されたライフ イベント オプションによって制限されます。 このオプションを選択しない場合、ライフ イベント時に計画の選択内容を変更できます。

## <a name="set-plan-change-restrictions"></a>計画変更制限の設定

**人事管理パラメータ** ページの **福利厚生管理** タブでは、次のフィールドを使用できます。

| フィールド | Description |
|-------|-------------|
| 確認済の計画 | 登録期間が有効な場合にのみプランの変更が許可される場合は、このオプションを選択します。 このオプションを選択しない場合は、いつでも変更できます。 |
| ライフ イベント オプション | ライフ イベントが、計画の種類で定義されたライフ イベント オプションによって制限されている間に計画を変更する場合は、このオプションを選択します。 このオプションを選択しない場合、ライフ イベント時に計画の選択内容を変更できます。 |
