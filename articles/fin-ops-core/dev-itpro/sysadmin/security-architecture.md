---
title: セキュリティ アークテクチャ
description: この記事では、財務と運用のセキュリティ アーキテクチャの概要を示します。
author: Peakerbl
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecConfiguration, SysUserGroupInfo, SysSecRoleExcludeUsers
audience: IT Pro
ms.reviewer: sericks
ms.custom: 15441
ms.assetid: bea829b3-38ce-463c-a7e3-c9393b79d559
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4dc0bd1f30964a0d58caa413d9e89e1a142ea328
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108547"
---
# <a name="security-architecture"></a>セキュリティ アークテクチャ
[!include [banner](../includes/banner.md)]

この記事では、財務と運用のセキュリティ アーキテクチャの概要を示します。

セキュリティ アーキテクチャを理解すると、業務の要件に合わせてセキュリティを容易にカスタマイズできます。 次の図は、セキュリティ アーキテクチャの高レベルな概要を示しています。 

[![セキュリティ アークテクチャの概要を示す図。](./media/security-architecture.png)](./media/security-architecture.png)

## <a name="authentication"></a>認証
既定では、ユーザー権利を持つ認証済みユーザーのみが接続を確立できます。 

Microsoft Azure Active Directory (AAD) は主要な ID プロバイダーです。 システムにアクセスするには、ユーザーは財務と運用のインスタンスにプロビジョニングされ、認可されたテナントに有効な AAD アカウントが必要です。

## <a name="authorization"></a>認証
承認は、財務と運用アプリケーションへのアクセスをコントロールします。 セキュリティ アクセス許可は、プログラムの個々の要素へのアクセスを制御するために使用されます: メニュー、メニュー項目、アクションおよびコマンド ボタン、レポート、サービス操作、Web URL のメニュー項目、Web コントロール、および財務と運用のクライアントのフィールド。 

個別のセキュリティ アクセス許可は特権に、特権は職務に組み込まれています。 管理者は、セキュリティ ロールに職務権限と権限を割り当てることにより、これらのセキュリティ ロールへのアクセス許可をプログラムに付与します。 

コンテキスト ベースのセキュリティは、セキュリティ設定が可能なオブジェクトへのアクセスをコントロールします。 特権がエントリ ポイント (メニュー項目またはサービス操作など) に関連付けられているとき、**読み取り** または **削除** などのアクセス レベルが指定されます。 承認サブシステムは、そのエントリ ポイントにアクセスがあると実行時にアクセスを検出し、エントリ ポイントが導かれるセキュリティ保護可能なオブジェクトに指定したレベルのアクセスを適用します。 この機能は、過剰なアクセス権がないことを保証し、開発者が意図したアクセス権を得るのに役立ちます。 

詳細については、[ロールベース セキュリティ](role-based-security.md)を参照してください。

## <a name="data-security"></a>データ セキュリティ
承認はプログラムの要素へのアクセスを許可するために使用されます。 対照的に、データ セキュリティはデータベース内のテーブル、フィールド、および行へのアクセスを拒否するために使用されます。

拡張可能なデータ セキュリティ フレームワークを使用してセキュリティ ポリシーに基づいてテーブル レコードへのアクセスを制限することにより、ロールベースのセキュリティを補うことができます。 セキュリティ アクセス許可がユーザー ロールの一部である場合、ユーザーがデータにアクセスできる割合が高くなりますが、セキュリティ ポリシーによってデータへのアクセスが減少します。

詳細については、[拡張可能なデータ セキュリティ ポリシー](extensible-data-security-policies.md) を参照してください。

また、テーブル アクセス許可フレームワークは、一部のデータを保護するのに役立ちます。 特定のテーブルのデータ セキュリティは、Application Object Server (AOS) によって適用されます。

## <a name="auditing"></a>監査
ユーザー サインインとサインアウトの監査が有効になります。つまり、ユーザーがアプリケーションからサインインまたはサインアウトするときにシステムに記録されることを意味します。 ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。

システム管理者またはセキュリティー管理者は、**ユーザー ログ** ページ (**システム管理** > **照会** > **ユーザー ログ**) に移動して監査ログにアクセスできます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
