---
title: 勘定科目表の区切り記号を一意にする
description: この記事では、勘定科目表と分析コード値に同じ区切り記号を所有できない方法について説明します。 アップグレード後に区切り記号値を変更する必要があります。
author: RyanCCarlson2
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: RCarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.openlocfilehash: 2184d26e104f803ae1bf59155cf18f560652f318
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292499"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>勘定科目表の区切り記号を一意にする

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012 では、勘定科目表および分析コード値に対して、同じ区切り記号を使用することができます。 財務と運用の現在のバージョンでは、勘定科目表と分析コード名、または値に対して同じ区切り記号を設けることはできません。 重複する区切り記号がある場合、アップグレード後に変更することができます。 

## <a name="update-delimiter"></a>区切り記号の更新
勘定科目表との競合が発生している場合、勘定科目表の区切り記号およびプロジェクト/下位プロジェクト ID の形式は変更できません。 その他の分析コードの区切り記号を変更することはできません。 
- **一般会計パラメーター** > **勘定科目表および分析コード** > **区切り記号を変更** で、アップグレード後、勘定科目表の区切り記号を変更することができます。 
- 競合が、プロジェクト/下位プロジェクト ID の形式にのみ発生している場合、**プロジェクト管理および会計パラメーター** > **一般** > **下位プロジェクト形式を変更する** の値を変更することができます。 

### <a name="other-considerations"></a>その他の考慮事項
プロジェクト/サブプロジェクト ID と同様に、仕入先や顧客などの財務分析コードとして使用される他のマスタ データ レコードには、勘定科目表の区切り記号と同じ文字を使用する勘定科目 ID 値を設定できません。 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>更新された区切り記号が環境で必要かどうかを判断する方法 
アップグレードされた環境の区切り記号が競合している場合、セグメント化エントリ コントロールまたは分析コード エントリ コントロールに値を入力する際に動作が不安定になることがあります つまり、勘定と分析コードの組み合わせを入力するときは、ルックアップまたはポップ アップ メニューを常に使用する必要があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

