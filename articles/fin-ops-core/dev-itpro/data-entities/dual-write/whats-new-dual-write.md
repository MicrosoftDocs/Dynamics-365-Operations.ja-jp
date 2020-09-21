---
title: 二重書き込みの新機能および変更された機能
description: このトピックでは、リリース計画、主要な発表、二重書き込みのドキュメントなどへのリンクを提供します。
author: robinarh
manager: AnnBe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2bbc269975b42637760c6224d2433d1a04b4afc2
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728536"
---
# <a name="whats-new-or-changed-in-dual-write"></a>二重書き込みの新機能および変更された機能

[!include [banner](../../includes/banner.md)]

二重書き込みは、Microsoft Dynamics 365 アプリと Finance and Operations アプリの Customer Engagement アプリ間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。 デュアル書き込みを開始する方法については、[デュアル書き込みホームページ](dual-write-home-page.md) を参照してください。

[リリース計画](https://go.microsoft.com/fwlink/?linkid=2010158) におけるデュアル書き込み機能および変更点に関する最新情報を確認してください。

+ [Common Data Service のデータ - フェーズ 1](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1)
+ [Common Data Service のデータ - フェーズ 1 と 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/finance-operations-crossapp-capabilities/data-common-data-service-phase-1-2)
+ [Common Data Service の Finance and Operations データ – フェーズ 3](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/finance-operations-data-common-data-service-phase-3)

## <a name="june-2020-release"></a>2020 年 6 月リリース

2020 年 6 月リリースのデュアル書き込みオーケストレーション パッケージには、次のテーブルに示す機能とバグ修正が含まれています。

| 機能 | 説明 |ステータス |
|------|---------|-------|
| 二重書き込み設定後に法人を編集する | 企業や法人の一覧は静的ではなく、常に変化しています。 たとえば、段階的なロールアウトや買収の際に、新しい会社を追加することが必要な場合があります。 以前は、会社や法人をシステムのダウンタイムなしで追加することはできませんでした。 このダウンタイム中に、環境のリンクを解除して再リンクする必要があります。 これは、特にデータが既に存在する場合は、費用がかかる可能性があります。 この機能を使用すると、リンクを解除して再リンクすることなく、ライブ環境で会社を追加できます。 | 一般提供 |


## <a name="may-2020-release"></a>2020 年 5 月リリース

2020 年 5 月リリースのデュアル書き込みオーケストレーション パッケージ (バージョン 2.0.777.353) には、次のテーブルに示す機能とバグ修正が含まれています。

| 機能 | 説明 |ステータス |
|------|---------|-------|
| 手持在庫の検索 | Customer Engagement アプリのフォームで、手持在庫と納期回答可能日を参照できます。 | 一般提供 |
| 単位換算 |    Finance and Operations アプリで見積もり明細行と注文明細行の単位換算が発生すると、Customer Engagement アプリによって、その単位換算が受け入れられ、顧客契約アプリの見積詳細と注文の詳細の単位と価格に対する変更が反映されます。 | 一般提供 |
| 通貨変更の制限 | 既存の見積もりや注文に対して Finance and Operations アプリの通貨を変更しようとすると、変更は失敗します。   | 一般提供 |
| **アカウント** フォームと **契約** フォームのパリティ | B2B と B2C の Customer Engagement アプリで **アカウント** フォームと **連絡先** フォームの属性アプリを持ち込みます。  | 一般提供 |
| アドレスの重複なし | Customer Engagement アプリの見積または注文に対して作成または更新のアクションがある場合は、Finance and Operations アプリでアドレスを重複させないでください。  | 一般提供 |
| **SalesTaxGroup** サポート | 企業間 (B2B) および企業と顧客間 (B2C) 顧客向けの **アカウント** フォームと **連絡先** フォームの **SalesTaxGroup** をサポートしています。 | 一般提供 |
| 販売可能の契約の作成 | Customer Engagement アプリの **簡易作成: 連絡先** フォームを使用して、販売可能な連絡先を作成できるようにします。 | 一般提供 |
| 見積もりと注文の作成 | B2C 顧客の見積もりと注文の作成を有効にします。 | 一般提供 |
| テナント管理者レベルの承認要件の削除 | これまでは、デュアル書き込みを有効にするには、アプリケーションに対する承認を明示的に行う必要がありました。 これは、実用的で、追加の承認が必要であるため、時間がかかる場合があります。 この機能を使用すると、この前提条件と、アプリケーションに対する同意を明示的に提供する必要がなくなりました。 | 一般提供 |
| デュアル書き込み環境の強制リンク解除 | これまでは、デュアル書き込みのテスト中に、すべてのエンティティ マップを無効にしてから、デュアル書き込み環境のリンクを解除する必要がありました。 この方法は煩雑になり、いずれかの環境が使用できない場合は不可能になることがあります。 この新しい機能を使用すると、テスト環境とトライアル環境を簡単にリンク解除することができます。 | 一般提供 |


