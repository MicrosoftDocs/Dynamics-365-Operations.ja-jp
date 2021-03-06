---
title: 小売店舗のユーザー定義の証明書プロファイル
description: このトピックでは、小売店舗で証明書を使用する方法についての概要を説明します。
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44042fc43fa3b43358120fb6f8f633abeae7005f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020316"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>小売店舗のユーザー定義の証明書プロファイル

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>概要

このトピックでは、Microsoft Dynamics 365 Commerce で利用できる証明書プロファイルの概要を提供します。 この機能は、ローカル証明書のサポートを追加することによって[小売チャネルのシークレットを管理](../dev-itpro/manage-secrets.md) の機能を拡張します。

販売時点管理 (POS) がオフライン モードで実行されている間、キー コンテナーに保存されている証明書にはアクセスできません。 代わりにローカル証明書を使用する必要があります。 次の機能がサポートされています。

- キー コンテナー予備シナリオでのローカル証明書の使用
- キー コンテナーを使用しないローカル証明書の使用 (たとえばオンプレミスのインストールで)
- 一部の店舗およびターミナルは証明書の新しいバージョンを使用しますが、他の店舗またはターミナルは以前のバージョンを引き続き使用する証明書の段階的な更新

証明書プロファイル機能を使用すると、既定の証明書を指定して、同じ証明書プロファイル内の証明書を検索する順序を設定できます。 この機能は、ローカル証明書および Key Vault 証明書についても同じような設定方法を提供します。 証明書に対して会社固有の設定を追加できますが、各証明書の会社間の一意の識別子を Commerce チャネルで使用できます。

### <a name="scenarios"></a>シナリオ

証明書プロファイル機能では、Commerce チャネルで次のシナリオをサポートしています。

- キー コンテナー予備シナリオでのローカル証明書を使用します。 予備シナリオの例を次に示します。

    - キー コンテナー ストレージにアクセスできません。
    - キー コンテナー ストレージに証明書が見つかりません。
    - POS はオフライン モードで実行されています。

- ローカル証明書を使用しますが、キー コンテナーには保存しません (たとえば、オンプレミスのインストールで)。
- 証明書の段階的な更新を実行すると、証明書の新しいバージョンは、新しいバージョンが既に利用可能な店舗またはターミナルでのみ使用されます。
- 複数の会社で同じ証明書を使用します。

## <a name="set-up-certificate-profiles"></a>証明書プロファイルの設定

次の手順では、証明書プロファイルの設定方法について説明します。 Commerce チャネルで証明書プロファイルを使用する前に、次の手順に従って設定をコンフィギュレーションします。

1. **機能管理** ワークスペースで、**小売店舗のユーザー定義の証明書プロファイル** 機能を有効にします。
2. **システム管理 \> 設定 \> 証明書プロファイル** の順に移動します。
3. レコードを作成し、その **証明書プロファイル**、**名前**、および **説明** のフィールドを設定します。

    > [!NOTE]
    > 証明書プロファイルは、すべての会社および Commerce コンポーネント間の証明書の一意識別子です。

3. **法人** タブで、明細行を追加し、現在の証明書プロファイルを使用する必要がある法人 (会社) を選択します。 証明書プロファイルを複数の法人に対して使用する必要がある場合は、この手順を繰り返して、追加の法人ごとに明細行を追加します。
4. **設定** を選択して、**証明書プロファイル設定** のページを開くと、証明書プロファイルの会社固有の設定を入力できます。

### <a name="certificate-profile-settings"></a>証明書プロファイル設定

証明書プロファイル明細行の **設定** を選択すると、**証明書プロファイル設定** のページが表示されます。 このページでは、現在の証明書プロファイルが Commerce チャネルで呼び出されたときに使用できる証明書を指定できます。 証明書を検索する順序を指定することもできます。

> [!NOTE]
> **優先順位** フィールドは自動的に設定されます。 値 **1** は、最も高い優先順位を表します。 新しい明細行が、**証明書プロファイル設定** のページに追加されると、その優先順位は前の明細行の優先順位より 1 大きい番号に設定されます。 特定の明細行の優先順位を変更するには、明細行を選択し、**上へ移動** を選択して優先順位を上げるか、**下に移動** を選択して優先順位を下げます。

