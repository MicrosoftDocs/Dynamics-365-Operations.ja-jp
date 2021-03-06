---
title: Power Apps ポータルと Finance and Operations
description: このトピックでは、Power Apps ポータルを Finance and Operations で使用する方法について説明します。
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
ms.openlocfilehash: 2e819a3134ccb62ad0a63b76bc72a1a3560ce091
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908686"
---
# <a name="power-apps-portals-with-finance-and-operations"></a>Power Apps ポータルと Finance and Operations

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Finance and Operations アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

Power Apps ポータルでは、Dataverse の仮想エンティティとして使用できる Finance and Operations エンティティに対して、作成、更新、および削除 (CRUD) 操作を行うことができます。 このトピックでは、Finance and Operations アプリの Power Apps ポータルに実装されているシナリオについて説明します。

## <a name="anonymous-access-from-power-apps-portals"></a>Power Apps ポータルからの匿名アクセス

Finance and Operations の入札やオンボードなどの業務プロセスのコラボレーション シナリオは、外部ユーザーが Finance and Operations アプリのユーザーではない場合でも、Power Apps ポータルからの参加を要求します。 匿名アクセスは、Finance and Operations アプリ ユーザーではないユーザーがログインしなくてもよいので、このような状況では匿名アクセスのシンプルさが魅力的です。 ただし、業務プロセス内の意味のあるタスクを完了するために、Finance and Operations で CRUD 処理を実行することが期待されます。

必要なエンティティのみが匿名アクセスに対して有効になるようにするには、Finance and Operations のユーザーが匿名アクセスに使用するユーザーとして指定されている必要があります。 この指定は、**システム パラメーター** ページ (**システム管理 \> システム パラメーター**) の **仮想エンティティ** タブにある **匿名ポータルのアクセス ユーザー ID** フィールドで構成します。 指定されたユーザーを職務とセキュリティ ロールに割り当てて、Power Portal から匿名でやりとりするすべてのユーザーが使用できるようにする必要がある特定のデータへのアクセスを制御することができます。

このシナリオには匿名アクセスが含まれるため、セキュリティの観点から、**匿名ポータルのアクセス ユーザー ID** フィールドで指定されているユーザーにのみ、重要なユーザー コンテキストがあります。

## <a name="authenticated-access-from-power-apps-portals"></a>Power Apps ポータルからの認証済みアクセス

Power Apps ポータルから Finance and Operations へのユーザーアクセスを完全に認証することによって、Finance and Operations のユーザーが Power Apps ポータルからも操作できるようにします。 Power Apps ポータルにサインインするユーザーは、作業要件に基づく適切なセキュリティ ロールを持つ Finance and Operations のユーザーであることもわかっています。 これらのロールは、Power Portal で認証されたユーザーのデータへのセキュリティ アクセスを制御します。 さらに、Power Apps も使用して Finance and Operations データにアクセスする予定の Finance and Operations ユーザーは、**CDSVirtualEntityAuthenticatedPortalUser** セキュリティ ロールにも属している必要があります。 これにより、追加のセキュリティ レベルが提供されるほか、Power Apps ポータルからのアクセス許可が与えられているユーザーの総数を把握することができます。 

Power Apps ポータル認証は Dataverse の連絡先エンティティにリンクされているため、Dataverse の連絡先と Finance and Operations の対応するユーザーの間にマッピングを確立する必要があります。 このマッピングは、エントリを **msdyn\_externalportalusermapping** エンティティに追加することによって実行できます。 セキュリティの観点から、認証されたユーザーが使用できる仮想エンティティの範囲は、Power Apps ポータルで **グローバル** としてコンフィギュレーションする必要があります。

別のテナントから認証されたユーザーをユーザーとして Finance and Operations に追加する必要がある場合、Finance and Operations で[新しいユーザーの作成](../sysadmin/tasks/create-new-users.md)プロセスを使用する必要があります。 このプロセスにより、Microsoft Azure Active Directory (Azure AD) 企業間 (B2B) ゲスト ユーザーとして、テナント間のユーザーが追加されます。

> [!NOTE]
> ユーザー (認証済または匿名) にいずれかの Finance and Operations アプリで、システム管理者ロールが割り当てられている場合、Power Apps ポータルからのアクセスは失敗します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]