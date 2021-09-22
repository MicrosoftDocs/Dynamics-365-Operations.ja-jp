---
title: アプリ接続を設定する際の証明書パス エラー
description: Warehouse Management アプリに「証明パスの信頼のアンカーが見つかりません」というエラーが表示される場合は、このページを使用して問題を解決または回避します。
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476879"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>アプリ接続の設定時に、証明書パスのトラスト アンカーが見つかりません

## <a name="symptoms"></a>現象

Supply Chain Management に接続しようとしているときに、Warehouse Management アプリで次のエラー メッセージが表示される場合があります。

> java.security.cert.certPathValidatorException: 証明書パスのトラスト アンカーが見つかりません。

この問題は、次のプロパティを使用してデバイスに影響する可能性があります。

- **OS バージョン**: Android 4.4.x (Zebra TC55 など)。 これは最新の Android バージョンにおいて問題はありません。
- **Supply Chain Management ロケーション**: Cloud
- **接続モード**: クライアント シークレットまたは証明書

## <a name="possible-cause"></a>考えられる原因

Microsoft が Supply Chain Management で使用するサーバー SSL 証明書を更新した可能性があります。 結果として、ルート証明書や中間証明書の 1 つが変更された可能性があるので、新しい証明書の変更は、モバイル デバイスの信頼済のシステム証明書の一覧に表示されません。 新しい Android バージョンでは、信頼済の証明書が自動的に更新されますが、Android 4.4.x では更新されません。

## <a name="resolution"></a>解決策

この問題を解決するには、次のいずれかを実行してください。

- 次のセクションで説明されている回避策を使用して、各関連デバイスを更新します。
- 信頼済システムの認証機関 (CA) 証明書の更新を利用するため、Zebra または Google に接続が可能 *かも* しれません。 ただし、確認されていません。
- 可能であれば、古いデバイスを、より新しい Android バージョン (信頼済の CA 証明書が自動的に更新される) を実行しているデバイスに置き 換えてください。

### <a name="workaround"></a>回避策

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>手順 1: Supply Chain Management から新しいルート証明書をエクスポートします

次の手順に従って、インターネット ブラウザーを使用して新しいルート証明書を手動でダウンロードします。

1. Dynamics Supply Chain Management にログインし、フロント ページを開きます。

1. ブラウザーのアドレス バーでロック アイコンを選択すると、**ロケーションが保護された** ダイアログ ボックスが開きます。
1. ダイアログ ボックスで、**証明書 (有効)** を選択し、その証明書の **証明書** ウィンドウを開きます。
1. **証明書** ウィンドウの **証明書パス** タブを開きます。
1. 階層に表示されている上位の証明書を選択します。 (これはルート証明書です)。
1. **詳細** ウィンドウの **証明書パス** タブを開きます。
1. **詳細** タブの下部で、**ファイルにコピー** ボタンを選択します。
1. **証明書エクスポート ウィザード** が開きます。 **次へ** を選択して続行します。
1. **エクスポート ファイル形式** ページが開きます。 **DER エンコード バイナリ X.509 (.CER)** を選択します。 その後、**次へ** を選択して続行します。
1. **エクスポートするファイル** ページが開き、ファイル名と場所を指定します。 その後、**次へ** を選択して続行します。
1. **証明書のエクスポート ウィザードは完了** ページが開き、エクスポートの結果が表示されます。 **完了** を選択します。

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>手順 2: 影響を受けるデバイスにダウンロードした証明書をインストールします

次の手順に従って、ダウンロードした証明書をインストールします。

1. 前の手順でダウンロードした証明書を更新するデバイスに転送します。 たとえば、デバイスで使用できるファイルを作成するために、SD カードやネットワーク接続を使用する場合があります。
1. デバイスのセキュリティ設定を開き、メニュー オプションを選択してファイルから証明書をインストールします。 (この手順はデバイスと OS のバージョンによって正確に異なります。)
1. 新しい証明書は、信頼済み証明書の **ユーザー** タブに表示されます。
1. 影響を受ける各デバイスに対して、この手順を繰り返します。
