---
title: 原価会計分析の Power BI コンテンツのセキュリティ設定
description: この記事では、Microsoft Power BI で行レベルのセキュリティに原価会計のアクセス レベルのセキュリティを反映する方法を説明します。
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267935"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>原価会計分析の Power BI コンテンツのセキュリティ設定

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Power BI で行レベルのセキュリティに原価会計のアクセス レベルのセキュリティを反映する方法を説明します。 この機能により、ユーザーがアクセス権を持つ Power BI データのみが表示されるようになります。

## <a name="overview"></a>概要

**原価会計分析** Microsoft Power BI コンテンツは、Power BI 行レベルのセキュリティを使用してユーザーのアクセスを制限します。 セキュリティは、原価会計パラメーターで設定されたアクセス レベルの組織階層に基づきます。 **原価会計分析** Power BI コンテンツに関する詳細については、「[原価会計分析 Power BI コンテンツ](cost-accounting-analysis-content-pack.md)」を参照してください。

## <a name="setup"></a>セットアップ
Power BI にアクセス レベルのセキュリティを反映するには、Power BI コンテンツの所有者は、次の手順に従います。

> [!NOTE]
> **原価会計分析** Power BI コンテンツを公開するユーザーが自動的に所有者になります。 所有者のみが Power BI のセキュリティを設定できます。 また、所有者が PowerBI.com で他のユーザーを追加するまで、所有者以外は **原価会計分析** Power BI コンテンツ内のデータを参照することはできません。

1. Power BI に定義ファイルを公開します。
2. PowerBI.com にサインインします。
3. **原価会計分析** Power BI コンテンツのデータセットを検索します。
4. セキュリティ ページを開きます。

    ![セキュリティ ページを開く。](./media/CA-picture-1.png)

5. **原価オブジェクト コントローラー** ロールが既に作成されています。 原価会計のアクセス レベル組織階層の一部であるほかのメンバを追加します。

    ![メンバーの追加。](./media/CA-picture-2.png)

**原価オブジェクト コントローラー** ロールに追加されているユーザーには、原価会計のアクセス レベル組織階層の定義に従って、許可されたデータのみが表示されます。

> [!NOTE]
> 行レベル セキュリティは、Power BI から埋め込まれたタイルとレポートに適用されます。

## <a name="updating-security"></a>セキュリティの更新
原価会計のアクセス レベルのセキュリティに更新が行われ、それらの更新を Power BI に反映したい場合、**原価会計分析** Power BI コンテンツのエンティティ格納を更新する必要があります。 エンティティ格納の更新を完了後、PowerBI.com のコンポーネントを更新する必要があります。 エンティティ格納の更新方法の詳細については、[エンティティ格納と Power BI の統合](power-bi-integration-entity-store.md#update-entity-store) を参照してください。 **原価会計分析** Power BI コンテンツの所有者は、新しいユーザーに組織階層へのアクセスが許可された場合にもエンティティ格納の更新を行う必要があります。 また、所有者はその新たなユーザーを PowerBI.com の **原価オブジェクト コントローラー** ロールに追加して、行レベルのセキュリティが適用されるようにする必要があります。

## <a name="disabling-security"></a>セキュリティの無効化
ここでは、組織がデータ アクセスを制限すると想定します。 何らかの理由で、原価会計を実行する際にセキュリティ パラメーターが無効になっている場合は、所有者は代わりにユーザーを Power BI の **原価経理担当** ロールに追加する必要があります。 セキュリティを有効状態から無効状態に変更する場合は、**原価オブジェクト コントローラー** ロールからユーザーを削除することをお勧めします。 セキュリティを再び有効にする場合は、その逆を行ないます。 ユーザーは両方のロールに属することができます。 結合アクセスとは両方のロールの結合のことです。 **原価会計分析** Power BI コンテンツの場合、結合アクセスを持つユーザーには無制限のデータ アクセス権があります。 目標がアクセス権を制限することである場合は、ユーザーを **原価オブジェクト コントローラー** ロールのみに割り当てる必要があります。 これらの行レベルのセキュリティの更新はすぐに反映されます。 影響を受けるユーザーは自分のブラウザを更新する必要があります。

## <a name="additional-resources"></a>追加リソース
Power BI の行レベルのセキュリティの詳細については、「[Power BI のモデルでのセキュリティ管理](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)」を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
