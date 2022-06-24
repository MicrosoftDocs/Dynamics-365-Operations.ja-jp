---
title: エジプト向けの電子請求
description: この記事では、Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management でエジプト向けの電子請求を使い始めるための情報を提供します。
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c2a46ef938c5dee62c0d0acd1648584df344c81a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904415"
---
# <a name="electronic-invoicing-for-egypt"></a>エジプト向けの電子請求

[!include [banner](../includes/banner.md)]

この記事では、エジプト向けの電子請求を使い始めるための情報を提供します。 Regulatory Configuration Service (RCS) における、国ごとに異なる構成手順について説明します。 これらの手順は、[電子請求の設定](e-invoicing-set-up-overview.md) で説明されている手順を補完しています。

## <a name="prerequisites"></a>必要条件

この記事の手順を開始する前に、以下の前提条件を完了します:

- [電子請求の概要](e-invoicing-service-overview.md) で説明されている電子請求について理解します。
- RCS に登録し、電子請求を設定します。 詳細については、次のトピックを参照してください。

    - [電子請求サービスへの登録およびインストール](e-invoicing-sign-up-install.md)
    - [電子請求のための Azure リソースの設定](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Services にマイクロサービス向けのアドインをインストールします](e-invoicing-install-add-in-microservices-lcs.md)
    
