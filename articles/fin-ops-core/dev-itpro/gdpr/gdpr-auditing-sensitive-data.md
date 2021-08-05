---
title: 機密データへのアクセスを管理
description: このトピックでは、ユーザー ログの機能に関する情報を提供します。
author: ToddLefor
ms.date: 12/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10031
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b752732e7836e24818b75793666f62dbc3b3d26
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360332"
---
# <a name="manage-access-to-sensitive-data"></a>機密データへのアクセスを管理

[!include [banner](../includes/banner.md)]

システム管理者は、**ユーザー ログ** ページを使用して、システムにログオンしたユーザーの監査ログを保持できます。 ログインしているユーザーを知ることは、組織のデータを保護するために役立ちます。 機密データへのアクセスを提供するロールを管理者が識別できるようにするために、ユーザーのログ機能を拡張しました。 

![顧客からのデータ フロー。](../media/gdpr-sensitive-data-1.jpg)

## <a name="what-is-sensitive-data"></a>機密データとは何ですか ?
組織は、ニーズにあった方法で *機密データ* を構成する要素を定義することができます。 一部の組織によっては、機密データが財務または人事データに関連付けられている任意のデータ、または個人のデータである単なるデータである可能性があります。 一部の業界や一部の国または地域には、組織自体が採用できる機密データのより詳細な定義がある場合があります。 機密データ識別子を使用するかどうか、およびその方法を決定するのは各組織次第です。 

機密データ識別子は、システム内で誰が機密データへのアクセス権を持っているかを示す監査ログを作成させることで、ユーザーのログ操作を向上させます。 この機能は、特定のデータへのアクセスの度合いが異なる複数のロールを持つ組織に役立ちます。 また、機密性の高いデータとして識別されているデータにアクセスしたユーザーを追跡する監査の詳細なレベルを必要とする組織でも役立ちます。

![機密データにアクセスできるロールを表示するユーザー ログ ページ。](../media/gdpr-sensitive-data-2.jpg)

## <a name="language-specific-information"></a>言語固有の情報
ユーザーログの役割情報は言語固有で、現在のユーザー言語と一致します。

![時間 ID を持つロール情報。](../media/gdpr-sensitive-data-3.jpg)

## <a name="log-retention"></a>ログの保持
機密データであると宣言されたデータにアクセスするユーザーのログ エントリは、ログ内の他のすべてのデータとは別に保持できます。 管理者は、**ユーザー ログのクリーンアップ** ページでオプションを設定して、この機能を有効にすることができます。

![ユーザー ログのクリーンアップ ページ。](../media/gdpr-sensitive-data-4.jpg)

>[!NOTE]
> この機能はバージョン 8.0 で使用することができます。 この機能は、Dynamics AX 2012 R3 (KB 4074643) で有効です。

## <a name="additional-resources"></a>追加リソース
GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。

### <a name="disclaimer"></a>免責事項
(c)2018 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]