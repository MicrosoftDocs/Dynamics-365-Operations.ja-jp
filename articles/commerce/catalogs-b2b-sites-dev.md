---
title: B2B カスタマイズ のためのコマース カタログの拡張性への影響
description: このトピックでは、Microsoft Dynamics 365 Commerce の B2B 機能のコマース カタログの拡張性への影響について説明します。
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: aff333bfe8003233dd5d8181aa8c5dd7eaeffcd0
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656868"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>B2B カスタマイズ のためのコマース カタログの拡張性への影響

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の **B2B のコマース カタログ** 機能の拡張性への影響について説明します。

カタログ コンテキストをカスタム シナリオに拡張することに関心を持っている場合は、カスタマイズを更新する必要があります。 この更新は、アップグレードの実行後にカスタマイズが最新の機能を自動的にサポートしない可能性があるため、顧客が従う必要のある標準プロセスに従います。 カスタマイズに新しい機能やバグ修正プログラムが含まれる場合は、それ経験に応じてカスタマイズ コードを更新することをお勧めします。 この更新は、Microsoft がコア コードに対して行った可能性のある変更に似ています。

以下のカスタマイズ ケースを確認して、カスタマイズを更新する必要があるかどうかを判断します。

> [!NOTE]
> - すべての販売促進アプリケーション プログラミング インターフェイス (APIs) は、カタログに対応している必要があります。 したがって、**CatalogID** パラメーターを渡すことが重要です。
> - 既定のカタログ (**CatalogID**=**0**) は、サインインした企業間 (B2B) ユーザーの有効なカタログではありません。 したがって、サイト ユーザーはカタログ 0 にアクセスできないため、「0」を渡すか既定値を使用するすべての API 呼び出しは失敗します。 正しいエクスペリエンスを得るには、カタログ ピッカーで選択されたカタログ ID を渡すように、カスタマー API 呼び出しを更新する必要があります。 既定値を使用し、ユーザーがカタログを切り替える場合、Web サイトは選択したカタログのデータを提供する必要があります。 したがって、コア コマース コードから実行される API と一致させるには、カスタマイズされた API が選択されたカタログを渡す必要があります。

次のカスタマイズ ケースでは、開発の更新が必要です。

- **ケース 1:** 顧客が製品関連 API またはデータ アクションを呼び出す独自の[データ アクション](e-commerce-extensibility/data-actions.md) を紹介します。 次の更新手順が必要です。

    1. データ アクションで直接 API 呼び出しを使用する場合は、次の例に示すように、データ アクションを更新して、カタログ ID を渡すようにします。

        ![カタログ ID を渡す更新されたデータ アクション。](./media/customization1_a.png)

    1. データ アクションがカスタマイズ内で別の製品関連のデータ アクションを呼び出す場合は、**requestContext** などの新しいパラメーターを渡すようにコードを更新する必要があります。 次の例に示すように、**requestContext** パラメーターは、現在のカタログ ID を取得するために使用されます。

        ![新しいパラメーターを渡す更新されたデータ アクション。](./media/customization1_b.png)

- **ケース 2 :** 顧客には、[上書きされたデータ アクション](e-commerce-extensibility/data-action-overrides.md) があります。 次の更新手順が必要です。

    - ケース 1 のデータ アクションを更新します。

- **ケース 3:** 顧客には、API またはデータ アクションの呼び出しが含まれるビュー拡張機能、スクリプトの挿入モジュール、または[クローン モジュール](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) があります。 次の更新手順が必要です。

    - 次の例に示すように、ケース 1 のコードを更新します。

       ![新しいパラメーターを渡す更新されたコード。](./media/customization3.png)

- **ケース 4:** 顧客は **getById** API 呼び出しを使用します。 次の更新手順が必要です。

    - **getById** APT 呼び出しにはいくつかの制限があり、カタログ認識をサポートしていないため、代わりに **getByIds** API 呼び出しに切り替えます。

- **ケース 5:** 顧客には、異なるカタログからの可能性がある複数の製品の情報を取得するデータ アクションがあります。 次の更新手順が必要です。

    - API 呼び出しをカタログ ID で分割します。 たとえば、カートの API の場合は、カートには異なるカタログの商品が含まれている可能性があります。 次の例に示すように、製品明細行はカタログ ID ごとにグループ化する必要があります。また、各カタログの API を個別に呼び出す必要があります。

        ![カタログ ID で製品明細行をグループ化するデータ アクションを更新しました。](./media/customization5.png)

## <a name="additional-resources"></a>追加リソース

[B2B サイトのコマース カタログの作成](catalogs-b2b-sites.md)

[B2B のコマース カタログに関するよく寄せられる質問](catalogs-b2b-sites-FAQ.md)
