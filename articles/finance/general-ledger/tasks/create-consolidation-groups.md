---
title: 連結グループおよび追加の連結勘定の作成
description: この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a02d6cf5516e63378f4aa356627c069404546e07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216523"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a>連結グループおよび追加の連結勘定の作成

[!include [banner](../../includes/banner.md)]

この手順では、連結勘定グループの作成方法と、グループへの勘定の追加方法について説明します。 この手順では、デモ データ会社 USMF を使用します。


## <a name="create-a-consolidation-account-group"></a>連結勘定グループの作成
1. [総勘定元帳] > [勘定科目表] > [勘定] > [連結勘定グループ] に移動します。
2. [新規] をクリックします。
3. [連結勘定グループ] フィールドに連結勘定グループ固有の ID を入力します。
4. [名前] フィールドに値を入力します。

## <a name="add-accounts-to-consolidation-account-group"></a>連結勘定グループに勘定を追加
1. ページを閉じます。
2. [総勘定元帳] > [勘定科目表] > [勘定] > [追加連結勘定] に移動します。
3. [新規] をクリックします。
4. [主勘定] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。
5. 一覧で、マップする主勘定をクリックします。
6. [連結勘定グループ] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。
7. 一覧で、連結勘定グループをクリックします。
8. [連結勘定] フィールドに値を入力します。
9. [連結勘定名] フィールドに値を入力します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]