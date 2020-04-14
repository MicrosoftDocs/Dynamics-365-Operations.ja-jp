---
title: ソリューションの認識に関する問題のトラブルシューティング
description: このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172624"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>ソリューションの認識に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、 ソリューションの認識に関する問題の修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="error-on-the-dual-write-page"></a>デュアル書き込みのページでエラーが発生する

**デュアル書き込み**ページでは、次のようなエラーメッセージが表示される場合があります。

*MetadataCache で 'msdyn\_dualwriteentitymap' with namemapping='Logical という名称のエンティティが見つかりませんでした。*

この問題を修正するには、Common Data Service にデュアル書き込みのコアソ リューションがインストールされていることを確認してください。 デュアル書き込みのコア ソリューションは、ソリューションを認識するにあたって必須となります。
