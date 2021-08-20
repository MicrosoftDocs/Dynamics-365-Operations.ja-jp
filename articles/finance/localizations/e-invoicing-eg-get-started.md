---
title: エジプト向けの電子請求を開始する
description: このトピックでは、Finance および Supply Chain Management でエジプト向けの電子請求を使い始めるための情報を提供します。
author: gionoder
ms.date: 04/20/2021
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
ms.openlocfilehash: 03ccc18d4c767dbb2a314e2eb1076b1c6e9019e991c6de3fc80be65d765fdd36
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758803"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>エジプト向けの電子請求を開始する

[!include [banner](../includes/banner.md)]

このトピックでは、エジプト向けの電子請求を使い始めるための情報を提供します。 このトピックでは、RCS (Regulatory Configuration Services) の国別の設定手順を説明し、[電子請求を開始する](e-invoicing-get-started.md)で説明されている手順を補完しています。

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>エジプトの電子請求 (EG) 機能の国別コンフィギュレーション

**エジプト請求書 (EG) 電子請求機能** のパラメーターの一部は、既定値で公開されます。 サービス環境に電子請求機能を導入する前に、値を確認し、業務処理のニーズをより反映するように更新してください。

このセクションは、トピック [電子請求を開始する](e-invoicing-get-started.md)の **電子請求機能の国別構成** セクションを補完するものです。

### <a name="prerequisites"></a>必要条件

このセクションの手順を完了する前に、以下のことを行います。

- [電子請求サービス管理を開始する](e-invoicing-get-started-service-administration.md)の **デジタル証明書シークレットを作成する** セクションの説明に従って、デジタル証明書シークレットを作成します。 テストの目的で、エジプトの税務当局は、テストおよびソリューション検証フェーズでのみ使用する必要がある特定のテスト デジタル証明書を提供しています。 詳細については、[エジプト電子請求 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) のリンクを使って、エジプト勢当局 Web サイトを参照してください。

1. RCS の **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。
2. **電子請求機能** ページで、作成した **エジプト電子請求 (EG)** 電子請求機能が選択されていることを確認します。
3. **バージョン** タブで、**ドラフト** バージョンが選択されていることを確認します。
4. グリッドの **設定** タブで、**売上請求書** 機能の設定を選択します。
5. **編集** を選択し、**アクション** フィールド グループの **アクション** タブで、**エジプト税務当局に向けた json 文書に署名する** を選択します。
6. **パラメーター** フィールド グループでパラメーター **証明書名** を選択し、電子請求機能で使用するために作成されたデジタル証明書の名前を選択します。
7. **アクション** フィールド グループで、**エジプト ETA サービスとの統合** を選択します。 このアクションが 2 回発生した場合は、この手順を繰り返します。
8. **パラメーター** フィールド グループで、**Web サービス URL** および **ログイン サービス URL** を選択し、必要に応じて URL パラメーターを確認してください。 [エジプトの電子請求の SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) で提供されているリンクを使用して、エジプトの税務当局の Web サイトを参照し、テストおよび実稼働の URL を取得してください。
9. **保存** を選択して、ページを閉じます。
10. 電子請求機能をサービス環境にデプロイするには、[電子請求を開始する](e-invoicing-get-started.md)を参照してください。

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>エジプトの電子請求 (EG) 機能のアプリケーション設定の国別コンフィギュレーション

Finance および Supply Chain Management に接続されたアプリケーションに対してアプリケーション設定をデプロイする前に、これらのステップを実行します。

このセクションは、トピック [電子請求を開始する](e-invoicing-get-started.md)の **アプリケーション設定** セクションを補完するものです。

1. RCS の **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。
2. **電子請求機能** ページで、**エジプト電子請求 (EG)** 電子請求機能が選択されていることを確認します。
3. **バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。
4. **設定** タブで、**アプリケーション設定** を選択し、**接続済みアプリケーション** フィールドで、配置するアプリケーションを選択します。
5. **テーブル名** フィールドで、顧客請求書仕訳帳が選択されているか確認します。
6. **応答タイプ** を選択し、**新規** を選択します。
7. **応答タイプ** フィールドに "Response" と入力し、**説明** フィールドに "Description" と入力します。
8. **提出の状態** フィールドで **保留** を選択します。
9. **モデル マッピング** フィールドで、**応答メッセージからモデル マッピング** を **(プレビュー) 応答メッセージのインポート形式** と共に選択し、**保存** を選択します。
10. **新規** を選択し、続いて **応答タイプ** フィールドで、固定値として "ResponseData" と入力します。 **説明** フィールドに、"Description" と入力します。
11. **提出の状態** フィールドで **保留** を選択します。
12. **データ エンティティ名** フィールドに、**売上請求書ヘッダー V2** と入力します。
13. **モデル マッピング** フィールドで、**エジプトの応答データのインポート** を **(プレビュー) エジプトの応答データのインポート** と共に選択し、**保存** を選択します。
14. Finance および Supply Chain Management に接続されたアプリケーションに対してアプリケーション設定をデプロイするには[電子請求を開始する](e-invoicing-get-started.md)を参照してください。

## <a name="privacy-notice"></a>プライバシー通知

**エジプトの電子請求 (EG)** 機能を有効にするには、組織の税務登録 ID を含む一部のデータの送信が必要となる場合があります。 このデータは、政府の Web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。 管理者は、**組織管理** > **設定** > **電子ドキュメント パラメーター** に移動して、機能を有効、または無効にすることができます。 **機能** タブで、**エジプトの電子請求 (EG)** 機能を含む行を選択して、適切な選択を行います。 これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。

## <a name="additional-resources"></a>追加リソース

- [電子請求の概要](e-invoicing-service-overview.md)
- [電子請求サービスの管理を開始する](e-invoicing-get-started-service-administration.md)
- [電子請求の使用を開始する](e-invoicing-get-started.md)
- [エジプトの顧客電子請求書](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
