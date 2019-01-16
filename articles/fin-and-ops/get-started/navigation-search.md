---
title: "ナビゲーション検索"
description: "このトピックでは、検索機能を使用して Microsoft Dynamics 365 for Finance and Operations のページに移動する方法を説明します。"
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 7c05098815c6b330cbb9c7f5ce886779927c6804
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="navigation-search"></a>ナビゲーション検索

[!include [banner](../includes/banner.md)]

このトピックでは、検索機能を使用して Microsoft Dynamics 365 for Finance and Operations のページに移動する方法を説明します。

Finance および Operations は、幅広い業界や業種に機能を提供します。 アプリケーションには、さまざまなタスクを実行するのに役立ついくつかの領域とページが含まれています。 タスクを完了するために必要なページをすばやく見つけるには、ナビゲーション検索機能を使用します。

この機能を使用するには、**検索** アイコンをクリックして **検索** ボックスを表示します。 その後、ボックスに 1 つ以上の単語を入力します。 システムはすぐに、アプリケーション内にある、入力した単語と一致する関連ページを検索します。 たとえば、入力として「仕入先請求書」と入力すると、システムはその入力に一致する結果を表示します。

> [!NOTE]
> **検索**ボックスは、ページの検索や移動に役立ちます。 特定のデータまたはアクションの検索には役立ちません。

[![検索ボックス](media/navigation-search.png "検索ボックス")

## <a name="quickly-navigate-to-a-particular-page"></a>特定のページにすばやく移動する

ナビゲーション検索機能は、特定のページへすばやく移動するためのよい手段でもあります。 たとえば、**支払仕訳帳** ページを頻繁に使用する買掛金担当者であれば、**検索** ボックスに "支払仕訳帳" と入力することができます。 入力はページのタイトルと完全に一致しているため、ページは検索結果の一番上に表示され、そのページにすばやく移動できます。

検索結果一覧には、ナビゲーション パスとページ タイトルが表示されます。 これはアプリケーション内のページの場所を示します。 また、結果内の複数の同じようなページを区別するのに役立ちます。

ページの検索時には、入力はページ タイトル、ナビゲーション パスと照合されます。 たとえば、**検索**ボックスに「売掛金」と入力した場合、ページ タイトルに「売掛金」という語を含んでいない場合にも、売掛金勘定エリアで使用できるページの結果が表示されます。

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>技術的なフォーム名に基づくページにすばやく移動する

また、ナビゲーション検索機能には、Power Users が非常に必要とする、技術的なフォーム名に基づくページにすぐに移動する機能があります。 多くのユーザーは、システムを非常に使い慣れているので、使用するフォームの正確な名前を知っています。 これらのユーザーの場合、**フォーム:** の後に探しているフォームの名前を入力できます。 たとえば、**フォーム: vendinvoice** と入力した場合、検索結果は、**vendinvoice** で始まるフォーム名を持つすべてのページを表示します。

## <a name="administration-and-security"></a>管理とセキュリティー

管理とセキュリティの観点から、ナビゲーション検索機能が表示するのは 2 つのタイプの結果だけです。

- 現在のコンフィギュレーションで有効なページ (コンフィギュレーション キー経由) 。
- ユーザーが、ユーザーのロールに基づいてアクセスするページ。

検索結果の一覧は、10 品目に限定されます。 結果内で検索したものが見つからなかった場合、入力を絞り込んだり、更新する必要があります。

## <a name="development"></a>開発

開発の観点からすれば、ナビゲーション検索機能は、メニュー項目の配置と検索結果の表示機能の間に遅延がないため、活用が非常に容易です。 メニュー項目は、ナビゲーション ウィンドウまたはダッシュボードにリンクされている場合、自動的に検索可能になります。

