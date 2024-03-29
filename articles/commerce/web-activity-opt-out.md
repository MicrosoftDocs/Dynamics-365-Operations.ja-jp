---
title: Web アクティビティ イベント コレクションのオプトアウト
description: この記事では、web サイトへの訪問者に対して、Microsoft Dynamics 365 Commerce の Web アクティビティ イベント コレクションをオプトアウトする方法について説明します。
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286728"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Web アクティビティ イベント コレクションのオプトアウト
[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で Web アクティビティ イベント コレクションを顧客にオプトアウトさせる方法について説明します。

Dynamics 365 Commerce では、サイト管理者が自社の e コマース サイトのユーザーのウェブ アクティビティ の分析をすることが可能となります。 そうすることで、自身のサイトがどのように使われているかをより理解することができ、ユーザー エクスペリエンスを向上させ、ビジネスの目標を達成するためにサイトを最適化することができるようになります。


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>管理者がオプトアウト エクスペリエンスを実装する方法

管理者がオプトアウト エクスペリエンスを実装する方法は、3 つあります。

### <a name="opt-out-on-behalf-of-users"></a>ユーザーに代わってオプト アウトする

Commerce 本部のアカウント管理では、管理者はユーザーに代わってオプト アウトを行うことができます。

1. HQ クライアントで **すべての顧客** ページで、顧客を検索して選択します。
1. [顧客の詳細] ページにて、 **小売** クイックタブの **プライバシー** セクションで、**アクティビティの追跡をしない** オプションを **はい** に設定します。

    ![プライバシー設定。](media/Disablepersonalizationpart2.png)

1. **保存** を選択し、ページを閉じます。

### <a name="module-based-opt-out-experience"></a>モジュールベースのオプトアウト エクスペリエンス

管理者は、認証されたユーザーが自分で Web アクティビティ イベント コレクションをオプトアウトを選択させることができます。 このオプトアウト エクスペリエンスを提供するには、顧客アカウント プロファイル ページにユーザーのオプトアウト モジュールを追加します。

### <a name="custom-extensions"></a>カスタムの拡張機能

管理者は、ユーザーのオプトアウト エクスペリエンスを管理するの独自の拡張機能を作成できます。 詳細については、[Retail サーバー API](e-commerce-extensibility/call-retail-server-apis.md) および [オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
