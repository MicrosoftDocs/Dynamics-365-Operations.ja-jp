---
title: 仮想エンティティの概要
description: このトピックでは、Finance and Operations アプリの仮想エンティティに関する一般情報を提供します。
author: RamaKrishnamoorthy
ms.date: 05/14/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2021-05-31
ms.openlocfilehash: ffe3a72eaa9267ae164a5ed5b02ef438aa85ee2d
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384525"
---
# <a name="virtual-entities-overview"></a>仮想エンティティの概要

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能には、バージョン 10.0.12 の Finance and Operations アプリ、および Microsoft Dataverse のサービス更新プログラム 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

## <a name="virtual-entities-for-finance-and-operations-apps"></a>Finance and Operations アプリの仮想エンティティ

Finance and Operations アプリは、Dataverse の仮想データ ソースであり、Dataverse および Microsoft Power Platform からの完全な作成、読み取り、更新、削除 (CRUD) 操作を可能にし ます。 定義上、仮想エンティティのデータは、Dataverse には存在しません。 その代わりに、属しているアプリで引き続き存在します。 Dataverse から Finance and Operations エンティティに対して CRUD 操作を実行する前に 、エンティティを Dataverse の仮想エンティティとして使用できるようにする必要があります。 これにより、Finance and Operations アプリに存在するデータに対して、Dataverse と Microsoft Power Platform から CRUD 処理を実行できるようになります。

Finance and Operations アプリ内のすべての Open Data Protocol (OData) エンティティは、Dataverse の仮想エンティティとして使用でき、したがって Microsoft Power Platform でも使用できます。 これで、作成者は Finance and Operations アプリからデータを直接使用して、Cuntomer Engagement アプリでエクスペリエンスを構築できます。 これらのエクスペリエンスは完全な CRUD 機能をオファーしており、Dataverse へのコピーを要求しません。 Power Apps ポータルは、Finance and Operations アプリで業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトを構築するために使用できます。

## <a name="virtual-entities-for-core-human-resources"></a>Core Human Resources の仮想エンティティ

Core Human Resources エンティティは、Finance and Operations エンティティが行うのと同じように仮想化することもできます。 詳細については、[Dataverse 仮想テーブルのコンフィギュレーション](../../../human-resources/hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。

## <a name="architecture"></a>アーキテクチャ

仮想エンティティは、Finance and Operations アプリ以外にも有用な Dataverse の概念です。 次の図は、仮想エンティティの Finance and Operations プロバイダーを実装する方法を示しています。 6 つの主要メソッドがプロバイダーによって実装されます。 最初の 5 つのメソッドは、**Create**、**Update**、**Delete**、**Retrieve**、**RetrieveMultiple** という標準的な CRUD 操作です。 最後のメソッドである **PerformAction** は、このトピックで後述するように OData アクションを呼び出すために使用されます。 Finance and Operations 仮想エンティティ データ プロバイダー (図では 「仮想エンティティ プラグイン」 と表示) を呼び出すと、Finance and Operations アプリの CDSVirtualEntityService Web API エンドポイントに対して Secure Sockets Layer (SSL)/トランスポート層セキュリティ (TLS) 1.2 セキュア Web 呼び出しが行われます。 その後、この Web サービスは、クエリを Finance and Operations アプリ内の関連する物理エンティティへの呼び出しに変換し、それらのエンティティで CRUD 操作または OData 操作を呼び出します。 Finance and Operations エンティティはすべての操作で直接呼び出されるため、エンティティまたはバッキング テーブルのビジネス ロジックも呼び出されます。

![Finance and Operations アプリの仮想エンティティのアーキテクチャ。](media/image1.png)

呼び出し時、Dataverse から Finance and Operations アプリまで 2 つの変換点があります。 変換の最初のポイントは、エンティティの物理名などの概念を Finance and Operations エンティティ名に変換する VE プラグインにあります。 また、会社の参照などの既知の概念も変換されます。 Web サービス呼び出しでは、引き続き EntityCollection、Entity、および QueryExpression オブジェクトを使用して、実行される操作が表されます。このとき、VE プラグインから変換されたエンティティ名と概念が使用されます。 最後に、Finance and Operations アプリの CDSVirtualEntityAdapterService Web API によって、QueryExpression から QueryBuildDataSource およびその他の内部 Finance and Operations 言語構成要素への変換が完了します。

仮想エンティティの一部としての Dataverse および Finance and Operations アプリ間での呼び出しはすべて、コンフィギュレーションで指定されている Azure Active Directory (Azure AD) アプリケーションを使用して、サービス間 (S2S) 呼び出しとして実行されます。 このアプリケーションのユーザーは、CDSVirtualEntityAdapterService Web API とカタログ エンティティ CDSVirtualEntityListEntity に **のみ** アクセスできる必要があります。 これらの特権は、CDSVirtualEntityApplication という名前の、標準のセキュリティ ロールに含まれています。 S2S 呼び出し中に、アクションを呼び出す Dataverse のユーザーの ID が Dataverse により提供されます。 CDSVirtualEntityAdapterService Web API は、Finance and Operations アプリで関連したユーザーを検索し、そのユーザーのコンテキストでクエリを実行します。 したがって、S2S 呼び出しでは、すべての Finance and Operations エンティティに明示的にアクセスする必要はありません。 代わりに、データ アクセスを決定するには、アクションを呼び出すユーザーの特権が必要な場合があります。

> [!NOTE]
> 仮想エンティティの呼び出しの待機時間を最適化するために、同じ Azure リージョンに Finance and Operations アプリと Dataverse の両方を同一配置することをお勧めします。 Finance and Operations アプリと Dataverse を同一配置する場合、仮想エンティティの間接費は 1 回の呼び出しあたり 30 ミリ秒 (ms) 未満である予定です。

Power Apps ポータルでは、仮想エンティティにもアクセスできます。 Power Apps ポータル認証は連絡先レコードに基づいているため、連絡先レコードと Finance and Operations ユーザーの間のマッピングは Dataverse での dyn\_externalportalusermapping テーブルで管理されます。 このテーブルは、Dataverse の高度な特権を持つユーザーのみが編集でき、このユーザーは、Finance and Operations 仮想エンティティに対してポータル ユーザーが持つセキュリティ アクセスを制御する権限を持っています。 Power Apps ポータル アクセス用に設定されたすべての Finance and Operations ユーザーには、CDSVirtualEntityAuthorizedPortalUser セキュリティ ロールが割り当てられている必要があります。また、システム管理者またはセキュリティ管理者ロールを割り当てることはできません。 仮想エンティティに適用される Power Apps ポータル セキュリティ設定に関係なく、Finance and Operations アプリへの結果のクエリは常に関連付けられた Finance and Operations ユーザーとして実行され、そのユーザーのエンティティと行のセキュリティ設定に従います。 匿名ポータルのアクセスもサポートされます。 このタイプのアクセスとその実行方法については、[Power Apps ポータル参照](power-portal-reference.md)を参照してください。
