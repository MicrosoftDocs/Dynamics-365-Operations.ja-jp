---
title: "拡張性 FAQ"
description: "このトピックでは、拡張機能に関してよくある質問に対する回答を示します。"
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 4b847a0025ab0e57bbe982d31b01c14a8c6b2254
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="extensibility-faq"></a>拡張性 FAQ

[!include [banner](../includes/banner.md)]

## <a name="will-source-code-be-available-after-the-hard-seal"></a>ハード シールの後にソース コードを使用できますか。

はい、ソース コードはハード シールの後に使用することができます。 効果的な実装とデバッグのために必須とされます。

## <a name="how-do-i-contact-microsoft-if-i-have-an-extensibility-request"></a>拡張機能の要求がある場合、Microsoft に連絡するにはどうすればよいですか。

Lifecycle Services (LCS) サイトには特別な拡張性要求書式があります。 

## <a name="where-can-i-ask-questions-about-extensibility-patterns"></a>拡張性のパターンについてはどこで質問できますか

Yammer で Operations Extensibility グループに対するアクセスを取得することができます。 Operations Extensibility は、パートナー契約の大部分を占める有効なグループです。 機密保持契約に署名することにより、接続サイト経由でアクセスできるようになります。

## <a name="where-can-i-find-documentation-about-extensibility-patterns"></a>拡張性のパターンについてのドキュメントはどこにありますか ?

拡張性パターンについてのドキュメントは、[拡張性 ホーム ページ](extensibility-home-page.md)で利用可能です。

## <a name="where-can-i-get-information-about-extensibility-training"></a>拡張性のトレーニングに関する情報を取得する場所は?

トレーニング セッションを複数の方法で公表します。 AppSource パートナーは、一部のセッションについて直接招待を受ける可能性があります。 Operations Extensibility Yammer グループおよびその他のフォーラムのワーク ショップも公表します。  

## <a name="what-is-the-goal-of-sealing-the-application"></a>アプリケーションの封印の目的は何ですか ?

アプリケーションは、エコシステムでのアップグレード コスト削減への第一歩としてシールされているため、顧客は、常に最新のリリースを利用できます。 顧客は、Microsoft およびパートナーの新しい革新を利用することができます。

拡張パッケージを使用すると、設計時のパフォーマンスが向上し、ビルドの自動化が迅速になり、単体テストが可能になります。 また、独立したソフトウェア ベンダー (ISV) や顧客から、さまざまなシステム間でより効率的にモデルを配布したりインストールできるようになります。

## <a name="what-is-microsoft-working-on-to-support-this-move"></a>この動きをサポートするために Microsoft は何に取り組んでいますか ?

製品チームは、製品の拡張性を向上させるためにいくつかの分野に取り組んでいます。 この作業には、広範な影響を与えるプラットフォームの変更から、追加フック ポイントを提供するリファクタリングされたアプリケーション コードまでさまざまなものがあります。 詳細については、Operations Extensibility Yammer グループおよび製品のリリース ノートを参照してください。

## <a name="after-the-application-is-sealed-what-should-customers-do-in-a-critical-situation-if-they-must-make-a-quick-change"></a>アプリケーションをシールした後、すばやく変更する必要がある場合、顧客は、重要な状態で何をすべきでしょうか?

このシナリオは、致命的なバグ修正が必要なシナリオと非常によく似ており、同じプロセスを実行する必要があります。 必要な最初の手順として、サポートのためのケースを作成する必要があります。

## <a name="can-i-overlayer-an-isv-solution-after-the-hard-seal-of-the-application-code"></a>アプリケーション コードのハード シールの後に ISV ソリューションをオーバーレイすることはできますか。

ISV もモデルを封印することをお勧めします。 このステップは、アップグレード コストを削減するというより広い目標を達成するのに役立ちます。 

## <a name="will-i-be-able-to-overlayer-an-on-premises-solution"></a>オンプレミス ソリューションをオーバーレイすることはできますか。

オンプレミス ソリューションは、クラウド ソリューションとして同じパターンに従います。 したがって、Microsoft コードのオーバーレイはサポートされません。
    
## <a name="how-often-will-microsoft-provide-external-updates-so-that-partners-can-see-what-extensibility-enhancements-have-been-made"></a>どのくらいの頻度で Microsoft は外部更新を提供することで、パートナーがどの拡張性の強化が実行されたかを確認できますか。

Microsoft Dynamics 365 for Finance and Operations release 8.0 より後は、プラットフォームとアプリケーションの毎月の更新プログラムの提供を予定しています。

