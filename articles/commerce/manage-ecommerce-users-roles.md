---
title: E コマース ユーザーとロールの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトの作成環境へのアクセスをユーザーに許可する方法について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d4987a824b786401c41c6ae63c8486ce7eb0c5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995694"
---
# <a name="manage-e-commerce-users-and-roles"></a>E コマース ユーザーとロールの管理


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイトの作成環境へのアクセスをユーザーに許可する方法について説明します。

ユーザーのアクセスを制御し、特定のタスクを実行するためのアクセス許可をユーザーに付与するために、サイトの作成環境では、Microsoft Azure Active Directory (Azure AD) で作成したセキュリティ グループを使用します。 最初に、Azure AD の新規または既存のセキュリティ グループを作成環境の各ロールに割り当てます。 その後、個々のユーザーを適切なセキュリティ グループに追加するか、そこから削除することにより、個々のユーザーにアクセス許可を付与または削除することができます。

## <a name="overview-of-roles-in-the-authoring-environment"></a>作成環境でのロールの概要

Dynamics 365 for Commerce 作成環境では、次のロールがサポートされています。

| 役割                 | 説明 |
|----------------------|-------------|
| システム管理者 | このロールを持つユーザーには、すべてのツール、および評価とレビューに対する権限が与えられます。 また、サイトを作成することもできます。 |
| 管理者   | このロールを持つユーザーは、特定のサイト構造内のすべてのツールおよび RnR に対する権限が与えられます。 |
| Web プロデューサー         | このロールを持つユーザーは、ページ、フラグメント、テンプレートを作成し、資産をアップロードおよび管理し、製品とカテゴリを拡充することができます。 |
| リーダー               | このロールを持つユーザーは、ページ、テンプレート、資産、フラグメント、レイアウト、および設定を表示できますが、変更することはできません。 |
| RnR モデレーター        | このロールを持つユーザーは、製品レビューを管理することができます。 |

## <a name="system-administrator-role"></a>システム管理者ロール

Microsoft Dynamics Lifecycle Services (LCS) 環境で Dynamics 365 Commerce をプロビジョニングする場合、**システム管理者** ロールのセキュリティ グループを提供するよう求められます。 このロールは、構成している環境で作成したすべてのサイトに自動的に適用されます。 このロールのセキュリティ グループは、LCS でのみ更新できます。 すべてのサイトの **サイトの管理** ページで読み取り専用として表示され、情報提供のみを目的としています。

## <a name="administrator-role"></a>管理者ロール

コマースで新しいサイトを作成すると、**管理者** ロールのセキュリティ グループを提供するように求められます。 このロールが付与するアクセス許可の概要については、このトピックの前の部分で示した表を参照してください。

## <a name="add-or-update-security-groups"></a>セキュリティグループの追加または更新

サイトの作成後、**システム管理者** および **管理者** のロールに関連付けられているセキュリティ グループ内のユーザーのみが、そのサイトの作成環境にアクセスできます。 ユーザーを **Web プロデューサー**、**RnR モデレーター**、および **リーダー** のロールに割り当てるには、これらのロールにセキュリティ グループを割り当てる必要があります。 セキュリティ グループをロールに追加したり、ロールに現在割り当てられているセキュリティ グループを更新したりするには、次の手順を実行します。

1. 更新するサイトに移動します。
1. **サイト管理** で、**セキュリティ** ページを開きます。
1. 変更するロールを選択します。
1. セキュリティ グループをロールに追加するか、ロールからセキュリティ グループを削除します。

## <a name="additional-resources"></a>追加リソース

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[サイトにおける検索エンジン最適化 (SEO) の考慮事項](search-engine-optimization-considerations.md)

[コンテンツ セキュリティ ポリシー (CSP) の管理](manage-csp.md)
