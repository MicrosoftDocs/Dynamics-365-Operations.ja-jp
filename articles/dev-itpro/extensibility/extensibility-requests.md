---
title: "拡張機能の要求"
description: "このトピックでは、Dynamics 365 for Finance and Operations で追加の拡張ポイントを要求する方法について説明します。"
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 2fa0b0790f22bc9c9cd009e5f88f767c3429a3d1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="extensibility-requests"></a>拡張機能の要求

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は拡張機能を排他的に使用して、製品をカスタマイズします。 この変更はパートナーのエコシステム全体に影響することを知っています。 [拡張性のホーム ページ](extensibility-home-page.md)に記載されているリソースを読むことをお勧めします。 これらのリソースは多くの質問に答え、拡張機能を使用してソリューションを構築するための準備を整えます。

拡張機能では、オーバーレイによって可能であったいくつかのカスタマイズが実行できないことが見つかります。 オーバーレイすることなく同じビジネス要件を可能にするために、多くの拡張機能を追加しており、今後さらに追加する予定です。 オーバーレイにより実行された一部のカスタマイズについては、ログ要求をして、顧客の必要に気付けるようにする必要があります。

## <a name="what-we-are-doing"></a>実行する内容
しばらくの間、拡張ベースのカスタマイズ モデルに向けて取り組みます。 過去のいくつかのリリースにわたって、段階的にモデルが封印されてきました。 Dynamics 365 for Finance and Operations リリース 8.0 以降、これでシールが完了しました。 このリリースより後は、拡張ベースのカスタマイズのみが許可されます。 

今後のリリースでは、より多くの拡張機能を追加して、独立系ソフトウェア ベンダー (ISV) と付加価値再販業者 (VAR) が包括的なビジネス ソリューションを提供できるようにします。 顧客ごとに公開の頻度に応じてこれらに優先順位を付けます。

## <a name="how-do-i-log-extensibility-requests"></a>拡張機能の要求を記録するにはどうすればよいですか。
拡張子として実装することができないカスタマイズが見つかった場合は、シナリオに対して適切な拡張子サポートが製品に追加されるように Microsoft にリクエストを記録する必要があります。

要求を記録する前に、考慮すべき点がいくつかあります。  
- 既存の拡張性機能を満たす必要がありますか。 拡張機能を備えたソリューションを構築するには、異なる設計および実装パターンが必要です。
- 顧客またはビジネス アナリストへの要求はどれほど重要ですか。  
- 実装のアップグレードは長期間利用しやすいですか。

高度なロードマップ情報を本質的に共有しているため、秘密保持契約の下にある組織はフィードバック コミュニティに登録する必要があります。

パートナーは、従業員ごとにではなく一度だけフィードバック コミュニティに参加する必要があります。 フィードバック コミュニティに登録するには。

1. [組織のプロファイル情報を提供します。](http://aka.ms/feedbackcommunitynomination)
2. [NDA に署名し、契約書、コード、およびデータ共有ポリシーを入力します。](http://aka.ms/feedbackcommunityagreement)

パートナーとして、契約書に署名した後、組織内のユーザーは Yammer グループのフィードバックにアクセスすることができます。 さまざまな拡張性のテーマについて検討している「オペレーションの拡張性」の Yammer グループに参加することをお勧めします。

> [!IMPORTANT]
> 今後のリリースで、拡張機能の要求が Lifecycle Services (LCS) 経由で送信できるようになります。 しばらくは、daxcf@microsoft.com まで要求を送信してください。

拡張機能の要求を記録するときは、拡張機能を有効にする必要がある対象に関する詳細情報を入力し、拡張を必要とする内容に関する情報を含めます。 これはマイクロソフトがお客様の要求に効率的に対処するのに役立ちます。 ニーズに効果的に取り組み、ユーザーが必要とする機能を標準アプリケーションで有効にする仕方を Microsoft に提案してください。

> [!NOTE]
> 拡張性の要求を修正プログラムとしてリリースしません。  

拡張性要求は、Dynamics 365 for Finance and Operations のみために排他的です。 Dynamics AX 2012 またはそれ以前のリリースの拡張機能の要求に対応する計画はありません。

## <a name="when-will-my-extensibility-requests-be-enabled"></a>個人の拡張機能の要求はいつ有効になりますか。

拡張性要求は、バックログに記録されます。 Microsoft エンジニアは、すべての要求に優先度付けを行ってから、優先順位で作業します。 Microsoft はすべての要求が処理されることを確証できないことに注意してください。 特に、本質的に煩雑な要求はシームレスなアップグレードを妨げるためサポートされません。

## <a name="how-will-extensibility-requests-be-made-available-to-deploy"></a>拡張機能の要求を展開するにはどうすればよいですか。
Dynamics 365 for Finance and Operations リリース 8.0 の後、新しい機能拡張の要求で頻繁にアプリケーション更新をリリースする予定です。 これは、プラットフォームの更新プログラムと同じリリース ケイデンスに従います。 

## <a name="still-have-questions"></a>疑問が解決されない場合

[拡張性についてよく寄せられる質問](app-sealing-faq.md)と[拡張機能のホーム ページ](extensibility-home-page.md)にリストされた他のリソースをご覧ください。

