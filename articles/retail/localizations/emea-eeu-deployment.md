---
title: チェコ共和国、ハンガリー、およびポーランドの事前請求書レポート印刷の配置ガイドライン
description: このトピックでは、チェコ共和国、ハンガリー、およびポーランドで POS から事前請求書の印刷を有効にする小売コンポーネントの拡張機能を作成する方法について説明します。
author: anmukh
manager: ezubov
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Eastern Europe
ms.search.industry: Retail
ms.author: anmukh
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 3803d51578e8f5301b851d1c8b1e12d0a1c3385f
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "760718"
---
# <a name="deployment-guidelines-for-cash-registers-for-czech-republic-hungary-and-poland"></a>チェコ共和国、ハンガリー、およびポーランドのキャッシュ レジスターの配置ガイドライン

[!include [banner](../includes/banner.md)]


このトピックでは、チェコ共和国、ハンガリー、およびポーランドで Microsoft Dynamics 365 for Retail のローカライゼーションを有効にする方法を示します。 ローカライズは、小売コンポーネントのいくつかの拡張機能で構成されます。 これらの拡張機能は、販売時点管理 (POS) から**事前請求書**レポートを印刷できるようにします。 チェコ共和国、ハンガリー、およびポーランド Retail ローカライズの詳細については、次を参照してください。[東ヨーロッパの小売り業向け事前請求書](./emea-eeu-advance-invoices-for-retail.md)

ローカライズは、小売ソフトウェア開発キット (SDK) の一部です。 リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

ローカライズは、Commerce runtime (CRT) と POS に対する拡張機能で構成されます。 このローカライズを有効にするには、CRT コンフィギュレーション ファイルを変更しおよび変更し、POS プロジェクトを構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Microsoft Visual Studio チーム サービスといった、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

開発環境を設定するこれらの手順を完了し、機能をテストできるようにします。

### <a name="crt-extension-components"></a>CRT 拡張コンポーネント

1. CRT 向け拡張機能のコンフィギュレーション ファイルを検索します。

    ファイル名は **commerceruntime.ext.config** で、IIS 小売サーバー サイトの下の **bin\\ext** フォルダーにあります。

2. 拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.UseAdvanceInvoice" />
    ```

    > [!WARNING]
    > commerceruntime.config ファイルは編集しては**いけません**。 このファイルは、カスタマイズのためのものではありません。

### <a name="modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

2. 適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能が読み込まれるようにします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AdvanceInvoice"
            }
        ]
    }
    ```

3. ソリューションをリビルドします。
4. デバッガーで Modern POS を実行し、機能をテストします。

### <a name="cloud-pos-extension-components"></a>クラウド POS 拡張コンポーネント

1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. 適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能が読み込まれるようにします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AdvanceInvoice"
            }
        ]
    }
    ```

3. ソリューションをリビルドします。
4. デバッガーでクラウド POS を実行し、機能をテストします。

### <a name="set-up-required-parameters-in-retail-headquarters"></a>小売用バックオフィスで要求されるパラメーターを設定します。

詳細な情報は、[東ヨーロッパにおける小売向け事前請求書](./emea-eeu-advance-invoices-for-retail.md)を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。

1. **クラウド POS 拡張コンポーネント**、またはこのトピックで既に見た**Modern POS 拡張コンポーネント**セクションで手順を完了します。
2. **RetailSdk\\Assets** フォルダーの下にあるパッケージ構成ファイルに、次の変更を加えます。

    **Commerceruntime.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.UseAdvanceInvoice" />
    ```

3. Retail SDK で **msbuild** を実行し、配置可能なパッケージを作成します。
4. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
