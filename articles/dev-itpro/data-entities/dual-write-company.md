---
title: Common Data Service の企業概念
description: このトピックでは、Finance and Operations と Common Data Service 間の企業データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6eddd87c3ad3ea9de8aec2874b0514faa65374f1
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789214"
---
## <a name="company-concept-in-common-data-service"></a>Common Data Service の企業概念

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Microsoft Dynamics 365 for Finance and Operations では、*企業*の概念は、法的コンストラクトとビジネス コンストラクトの両方です。 また、データのセキュリティと可視性の境界でもあります。 ユーザーは常に単一の会社のコンテキストで作業し、データのほとんどは会社によってストライプされます。

Common Data Service は、同等の概念を持っていません。 最も近い概念は、主にユーザー データのセキュリティと可視性の境界である*事業単位*です。 この概念は、Finance and Operations の企業概念と同じ法的またはビジネス上の意味を持ちません。

事業単位と企業は同等の概念ではないため、Common Data Service 統合を目的として 1 対 1 (1:1) のマッピングを強制することはできません。 ただし、ユーザーは既定で Finance and Operations と Common Data Service にて同じレコードを表示する必要があるため、Microsoft では cdm\_ 企業、という名の Common Data Service に新しいエンティティが導入されています。 このエンティティは、Finance and Operations の企業エンティティと同等です。 レコードの可視性は Finance and Operations と Common Data Service 間ですぐに同等であることを保証するために、Common Data Service のデータに向けた次の設定をお勧めします。

+ デュアル書き込みが有効になっている Finance and Operations の企業レコードごとに、関連付けられた cdm\_ 企業レコードが作成されます。
+ cdm\_ 企業レコードが作成され、デュアル書き込みが有効になると、同じ名前の既定の事業単位が作成されます。 既定のチームは、その事業単位に対して自動的に作成されますが、事業単位は使用されません。
+ 同じ名前を持つ別の所有者チームが、作成されます。 また、事業単位にも関連付けられています。
+ 既定では、Finance and Operations で作成され、デュアル書き込み先のレコードの所有者 Common Data Service は、関連付けられた事業単位にリンクされている「DW 所有者」チームに設定されます。

次の図では、Common Data Service のデータ設定の例を示します。

![Common Data Service のデータ設定](media/dual-write-company-1.png)

この構成により、USMF 会社に関連する Finance and Operations レコードは、Common Data Serviceの USMF 事業単位にリンクされているチームによって所有されます。 したがって、事業単位レベルの可視性に設定されたセキュリティ ロールを通じて、その事業単位にアクセスできるユーザーは、これらのレコードを表示できるようになりました。 次の例は、チームを使用してこれらのレコードへの正しいアクセスを提供する方法を示しています。

+ 「営業マネージャー」のロールは、「USMF セールス」チームのメンバーに割り当てられます。
+ 「営業マネージャー」のロールを持つユーザーは、自分が所属する同じ事業単位のメンバーである任意の取引先企業レコードにアクセスできます。
+ 「USMF セールス」チームは、前述の USMF 事業単位にリンクされています。
+ したがって、「USMF セールス」チームのメンバーは、 Finance and Operations の USMF 会社エンティティから来た「USMF DW」ユーザーが所有するアカウントを確認できます。

![チームの使用方法](media/dual-write-company-2.png)

前の図に示すように、事業単位、企業、およびチーム間の 1:1 マッピングは、出発点に過ぎません。 この例では、新しい「ヨーロッパ」の事業単位が DEMF と ESMF の両方の Common Data Service にて手動で作成されます。 この新しいルートの事業単位は、デュアル書き込みとは無関係です。 ただし、関連するセキュリティー ロールの**親 / 子 BU** にデータの可視性を設定することにより、DEMF および ESMF の両方のアカウント データに対する「EUR 営業」チームのメンバーにアクセスできるよう使用できます。

最後に、デュアル書き込みによってどの所有者チームが決定されるかについて説明します。 この動作は、cdm\_ 企業レコードの**既定の所有チーム**フィールドによって制御されます。 cdm\_ 企業レコードがデュアル書き込みに対して有効になっている場合、プラグインは関連付けられた事業単位と所有者チームを自動的に作成し (存在しない場合)、**既定の所有チーム**フィールドを設定します。 管理者は、このフィールドを別の値に変更できます。 ただし、エンティティがデュアル書き込みを有効にしている限り、管理者はフィールドをクリアできません。

![既定の所有チーム フィールド](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>企業のストライピングとブートストラップ

Common Data Service 統合は、企業の識別子を使用してデータをストライプすることにより、企業パリティをもたらします。 次の図に示すように、すべての企業の固有エンティティは、cdm\_ 企業エンティティと多対1 (N:1) の関係を持つよう拡張されます。

![企業の固有エンティティと cdm_ 企業エンティティ間の N:1 関係](media/dual-write-bootstrapping.png)

+ レコードの場合、企業が追加および保存された後、値は読み取り専用になります。 したがって、ユーザーは正しい企業を選択する必要があります。
+ 企業データを持つレコードのみが、Finance and Operations と Common Data Service 間のデュアル書き込みの資格があります。
+ 既存の Common Data Service データによって、管理者主導のブートストラップ エクスペリエンスがまもなく利用可能になります。
