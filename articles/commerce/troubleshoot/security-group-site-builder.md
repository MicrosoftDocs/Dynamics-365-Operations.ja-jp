---
title: 初期配置中に Commerce サイト ビルダーのセキュリティ グループを構成できない
description: この記事には、新しい eコマース テナントの初期配置中に、Microsoft Dynamics Lifecycle Services (LCS) で eコマース コンポーネントを作成するときに、Commerce サイト ビルダーの Microsoft Azure Active Directory (Azure AD) セキュリティ グループがオプションとして表示されない場合に役立つトラブルシューティング ガイドが含まれます。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 797df828df16547eb3aef1f9865a663281fb9224
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899018"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>初期配置中に Commerce サイト ビルダーのセキュリティ グループを構成できない

[!include [banner](../../includes/banner.md)]

この記事には、新しい eコマース テナントの初期配置中に、Microsoft Dynamics Lifecycle Services (LCS) で eコマース コンポーネントを作成するときに、Commerce サイト ビルダーの Microsoft Azure Active Directory (Azure AD) セキュリティ グループがオプションとして表示されない場合に役立つトラブルシューティング ガイドが含まれます。

## <a name="description"></a>説明

Commerce サイト ビルダー コンポーネントを含む新しい eコマース テナントを配置するプロセスの一部として eコマース コンポーネントを作成した場合、Azure AD セキュリティ グループはダイアログ ボックスにオプションとして表示されません。

## <a name="resolution"></a>解像度

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>正しいテナントのユーザーでの eコマース サイトのプロビジョニング

1. [Azure ポータル](https://portal.azure.com/) に移動します。
1. eコマース サイトの LCS プロジェクトがプロビジョニングされたテナントで、[Azure Active Directory を使用して基本グループを作成してメンバーを追加する](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) の手順に従ってください 。
1. [LCS](https://lcs.dynamics.com/) に移動し、作成した Azure AD セキュリティ グループと同じテナントを共有するアカウントを使用してサインインします。 このアカウントは、Azure AD セキュリティ グループを表示するためのアクセス権が必要です。
1. 設定手順を完了して、eコマース サイトを構成します。 eコマース コンポーネントをプロビジョニングすると、セキュリティ グループがダイアログ ボックスのオプションとして表示されるようになります。

> [!NOTE]
> ダイアログ ボックスのフィールドにセキュリティ グループの一覧が表示されるようにするには、作成した Azure AD セキュリティ グループの名前を入力した後に **入力** を選択する必要があります。 検索結果には、ユーザーがアクセスできる、検索テキストで始まるすべての Azure AD セキュリティ グループが一覧表示されます。 より短い検索用語を使用して、より広範な検索結果を得ることができます。

## <a name="additional-resources"></a>追加リソース

[Azure Active Directory を使用して基本グループを作成してメンバーを追加する](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[新しい eコマース テナントの配置](../deploy-ecommerce-site.md)