---
title: "Microsoft Dynamics AX 2012 を使用して個人データ要求に対応"
description: "このトピックは、Microsoft Dynamics AX 2012 を使用する企業、実装パートナー、および独立系ソフトウェア ベンダー (ISV) が、EUデータ保護規則 (GDPR) の下にある個人データに関する、データ主体からの要求に適合するのに役立つことができます。"
author: ryanc
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: rschloma
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: ryanc
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f2e3a40f58b57785079e1940b2d24a3598a3ad1b
ms.openlocfilehash: 08af1e8565f8bb794be976cc680287dd737ab234
ms.contentlocale: ja-jp
ms.lasthandoff: 07/09/2018

---


# <a name="respond-to-a-request-for-personal-data-using-microsoft-dynamics-ax-2012"></a>Microsoft Dynamics AX 2012 を使用して個人データ要求に対応

[!include [banner](../includes/banner.md)]

このトピックは、Microsoft Dynamics AX 2012 を使用する企業、実装パートナー、および独立系ソフトウェア ベンダー (ISV) が、EUデータ保護規則 (GDPR) の下にある個人データに関する、データ主体からの要求に適合するのに役立つことができます。 GDPR および Microsoft が提供する関連するリソースの詳細については、[Microsoft Dynamics 365 for Finance and Operation の GDPR に関するガイド](./gdpr-guide.md) を参照してください。 「GDPR for Finance and Operation へのガイド」は、 Microsoft Dynamics 365 for Finance and Operations のために書かれたものですが、Dynamics AX 2012 を使用している組織に GDPR の下でデータ主体の権利が適用されます。 「Finance and Operations の GDPR に関するガイド」に記載されている手順は、個人データの要求に応答する組織により使用され、Dynamics AX 2012 を使用する組織にも適していますが、Dynamics AX 2012 では**人物検索**レポートを利用できません。 このトピックでは、Dynamics AX 2012 に固有の追加項目を一覧表示します。 

## <a name="applicable-product-updates-for-dynamics-ax-2012"></a>Dynamics AX 2012 の適用製品更新プログラム

AX 2012 に固有の追加の製品更新と GDPR に関連する情報は、[Microsoft Dynamics Lifecycle Services](https://fix.lcs.dynamics.com/Issue/Results?q=3909273) (LCS) から入手できます。 LCS へのアクセスには、サインインが必要です。 

次に示す、AX 2012 で使用可能な照会およびレポートのいくつかの例は、個人データを検索およびレポートするのに役立ちます。

+ **ホーム** &gt; **一般的な** &gt; **グローバル アドレス帳**

    照会ウィンドウで、検索ボックスに担当者の名前を入力します。

+ **買掛金勘定**&gt;**共通**&gt;**仕入先**&gt;**すべての仕入先**
+ **売掛金勘定**&gt;**共通**&gt;**顧客**&gt;**すべての顧客**
+ **人事管理** &gt; **共通** &gt; **作業者**
+ **販売とマーケティング** &gt; **共通** > **顧客**、**見込顧客**、**潜在顧客**、または **連絡先**

## <a name="additional-resources"></a>その他のリソース
GDPR の詳細については、[欧州連合の Web サイト](http://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。

### <a name="disclaimer"></a>免責事項
(c)2018 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。

