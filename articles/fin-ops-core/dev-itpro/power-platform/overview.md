---
title: Finance and Operations アプリと Microsoft Power Platform の統合
description: このトピックでは Microsoft Dataverse および Finance and Operations アプリ の Microsoft Dynamics Lifecycle Services を介して Microsoft Power Platform の統合の概要を提供します。
author: Sunil-Garg
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: f64a15ded77bc1a157253c25135db8ab565f2548
ms.sourcegitcommit: ef3e0f5d44df7ed60bc1263ca44f09d4080333a5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2021
ms.locfileid: "7746669"
---
# <a name="microsoft-power-platform-integration-with-finance-and-operations-apps"></a>Finance and Operations アプリと Microsoft Power Platform の統合

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Power Platform は、Power Platform 管理者センターを介した Dynamics 365 アプリケーションの一連の機能を提供します。 今日、Finance and Operations アプリは Power Platform 管理者センターで管理されていません。 ただし、時間の経過とともに、Microsoft Dynamics Lifecycle Services (LCS) から管理センターに移行される管理機能がますます増えています。 暫定的に、顧客は、LCS の Microsoft Power Platform 統合機能を介して、二重書き込み機能、仮想エンティティ、アドインなどの機能のロックを解除できるようになります。

## <a name="prerequisite-reading"></a>前提条件の参照先

Microsoft Power Platform、Dataverse、二重書き込み、および Finance and Operations アプリの仮想エンティティのアーキテクチャを理解するには、それらのしくみを理解しておく必要があります。 したがって、次のドキュメントが前提条件になります。

- [Power Platform の管理](/power-platform/admin/admin-documentation)
- [Dataverse とは](/powerapps/maker/common-data-service/data-platform-intro)
- [Dataverse のテーブル](/powerapps/maker/common-data-service/entity-overview)
- [エンティティの関連付けの概要](/powerapps/maker/common-data-service/relationships-overview)
- [外部データ ソースのデータを含む仮想テーブルの作成と編集](/powerapps/maker/common-data-service/create-edit-virtual-entities)
- [Power Apps ポータルについて](/powerapps/maker/portals/overview)
- [Power Apps でのアプリの作成の概要](/powerapps/maker/)

## <a name="tools-and-services-unlocked-with-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合によってロックが解除されたツールとサービス

同時に、仮想エンティティ、二重書き込み、ビジネス イベントおよびデータ イベントは、Finance and Operations アプリと Dataverse プラットフォームの収束性に対する共有データ レイヤーを構成しています。 これらは、一緒に仕様することを目的とした補完的なテクノロジです。 

**仮想エンティティ** により、Microsoft Power Platform または Dataverse ネイティブ アプリから Finance and Operations データへのアクセスが必要になるシナリオが有効になります。 そのデータをクエリしてフォームをバインドし、一般的には、Finance and Operations アプリの全機能に対して Microsoft Power Platform の完全な機能を使用することができます。 システム間でデータはコピーされません。 代わりに、Microsoft Power Platform テクノロジが既にバインドすることができる標準の仮想エンティティ インフラストラクチャを通して直接アクセスします。 詳細については、[仮想エンティティの概要](virtual-entities-overview.md)を参照してください。 

**ビジネス イベント** により、Microsoft Power Platform を使用して Finance and Operations アプリで発生するイベントに応答できます。 これらのイベントは、ビジネス ロジックを使用してアプリケーションでプロセスを実行するときに発生します。 ビジネス イベントは、Finance and Operations アプリを含め、任意のアプリから発生させることができ、Microsoft Power Platform ビジネス ロジックによって処理することができます。 多くの場合、この処理には、ネイティブ エンティティまたは仮想エンティティを通じた追加データのクエリや操作が含まれます。 

**データ イベント** は、ビジネス イベントと同様に、イベントが発生した場合に外部アプリケーションが Finance and Operations アプリケーションから通知を受信できます。 データ イベントは、アプリケーション データのレコードに変更がある場合に発生します。 外部システムは、データ内で作成、更新、または削除 (CUD) の操作が行われると、通知に反応できます。

シナリオのサブセットについては、Finance and Operations アプリと Dataverse ネイティブ エンティティの間でデータを物理的にコピーする必要があります。 これらのシナリオは、Dataverse ネイティブ アプリと Finance and Operations アプリの両方でバインドされた大量のロジックを持つ重複するエンティティを対象としているので、データを各タイプのアプリのローカル データベースに配置する必要があります。 これらのエンティティの数は比較的少ないがが、アカウント/顧客、会社、製品、および販売注文などの最も重要なエンティティの一部が含まれます。 これらのシナリオでは、**二重書き込み** により、ほぼリアルタイムの同期コピーが可能になります。 この機能により、既存のアプリはローカル データに対する操作を設計通りに継続することができ、また対応する重複エンティティが同期されていることを確認することができます。詳細については、[二重書き込みのホームページ](../data-entities/dual-write/dual-write-home-page.md)を参照してください。 

