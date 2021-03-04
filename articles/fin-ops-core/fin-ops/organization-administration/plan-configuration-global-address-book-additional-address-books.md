---
title: グローバル アドレス帳およびその他のアドレス帳の設定
description: このトピックでは、グローバル アドレス帳と追加のアドレス帳を設定しコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d83d6536d85100ef6a91e909be5a8e57e423371
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693933"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>グローバル アドレス帳およびその他のアドレス帳の計画

[!include [banner](../includes/banner.md)]

このトピックでは、グローバル アドレス帳と追加のアドレス帳を設定しコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。 決定の中には、組織階層など、製品の他の領域に対して行われている決定を確認する必要があります。

## <a name="global-address-book"></a>グローバル アドレス帳

グローバル アドレス帳の使用を開始する前に、その既定値を決定する必要があります。 これらの既定値は作成した追加のアドレス帳に使用されます。

**意思決定**

- どの順序で、名前を **個人** タイプの関係者レコードに表示しますか。 姓、ミドルネーム、名の順序など。
- ロール レコードが削除された場合、関係者レコードをアドレス帳から削除しますか。 たとえば、顧客レコードを削除する場合、関係者レコードも削除しますか。
- 新しいレコードを作成する場合、重複レコードがグローバル アドレス帳にあることをユーザーに通知しますか。
- 関係者レコードの情報にデータ普遍的の番号付けシステム (DUNS) 番号を含めますか。
- DUNS 番号が関係者レコードに含まれる場合、番号の独自性をチェックしますか。
- 関係者レコードをグローバル アドレス帳に作成する場合、既定の関係者タイプ、担当者、または組織は必要ですか。
- どのユーザー ロールが関係者レコードの個人住所および連絡先情報へのアクセス権を持ちますか。

## <a name="additional-address-books"></a>追加のアドレス帳

グローバル アドレス帳を作成すると、必要に応じて組織の各会社別または事業品目別のアドレス帳など追加のアドレス帳を作成できます。 たとえば、Fabrikam は、複数の会社と複数の事業品目を持つ国際組織です。 Fabrikam では、事業品目ごとにアドレス帳を作成しようとしています。 エアー ツール事業といった複数の場所にまたがる事業品目に対して、Fabrikam では場所ごとのアドレス帳の作成を計画します。 Fabrikam の IT マネージャーの Chris は、必要なアドレス帳の一覧を次のように作成しました。 この一覧には、各アドレス帳に含める必要がある関係者レコードについても記載しています。

- **公共部門契約 (PubSC)** – Fabrikam が結ぶ公共部門契約に関連するすべての関係者の関係者レコード。
- **民間部門契約 (PriSC)** – Fabrikam が結ぶ民間部門契約に関連するすべての関係者の関係者レコード。
- **電子ツール (ET)** – 電子ツールの購買または販売に関わるすべての関係者、または Fabrikam-Japan で Fabrikam による提供または Fabrikam のために購入する電子ツールに関係するすべての関係者の関係レコード。
- **エアー ツール (PTJPN)** – エアー ツールの購買または販売に関わるすべての関係者、または Fabrikam-Japan で Fabrikam による提供または Fabrikam のために購入するエアー ツールに関係するすべての関係者の関係レコード。
- **エアー ツール (PTUSA)** – エアー ツールの購買または販売に関わるすべての関係者、または Fabrikam-US で Fabrikam による提供または Fabrikam のために購入するエアー ツールに関係するすべての関係者の関係レコード。

**意思決定:**

- 追加のアドレス帳をいくつ作成しますか。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]