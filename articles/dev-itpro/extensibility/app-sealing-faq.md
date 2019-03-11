---
title: 拡張性 FAQ
description: このトピックでは、拡張機能に関してよくある質問に対する回答を示します。
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 28568d7a959d3b29e7ea179c018c7e2fb9bd7e7e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368733"
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

トレーニング セッションを複数の方法で公表します。 AppSource パートナーは一部のセッションについて直接招待を受ける可能性があります。 Operations Extensibility Yammer グループおよびその他のフォーラムのワーク ショップも公表します。  

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

Microsoft Dynamics 365 for Finance and Operations リリース 8.0 の後、プラットフォームおよびアプリケーションの月ごとの更新プログラムを提供する計画です。

## <a name="why-wasnt-my-extensibility-request-accepted"></a>拡張性要求が承認されなかった理由を教えてください。

一部の拡張性は、重大な変更を要求します。 重大な可能性のあるよくある要求の一部を、その考えられる回避策と共に以下に掲載します。 さらに、[拡張の作成](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/add-enum-value)を読んで既存のプラットフォーム拡張機能については理解し、[拡張性要求を記録するためのヒント](https://blogs.msdn.microsoft.com/mfp/2018/09/15/tips-for-logging-extensibility-requests/)を読んで、機能が最新リリースに存在しない場合に適切な要求を作成する方法を確認してください。

### <a name="why-cant-edtstringsize-be-made-extensible"></a>EDT.StringSize を拡張可能にできないのはなぜですか?

- 要求: 拡張を通じて EDT.StringSize を変更可能にする。
- 問題: テーブル文字列フィールド (FieldX) のタイプが "親 EDT" であり、タイプが EDT2 (EDT2 は "親 EDT" から派生) の別のテーブルのフィールド (FieldY) に関連付けられている (テーブル関係を通じて) いる場合。 EDT2.StringSize の増加を許可することで FieldY が大きい文字列を持つ可能性がある場合、FieldX は新しい文字列サイズを処理できません。 
- 回避策: 新しい EDT を作成し、テーブル フィールド FieldY にそれを使用します。

### <a name="why-cant-a-unique-table-index-be-made-extensible"></a>固有のテーブル インデックスを拡張可能にできないのはなぜですか?

- 要求: 拡張を通じて固有のテーブル インデックスを拡張可能にする。たとえば、余分なフィールドの追加を許可するによってなど。
- 問題: 固有のテーブル インデックスが変更され、すべてのデータが新しいインデックスに準拠していない場合、重大な変更となります。 また、重複レコードを取得できるようになったため、クエリに影響を与えます。 たとえば、Person テーブルにキー "Name" があり、name="Chris" が適切な担当者を選択したが、BirthDate がキーに追加された場合、"Chris" に複数のレコードが返される可能性があります。
- 回避策: validateWrite または validateInsert メソッドに "soft" 制約を追加します。

### <a name="why-cant-countryregioncode-be-made-extensible-it-already-is"></a>CountryRegionCode を拡張可能にできないのはなぜですか? (*既にこのようになっています*)
- 要求: 拡張を通じて CountryRegionCode を変更可能にする。
- 問題: プラットフォーム更新 14 以降、CountryRegionCode への変更は、CountryRegionCode プロパティに値が既にある場合にサポートされます。 変更の制限が厳しくなり (要素は一部の国/地域でのみ利用可能になりました)、重大な変更となる可能性があるため、空の CountryRegionCode プロパティを変更することはできません。
- 回避策: 要素が既に国/地域に固有の場合、既存の CountryRegionCode 拡張機能を使用します。

### <a name="why-cant-the-table-field-properties-allowedit-alloweditoncreate-mandatory-or-ignoreedtrelation-be-made-extensible"></a>テーブル フィールド プロパティ AllowEdit、AllowEditOnCreate、Mandatory、または IgnoreEDTRelation を拡張可能にできないのはなぜですか?
- リクエスト: テーブル フィールド プロパティ AllowEdit、AllowEditOnCreate、Mandatory、IgnoreEDTRelation を拡張機能経由で変更可能にします。
- 問題: テーブル フィールドで "編集を許可"、"作成時の編集を許可"、"必須"、"IgnoreEDTRelation" プロパティを変更できると、重大な変更が生じます。 編集を許可するフィールドを変更すると、フィールドの目的が変更されます。 フィールドの編集を許可しないと、既存の動作が遮断されることがあります。 関係を変更すると、その関係の当初の目的が中断され、重大な変更となります。 フィールドを必須にすると、既存の動作が中断される可能性があります。
- 対応策: 拡張機能経由で新しいテーブル フィールドを追加し、必要に応じてそれを制御します。

### <a name="why-cant-security-privileges-be-made-extensible"></a>セキュリティ権限を拡張可能にできないのはなぜですか?
- 要求: 拡張を通じてセキュリティ権限を変更可能にする。
- 問題: セキュリティ権限を変更できると、変更が分割される可能性があります。これはセキュリティ メタデータの最下位レベルであるためです。
- 対応策: 必要な場合は、新しいセキュリティ権限を作成し、それを使用します。