- [電子請求との統合の有効化と設定](e-invoicing-activate-setup-integration.md)の説明に従って、Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management アプリケーションと電子請求サービスの間の統合を有効にします。
- Azure Key Vault にデジタル証明書シークレットを作成し、[顧客の証明書とシークレット](e-invoicing-customer-certificates-secrets.md) の説明に従って設定します。 テストの目的で、エジプトの税務当局は、テストおよびソリューション検証フェーズでのみ使用する必要がある特定のテスト デジタル証明書を提供しています。 詳細については、[エジプト電子請求 SDK](https://sdk.invoicing.eta.gov.eg/faq/) で提供されているリンクを使用して、エジプト税務当局 Web サイトを参照してください。

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>エジプトの電子請求書 (EG) 機能の国固有の構成

**エジプト電子請求書 (EG)** 電子請求機能のパラメーターの一部は、既定値で公開されます。 電子請求機能をサービス環境に配置する前に、既定値を確認し、必要に応じて更新して、事業運営がより適切に反映されるようにします。

1. [グローバル リポジトリからの機能のインポート](e-invoicing-import-feature-global-repository.md) に記載の **エジプト電子請求書 (EG)** グローバリゼーション機能の最新バージョンをインポートします。
2. [グローバリゼーション機の作成](e-invoicing-create-new-globalization-feature.md) に記載されているように、インポートされたグローバリゼーション機能のコピーを作成し、その構成プロバイダーを選択します。
3. **バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。
4. **設定** タブのグリッドで、**売上請求書派生** 機能の設定を選択します。
5. **編集** を選択します。
6. **処理パイプライン** タブの **処理パイプライン** セクションで、**エジプト税務当局の JSON ドキュメントに署名する** を選択します。
7. **パラメーター** セクションで、**証明書名** を選択し、作成したデジタル証明書の名前を選択します。
8. **処理パイプライン** セクションで、**エジプト ETA サービスとの統合** を選択します。 このアクションが 2 回発生した場合は、この手順を繰り返します。
9. **パラメーター** セクションで、**Web サービス URL** および **ログイン サービス URL** を選択します。 次に、URL パラメーターを確認します。 テストおよび運用の URL を取得するには、[エジプト電子請求 SDK](https://sdk.invoicing.eta.gov.eg/faq/) で提供されているリンクを使用して、エジプト税務当局の Web サイトにアクセスします。
10. **保存** を選択して、ページを閉じます。
11. **プロジェクト請求書派生** 機能の設定について、ステップ 4 - 10 を繰り返します。

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>エジプト 電子請求書 (EG) アプリケーション設定の国固有の構成

Finance 環境または Supply Chain Management 環境で設定する必要があるパラメーターがあります。 この設定は、次の 2 か所のいずれかで完了することができます。

- Finance または Supply Chain Management 環境で直接。 詳細については、[電子請求書パラメーターの設定](e-invoicing-set-up-parameters.md) を参照してください。
- RCS で。 電子請求書機能の設定の範囲では、すべてのパラメーターを定義し、電子請求書機能を配置する際に Finance または Supply Chain Management 環境に直接配置できます。

どちらのオプションの場合もパラメーターは同じです。 電子請求サービスの最初の機能を設定する場合は、次の手順に従って RCS のパラメーターを設定し、接続されているアプリケーションに配置することをお勧めします。

> [!NOTE]
> 一部の電子請求書機能のバージョンには、Finance または Supply Chain Management 向けに事前定義された一連のアプリケーション固有パラメーターが含まれている場合があります。 この場合は、データが正しいことを確認する必要があります。 それ以外の場合は、手動でパラメーターを設定します。

1. 作成した **エジプト電子請求書 (EG)** グローバリゼーション機能のコピーを検索します。
2. **バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。
3. **設定** タブで、**アプリケーションの設定** を選択します。
4. **接続アプリケーション** フィールドで、パラメーターを配置するアプリケーションを選択します。
5. **電子ドキュメントのタイプ** ページで、**追加** を選択してレコードを作成します。
6. **テーブル名** フィールドに、**CustInvoiceJour** を追加します。
7. **コンテキスト** フィールドに、**顧客請求書コンテクスト** マッピング名への参照を追加します。 構成は、**顧客請求書コンテクスト モデル** です。
8. **電子ドキュメント マッピング** フィールドに、**顧客請求書** マッピング名への参照を追加します。 構成は、**請求書モデル マッピング** です。
9. **保存** を選択します。
10. **応答タイプ** ページで、**追加** を選択します。
11. **応答タイプ** フィールドに、**応答** と入力します。
12. **説明** フィールドに **プロセス応答** と入力します。
13. **提出の状態** フィールドで **保留** を選択します。
14. **モデル マッピング** フィールドで、**応答メッセージのインポート** を選択します。 構成は、**エジプト応答メッセージのインポート (EG)** です。
15. **保存** を選択します。
16. **追加** を選択します。
17. **応答タイプ** フィールドに、**ResponseData** と入力します。
18. **説明** フィールドに **プロセス応答データ** と入力します。
19. **提出の状態** フィールドで **保留** を選択します。
20. **データ エンティティ名** フィールドで **SalesInvoiceHeaderV2Entity** を選択します。
21. **モデル マッピング** フィールドで、**応答データのインポート** を選択します。 構成は、**エジプト応答データのインポート (EG)** です。
22. **保存** を選択して、ページを閉じます。
23. ページを閉じます。

機能をサービス環境に配置し、アプリケーション設定を Finance または Supply Chain Management に接続されたアプリケーションに配置するには、[グローバリゼーション機能の完了、公開、および配置](e-invoicing-complete-publish-deploy-globalization-feature.md) を参照してください

## <a name="privacy-notice"></a>プライバシー通知

**エジプト電子請求書 (EG)** 機能を有効化する場合は、制限付きのデータ送信が必要な場合があります。 このデータは組織の税登録 ID を含みます。 データは、政府の Web サービスとの統合に必要な所定の形式で、その税務当局に電子請求書を送信するために税務当局によって承認された第三者機関に送信されます。 管理者は、**組織管理** \> **設定** \> **電子ドキュメント パラメーター** に移動して、機能を有効、または無効にすることができます。 **機能** タブで、**エジプトの電子請求 (EG)** 機能を含む行を選択して、適切な選択を行います。 外部システムからこの Dynamics 365 オンライン サービスにインポートされたデータは、当社の [プライバシーに関する声明](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、各国固有の機能ドキュメントの "プライバシーに関する注意事項" セクションを参照してください。

## <a name="additional-resources"></a>追加リソース

- [電子請求の概要](e-invoicing-service-overview.md)
- [電子請求サービスの管理を開始する](e-invoicing-get-started-service-administration.md)
- [電子請求の使用を開始する](e-invoicing-get-started.md)
- [エジプトの顧客電子請求書](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
