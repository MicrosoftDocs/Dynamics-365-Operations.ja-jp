---
title: ソリューションの認識に関する問題のトラブルシューティング
description: この記事では、 ソリューションの認識に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871498"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>ソリューションの認識に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]





この記事では、財務と運用アプリと Dataverse 間のデュアル書き込み統合に関するトラブル シューティングの情報を提供します。 このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> この記事で説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="error-on-the-dual-write-page"></a>デュアル書き込みのページでエラーが発生する

**デュアル書き込み** ページでは、次のようなエラーメッセージが表示される場合があります。

*MetadataCache で 'msdyn\_dualwriteentitymap' with namemapping='Logical という名称のエンティティが見つかりませんでした。*

この問題を修正するには、Dataverse にデュアル書き込みのコアソ リューションがインストールされていることを確認してください。 デュアル書き込みのコア ソリューションは、ソリューションを認識するにあたって必須となります。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]