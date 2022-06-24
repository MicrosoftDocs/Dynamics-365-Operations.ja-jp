---
title: グローバル在庫会計ホーム ページ
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 用のグローバル在庫会計アドインのホーム ページについて解説します。
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 27470f302b91fa3fa22f47438fa0f936beb7e7d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846187"
---
# <a name="global-inventory-accounting-home-page"></a>グローバル在庫会計ホーム ページ

[!INCLUDE [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

国際的な組織は、当局からのローカルおよびグローバルの会計基準に準拠する必要性が高まっています。 在庫の評価は、コンプライアンスを保証する上で重要な役割を果たします。 Microsoft Dynamics 365 Supply Chain Management 用のグローバル在庫会計アドインは、組織 (特に国際的な組織) が複数の原価元帳を使用して在庫会計を行うことを可能にする包括的なソリューションを提供します。 したがって、それらの組織は複数の会計基準と内部管理会計とに同時に準拠できます。

グローバル在庫会計により、適切な評価方法 (標準原価、平均、または特定の ID) と、選択した会計通貨をインスタンスごとに適用することによって、複数の表現で在庫を考慮することができます。 グローバル在庫会計により、組織は多くの場合二重評価や二重通貨として参照される方法で、在庫明細書および補助元帳の値 (在庫残高および売却済商品の原価とも呼ばれます) を報告することができるようになります。

在庫会計は個別の元帳で行われます。 必要に応じて、組織内の各法人に対して複数のグローバル在庫会計元帳を作成できます。 したがって、複数の在庫表現を取得することができます。 法人内で転記されるドキュメントすべて (発注書、販売注文、移動オーダーなど) は、その法人に関連付けられているすべての原価元帳に計上されます。

グローバル在庫会計元帳は、次の要素の組み合わせによって定義されます。

- カレンダー
- 通貨
- 為替レート テーブル
- 規則

規則は、1 つ以上の元帳に関連付けることができる在庫会計ポリシーのコレクションです。 規則により、組織内で一連の共通のポリシーを共有できます。

## <a name="availability"></a>適用の対象

グローバル在庫会計は、現在、次の地理上の Azure リージョンで使用可能です。

- 米国
- ヨーロッパ
- 英国
- オーストラリア
- カナダ

他の地域からのアドインをインストールしようとすると、Microsoft Dynamics Lifecycle Services (LCS) は、ユーザーの地理的な地域はサポートされていないというメッセージを表示します。 グローバル在庫会計は、Supply Chain Management のオンプレミス配置をサポートしていません。

ここに記載されているサポート対象地域のいずれかでグローバル在庫会計を有効にする際に問題が発生した場合は、検証のために環境 ID を記載したメールメッセージを[グローバル在庫会計](mailto:GlobalInvAccount@microsoft.com)チームに送信してください。

## <a name="licensing"></a>ライセンス

グローバル在庫会計は、Supply Chain Management で使用可能な標準原価管理機能と共にライセンス供与されます。 グローバル在庫会計を使用するのに、追加のライセンスを購入する必要はありません。