**証明書プロファイル設定** のページに新しい明細行を追加するときは、次のフィールドを設定します。

- **場所タイプ** – 証明書を保存されている場所を選択します。 このフィールドには次の 2 つの値があります: **ローカル証明書** と **Key Vault** です。
- **Key Vault 証明書** – **場所のタイプ** フィールドを **Key Vault** に設定する場合、このフィールドは必須です。 これを使用して、Key Vault 証明書のシークレットを指定します。

    > [!NOTE]
    > 証明書プロファイルで Key Vault 証明書を使用する前に、必ずキー コンテナー ストレージに証明書をアップロードし、[Azure Key Vault クライアントの設定](../../finance/localizations/setting-up-azure-key-vault-client.md) の指示に従ってください。

- **店舗名** – このフィールドはオプションであり、**場所タイプ** フィールドを **ローカル証明書** に設定した場合にのみ利用できます。 これを使用して、ローカル証明書の検索に使用する既定の店舗名を指定します。
- **店舗の場所** – このフィールドはオプションであり、**場所タイプ** フィールドを **ローカル証明書** に設定した場合にのみ利用できます。 これを使用して、ローカル証明書の検索に使用する既定の店舗の場所を指定します。

    > [!NOTE]
    > Commerce Runtime でローカル証明書を検索するプロセスを簡略化するために、既定の店舗名および店舗の場所が追加されます。 X509StoreProvider には、証明書が保存されるフォルダーの一覧があります。 既定の店舗名および既定の店舗場所が指定されていない場合、X509StoreProvider はその一覧の他のフォルダーにある証明書を検索しようとします。

- **サムプリント** – このフィールドは必須であり、**場所タイプ** フィールドを **ローカル証明書** に設定した場合にのみ利用できます。 これを使用して、証明書のサムプリントを指定します。
- **コメント** – このフィールドはオプションであり、ユーザーはメモを入力できます。

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>ワークフロー: Commerce Runtime での証明書の検索

Commerce Runtime で、証明書プロファイルが呼び出されたときに証明書を検索するために使用される、基本的なワークフローを次に示します。

1. システムでは、証明書プロファイルに現在の法人に対する会社固有の設定があるかどうかが識別されます。
1. システムでは、**優先順位** フィールドが **1** に設定された明細行に対する **証明書プロファイル設定** のページの値を使用して証明書を検索しようとします。

    - **場所のタイプ** フィールドが **Key Vault** に設定されている場合、**Key Vault 証明書のシークレット** フィールドの値は **キー コンテナー パラメーター** のページの証明書を検索するために使用されます。 次に、証明書がキー コンテナー ストレージで検索されます。
    - **場所タイプ** フィールドが **ローカル証明書** に設定される場合、既定の店舗名および店舗の場所を使用して、これらのパラメータが指定されている場合、X509StoreProvider は最初に証明書を検索します。 次に、そのフォルダーの一覧にある他のすべてのフォルダーを検索します。

1. 証明書が見つからない場合は、**優先順位** フィールドが **2** などに設定されている明細行に対してプロセスが繰り返されます。

> [!NOTE]
> 証明書プロファイルに現在の法人の設定がない場合、または証明書検索が **証明書プロファイル設定** のページのすべての明細行で失敗した場合、証明書は見つかりません。

#### <a name="caching-the-results-of-certificate-searches"></a>証明書検索の結果のキャッシュ

証明書検索の結果がキャッシュされます。 キャッシュの既定の有効期限は 1 時間です。 ただし、この時間はカスタマイズ可能で、最大 24 時間に設定できます。

### <a name="gradual-update"></a>段階的更新

証明書の新しいバージョンが導入されても、すべての店舗で同時に更新できない場合は、証明書プロファイル機能により証明書を段階的に更新できます。

1. 証明書プロファイルおよび更新する明細行を検索し、**設定** を選択します。
1. 明細行を追加し、証明書の最新バージョンに関連する設定を指定します。
1. 新しい明細行の **優先順位** の値を増やします。 **上へ移動** ボタンを使用し、同じ証明書の以前のバージョンの明細行の上になるように明細行を移動します。

> [!NOTE]
> Commerce Runtime では、証明書の新しいバージョンが最初に呼び出されます。 証明書がまだ特定の店舗または特定のターミナルで更新されていない場合は、以前のバージョンが呼び出されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]