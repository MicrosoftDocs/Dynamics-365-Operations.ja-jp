---
title: 財務と運用を使用した Power Apps ポータル
description: この記事では、財務と運用と共に Power Apps ポータルを使用する方法について説明します。
author: Sunil-Garg
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 74fca54649e5be1980b13a143c6934fa36d99d7a
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108387"
---
# <a name="power-apps-portals-with-finance-and-operations"></a>財務と運用を使用した Power Apps ポータル

[!include[banner](../includes/banner.md)]



> [!IMPORTANT]
> この機能を使用するには、財務と運用アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新プログラム 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

Power Apps ポータルでは、Dataverse の仮想エンティティとして使用できる財務と運用エンティティに対して、作成、更新、および削除 (CRUD) 操作を行うことができます。 この記事では、財務と運用アプリの Power Apps ポータルに実装されているシナリオについて説明します。

## <a name="anonymous-access-from-power-apps-portals"></a>Power Apps ポータルからの匿名アクセス

財務と運用の入札やオンボードなどの業務プロセスのコラボレーション シナリオは、外部ユーザーが財務と運用アプリのユーザーではない場合でも、Power Apps ポータルからの参加を要求します。 ユーザーは財務と運用アプリ ユーザーでなくてもサインインする必要がないため、このようなシナリオでは匿名アクセスの簡便さが魅力的です。 ただし、業務プロセス内の意味のあるタスクを完了するために、財務と運用で CRUD 処理を実行することが期待されます。

必要なエンティティのみが匿名アクセスに対して有効にするには、財務と運用のユーザーが匿名アクセスに使用するユーザーとして指定されている必要があります。 この指定は、**システム パラメーター** ページ (**システム管理 \> システム パラメーター**) の **仮想エンティティ** タブにある **匿名ポータルのアクセス ユーザー ID** フィールドで構成します。 指定されたユーザーを職務とセキュリティ ロールに割り当てて、Power Portal から匿名でやりとりするすべてのユーザーが使用できるようにする必要がある特定のデータへのアクセスを制御することができます。

このシナリオには匿名アクセスが含まれるため、セキュリティの観点から、**匿名ポータルのアクセス ユーザー ID** フィールドで指定されているユーザーにのみ、重要なユーザー コンテキストがあります。

## <a name="authenticated-access-from-power-apps-portals"></a>Power Apps ポータルからの認証済みアクセス

Power Apps ポータルから財務と運用へのユーザーアクセスを完全に認証することによって、財務と運用のユーザーが Power Apps ポータルからも操作できるようにします。 Power Apps ポータルにサインインするユーザーは、作業要件に基づく適切なセキュリティ ロールを持つ財務と運用のユーザーであることもわかっています。 これらのロールは、Power Portal で認証されたユーザーのデータへのセキュリティ アクセスを制御します。 さらに、Power Apps ポータルも使用して財務と運用データにアクセスする予定の財務と運用ユーザーは、**CDSVirtualEntityAuthenticatedPortalUser** セキュリティ ロールにも属している必要があります。 これにより、追加のセキュリティ レベルが提供されるほか、Power Apps ポータルからのアクセス許可が与えられているユーザーの総数を把握することができます。 

Power Apps ポータル認証は Dataverse の連絡先エンティティにリンクされているため、Dataverse の連絡先と財務と運用の対応するユーザーの間にマッピングを確立する必要があります。 このマッピングは、エントリを **msdyn\_externalportalusermapping** エンティティに追加することによって実行できます。 セキュリティの観点から、認証されたユーザーが使用できる仮想エンティティの範囲は、Power Apps ポータルで **グローバル** としてコンフィギュレーションする必要があります。

別のテナントから認証されたユーザーをユーザーとして財務と運用に追加する必要がある場合、財務と運用で[新しいユーザーの作成](../sysadmin/tasks/create-new-users.md)プロセスを使用する必要があります。 このプロセスにより、Microsoft Azure Active Directory (Azure AD) 企業間 (B2B) ゲスト ユーザーとして、テナント間のユーザーが追加されます。

> [!NOTE]
> ユーザー (認証済または匿名) にいずれかの財務と運用アプリで、システム管理者ロールが割り当てられている場合、Power Apps ポータルからのアクセスは失敗します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