同時に、仮想エンティティ、二重書き込み、ビジネス イベントおよびデータ イベントにより、Finance and Operations アプリと ネイティブ Dataverse アプリ間の境界をまたぐアプリと業務プロセスをビルドすることができます。 ほとんどのアプリと業務プロセスでは、これら共有データ レイヤーの 3 つの部分の組み合わせかすべてのいずれかが使用されます。 同様に、拡張機能およびカスタマイズにおいて、データベース間でコピーされるデータ量を可能な限り減少させる必要があり、これらのツールを使用する際に、最も有利なユーザー エクスペリエンス用に最適化する必要もあります。 

### <a name="add-ins-functionality"></a>アドイン機能

アドインを使用すると、Finance and Operations アプリの機能を拡張できます。 すべてのアドインは、サンドボックスおよび実稼働タイプの環境の環境詳細ページの Lifecycle Services を介してインストールされ、管理されます。 インストールされているアドインと各アドインの構成オプションに関するメタデータは、Microsoft Power Platform 統合の一部としてプロビジョニングされている Microsoft Dataverse データベースに格納されます。 一部のアドインは、Dataverse データベースにビジネス データも格納します。 使用可能なアドインの詳細については、[アドインの概要](add-ins-overview.md) を参照してください。

## <a name="typical-scenarios-and-patterns-that-use-dual-write"></a>二重書き込みを使用する一般的なシナリオとパターン

二重書き込みを使用する一般的なシナリオを次に示します。

### <a name="customer-service-representatives-can-facilitate-a-change-of-address-for-finance-and-operations-customers"></a>顧客サービス担当者が Finance and Operations の顧客の住所変更を容易にできるようにする

顧客が移転し、請求先住所と送付先住所の情報を変更したいとします。 この顧客は、顧客サービス担当者に連絡して、住所の変更を依頼します。 顧客サービス担当者が電話を受け、顧客の請求先住所と送付先住所を変更します。

| 意思決定 | 情報 | 
|----------|-------------|
| リアルタイムな日付が必要ですか。 | あり |
| ピーク データ量 | 適用できません |
| 頻度 | アドホック |

#### <a name="recommended-solution"></a>推奨される解決策

ほぼリアルタイムのデータ同期が関係するシナリオでは、二重書き込みで実装するのが最適です。

1. 顧客情報は、Finance and Operations アプリから取得されます。
2. 顧客が顧客サービスに電話し、請求先住所と送付先住所の情報を変更するよう依頼します。
3. 顧客サービス担当者は、Dynamics 365 Customer Service の顧客レコードを取得します。
4. 顧客サービス担当者は、請求先住所と送付先住所を更新してデータを保存します。
5. 新しい請求先住所と送付先住所は、リアルタイムで Finance and Operations アプリに同期されます。

### <a name="sales-representatives-can-change-customer-credit-limits-without-signing-in-to-a-finance-and-operations-app"></a>販売担当者は、Finance and Operations アプリにサインインすることなく、顧客の与信限度額を変更できます

顧客には $2,000 の与信限度額があり、$5,000 に引き上げたいと考えています。 この顧客が電話をかけて、増額を要求します。 チケットが、販売部門に割り当てられます。 販売責任者は依頼を検討し、顧客の支払履歴を確認し、顧客が与信限度額の増加の資格があると判断します。 販売責任者は依頼を承認し、チケットに応答します。 顧客は与信限度額 $5,000 の承認に関する電子メールを受け取ります。

| 意思決定 | 情報 | 
|---------|--------------|
| リアルタイムな日付が必要ですか。 | あり |
| ピーク データ量 | 適用できません |
| 頻度 | アドホック |

#### <a name="recommended-solution"></a>推奨される解決策

このシナリオでは、二重書き込みを使用して実装するのが最適です。

1. 顧客は電話し、与信限度額を $2,000 から $5,000 に引き上げたいと考えています。
2. 顧客サポート担当者が Dynamics 365 Customer Service でチケットを作成します。
3. チケットが、販売部門に割り当てられます。
4. 販売部門の販売担当者が依頼を確認して、承認します。
5. Dynamics 365 Sales で顧客の与信限度額が $5,000 に増額されます。
6. Finance and Operations アプリの与信限度額が $5,000 に更新されます。
7. 販売担当者は、チケットに応答して解決します。
8. 顧客は、与信限度額の引き上げに関する電子メールを受け取ります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
