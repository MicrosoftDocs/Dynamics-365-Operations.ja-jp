---
title: "勘定科目表の区切り記号を一意にする"
description: "Dynamics 365 for Finance and Operations では、勘定科目表および分析コード値に対して同じ区切り記号を設けることはできません。 アップグレード後に区切り記号値を変更する必要があります。"
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a>勘定科目表の区切り記号を一意にする

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012 では、勘定科目表および分析コード値に対して、同じ区切り記号を使用することができます。 Dynamics 365 for Finance and Operations では、勘定科目表および分析コード値に対して同じ区切り記号を設けることはできません。 重複する区切り記号がある場合、アップグレード後に変更することができます。 

この機能は次で使用することができます。
- Dynamics 365 for Finance and Operations バージョン 8.0
- 分析コード値が勘定科目表の区切り記号を含んでいる場合、Dynamics 365 for Finance and Operations バージョン 7.1、KB 4094701 は財務分析コードを入力することができません
- 下位プロジェクトの形式が分析コードの区切り記号を含んでいるとき、Dynamics 365 for Finance and Operations バージョン 7.2、KB 4092967 は下位プロジェクトを分析コードとして選択することができません

## <a name="update-delimiter"></a>区切り記号の更新
勘定科目表との競合が発生している場合、勘定科目表の区切り記号およびプロジェクト/下位プロジェクト ID の形式は変更できません。 その他の分析コードの区切り記号を変更することはできません。 
- **一般会計パラメーター** > **勘定科目表および分析コード** > **区切り記号を変更**で Finance and Operations をアップグレード後、勘定科目表の区切り記号を変更することができます。 
- 競合が、プロジェクト/下位プロジェクト ID の形式にのみ発生している場合、**プロジェクト管理および会計パラメーター** > **一般** > **下位プロジェクト形式を変更する**の値を変更することができます。 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>更新された区切り記号が環境で必要かどうかを判断する方法 
アップグレードされた環境の区切り記号が競合している場合、セグメント化エントリ コントロールまたは分析コード エントリ コントロールに値を入力する際に動作が不安定になることがあります つまり、勘定と分析コードの組み合わせを入力するときは、ルックアップまたはポップ アップ メニューを常に使用する必要があります。

