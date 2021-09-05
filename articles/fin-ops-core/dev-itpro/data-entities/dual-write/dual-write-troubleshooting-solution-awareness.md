---
title: ソリューションの認識に関する問題のトラブルシューティング
description: このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b53e07f69992a567d5b300ae1f2b24b74541d176
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416355"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>ソリューションの認識に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="error-on-the-dual-write-page"></a>デュアル書き込みのページでエラーが発生する

**デュアル書き込み** ページでは、次のようなエラーメッセージが表示される場合があります。

*MetadataCache で 'msdyn\_dualwriteentitymap' with namemapping='Logical という名称のエンティティが見つかりませんでした。*

この問題を修正するには、Dataverse にデュアル書き込みのコアソ リューションがインストールされていることを確認してください。 デュアル書き込みのコア ソリューションは、ソリューションを認識するにあたって必須となります。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]